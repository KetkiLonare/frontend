// paginationData.current = {
      //   ...paginationData?.current,
      //   currentPage: pageNumber,
      // };
      // const spliceFrom: any =
      //   (paginationData?.current?.currentPage - 1) *
      //   paginationData?.current?.itemCount;
      // const spliceTo: any = paginationData?.current?.currentPage * 10;

      // const spliceArray = get_gtdb_tds_tran_load.slice(spliceFrom, spliceTo);

      // setrows([...rows, ...spliceArray])
      //  setTableRows(get_gtdb_tds_tran_load);


      <Drawer
                        dwidth={50}
                        title="ADD NEW TRANSACTIONS"
                        show={show}
                        setShow={setShow}
                        childCompState="add"
                        ChildComp={drawerFormComp}
                    />



                    
    const drawerFormComp = ({ state }) => {
        const data = [
            {
                compHeader: "Deductee Details",
                fields: [
                    {
                        label: "PAN Number",
                        controlId: "pannumber",
                        value: "AAYPA0998D",
                    },
                    {
                        label: "Deductee Name",
                        controlId: "dedutee",
                        value: "RAVI KANT AGARWAL HRM",
                    },
                    {
                        label: "Deductee PAN Verified",
                        controlId: "deducteepannumber",
                        value: "NOT VERIFIED",
                    },
                    {
                        label: "Customer ID",
                        controlId: "customerid",
                        value: "ABCD1234",
                    },
                    {
                        label: "Account Number",
                        controlId: "accountnumber",
                        value: "500014788954",
                    },
                    {
                        label: "TIN UIN Number",
                        controlId: "tinuin",
                        value: "58745555345",
                    },
                    {
                        label: "Email-ID",
                        controlId: "emailid",
                        value: "RAMC7W@GMAIL.COM",
                    },
                    {
                        label: "Address",
                        controlId: "address",
                        value: "PAWANSUT APPARTMENT, ....",
                    },
                ],
            },
        ];

        return (
            <>
                <Form className="drawar-form">
                    <div className="form-body">
                        <Row className="mb-20">
                            <h6 className="fs-16 int-semibold clr-black mb-20">
                                {data[0]?.compHeader}
                            </h6>
                            {data[0]?.fields &&
                                data[0]?.fields.map((each, key) => (
                                    <Col key={key} lg={4}>
                                        <Form.Group
                                            className="mb-10 clr-black int-regular fs-14"
                                            controlId={each?.controlId}
                                        >
                                            <Form.Label>{each?.label}</Form.Label>
                                            <Form.Control
                                                type="text"
                                                placeholder={`Enter ${each?.label}`}
                                                value={state == "edit" ? each?.value : ""}
                                            />
                                        </Form.Group>
                                    </Col>
                                ))}
                        </Row>
                        <Row className="mt-20">
                            <h6 className="fs-16 int-semibold clr-black mb-20 mt-20">
                                Transaction Details
                            </h6>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="transactionreference"
                                >
                                    <Form.Label>Transaction Reference Date</Form.Label>
                                    <Form.Control
                                        type="text"
                                        placeholder="Enter Transaction Reference Date"
                                        value={state == "edit" ? "12-10-2021" : ""}
                                    />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="tdsdeduction"
                                >
                                    <Form.Label>TDS Deduction Date</Form.Label>
                                    <Form.Control
                                        type="text"
                                        placeholder="Enter TDS Deduction Date"
                                        value={state == "edit" ? "11-04-2021" : ""}
                                    />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="tdssection"
                                >
                                    <Form.Label>TDS Section</Form.Label>
                                    <Form.Select className="int-regular fs-10">
                                        {["Select TDS Section", "15GH", "23FQ", "12JK"].map(
                                            (each, key) => (
                                                <option key={key} className="int-regular">
                                                    {each}
                                                </option>
                                            )
                                        )}
                                    </Form.Select>
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="tdsdeductreason"
                                >
                                    <Form.Label>TDS Deduct Reason</Form.Label>
                                    <Form.Select className="int-regular fs-10">
                                        {[" Select TDS Deduct Reason", "15GH", "23FQ", "12JK"].map(
                                            (each, key) => (
                                                <option key={key} className="int-regular">
                                                    {each}
                                                </option>
                                            )
                                        )}
                                    </Form.Select>
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="tdsseductiondate"
                                >
                                    <Form.Label>TDS Deduction Date</Form.Label>
                                    <Form.Control
                                        type="text"
                                        placeholder="Enter TDS Deduction Date"
                                    />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="certificatetdsrate"
                                >
                                    <Form.Label>Certificate TDS rate</Form.Label>
                                    <Form.Control
                                        type="text"
                                        placeholder="Enter Certificate TDS rate"
                                    />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="pannumber"
                                >
                                    <Form.Label>Country</Form.Label>
                                    <Form.Select className="int-regular fs-10">
                                        {[
                                            "Select Country",
                                            "Afghanistan",
                                            "India",
                                            "Indonesia",
                                        ].map((each, key) => (
                                            <option key={key} className="int-regular">
                                                {each}
                                            </option>
                                        ))}
                                    </Form.Select>
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="pannumber"
                                >
                                    <Form.Label>Tax Rate Type</Form.Label>
                                    <Form.Select className="int-regular fs-10">
                                        {["Select Tax Rate Type", "15GH", "23FQ", "12JK"].map(
                                            (each, key) => (
                                                <option key={key} className="int-regular">
                                                    {each}
                                                </option>
                                            )
                                        )}
                                    </Form.Select>
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="pannumber"
                                >
                                    <Form.Label>Remittance type</Form.Label>
                                    <Form.Control
                                        type="text"
                                        placeholder="Enter Remittance type"
                                    />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="pannumber"
                                >
                                    <Form.Label>Transaction Amount</Form.Label>
                                    <Form.Control
                                        type="text"
                                        placeholder="Enter Transaction Amount"
                                    />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="pannumber"
                                >
                                    <Form.Label>Party Bill Amount</Form.Label>
                                    <Form.Control
                                        type="text"
                                        placeholder="Enter Party Bill Amount"
                                    />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="pannumber"
                                >
                                    <Form.Label>Transaction Reference Number</Form.Label>
                                    <Form.Control
                                        type="text"
                                        placeholder="Enter Transaction Reference Number"
                                    />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="pannumber"
                                >
                                    <Form.Label className="percentage-badge ">
                                        TDS Amount<Badge className="mlf-5">10.00 %</Badge>
                                    </Form.Label>
                                    <Form.Control type="text" placeholder="Enter TDS Amount" />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="pannumber"
                                >
                                    <Form.Label className="percentage-badge ">
                                        Surcharge Amount <Badge className="mlf-5">10.00 %</Badge>
                                    </Form.Label>
                                    <Form.Control
                                        type="text"
                                        placeholder="Enter Surcharge Amount"
                                    />
                                </Form.Group>
                            </Col>
                            <Col lg={4}>
                                <Form.Group
                                    className="mb-10 clr-black int-regular fs-14"
                                    controlId="pannumber"
                                >
                                    <Form.Label className="percentage-badge ">
                                        Cess Amount<Badge className="mlf-5">10.00 %</Badge>
                                    </Form.Label>
                                    <Form.Control type="text" placeholder="Enter Cess Amount" />
                                </Form.Group>
                            </Col>
                        </Row>
                    </div>
                    <div className="d-flex justify-content-between form-footer">
                        <div>
                            <button className="btn-gray mrf-5 ">Save</button>
                            <button className="btn-light mlf-5">Cancel</button>
                        </div>
                        <div>
                            <button className="success-btn mrf-5">Approve</button>
                            <button className="danger-btn mlf-5">Delete</button>
                        </div>
                    </div>
                </Form>
            </>
        );
    };




    import React, { useEffect, useRef, useState, useContext } from "react";
import { Col, Container, Form, Row } from "react-bootstrap";
import Datatable from "../../components/datatable/Datatable";
import DeductorDetails from "../../components/deductorDetails";
import { Drawer } from "../../components/drawer";
import Badge from "react-bootstrap/Badge";
import { Filter } from "../../components/filters";
import DatatableFilter from "../../components/datatable/datatableFilter";
import ExportDatabledata from "../../components/datatable/exportDatabledata";
import { getReq, postReq } from "../../http";
import { CssLoader } from "../../components/loader";
import { UserContext } from "../../hooks/UserContext";
import { fyYearFormater } from "../../utils/caseConsistent";
import useForm from "../../hooks/useForm";
import { filterTransactionValidate } from "../../validate/validateTransaction";

const Transaction = ({ loader }: { loader: Boolean }) => {
    const [show, setShow] = useState(false);
    const [filter, setFilter]: any = useState({});
    const [update, setUpdate] = useState(false);

    const [pageRecords, setPageRecords] = useState(5);
    const [pageCount, setPageCount] = useState(0);

    const [tablerows, setTableRows]: any = useState([]);
    const [theader, setTheader] = useState([]);
    const [laodingState, setLoadingState]: any = useState(false);
    const { user }: any = useContext(UserContext);
    const paginationData: any = useRef({ itemCount: 10, currentPage: 1 });
    const [rowsData, setRowsData]: any = useState([]);
    const [header, setHeader]: any = useState([]);
    const [rows, setrows]: any = useState([]);

    let rowData: any = [];

    const myStyle = {
        width: "50rem",
    };

    const httpGet = async () => {
        const res = await getReq({
            url: "http://localhost:4002/get-transaction-filter",
            returnDataKey: "filterCode",
        });
        if (res) {
            setFilter({
                advance_filter: res?.advance_filter,
                basic_filter: res?.basic_filter,
            });
        }
    };
    const httpPost = async (values, pageNumber) => {
        setLoadingState(true);

        const res = await postReq({
            url: "http://localhost:4003/get-transactions",
            returnDataKey: "transactionCodes",
            data: values,
        });
        const {
            data,
            get_gtdb_tds_tran_load,
            get_gtdb_tds_tran_load_header,
            status,
        } = res;

        if (res) {
            for (let i = 0; i < get_gtdb_tds_tran_load_header.length; i++) {
                if (get_gtdb_tds_tran_load_header[i].display != 0) {
                    header.push(get_gtdb_tds_tran_load_header[i]);
                }
            }
            setTableRows(get_gtdb_tds_tran_load);
            setLoadingState(false);
        }
    };

    const getData = async (pageNumber) => {
        setValues((pre: any) => ({
            ...pre,
            a_pagination_count: 10
        }));
        setPageCount(10);
        // paginationData.current = {
        //     ...paginationData?.current,
        //     currentPage: pageNumber,
        // };
        // const spliceFrom: any =
        //     (paginationData?.current?.currentPage - 1) *
        //     paginationData?.current?.itemCount;
        // const spliceTo: any = paginationData?.current?.currentPage * 10;
        // const spliceArray = rows.slice(spliceFrom, spliceTo);
        // setRowsData([...rowsData, ...spliceArray]);
    };

    useEffect(() => {
        httpPost(values, 20);
    }, [pageCount]);

    
    const submit = async () => {
        try {
        } catch (error) { }
    };


    useEffect(() => {
        // getData(paginationData?.current?.currentPage);
        // httpPost(values, paginationData?.current?.currentPage);
        httpGet();
    }, []);

    const formInputObj: any = {
        a_db_total_records: 10,
        a_pagination_count: 0
    };
    const { handleChange, handleSubmit, values, errors, setErrors, setValues } = useForm(submit, filterTransactionValidate, formInputObj);

    return (
        <>
            <div className="transaction-section">
                <Container fluid="lg">
                    <DeductorDetails
                        deductor="Webakruti Software Pvt. Ltd."
                        tanno="DELE10221B"
                        link="/edit"
                        financialyear={fyYearFormater(user.default_acc_year)}
                        formtype={`${user.default_tds_type_code} | Q${user.default_quarter_no}`}
                    />
                    <div>
                        <div className="d-flex justify-content-between mb-3 mt-3">
                            <div>
                                <h6 className="fs-18 int-semibold clr-blue">Transactions</h6>
                            </div>
                            <div>
                                <button className="btn-secondary" onClick={() => setShow(true)}>
                                    Add New Transaction
                                </button>
                            </div>
                        </div>
                    </div>
                    <div className="d-flex justify-content-between align-items-center">
                        <Filter
                            baseFilter={filter?.basic_filter ? filter?.basic_filter : []}
                            advFilter={filter?.advance_filter ? filter?.advance_filter : []}
                            submit={(values) => {
                                httpPost(values, paginationData?.current?.currentPage);
                            }}
                            pageRecords={pageRecords}
                            pageCount={pageCount}
                        />
                        <div className="d-flex ">
                            <DatatableFilter />
                            <ExportDatabledata />
                        </div>
                    </div>
                    {laodingState && <CssLoader />}

                    <Datatable
                        rows={header}
                        columns={tablerows}
                        itemperpage="50"
                        setUpdate={setUpdate}
                        getData={getData}
                        pageNumber={paginationData?.current?.currentPage}
                    />

                    
                </Container>
            </div>
        </>
    );
};

export default Transaction;


// const Transaction = () => {
//     const { user }: any = useContext(UserContext);

//     const [pageLoader, setPageLoader] = useState(true);
//     const [filter, setFilter]: any = useState({});

//     const [header, setHeader]: any = useState([]);
//     const [rows, setRows]: any = useState([]);

//     const [pageRecords, setPageRecords] = useState(10);
//     const [pageCount, setPageCount] = useState(0);

//     const httpPost = async () => {
//         setPageLoader(true);
//         const res = await postReq({
//             url: "http://localhost:4003/get-transactions",
//             returnDataKey: "transactionCodes",
//             data: values,
//         });
//         const { data, get_gtdb_tds_tran_load, get_gtdb_tds_tran_load_header, status } = res;
//         if (header.length === 0) {
//             setHeader(get_gtdb_tds_tran_load_header);
//         }
//         const newrows = [...rows];
//         for (let row of get_gtdb_tds_tran_load) {
//             newrows.push(row);
//         }
//         setRows(newrows);
//         setPageLoader(false);
//     }

//     const getFilter = async () => {
//         setPageLoader(true);
//         const res = await getReq({
//             url: "http://localhost:4002/get-transaction-filter",
//             returnDataKey: "filterCode",
//         });
//         if (res) {
//             setFilter({
//                 advance_filter: res?.advance_filter,
//                 basic_filter: res?.basic_filter,
//             });
//         }
//         setPageLoader(false);
//     }

//     useEffect(() => {
//         httpPost();
//         getFilter();
//     }, []);

//     useEffect(() => {
//         httpPost();
//     }, [pageCount]);

//     useEffect(() => {
//     }, [pageLoader]);

//     const formInputObj: any = {
//         a_db_total_records: pageRecords,
//         a_pagination_count: pageCount,
//     };
//     const { handleChange, handleSubmit, values, errors, setErrors, setValues } = useForm(() => { }, {}, formInputObj);

//     return (
//         <>
//         Transaction
//             <div className="transaction-section">
//                 <Container fluid="lg">
//                     <DeductorDetails
//                         deductor="Webakruti Software Pvt. Ltd."
//                         tanno="DELE10221B"
//                         link="/edit"
//                         financialyear={fyYearFormater(user.default_acc_year)}
//                         formtype={`${user.default_tds_type_code} | Q${user.default_quarter_no}`}
//                     />
//                     <div>
//                         <div className="d-flex justify-content-between mb-3 mt-3">
//                             <div>
//                                 <h6 className="fs-18 int-semibold clr-blue">Transactions</h6>
//                             </div>
//                             <div>
//                                 <button className="btn-secondary" onClick={() => console.log("Add New Transaction button click")}>
//                                     Add New Transaction
//                                 </button>
//                             </div>
//                         </div>
//                     </div>
//                     {
//                         pageLoader && <CssLoader />
//                     }

//                     {
//                         !pageLoader &&

//                         <div className="d-flex justify-content-between align-items-center">
//                             <Filter
//                                 baseFilter={filter?.basic_filter ? filter?.basic_filter : []}
//                                 advFilter={filter?.advance_filter ? filter?.advance_filter : []}
//                                 submit={(values) => {
//                                     setValues({
//                                         ...values,
//                                         a_db_total_records: pageRecords,
//                                         a_pagination_count: 10,
//                                     });
//                                     setPageCount(10);
//                                 }}
//                             />
//                         </div>
//                     }

//                     <Datatable
//                         headers={header}
//                         rows={rows}
//                         itemperpage={pageRecords}
//                     />
//                 </Container>
//             </div>
//         </>
//     );
// }



<!-- gh -->

import React, { useEffect, useState } from 'react'
import { Badge, Col, Dropdown, Form, Row, Table } from 'react-bootstrap';
import useForm from '../../../hooks/useForm';
import { addTransaction } from '../../../validate/validateTransaction'
import { REACT_APP_ENV } from '../../../utils/envConfig';
import getReq, { postReq } from '../../../http';
import 'react-toastify/dist/ReactToastify.css';
import { HeaderMasterData } from '../../../components/layout';
import { CssLoader } from '../../../components/loader';
import { dateDMYFormater, dateFormater } from '../../../utils/normConsistent';
import ContextUser from "../../../utils/contextHandler";
import { Loader } from "../../../components/loader";
import Select from "react-select";
import { PanValidation } from '../../../components/panFormGroup';
import { DrawerTop } from '../../../components/drawer';
import Allocation, { allocationReq } from '../../../components/allocation';
import { addDeductorErrors } from '../../../validate/validateDeductor';
const FormGroupInput = ({ name, label, value, handleChange, placeholder, error, disabled = false }: any) => {
    return <Col lg={4}>
        <Form.Group className="mb-10 clr-black int-regular fs-14">
            <Form.Label htmlFor={name}>{label}</Form.Label>
            <Form.Control disabled={disabled} type='text' id={name} name={name} value={value ? value : ""} onChange={handleChange} placeholder={placeholder ? `Enter ${placeholder}` : `Enter ${label}`} />
            <div className="int-regular fs-10 clr-red">{error && <span>{error}</span>}</div>
        </Form.Group>
    </Col>
}

const GHForm = ({ endpoint, data, state, setShow, getSingleGh, globalRef }) => {
    const [addChecked, setAddChecked] = useState(false);
    const [codeParent, setCodeParent] = useState([]);
    const [clientCode, setClientCode] = useState([]);
    const [codeLevel, setCodeLevel] = useState([]);
    const [loader, setLoader] = useState(false);
    const [isSearchable, setIsSearchable] = useState(true);
    const [isClearable, setIsClearable] = useState(true);
    const [pinMasterCode, setPinMasterCode]: any = useState([]);
    const [masters, setMasters] = useState({ state: [], category: [] });
    const [masterLoader, setMasterLaoder] = useState(!HeaderMasterData());
    const addressFields = [{ name: "deducteeMast15gh.add1", label: "Address" }, { name: "deducteeMast15gh.add2", label: "Street Address" }, { name: "deducteeMast15gh.add3", label: "Landmark" }, { name: "deducteeMast15gh.add4", label: "Area" }];
    const contactFields = [{ name: "deducteeMast15gh.stdcode", label: "STD Code" }, { name: "deducteeMast15gh.email_id", label: "Email" }, { name: "deducteeMast15gh.mobileno", label: "Mobile Number" }];
    const frequentFields = [...addressFields.reduce((acc: any, cur) => (acc.push(cur?.name) && acc), []), "city", "pin", "state_code", "country_code", ...contactFields.reduce((acc: any, cur) => (acc.push(cur?.name) && acc), [])];

    const [formObj, setFormobj] = useState(state != "edit" ?
        {
            ...(frequentFields.reduce((acc, cur) => ((Object.assign(acc, { [cur]: "" })) && acc), {})),
            ...(frequentFields.reduce((acc, cur) => ((Object.assign(acc, { [`deductor_${cur}`]: "" })) && acc), {})),
            panno: "",
            client_name: "",
            code_level: "",
            ain_no: "",
            ministry_code: "",
            pao_code: "",
            pao_registration_no: "",
            alternate_mobileno: "",
            ddo_code: "",
            ddo_registration_no: "",
            ministry_name_other: "",
            ministry_state_code: "",
            sub_ministry_code: "",
            gstn_no: "",
            bank_branch_code: "",
            parent_code: "",
            client_type_code: "",
            branch_division: "",
            client_catg_code: "",
            deductor_name: "",
            deductor_desig: "",
            deductor_panno: "",
            deductor_add_change: "",
            deductor_add_change_on: "",
        }
        : data);

    const submit = async (action: any = null) => {
        action
        !action && setLoader(true);
        const response = await postReq({
            url: `${endpoint}${state}-deductor`,
            data: { ...values, deductor_add_change_on: dateFormater(values.deductor_add_change_on, "DD-MMM-YYYY") },
            returnDataKey: "",
            errorCallback: setErrors
        });
        if (response) {
            setShow(false);
        }
        !action && setLoader(false);
    };

    const [panValidation, setPanValidation]: any = useState(false);

    const handlePanValidation = async (data: any = null) => {
        setPanValidation("loading");
        const res = await postReq({
            url: `${REACT_APP_ENV == "PROD" ? "/transactions" : "http://localhost:4003"}/get-deductor-pan-validation`,
            data: { "panno": values.panno },
            returnDataKey: "panValidation"
        });
        if (res === "Y") {
            setPanValidation(true);
            setValues((pre) => ({ ...pre, client_type_code: values.panno.charAt(3) }))
        }
        (res === "N") && setPanValidation(false)
    };

    const [tanValidation, setTanValidation]: any = useState(false);

    const handleTanValidation = async (data: any = null) => {
        const res = await postReq({
            url: `${REACT_APP_ENV == "PROD" ? "/transactions" : "http://localhost:4003"}/get-tan-validation`,
            data: { "tanno": values.tanno },
            returnDataKey: "tanValidation"
        });
        (res) && setErrors((pre) => ({ ...pre, tanno: (res === "N" && "Invalid") }));
        (res) && setTanValidation(res === "Y" ? true : false);
    }

    const codeLevelCode = async () => {
        const res = await getReq({
            url: `${endpoint}get-code-level`,
            returnDataKey: "data"
        });
        setCodeLevel(res);
    }

    const parentCode = async () => {
        const res = await postReq({
            url: `${endpoint}get-parent-code`,
            data: { ...values, code_level: values?.code_level },
            returnDataKey: "result"
        });
        setCodeParent(res);
    }
    const clientTypeCode = async () => {
        const res = await postReq({
            url: `${endpoint}get-client-type-code`,
            data: { ...values, client_type: values?.client_type_code },
            returnDataKey: "result"
        });
        setClientCode(res.data);

    }

    const masterPinCode = async () => {
        const res = await getReq({
            url: `${endpoint}get-pin-master-code`,
            returnDataKey: "data"
        });
        if (res && res.length) {
            setPinMasterCode(res.reduce((acc, curr) => {
                acc.push(curr?.pin_code_detail);
                return acc
            }, []));
        }
    }

    const handlePinSearch = (ele) => {
        if (values?.[ele] && values?.[ele].length == 6) {
            for (let index = 0; index < pinMasterCode.length; index++) {
                if (pinMasterCode[index].includes(values?.[ele])) {
                    const city: any = pinMasterCode[index].split("=>")[3];
                    const stateCode: any = pinMasterCode[index].split("=>")[4];
                    if (ele == "pin") {
                        setValues((pre) => ({ ...pre, state_code: stateCode, city: city ? city : "" }));
                    }
                    if (ele == "deductor_pin") {
                        setValues((pre) => ({ ...pre, deductor_state_code: stateCode, deductor_city: city ? city : "" }));
                    }
                    break;
                };
            }
        }
    }

    const handleAddressClone = (e) => {
        const { checked } = e.target
        setAddChecked(checked);
        const clonedObj = [...addressFields.reduce((acc: any, cur) => (acc.push(cur?.name) && acc), []), "city", "pin", "state_code"].reduce((acc, cur) => {
            acc[`deductor_${cur}`] = checked ? values?.[cur] : "";
            return acc
        }, {});
        setValues((pre) => ({ ...pre, ...clonedObj }));
    }

    const { handleChange, handleSubmit, values, errors, setErrors, setValues } = useForm(
        submit,
        addDeductorErrors,
        formObj
    );



    useEffect(() => {
        const intervalId = setInterval(() => {
            if (HeaderMasterData()) {
                const { get_gmdt_state_mast, get_gmdt_client_catg_mast } = HeaderMasterData();
                setMasters({
                    state: get_gmdt_state_mast ? get_gmdt_state_mast : [],
                    category: get_gmdt_client_catg_mast ? get_gmdt_client_catg_mast : []
                })
                clearInterval(intervalId);
                setMasterLaoder(false);
            }
        }, 1000);
        state == "edit" && handlePanValidation(state != "add" && data);
        state == "edit" && handleTanValidation(state != "add" && data);
    }, [masterLoader])

    useEffect(() => {
        codeLevelCode();
        clientTypeCode();
        masterPinCode();
        if (values?.code_level) {
            parentCode();
        }
    }, [values?.code_level]);

    return (
        <Form className='drawar-form' id="deductor-form">
            <div className='form-body' >
                <Row className='mb-20'>
                    <h6 className='fs-16 int-semibold clr-black mb-20'>Transaction Entry</h6>
                    <Col lg={4}>
                        <Form.Group className="mb-10 clr-black int-regular fs-14">
                            <Form.Label htmlFor='deducteeMast15gh.deductee_catg' >Deductor Category</Form.Label>
                            <Select
                                classNamePrefix="select"
                                isSearchable={isSearchable}
                                isClearable={isClearable}
                                onChange={(e: any) => {
                                    handleChange({ target: { value: e ? e.client_catg_code : "", name: "deducteeMast15gh.deductee_catg" } });
                                }}
                                getOptionLabel={(option: any) => option.client_catg_name}
                                getOptionValue={(option: any) => option.client_catg_code}
                                options={masters?.category}
                                value={masters?.category?.reduce((acc: any, cur: any) => {
                                    if (cur?.client_catg_code == values?.client_catg_code) {
                                        acc = { client_catg_code: cur?.client_catg_code, client_catg_name: cur?.client_catg_name };
                                    }
                                    return acc;
                                }, [])}
                            />
                        </Form.Group>
                    </Col>
                    <Col lg={4}>
                        <PanValidation label="PAN Number" name="deducteeMast15gh.panno" value={values?.panno} error={errors?.panno} disabled={panValidation} placeholder="Enter your PAN Number" handleChange={(e) => {
                            e.target.value.length < 10 && setPanValidation(false);
                            handleChange(e);
                        }} onClickCallback={() => {
                            setErrors({
                                ...errors,
                                panno: values?.panno.length != 10 ? "Pan No is Invalid" : "",
                            });
                            (values?.panno.length == 10 && handlePanValidation())
                        }} />
                    </Col>
                    <FormGroupInput name={`deducteeMast15gh.deductee_name`} label={`Deductee Name`} value={values?.deductee_name} handleChange={handleChange} />
                    <FormGroupInput name={`deducteeMast15gh.deduction_ref_no`} label={`Identification Number`} value={values?.identification_number} handleChange={handleChange} />
                    <Col lg={4}>
                        <Form.Group className="mb-10 clr-black int-regular fs-14">
                            <Form.Label htmlFor='codelevel'>Resident Status</Form.Label>
                            <Select
                                classNamePrefix="select"
                                isSearchable={isSearchable}
                                isClearable={isClearable}
                            />
                        </Form.Group>
                    </Col>
                    {addressFields.map((each, key) => <FormGroupInput key={key} name={each?.name} label={each?.label} value={values?.[each?.name]} error={errors?.[each?.name]} handleChange={handleChange} />)}
                    <Col lg={4}>
                        <Form.Group className="mb-10 clr-black int-regular fs-14">
                            <Form.Label htmlFor='pincode' >Pin Code</Form.Label>
                            <div className="d-flex">
                                <Form.Control id='pincode' type='search' name='deducteeMast15gh.pin' value={values?.pin ? values?.pin : ''} onChange={handleChange} placeholder='Enter PIN' />
                                <button onClick={() => handlePinSearch('pin')} type="button" className='btn'><span className='icon-search clr-careys-pink'></span></button>
                            </div>
                        </Form.Group>
                    </Col>
                    <FormGroupInput name={`deducteeMast15gh.city_code`} label={`City`} value={values?.city} handleChange={handleChange} />
                    <Col lg={4}>
                        <Form.Group className="mb-10 clr-black int-regular fs-14">
                            <Form.Label htmlFor='state' >State</Form.Label>
                            <Select
                                classNamePrefix="select"
                                isSearchable={isSearchable}
                                isClearable={isClearable}
                                onChange={(e: any) => {
                                    handleChange({ target: { value: e ? e.state_code : "", name: "deducteeMast15gh.state_code" } });
                                }}
                                getOptionLabel={(option: any) => option.state_name}
                                getOptionValue={(option: any) => option.state_code}
                                options={masters?.state}
                                value={masters?.state?.reduce((acc: any, cur: any) => {
                                    if (cur?.state_code == values?.state_code) {
                                        acc = { state_code: cur?.state_code, state_name: cur?.state_name };
                                    }
                                    return acc;
                                }, [])}
                            />
                        </Form.Group>
                    </Col>
                    {contactFields.map((each, key) => <FormGroupInput key={key} name={each?.name} label={each?.label} value={values?.[each?.name]} error={errors?.[each?.name]} handleChange={handleChange} />)}
                    <Col lg={4}>
                        <Form.Group className="mb-10 clr-black int-regular fs-14">
                            <Form.Label htmlFor='deducteeMast15gh.bflag' >File Type</Form.Label>
                            <Select
                                classNamePrefix="select"
                                isSearchable={isSearchable}
                                isClearable={isClearable}
                            />
                        </Form.Group>
                        <div className="int-regular fs-10 clr-red">{errors?.parent_code && <span>{errors?.parent_code}</span>}</div>
                    </Col>
                    <Col lg={4}>
                        <Form.Group className="mb-10 clr-black int-regular fs-14">
                            <Form.Label htmlFor='parentcode' >Reference Number</Form.Label>
                            <Select
                                classNamePrefix="select"
                                isSearchable={isSearchable}
                                isClearable={isClearable}
                            />
                        </Form.Group>
                        <div className="int-regular fs-10 clr-red">{errors?.parent_code && <span>{errors?.parent_code}</span>}</div>
                    </Col>
                    <Col lg={4}>
                        <Form.Group className="mb-10 clr-black int-regular fs-14">
                            <Form.Label htmlFor='parentcode' >PAN Staatus</Form.Label>
                            <Select
                                classNamePrefix="select"
                                isSearchable={isSearchable}
                                isClearable={isClearable}
                            />
                        </Form.Group>
                        <div className="int-regular fs-10 clr-red">{errors?.parent_code && <span>{errors?.parent_code}</span>}</div>
                    </Col>
                    {[{ name: "deducteeMast15gh.dob", label: "DOB" }].map((each, key) => <FormGroupInput key={key} name={each?.name} label={each?.label} value={values?.[each?.name]} handleChange={handleChange} error={errors?.[each?.name]} />)}
                    <Col lg={4}>
                        <Form.Group className="mb-10 clr-black int-regular fs-14">
                            <Form.Label htmlFor='parentcode' >Whether assessed to tax under the income Tax Act 1961</Form.Label>
                            <Select
                                classNamePrefix="select"
                                isSearchable={isSearchable}
                                isClearable={isClearable}
                            />
                        </Form.Group>
                        <div className="int-regular fs-10 clr-red">{errors?.parent_code && <span>{errors?.parent_code}</span>}</div>
                    </Col>
                    {[{ name: "deducteeMast15gh.est_declaration_income", label: "Enstimate Income For Declaration" }].map((each, key) => <FormGroupInput key={key} name={each?.name} label={each?.label} value={values?.[each?.name]} handleChange={handleChange} error={errors?.[each?.name]} />)}
                    <Col lg={4}>
                        <Form.Group className="mb-10 clr-black int-regular fs-14">
                            <Form.Label htmlFor='parentcode' >Latest Assesment for year which assessted</Form.Label>
                            <Select
                                classNamePrefix="select"
                                isSearchable={isSearchable}
                                isClearable={isClearable}
                            />
                        </Form.Group>
                        <div className="int-regular fs-10 clr-red">{errors?.parent_code && <span>{errors?.parent_code}</span>}</div>
                    </Col>
                    {[{ name: "deducteeMast15gh.est_total_income", label: "Enstimate Total Income Including Above" }, { name: "deducteeMast15gh.total_no_form", label: "Total Numbe Of Form Filled(Other Than This)" }, { name: "deducteeMast15gh.aggregate_income_amt", label: "Aggregate Amount Of Income(Other Than This)" }, { name: "deducteeMast15gh.declaration_date", label: "Date Of Declaration" }, { name: "deducteeMast15gh.income_amount_paid", label: "Amount Of Income Paid" }, { name: "deducteeMast15gh.income_paid_date", label: "Date Of Income Paid" }].map((each, key) => <FormGroupInput key={key} name={each?.name} label={each?.label} value={values?.[each?.name]} handleChange={handleChange} error={errors?.[each?.name]} />)}
                </Row>
                <form action="">
                    <Row>
                        <Col sm={4}>
                            <Form.Group className="mb-3" controlId="exampleForm.ControlInput1">
                                <Form.Label>Identification No Of Relevant Investment/Account,Etc.</Form.Label>
                                <Form.Control type="email" placeholder="name@example.com" />
                            </Form.Group>
                        </Col>
                        <Col sm={4}>
                            <Form.Group className="mb-3" controlId="exampleForm.ControlInput1">
                                <Form.Label>Section Under Which Tax is Deductable</Form.Label>
                                <Form.Control type="email" placeholder="name@example.com" />
                            </Form.Group>
                        </Col>
                        <Col sm={4}>
                            <Form.Group className="mb-3" controlId="exampleForm.ControlInput1">
                                <Form.Label>Nature Of Income</Form.Label>
                                <Form.Control type="email" placeholder="name@example.com" />
                            </Form.Group>
                        </Col>
                        <Col sm={4}>
                            <Form.Group className="mb-3" controlId="exampleForm.ControlInput1">
                                <Form.Label>Amount Of Income</Form.Label>
                                <Form.Control type="email" placeholder="name@example.com" />
                            </Form.Group>
                        </Col>
                    </Row>
                </form>
                <hr />
                <Table>
                    <thead>
                        <tr>
                            <th className='fs-12 pb-3'>
                                #
                            </th>
                            <th className='fs-12'>
                                <Form.Label htmlFor='accountnu' className='fs-10'>Identification No. Of Relevant Investment/Account Etc.</Form.Label>
                                <Form.Control type="text" id='accountnu' placeholder="Identification No. Of Relevant Investment/Account Etc." />
                            </th>
                            <th className='fs-12'>
                                <Form.Label htmlFor='deductable' className='fs-10'>Section Under Which Tax is Deductable</Form.Label>
                                <Select
                                />
                            </th>
                            <th className='fs-12'>
                                <Form.Label htmlFor='natureincome' className='fs-10'>Nature Of Income</Form.Label>
                                <Form.Control id="natureincome" type="text" placeholder="Nature Of Income" />
                            </th>
                            <th className='fs-12'>
                                <Form.Label htmlFor='ammountincome' className='fs-10'>Ammount Of Income</Form.Label>
                                <Form.Control id='ammountincome' type="text" placeholder="Ammount Of Income" />
                            </th>
                            <th className='fs-12'>
                                <button className='btn-primary'>Add</button>
                            </th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td className='fs-12 pt-2'>1</td>
                            <td className='fs-12'>
                                <Form.Control type="text" readOnly placeholder="" />
                            </td>
                            <td className='fs-12'>
                                <Form.Control type="text" readOnly placeholder="" />
                            </td>
                            <td className='fs-12'>
                                <Form.Control type="text" readOnly placeholder="" />
                            </td>
                            <td className='fs-12'>
                                <Form.Control type="text" readOnly placeholder="" />
                            </td>
                            <td className='fs-12'>
                                <button className="btn-primary">
                                    Edit
                                </button>
                            </td>
                        </tr>
                    </tbody>
                </Table>
            </div>
            <div className="d-flex justify-content-between form-footer">
                <div>
                    <button type='submit' className="btn-primary mrf-5" onClick={handleSubmit} id="submit"
                    >{(state === "add" ? 'Save' : 'Update')}
                        {loader &&
                            <span className='ms-1'>
                                <CssLoader color={"#fff"} size={"10px"} />
                            </span>
                        }</button>
                    <button type='button' className="btn-light mlf-5" onClick={() => setShow(false)}>Cancel</button>
                </div>
            </div>
        </Form>
    )
}

export default GHForm;

## Downloads Old Code

import React, { useState } from "react";
import { Col, Dropdown, Form, Row, Table } from "react-bootstrap";

const colunm = [
	{ filename: "Deductee Details Record", tknnu: "RTT155211", filesize: "2.3 MB", dttm: "02/12/2022, 06:17PM" },
	{ filename: "Deductee Details Record", tknnu: "RTT155212", filesize: "2.4 MB", dttm: "02/12/2022, 06:17PM" },
	{ filename: "Deductee Details Record", tknnu: "RTT155213", filesize: "2.5 MB", dttm: "02/12/2022, 06:17PM" },
	{ filename: "Deductee Details Record", tknnu: "RTT155215", filesize: "2.6 MB", dttm: "02/12/2022, 06:17PM" },
]
const Download = () => {
	const [data, setData] = useState(colunm);
	const [order, setOrder] = useState("ASC");

	const sorting = (col: any) => {
		if (order === "ASC") {
			const sorted = [...colunm].sort((a: any, b: any) =>
				a[col].toLowerCase() > b[col].toLowerCase() ? 1 : -1
			)
			setData(sorted);
			setOrder("DSC");
		}
		if (order === "DSC") {
			const sorted = [...colunm].sort((a: any, b: any) =>
				a[col].toLowerCase() < b[col].toLowerCase() ? 1 : -1
			)
			setData(sorted);
			setOrder("ASC");
		}
	}
	return <>
		<div className="downloadpage mt-20">
			<div className="d-flex justify-content-between  container-section ">
				<h5 className="int-bold fs-24 clr-black">Download</h5>
				<Form.Group controlId="dob">
					<Form.Control type="date" name="dob" placeholder="Date of Birth" />
				</Form.Group>
			</div>
			<div className="download-section mt-20 py-20">
				<Row className="w-100">
					<Col lg={7} className="m-auto">
						<div className="d-flex justify-content-between align-items-center search-filter">
							<Form.Group className="d-flex align-items-center" controlId="formBasicEmail">
								<div className='search-box'>
									<span className='icon-search fs-14 clr-dark-bell'></span>
									<Form.Control type="text" placeholder="Search" />
								</div>
								<button className="btn-secondary mlf-10">Search</button>
							</Form.Group>
							<Dropdown className="share">
								<Dropdown.Toggle variant="success" id="dropdown-basic">
									<span className="icon-share"></span>
								</Dropdown.Toggle>

								<Dropdown.Menu>
									<Dropdown.Item href="# /action-1">Capture Page Data in Excel</Dropdown.Item>
									<Dropdown.Item href="#/action-2">Request Download</Dropdown.Item>
								</Dropdown.Menu>
							</Dropdown>
						</div>
						<div className="mt-30">
							<Table hover className="border">
								<thead>
									<tr>
										<th className="int-semibold fs-12 pointer">
											<div className="d-flex">
												<button onClick={() => sorting("filename")}>FILE NAME </button>
												<div className="arrow">{order == "ASC" ? (<span className="icon-uparrow"></span>) : (<span className="icon-down-arrow"></span>)}</div>
											</div>
										</th>
										<th className="int-semibold fs-12 pointer">
											<div className="d-flex">
												<button onClick={() => sorting("tknnu")}>TOKEN NUMBER</button>
												<div className="arrow">{order == "ASC" ? (<span className="icon-uparrow"></span>) : (<span className="icon-down-arrow"></span>)}</div>
											</div>
										</th>
										<th className="int-semibold fs-12 pointer">
											<div className="d-flex">
												<button onClick={() => sorting("filesize")}>FILE SIZE</button>
												<div className="arrow">{order == "ASC" ? (<span className="icon-uparrow"></span>) : (<span className="icon-down-arrow"></span>)}</div>
											</div>
										</th>
										<th className="int-semibold fs-12 pointer">
											<div className="d-flex">
												<button onClick={() => sorting("dttm")}>DATE AND TIME</button>
												<div className="arrow">{order == "ASC" ? (<span className="icon-uparrow"></span>) : (<span className="icon-down-arrow"></span>)}</div>
											</div>
										</th>
										<th className="int-semibold fs-12 pointer">ACTION</th>
									</tr>
								</thead>
								<tbody>
									{data.map((d) => {
										return (
											<tr>
												<td className="int-regular fs-14">{d.filename}</td>
												<td className="int-regular fs-14">{d.tknnu}</td>
												<td className="int-regular fs-14">{d.filesize}</td>
												<td className="int-regular fs-14">{d.dttm}</td>
												<td className="int-regular fs-14"><button><span className="icon-downloding"></span> Download</button></td>
											</tr>
										)
									})}
								</tbody>
							</Table>
						</div>
					</Col>
				</Row>
			</div>
		</div>
	</>
};

export default Download;

// for text file download
const download = new Downloader({
	url: fileUrl,
    autoStart: true,
});

