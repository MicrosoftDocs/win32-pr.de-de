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
# <a name="extracting-patch-information-as-xml"></a><span data-ttu-id="b9852-103">Extrahieren von Patchinformationen als XML</span><span class="sxs-lookup"><span data-stu-id="b9852-103">Extracting Patch Information as XML</span></span>

<span data-ttu-id="b9852-104">Die Patchsequenzierung und die anwendbarkeits Informationen, die von der [**msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) -Funktion oder der [**extractpatchxmldata**](installer-extractpatchxmldata.md) -Methode zurückgegeben werden, haben das Format eines XML-BLOBs, das die in diesem Thema identifizierten Elemente und Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="b9852-104">The patch sequencing and applicability information that is returned by the [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa) function or the [**ExtractPatchXMLData**](installer-extractpatchxmldata.md) method is in the format of an XML blob that contains the elements and attributes that are identified in this topic.</span></span> <span data-ttu-id="b9852-105">Das XML-BLOB kann für [**msideterminepatchsequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) und [**msidetermineapplicablepatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) anstelle der vollständigen Patchdatei bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b9852-105">The XML blob can be provided to [**MsiDeterminePatchSequence**](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea) and [**MsiDetermineApplicablePatches**](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa) instead of the full patch file.</span></span>

-   <span data-ttu-id="b9852-106">Das msipatch-Element ist das oberste Element des XML-BLOBs und enthält Informationen über den Patch.</span><span class="sxs-lookup"><span data-stu-id="b9852-106">The MsiPatch element is the top element of the XML blob, and contains information about the patch.</span></span>

    <span data-ttu-id="b9852-107">Das schemaVersion-Attribut gibt die Version der Schema Definition an.</span><span class="sxs-lookup"><span data-stu-id="b9852-107">The SchemaVersion attribute specifies the version of the schema definition.</span></span> <span data-ttu-id="b9852-108">Das Schema wird von msipatchanwendbarkeit. xsd angegeben, und die aktuelle Schema Version ist 1.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="b9852-108">The schema is specified by MSIPatchApplicability.xsd and the current schema version is 1.0.0.0.</span></span> <span data-ttu-id="b9852-109">Der Wert des patchguid-Attributs ist der GUID-Patchcode für das Patchpaket, das aus der [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " im [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) des Patches abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b9852-109">The value of the PatchGUID attribute is the GUID patch code for the patch package obtained from the [**Revision Number Summary**](revision-number-summary.md) Property in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span> <span data-ttu-id="b9852-110">Minmsiversion ist die Mindestversion der Windows Installer, die erforderlich ist, um den Patch zu installieren, der aus der Eigenschaft [**Wort Anzahl Zusammenfassung**](word-count-summary.md) abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b9852-110">The MinMsiVersion is the minimum version of the Windows Installer required to install the patch obtained from the [**Word Count Summary**](word-count-summary.md) Property.</span></span>

-   <span data-ttu-id="b9852-111">Das targetproduct-Element ist ein Containerelement für Informationen zu einer Anwendung, auf die ein Patch abzielt.</span><span class="sxs-lookup"><span data-stu-id="b9852-111">The TargetProduct element is a container element for information about an application that a patch targets.</span></span>

    <span data-ttu-id="b9852-112">Wenn der Patch auf mehrere Anwendungen angewendet werden kann, können mehrere targetproduct-Elemente vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b9852-112">There can be multiple TargetProduct elements if the patch can be applied to multiple applications.</span></span> <span data-ttu-id="b9852-113">Die Informationen im targetproduct-Element werden aus Transformationen extrahiert, die in den Patch eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="b9852-113">The information in the TargetProduct element is extracted from transforms that are embedded within the patch.</span></span>

-   <span data-ttu-id="b9852-114">Das targetproductcode-Element enthält den Wert der [**ProductCode**](productcode.md) -Eigenschaft der Zielanwendung, bevor der Patch angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b9852-114">The TargetProductCode element contains the value of the [**ProductCode**](productcode.md) property of the target application before the patch has been applied.</span></span>

    <span data-ttu-id="b9852-115">Wenn der Patch auf mehrere Anwendungen angewendet werden kann, können mehrere targetproductcode-Elemente vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b9852-115">There can be multiple TargetProductCode elements if the patch can be applied to multiple applications.</span></span>

-   <span data-ttu-id="b9852-116">Das updatedproductcode-Element enthält die Produktcode-GUID der Zielanwendung, nachdem der Patch angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b9852-116">The UpdatedProductCode element contains the product code GUID of the target application after the patch is applied.</span></span>

    <span data-ttu-id="b9852-117">Dieses Element ist nur vorhanden, wenn der Patch den Wert der [**ProductCode**](productcode.md) -Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="b9852-117">This element is only present if the patch changes the value of the [**ProductCode**](productcode.md) property.</span></span> <span data-ttu-id="b9852-118">Ein Patch, bei dem der **ProductCode** geändert wird, wird als [Haupt Upgrade](major-upgrades.md)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b9852-118">A patch that changes the **ProductCode** is referred to as a [Major Upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="b9852-119">Das targetversion-Element enthält die [**ProductVersion**](productversion.md) -Eigenschaft der Zielanwendung, bevor der Patch angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b9852-119">The TargetVersion element contains the [**ProductVersion**](productversion.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="b9852-120">Das Update Update-Element enthält den Wert der [**ProductVersion**](productversion.md) -Eigenschaft der Zielanwendung, nachdem der Patch angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b9852-120">The UpdateVersion element contains the value of the [**ProductVersion**](productversion.md) property of the target application after the patch is applied.</span></span>

    <span data-ttu-id="b9852-121">Dieses Element ist nur vorhanden, wenn der Patch den Wert der [**ProductVersion**](productversion.md) -Eigenschaft ändert.</span><span class="sxs-lookup"><span data-stu-id="b9852-121">This element is only present if the patch changes the value of the [**ProductVersion**](productversion.md) property.</span></span> <span data-ttu-id="b9852-122">Das XML-BLOB für einen Patch, der ein [kleines Update](small-updates.md)implementiert, das auch als QFE bezeichnet wird, enthält dieses Element nicht.</span><span class="sxs-lookup"><span data-stu-id="b9852-122">The XML blob for a patch that implements a [Small Update](small-updates.md), also referred to as a QFE, will not include this element.</span></span> <span data-ttu-id="b9852-123">Das XML-BLOB für einen Patch, der ein kleineres Upgrade implementiert, das auch als Service Pack bezeichnet wird, enthält dieses Element.</span><span class="sxs-lookup"><span data-stu-id="b9852-123">The XML blob for a patch that implements a minor upgrade, also referred to as a service pack, will include this element.</span></span>

-   <span data-ttu-id="b9852-124">Das targetlanguage-Element enthält den Wert der [**productlanguage**](productlanguage.md) -Eigenschaft der Zielanwendung, bevor der Patch angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b9852-124">The TargetLanguage element contains the value of the [**ProductLanguage**](productlanguage.md) property of the target application before the patch has been applied.</span></span>
-   <span data-ttu-id="b9852-125">Das updatedlanguages-Element enthält den Wert der [**productlanguage**](productlanguage.md) -Eigenschaft, nachdem der Patch angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b9852-125">The UpdatedLanguages element contains the value of the [**ProductLanguage**](productlanguage.md) property after the patch has been applied.</span></span>
-   <span data-ttu-id="b9852-126">Das UpgradeCode-Element enthält den Wert der [**UpgradeCode**](upgradecode.md) -Eigenschaft der Zielanwendung.</span><span class="sxs-lookup"><span data-stu-id="b9852-126">The UpgradeCode element contains the value of the [**UpgradeCode**](upgradecode.md) property of the target application.</span></span>
-   <span data-ttu-id="b9852-127">Das obsoletedpatch-Element enthält die Patchcodes (GUIDs) der Patches, die von diesem Patch als veraltet angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b9852-127">The ObsoletedPatch element contains the patch codes (GUIDs) of the patches that are specified as obsolete by this patch.</span></span>

    <span data-ttu-id="b9852-128">Die Liste der veralteten Patches wird aus der [**Zusammenfassung der Revisionsnummer**](revision-number-summary.md) im [Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) des Patches abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b9852-128">The list of obsolete patches is obtained from [**Revision Number Summary**](revision-number-summary.md) in the [Summary Information Stream](summary-information-stream.md) of the patch.</span></span>

-   <span data-ttu-id="b9852-129">Das sequencedata-Element enthält patchsequenzierungs Informationen für den Patch.</span><span class="sxs-lookup"><span data-stu-id="b9852-129">The SequenceData element contains patch sequencing information for the patch.</span></span>

    <span data-ttu-id="b9852-130">Es können mehrere sequencedata-Elemente im XML-BLOB vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b9852-130">There can be multiple SequenceData elements in the XML blob.</span></span> <span data-ttu-id="b9852-131">Jedes sequencedata-Element enthält die Informationen in einer Zeile der [msipatchsequence-Tabelle](msipatchsequence-table.md) des Patches.</span><span class="sxs-lookup"><span data-stu-id="b9852-131">Each SequenceData element contains the information in one row of the [MsiPatchSequence table](msipatchsequence-table.md) of the patch.</span></span> <span data-ttu-id="b9852-132">Das sequencedata-Element enthält ein ProductCode-, Sequence-und Attribute-Unterelement für die Informationen in den entsprechenden Feldern in der msipatchsequence-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b9852-132">The SequenceData element contains a ProductCode, Sequence, and Attributes subelement for the information in the corresponding fields in the MsiPatchSequence table.</span></span> <span data-ttu-id="b9852-133">Eine Beschreibung der einzelnen Felder finden Sie im Abschnitt [msipatchsequence-Tabelle](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="b9852-133">See the [MsiPatchSequence table](msipatchsequence-table.md) section for a description of each field.</span></span>

## <a name="extracting-applicability-information"></a><span data-ttu-id="b9852-134">Extrahieren von anwendbarkeits Informationen</span><span class="sxs-lookup"><span data-stu-id="b9852-134">Extracting Applicability Information</span></span>

<span data-ttu-id="b9852-135">Im folgenden Beispiel wird gezeigt, wie die anwendbarkeits Informationen für einen Windows Installer Patch (MSP-Datei) mithilfe von " [**msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)" extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="b9852-135">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) using [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span> <span data-ttu-id="b9852-136">Das extrahierte XML-BLOB basiert auf der Schema Definition in msipatchanwendbarkeit. xsd und wird an szxmldata zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b9852-136">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned to szXMLData.</span></span>


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



<span data-ttu-id="b9852-137">Im folgenden Beispiel wird gezeigt, wie Sie die anwendbarkeits Informationen für einen Windows Installer Patch (MSP-Datei) in XML-Form extrahieren.</span><span class="sxs-lookup"><span data-stu-id="b9852-137">The following example shows you how to extract the applicability information for a Windows Installer Patch (.msp file) in XML form.</span></span> <span data-ttu-id="b9852-138">Das extrahierte XML-BLOB basiert auf der Schema Definition in "msipatchanwendbarkeit. xsd" und wird in "strinpatchxml" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b9852-138">The extracted XML blob is based on the schema definition in MSIPatchApplicability.xsd and returned in strPatchXML.</span></span>

``` syntax
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")
strPatchXML = installer.ExtractPatchXMLData("c:\example\patch.msp")
```

## <a name="patch-applicability-schema-definition"></a><span data-ttu-id="b9852-139">Schema Definition für patchanwendbarkeit</span><span class="sxs-lookup"><span data-stu-id="b9852-139">Patch Applicability Schema Definition</span></span>

<span data-ttu-id="b9852-140">Kopieren Sie den folgenden Text in Editor oder einen anderen Text-Editor, um die Schema Definitionsdatei für die patchanwendungsinformationen im XML-BLOB zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9852-140">Copy the following text into Notepad or another text editor to create the schema definition file for the patch applicability information in the XML blob.</span></span> <span data-ttu-id="b9852-141">Nennen Sie diese Datei "msipatchanwendbarkeit. xsd".</span><span class="sxs-lookup"><span data-stu-id="b9852-141">Name this file MSIPatchApplicability.XSD.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b9852-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b9852-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9852-143">**Extractpatchxmldata**</span><span class="sxs-lookup"><span data-stu-id="b9852-143">**ExtractPatchXMLData**</span></span>](installer-extractpatchxmldata.md)
</dt> <dt>

[<span data-ttu-id="b9852-144">**Msideterminepatchsequence**</span><span class="sxs-lookup"><span data-stu-id="b9852-144">**MsiDeterminePatchSequence**</span></span>](/windows/desktop/api/Msi/nf-msi-msideterminepatchsequencea)
</dt> <dt>

[<span data-ttu-id="b9852-145">**Msidetermineapplicablepatches**</span><span class="sxs-lookup"><span data-stu-id="b9852-145">**MsiDetermineApplicablePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msidetermineapplicablepatchesa)
</dt> <dt>

[<span data-ttu-id="b9852-146">**Msiextractpatchxmldata**</span><span class="sxs-lookup"><span data-stu-id="b9852-146">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> </dl>

 

 



