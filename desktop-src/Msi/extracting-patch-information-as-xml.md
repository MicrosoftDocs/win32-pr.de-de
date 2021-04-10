---
description: Die Patchsequenzierung und die anwendbarkeits Informationen, die von der msiextractpatchxmldata-Funktion oder der extractpatchxmldata-Methode zurückgegeben werden, haben das Format eines XML-BLOBs, das die in diesem Thema identifizierten Elemente und Attribute enthält.
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: Extrahieren von Patchinformationen als XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e1e594d3ff2870ca1aaf87245c537045f95d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130680"
---
# <a name="extracting-patch-information-as-xml"></a>Extrahieren von Patchinformationen als XML

Die Patchsequenzierung und die anwendbarkeits Informationen, die von der [**msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) -Funktion oder der [**extractpatchxmldata**](installer-extractpatchxmldata.md) -Methode zurückgegeben werden, haben das Format eines XML-BLOBs, das die in diesem Thema identifizierten Elemente und Attribute enthält. Das XML-BLOB kann für [**msideterminepatchsequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) und [**msidetermineapplicablepatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) anstelle der vollständigen Patchdatei bereitgestellt werden.

-   Das msipatch-Element ist das oberste Element des XML-BLOBs und enthält Informationen über den Patch.

    Das schemaVersion-Attribut gibt die Version der Schema Definition an. Das Schema wird von msipatchanwendbarkeit. xsd angegeben, und die aktuelle Schema Version ist 1.0.0.0. Der Wert des patchguid-Attributs ist der GUID-Patchcode für das Patchpaket, das aus der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " im [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) des Patches abgerufen wurde. Minmsiversion ist die Mindestversion der Windows Installer, die erforderlich ist, um den Patch zu installieren, der aus der Eigenschaft [**Wort Anzahl Zusammenfassung**](word-count-summary.md) abgerufen wurde.

-   Das targetproduct-Element ist ein Containerelement für Informationen zu einer Anwendung, auf die ein Patch abzielt.

    Wenn der Patch auf mehrere Anwendungen angewendet werden kann, können mehrere targetproduct-Elemente vorhanden sein. Die Informationen im targetproduct-Element werden aus Transformationen extrahiert, die in den Patch eingebettet sind.

-   Das targetproductcode-Element enthält den Wert der [**ProductCode**](productcode.md) -Eigenschaft der Zielanwendung, bevor der Patch angewendet wurde.

    Wenn der Patch auf mehrere Anwendungen angewendet werden kann, können mehrere targetproductcode-Elemente vorhanden sein.

-   Das updatedproductcode-Element enthält die Produktcode-GUID der Zielanwendung, nachdem der Patch angewendet wurde.

    Dieses Element ist nur vorhanden, wenn der Patch den Wert der [**ProductCode**](productcode.md) -Eigenschaft ändert. Ein Patch, bei dem der **ProductCode** geändert wird, wird als [Haupt Upgrade](major-upgrades.md)bezeichnet.

-   Das targetversion-Element enthält die [**ProductVersion**](productversion.md) -Eigenschaft der Zielanwendung, bevor der Patch angewendet wurde.
-   Das Update Update-Element enthält den Wert der [**ProductVersion**](productversion.md) -Eigenschaft der Zielanwendung, nachdem der Patch angewendet wurde.

    Dieses Element ist nur vorhanden, wenn der Patch den Wert der [**ProductVersion**](productversion.md) -Eigenschaft ändert. Das XML-BLOB für einen Patch, der ein [kleines Update](small-updates.md)implementiert, das auch als QFE bezeichnet wird, enthält dieses Element nicht. Das XML-BLOB für einen Patch, der ein kleineres Upgrade implementiert, das auch als Service Pack bezeichnet wird, enthält dieses Element.

-   Das targetlanguage-Element enthält den Wert der [**productlanguage**](productlanguage.md) -Eigenschaft der Zielanwendung, bevor der Patch angewendet wurde.
-   Das updatedlanguages-Element enthält den Wert der [**productlanguage**](productlanguage.md) -Eigenschaft, nachdem der Patch angewendet wurde.
-   Das UpgradeCode-Element enthält den Wert der [**UpgradeCode**](upgradecode.md) -Eigenschaft der Zielanwendung.
-   Das obsoletedpatch-Element enthält die Patchcodes (GUIDs) der Patches, die von diesem Patch als veraltet angegeben werden.

    Die Liste der veralteten Patches wird aus der [**Zusammenfassung der Revisionsnummer**](revision-number-summary.md) im [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) des Patches abgerufen.

-   Das sequencedata-Element enthält patchsequenzierungs Informationen für den Patch.

    Es können mehrere sequencedata-Elemente im XML-BLOB vorhanden sein. Jedes sequencedata-Element enthält die Informationen in einer Zeile der [msipatchsequence-Tabelle](msipatchsequence-table.md) des Patches. Das sequencedata-Element enthält ein ProductCode-, Sequence-und Attribute-Unterelement für die Informationen in den entsprechenden Feldern in der msipatchsequence-Tabelle. Eine Beschreibung der einzelnen Felder finden Sie im Abschnitt [msipatchsequence-Tabelle](msipatchsequence-table.md) .

## <a name="extracting-applicability-information"></a>Extrahieren von anwendbarkeits Informationen

Im folgenden Beispiel wird gezeigt, wie die anwendbarkeits Informationen für einen Windows Installer Patch (MSP-Datei) mithilfe von " [**msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)" extrahiert werden. Das extrahierte XML-BLOB basiert auf der Schema Definition in msipatchanwendbarkeit. xsd und wird an szxmldata zurückgegeben.


```C++
#include <windows.h>
#include <msi.h>

#pragma comment( lib, "msi.lib" )

void main()
{
     TCHAR szPatchPath[] = TEXT("c:\\scratch\\RTM-RTMQFE.msp");
    TCHAR* szXMLData = NULL;
    DWORD cchXMLData = 0;

    UINT uiStatus = ERROR_SUCCESS;

    // Determine size of XML blob buffer.
    if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
         /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
    {
        // cchXMLData now includes size of szXMLData in characters not including terminating NULL
        ++cchXMLData;

        szXMLData = new TCHAR[cchXMLData];
        if (ERROR_SUCCESS == (uiStatus = MsiExtractPatchXMLData(szPatchPath, 
            /*dwReserved: must be 0*/ 0, szXMLData, &cchXMLData)))
        {
            //
            // szXMLData now contains the XML patch applicability blob. This could be
            // provided to MsiDetermineApplicablePatches or MsiDeterminePatchSequence in the
            // proper format to evaluate patch applicability.
            //

        }

        delete [] szXMLData;
        szXMLData = NULL;
    }
}
```



Im folgenden Beispiel wird gezeigt, wie Sie die anwendbarkeits Informationen für einen Windows Installer Patch (MSP-Datei) in XML-Form extrahieren. Das extrahierte XML-BLOB basiert auf der Schema Definition in "msipatchanwendbarkeit. xsd" und wird in "strinpatchxml" zurückgegeben.

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a>Schema Definition für patchanwendbarkeit

Kopieren Sie den folgenden Text in Editor oder einen anderen Text-Editor, um die Schema Definitionsdatei für die patchanwendungsinformationen im XML-BLOB zu erstellen. Nennen Sie diese Datei "msipatchanwendbarkeit. xsd".

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema id="Applicability" 
    targetNamespace="https://www.microsoft.com/msi/patch_applicability.xsd" 
    elementFormDefault="qualified" 
    xmlns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:mstns="https://www.microsoft.com/msi/patch_applicability.xsd" 
    xmlns:xs="https://www.w3.org/2001/XMLSchema">
    
    <xs:element name="MsiPatch">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="TargetProduct" minOccurs="1" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="TargetProductCode" type="ValidateGUID" />
                            <xs:element name="UpdatedProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetVersion" type="ValidateVersion" />
                            <xs:element name="UpdatedVersion" type="Version" minOccurs="0" maxOccurs="1" />
                            <xs:element name="TargetLanguage" type="ValidateLanguage" />
                            <xs:element name="UpdatedLanguages" type="intList" minOccurs="0" maxOccurs="1" />
                            <xs:element name="UpgradeCode" type="ValidateGUID" />
                            <xs:element name="UpdatedUpgradeCode" type="GUID" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                        <xs:attribute name="MinMsiVersion" type="xs:int" />
                    </xs:complexType>
                </xs:element>
                <xs:element name="TargetProductCode" type="GUID" minOccurs="1" maxOccurs="unbounded" />
                <xs:element name="ObsoletedPatch" minOccurs="0" maxOccurs="unbounded" type="GUID" />
                <xs:element name="SequenceData" minOccurs="0" maxOccurs="unbounded">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element name="PatchFamily" type="Identifier" />
                            <xs:element name="ProductCode" type="GUID" minOccurs="0" maxOccurs="1" />
                            <xs:element name="Sequence" type="Version" />
                            <xs:element name="Attributes" type="xs:int" minOccurs="0" maxOccurs="1" />
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:sequence>
            <xs:attribute name="SchemaVersion" type="Version" />
            <xs:attribute name="PatchGUID" type="GUID" />
            <xs:attribute name="MinMsiVersion" type="xs:int" />
            <xs:attribute name="TargetsRTM" type="xs:boolean" use="optional" />
        </xs:complexType>
    </xs:element>
    <xs:simpleType name="GUID">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[0-9A-Fa-f]{8}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{4}-[0-9A-Fa-f]{12}\}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:simpleType name="Version">
        <xs:restriction base="xs:string">
            <xs:pattern value="[0-9]{1,5}(\.[0-9]{1,5}){0,3}" />
        </xs:restriction>
    </xs:simpleType>
    <xs:complexType name="ValidateGUID">
        <xs:simpleContent>
            <xs:extension base="GUID">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateVersion">
        <xs:simpleContent>
            <xs:extension base="Version">
                <xs:attribute name="ComparisonType">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="LessThan" />
                            <xs:enumeration value="LessThanOrEqual" />
                            <xs:enumeration value="Equal" />
                            <xs:enumeration value="GreaterThanOrEqual" />
                            <xs:enumeration value="GreaterThan" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="ComparisonFilter">
                    <xs:simpleType>
                        <xs:restriction base="xs:string">
                            <xs:enumeration value="Major" />
                            <xs:enumeration value="MajorMinor" />
                            <xs:enumeration value="MajorMinorUpdate" />
                            <xs:enumeration value="None" />
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:complexType name="ValidateLanguage">
        <xs:simpleContent>
            <xs:extension base="xs:int">
                <xs:attribute name="Validate" type="xs:boolean" />
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>
    <xs:simpleType name="intList">
        <xs:list itemType="xs:int" />
    </xs:simpleType>
    <xs:simpleType name="Identifier">
        <xs:restriction base="xs:string">
            <xs:pattern value="[_a-zA-Z][_a-zA-Z0-9\.]*" />
        </xs:restriction>
    </xs:simpleType>
</xs:schema>
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Extractpatchxmldata**](installer-extractpatchxmldata.md)
</dt> <dt>

[**Msideterminepatchsequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[**Msidetermineapplicablepatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[**Msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



