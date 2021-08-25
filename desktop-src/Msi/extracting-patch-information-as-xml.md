---
description: Die Patchsequenzierungs- und Anwendbarkeitsinformationen, die von der MsiExtractPatchXMLData-Funktion oder der ExtractPatchXMLData-Methode zurückgegeben werden, haben das Format eines XML-Blobs, das die in diesem Thema identifizierten Elemente und Attribute enthält.
ms.assetid: ea40ed1d-1ef9-44f3-8ae8-3d854e308a49
title: Extrahieren von Patchinformationen als XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0574d953609b467c42467853f540dc85c9c24a31c07b3b3d006eaa6633472d53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821680"
---
# <a name="extracting-patch-information-as-xml"></a>Extrahieren von Patchinformationen als XML

Die Patchsequenzierungs- und Anwendbarkeitsinformationen, die von der [**MsiExtractPatchXMLData-Funktion**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) oder der [**ExtractPatchXMLData-Methode**](installer-extractpatchxmldata.md) zurückgegeben werden, haben das Format eines XML-Blobs, das die in diesem Thema identifizierten Elemente und Attribute enthält. Das XML-Blob kann anstelle der vollständigen Patchdatei für [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) und [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) bereitgestellt werden.

-   Das MsiPatch-Element ist das oberste Element des XML-Blobs und enthält Informationen zum Patch.

    Das SchemaVersion-Attribut gibt die Version der Schemadefinition an. Das Schema wird von MSIPatchApplicability.xsd angegeben, und die aktuelle Schemaversion ist 1.0.0.0. Der Wert des PatchGUID-Attributs ist der GUID-Patchcode für das Patchpaket, das aus der Eigenschaft Zusammenfassung der [**Revisionsnummer**](revision-number-summary.md) im Zusammenfassungsinformationsstream des Patches ermittelt wurde. [](summary-information-stream.md) MinMsiVersion ist die Mindestversion des Windows Installers, die erforderlich ist, um den Patch zu installieren, der von der Eigenschaft Zusammenfassung der [**Wortanzahl erhalten**](word-count-summary.md) wurde.

-   Das TargetProduct-Element ist ein Containerelement für Informationen zu einer Anwendung, auf die ein Patch zielt.

    Es kann mehrere TargetProduct-Elemente geben, wenn der Patch auf mehrere Anwendungen angewendet werden kann. Die Informationen im TargetProduct-Element werden aus Transformationen extrahiert, die in den Patch eingebettet sind.

-   Das TargetProductCode-Element enthält den Wert der [**ProductCode-Eigenschaft**](productcode.md) der Zielanwendung, bevor der Patch angewendet wurde.

    Es kann mehrere TargetProductCode-Elemente geben, wenn der Patch auf mehrere Anwendungen angewendet werden kann.

-   Das UpdatedProductCode-Element enthält die Produktcode-GUID der Zielanwendung, nachdem der Patch angewendet wurde.

    Dieses Element ist nur vorhanden, wenn der Patch den Wert der [**ProductCode-Eigenschaft**](productcode.md) ändert. Ein Patch, der den **ProductCode ändert,** wird als [Hauptupgrade bezeichnet.](major-upgrades.md)

-   Das TargetVersion-Element enthält die [**ProductVersion-Eigenschaft**](productversion.md) der Zielanwendung, bevor der Patch angewendet wurde.
-   Das UpdateVersion-Element enthält den Wert der [**ProductVersion-Eigenschaft**](productversion.md) der Zielanwendung, nachdem der Patch angewendet wurde.

    Dieses Element ist nur vorhanden, wenn der Patch den Wert der [**ProductVersion-Eigenschaft**](productversion.md) ändert. Das XML-Blob für einen Patch, der ein [Small Update](small-updates.md)implementiert, das auch als QFE bezeichnet wird, enthält dieses Element nicht. Das XML-Blob für einen Patch, der ein kleineres Upgrade implementiert, das auch als Service Pack bezeichnet wird, enthält dieses Element.

-   Das TargetLanguage-Element enthält den Wert der [**ProductLanguage-Eigenschaft**](productlanguage.md) der Zielanwendung, bevor der Patch angewendet wurde.
-   Das UpdatedLanguages-Element enthält den Wert der [**ProductLanguage-Eigenschaft,**](productlanguage.md) nachdem der Patch angewendet wurde.
-   Das UpgradeCode-Element enthält den Wert der [**UpgradeCode-Eigenschaft**](upgradecode.md) der Zielanwendung.
-   Das ObsoletedPatch-Element enthält die Patchcodes (GUIDs) der Patches, die von diesem Patch als veraltet angegeben werden.

    Die Liste der veralteten Patches wird aus der [**Zusammenfassung der Revisionsnummer**](revision-number-summary.md) im [Zusammenfassungsinformationsstream des](summary-information-stream.md) Patches ermittelt.

-   Das SequenceData-Element enthält Informationen zur Patchsequenzierung für den Patch.

    Das XML-Blob kann mehrere SequenceData-Elemente enthalten. Jedes SequenceData-Element enthält die Informationen in einer Zeile der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) des Patches. Das SequenceData-Element enthält ein ProductCode-, Sequence- und Attributes-Unterelement für die Informationen in den entsprechenden Feldern in der MsiPatchSequence-Tabelle. Eine Beschreibung der einzelnen Felde finden Sie im Abschnitt [MsiPatchSequence-Tabelle.](msipatchsequence-table.md)

## <a name="extracting-applicability-information"></a>Extrahieren von Anwendbarkeitsinformationen

Im folgenden Beispiel wird gezeigt, wie Sie die Anwendbarkeitsinformationen für einen Windows Installer Patch (MSP-Datei) mit [**msiExtractPatchXMLData extrahieren.**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) Das extrahierte XML-Blob basiert auf der Schemadefinition in MSIPatchApplicability.xsd und wird an szXMLData zurückgegeben.


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



Im folgenden Beispiel wird gezeigt, wie Sie die Anwendbarkeitsinformationen für einen Windows Installer Patch (MSP-Datei) im XML-Format extrahieren. Das extrahierte XML-Blob basiert auf der Schemadefinition in MSIPatchApplicability.xsd und wird in strPatchXML zurückgegeben.

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a>Patch-Anwendbarkeitsschemadefinition

Kopieren Sie den folgenden Text in Editor oder einen anderen Text-Editor, um die Schemadefinitionsdatei für die Patch-Anwendbarkeitsinformationen im XML-Blob zu erstellen. Nennen Sie diese Datei MSIPatchApplicability.XSD.

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

[**ExtractPatchXMLData**](installer-extractpatchxmldata.md)
</dt> <dt>

[**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



