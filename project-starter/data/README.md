# **DATA**

## Waste_Geology.csv

- **`Site_ID`: Site ID: an alpha-numeric identification assigned to each site.**
- `Site_Name`: Site Name
- `Ftr_ID`: Feature ID: a unique alpha-numeric value assigned to each feature.
- `Ftr_Name`: Feature Name 
- `Dep_Type_1`: Primary Deposit Type: primary reported deposit type for the site and/or feature.
- `Dep_Type_2`: Other Deposit Type/s: other reported deposit types for the site and/or feature.
- **`Commodity`: Commodity: produced commodity/s reported by the source mine or mining district.**
- **`Ore_Min`: Ore Minerals: minerals identified to be commodities or could be economically beneficial.** 
- **`Gangue_Min`: Gangue Minerals: minerals identified to be economically undesirable.**
- `Remarks`: Remarks: field that contains general remarks not accommodated by the data structure.  
- `Prim_Cit`: Primary Citation: shortened version of the primary citation including author name/s and publication year.  
- `Sec_Cit`: Secondary Citation/s: shortened version of the secondary citation including author name/s and publication year.  
- `Last_Updt`: Last Updated: date the record was last updated.

## Waste_Geology.csv

- **`Site_ID`: Site ID: an alpha-numeric identification assigned to a site**
- `Site_Name`: Site Name: name that best represents the grouping of features.  
- `Ftr_ID`: Feature ID: a unique alpha-numeric value assigned to each feature. The identifier includes the Site ID (`Site_ID`).  
- `Ftr_Name`: Feature Name: known name of the feature.  

- `Rep_Vol`: Reported Volume: reported volume of the waste feature. Associated units are reported in `Rep_V_Ut`.  
- `Rep_V_Ut`: Reported Volume Units: units of the reported volume (`Rep_Vol`).  
- **`Calc_Vol`: Calculated Volume: volume calculated by USGS. Associated units are reported in `Calc_V_Ut`.**
- `Calc_V_Ut`: Calculated Volume Units: units of the calculated volume (`Calc_Vol`) in cubic meters.  
- `DEM_Date`: Digital Elevation Model Date: publication year of the DEM used for volume calculation.  

- `Ton_Factor`: Tonnage Factor: reported tonnage factor of the waste feature. Associated units are reported in `Ton_F_Ut`.  
- `Ton_F_Ut`: Tonnage Factor Units: units of the tonnage factor (`Ton_Factor`).  

- **`Material`: Material reported by the source document. May be elemental or compound form.**
- `Mat_Type`: Material Type: type of material reported (equivalent to feature type).  
- **`Mat_Amnt`: Material Amount: reported amount of material. Associated units are reported in `Mat_Units`.**
- `Mat_Units`: Material Units: units of the material amount (`Mat_Amnt`).  

- **`Grade`: Grade: reported grade of the waste feature material. Associated units are reported in `Grade_Units`.**
- `Grade_Units`: Grade Units: units of grade.  

- `Contained`: Contained: contained commodity amount reported for the waste feature. Associated units are reported in `ContUnits`.  
- `ContUnits`: Contained Units: units of the contained commodity (`Contained`).  

- `Rep_Vol_SI`: Reported Volume SI: reported volume converted to SI units. Associated units are reported in `Rep_Vut_SI`.  
- `Rep_Vut_SI`: Reported Volume SI Units: units of `Rep_Vol_SI`.  

- `Ton_F_SI`: Tonnage Factor SI: tonnage factor converted to SI units. Associated units are reported in `Ton_F_SI_U`.  
- `Ton_F_SI_U`: Tonnage Factor SI Units: units of `Ton_F_SI`.  

- `MatAmntSI`: Material Amount SI: material amount converted to SI units. Associated units are reported in `MatUnitSI`.  
- `MatUnitSI`: Material Units SI: units of `MatAmntSI`.  

- `GradeSI`: Grade SI: grade converted to SI units. Associated units are reported in `GradeUntSI`.  
- `GradeUntSI`: Grade Units SI: units of `GradeSI`.  

- `CntSIComAm`: Contained SI Commodity Amount: contained commodity amount converted to metric tons. Associated units are reported in `CntSIComUt`.  
- `CntSIComUt`: Contained SI Commodity Units: units of `CntSIComAm`.  
- `CntSIComod`: Contained SI Commodity: contained commodity reported as element or compound.  

- `Rsrc_Class`: Resource Classification: classification of the resource as reported in source document.  
- `Rsrc_Code`: Resource Code: standard classification system used for resource reporting.  
- `Rsrc_Date`: Resource Date: year the resource was estimated.  
- `RsrcMethod`: Resource Method: brief description of the resource estimation method.  

- `Remarks`: Remarks: general notes not captured elsewhere in the dataset.  
- `Prim_Cit`: Primary Citation: shortened primary citation including author(s) and year.  
- `Sec_Cit`: Secondary Citation(s): shortened secondary citation(s) including author(s) and year.  
- `Last_Updt`: Last Updated: date the record was last updated.  
