---
description: Das- <url> Element gibt eine URL für den Speicherort für diesen Suchconnector an.
ms.assetid: fdc9e138-2e98-4f01-ab7b-0c3dfad5a4dd
title: simpleloation-URL-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c40f45ccecb9a1fb81a64f6d749c5050ed1958a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345670"
---
# <a name="simplelocation-url-element-search-connector-schema"></a><span data-ttu-id="42b63-103">simpleloation-URL-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="42b63-103">simpleLocation url Element (Search Connector Schema)</span></span>

<span data-ttu-id="42b63-104">Das- <url> Element gibt eine URL für den Speicherort für diesen Suchconnector an.</span><span class="sxs-lookup"><span data-stu-id="42b63-104">The <url> element specifies a URL for the location for this search connector.</span></span> <span data-ttu-id="42b63-105">Bei diesem Wert kann es sich um eine reguläre file://-URL handeln, die in RFC 1738 definiert ist ( https://www.ietf.org/rfc/rfc1738.txt) Dokument oder oder eine URL, die das KnownFolders:-Protokoll verwendet.</span><span class="sxs-lookup"><span data-stu-id="42b63-105">This value can be a regular file:// URL as defined in the RFC 1738 (https://www.ietf.org/rfc/rfc1738.txt) document or or a URL that uses the knownfolders: protocol.</span></span> <span data-ttu-id="42b63-106">Dieses Element hat keine untergeordneten Elemente und keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="42b63-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="42b63-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="42b63-107">Syntax</span></span>


```
<!-- url element for simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="42b63-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="42b63-108">Element Information</span></span>



| <span data-ttu-id="42b63-109">Übergeordnetes Element</span><span class="sxs-lookup"><span data-stu-id="42b63-109">Parent Element</span></span>                                                                             | <span data-ttu-id="42b63-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42b63-110">Child Elements</span></span> |
|--------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="42b63-111">simpleloation-Element (Suchconnector-Schema)</span><span class="sxs-lookup"><span data-stu-id="42b63-111">simpleLocation Element (Search Connector Schema)</span></span>](search-schema-sconn-simplelocation.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="42b63-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42b63-112">Remarks</span></span>

<span data-ttu-id="42b63-113">Eine Liste bekannter Ordner-GUIDs finden Sie unter [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid) .</span><span class="sxs-lookup"><span data-stu-id="42b63-113">See [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid) for a list of known folder GUIDs.</span></span> <span data-ttu-id="42b63-114">Verwenden Sie das folgende Format für den Wert dieses Elements, wenn Sie das knownfolder:-Protokoll verwenden.</span><span class="sxs-lookup"><span data-stu-id="42b63-114">Use the following format for the value of this element when using the knownfolder: protocol.</span></span>


```
<url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
```



<span data-ttu-id="42b63-115">In der folgenden Tabelle werden die Windows 7-GUIDs für bekannte Ordner angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42b63-115">The following table shows the Windows 7 known folder GUIDs.</span></span>



| <span data-ttu-id="42b63-116">Bekannter Ordner</span><span class="sxs-lookup"><span data-stu-id="42b63-116">Known folder</span></span>                     | <span data-ttu-id="42b63-117">GUID</span><span class="sxs-lookup"><span data-stu-id="42b63-117">GUID</span></span>                                         |
|----------------------------------|----------------------------------------------|
| <span data-ttu-id="42b63-118">Folderid \_ admintools</span><span class="sxs-lookup"><span data-stu-id="42b63-118">FOLDERID\_AdminTools</span></span>             | <span data-ttu-id="42b63-119">{724ef170-A42D-4fef-9F-26-B6-0E-84-6f-BA-4f}</span><span class="sxs-lookup"><span data-stu-id="42b63-119">{724EF170-A42D-4FEF-9F-26-B6-0E-84-6F-BA-4F}</span></span> |
| <span data-ttu-id="42b63-120">Folderid \_ appupdates</span><span class="sxs-lookup"><span data-stu-id="42b63-120">FOLDERID\_AppUpdates</span></span>             | <span data-ttu-id="42b63-121">{a305ce99-F527-492b-8B-1a-7e-76-FA-98-D6-E4}</span><span class="sxs-lookup"><span data-stu-id="42b63-121">{a305ce99-f527-492b-8b-1a-7e-76-fa-98-d6-e4}</span></span> |
| <span data-ttu-id="42b63-122">Folderid \_ addnewprograms</span><span class="sxs-lookup"><span data-stu-id="42b63-122">FOLDERID\_AddNewPrograms</span></span>         | <span data-ttu-id="42b63-123">{de61d971-5ebc-4f 02-a3-A9-6C-82-89-5E-5C-04}</span><span class="sxs-lookup"><span data-stu-id="42b63-123">{de61d971-5ebc-4f02-a3-a9-6c-82-89-5e-5c-04}</span></span> |
| <span data-ttu-id="42b63-124">Folderid \_ cdburning</span><span class="sxs-lookup"><span data-stu-id="42b63-124">FOLDERID\_CDBurning</span></span>              | <span data-ttu-id="42b63-125">{9e52ab10-F80D-49df-AC-B8-43 00-F5-68-78-55}</span><span class="sxs-lookup"><span data-stu-id="42b63-125">{9E52AB10-F80D-49DF-AC-B8-43-30-F5-68-78-55}</span></span> |
| <span data-ttu-id="42b63-126">Folderid \_ changeremuveprograms</span><span class="sxs-lookup"><span data-stu-id="42b63-126">FOLDERID\_ChangeRemovePrograms</span></span>   | <span data-ttu-id="42b63-127">{df7266ac-9274-4867-8D-55-3B-D6-61-de-87-2D}</span><span class="sxs-lookup"><span data-stu-id="42b63-127">{df7266ac-9274-4867-8d-55-3b-d6-61-de-87-2d}</span></span> |
| <span data-ttu-id="42b63-128">Folderid \_ commonadmintools</span><span class="sxs-lookup"><span data-stu-id="42b63-128">FOLDERID\_CommonAdminTools</span></span>       | <span data-ttu-id="42b63-129">{D0384E7D-BAC3-4797-8F-14-CB-a2-29-B3-92-B5}</span><span class="sxs-lookup"><span data-stu-id="42b63-129">{D0384E7D-BAC3-4797-8F-14-CB-A2-29-B3-92-B5}</span></span> |
| <span data-ttu-id="42b63-130">Folderid \_ commonoemlinks</span><span class="sxs-lookup"><span data-stu-id="42b63-130">FOLDERID\_CommonOEMLinks</span></span>         | <span data-ttu-id="42b63-131">{C1BAE2D0-10df-4334-be-DD-7a-a2-0B-22-7a-9d}</span><span class="sxs-lookup"><span data-stu-id="42b63-131">{C1BAE2D0-10DF-4334-BE-DD-7A-A2-0B-22-7A-9D}</span></span> |
| <span data-ttu-id="42b63-132">Folderid \_ commonprograms</span><span class="sxs-lookup"><span data-stu-id="42b63-132">FOLDERID\_CommonPrograms</span></span>         | <span data-ttu-id="42b63-133">{0139d44e-6afe-49F 2-86-90-3D-AF-ca-E6-FF-B8}</span><span class="sxs-lookup"><span data-stu-id="42b63-133">{0139D44E-6AFE-49F2-86-90-3D-AF-CA-E6-FF-B8}</span></span> |
| <span data-ttu-id="42b63-134">Folderid \_ commonstartmenu</span><span class="sxs-lookup"><span data-stu-id="42b63-134">FOLDERID\_CommonStartMenu</span></span>        | <span data-ttu-id="42b63-135">{A4115719-D62E-491d-AA-7C-E7-4B-8B-E3-B0-67}</span><span class="sxs-lookup"><span data-stu-id="42b63-135">{A4115719-D62E-491D-AA-7C-E7-4B-8B-E3-B0-67}</span></span> |
| <span data-ttu-id="42b63-136">Folderid \_ commonstartup</span><span class="sxs-lookup"><span data-stu-id="42b63-136">FOLDERID\_CommonStartup</span></span>          | <span data-ttu-id="42b63-137">{82a5ea35-D9CD-47c5-96 -29-E1-5D-2F-71-4E-6E}</span><span class="sxs-lookup"><span data-stu-id="42b63-137">{82A5EA35-D9CD-47C5-96-29-E1-5D-2F-71-4E-6E}</span></span> |
| <span data-ttu-id="42b63-138">Folderid \_ commontemplates</span><span class="sxs-lookup"><span data-stu-id="42b63-138">FOLDERID\_CommonTemplates</span></span>        | <span data-ttu-id="42b63-139">{B94237E7-57ac-4347-91-51-B0-8c-6C-32-D1-F7}</span><span class="sxs-lookup"><span data-stu-id="42b63-139">{B94237E7-57AC-4347-91-51-B0-8C-6C-32-D1-F7}</span></span> |
| <span data-ttu-id="42b63-140">Ordner "folderid \_ Computer"</span><span class="sxs-lookup"><span data-stu-id="42b63-140">FOLDERID\_ComputerFolder</span></span>         | <span data-ttu-id="42b63-141">{0ac0837c-BBF8-452A-85-0d-79-D0-8E-66-7C-A7}</span><span class="sxs-lookup"><span data-stu-id="42b63-141">{0AC0837C-BBF8-452A-85-0D-79-D0-8E-66-7C-A7}</span></span> |
| <span data-ttu-id="42b63-142">Ordner-ID \_ conflictfolder</span><span class="sxs-lookup"><span data-stu-id="42b63-142">FOLDERID\_ConflictFolder</span></span>         | <span data-ttu-id="42b63-143">{4bfef B45-347d-4006-A5-be-AC-0C-B0-56-71-92}</span><span class="sxs-lookup"><span data-stu-id="42b63-143">{4bfefb45-347d-4006-a5-be-ac-0c-b0-56-71-92}</span></span> |
| <span data-ttu-id="42b63-144">\_Ordnerid ConnectionsFolder</span><span class="sxs-lookup"><span data-stu-id="42b63-144">FOLDERID\_ConnectionsFolder</span></span>      | <span data-ttu-id="42b63-145">{6f 0cd92b-2e97-45D1-88-FF-B0-D1-86-B8-de-DD}</span><span class="sxs-lookup"><span data-stu-id="42b63-145">{6F0CD92B-2E97-45D1-88-FF-B0-D1-86-B8-DE-DD}</span></span> |
| <span data-ttu-id="42b63-146">Folderid- \_ Kontakte</span><span class="sxs-lookup"><span data-stu-id="42b63-146">FOLDERID\_Contacts</span></span>               | <span data-ttu-id="42b63-147">{56784854-C6CB-462b-81-69-88-E3-50-AC-B8-82}</span><span class="sxs-lookup"><span data-stu-id="42b63-147">{56784854-c6cb-462b-81-69-88-e3-50-ac-b8-82}</span></span> |
| <span data-ttu-id="42b63-148">Folderid \_ ControlPanelFolder</span><span class="sxs-lookup"><span data-stu-id="42b63-148">FOLDERID\_ControlPanelFolder</span></span>     | <span data-ttu-id="42b63-149">{82a74aeb-AEB4-465c-a0-14-D0-97-EE-34-6D-63}</span><span class="sxs-lookup"><span data-stu-id="42b63-149">{82A74AEB-AEB4-465C-A0-14-D0-97-EE-34-6D-63}</span></span> |
| <span data-ttu-id="42b63-150">Folderid- \_ Cookies</span><span class="sxs-lookup"><span data-stu-id="42b63-150">FOLDERID\_Cookies</span></span>                | <span data-ttu-id="42b63-151">{2b0f 765D-C0E9-4171-90-8E-08-A6-11-B8-4f-F6}</span><span class="sxs-lookup"><span data-stu-id="42b63-151">{2B0F765D-C0E9-4171-90-8E-08-A6-11-B8-4F-F6}</span></span> |
| <span data-ttu-id="42b63-152">Folderid \_ Desktop</span><span class="sxs-lookup"><span data-stu-id="42b63-152">FOLDERID\_Desktop</span></span>                | <span data-ttu-id="42b63-153">{B4BFCC3A-DB2C-424C-B0-29-7F-E9-9a-87-C6-41}</span><span class="sxs-lookup"><span data-stu-id="42b63-153">{B4BFCC3A-DB2C-424C-B0-29-7F-E9-9A-87-C6-41}</span></span> |
| <span data-ttu-id="42b63-154">Folderid \_ DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="42b63-154">FOLDERID\_DeviceMetadataStore</span></span>    | <span data-ttu-id="42b63-155">{5ce4a5e9-e4eb-479d-B8-9F-13-0C-02-88-61-55}</span><span class="sxs-lookup"><span data-stu-id="42b63-155">{5ce4a5e9-e4eb-479d-b8-9f-13-0c-02-88-61-55}</span></span> |
| <span data-ttu-id="42b63-156">Folderid- \_ Dokumente</span><span class="sxs-lookup"><span data-stu-id="42b63-156">FOLDERID\_Documents</span></span>              | <span data-ttu-id="42b63-157">{FDD39AD0-238f-46af-AD-B4-6C-85-48-03-69-C7}</span><span class="sxs-lookup"><span data-stu-id="42b63-157">{FDD39AD0-238F-46AF-AD-B4-6C-85-48-03-69-C7}</span></span> |
| <span data-ttu-id="42b63-158">Folderid \_ documentslibrary</span><span class="sxs-lookup"><span data-stu-id="42b63-158">FOLDERID\_DocumentsLibrary</span></span>       | <span data-ttu-id="42b63-159">{7b0db17d-9cd2-4A93-97-33 -46-CC-89-02-2E-7C}</span><span class="sxs-lookup"><span data-stu-id="42b63-159">{7b0db17d-9cd2-4a93-97-33-46-cc-89-02-2e-7c}</span></span> |
| <span data-ttu-id="42b63-160">Folderid- \_ Downloads</span><span class="sxs-lookup"><span data-stu-id="42b63-160">FOLDERID\_Downloads</span></span>              | <span data-ttu-id="42b63-161">{374de 290-123f-4565-91-64-39-C4-92-5E-46-7B}</span><span class="sxs-lookup"><span data-stu-id="42b63-161">{374de290-123f-4565-91-64-39-c4-92-5e-46-7b}</span></span> |
| <span data-ttu-id="42b63-162">Folderid- \_ Favoriten</span><span class="sxs-lookup"><span data-stu-id="42b63-162">FOLDERID\_Favorites</span></span>              | <span data-ttu-id="42b63-163">{1777f-68-68AD-4D8A-87-Bd-30-B7-59-FA-33-DD}</span><span class="sxs-lookup"><span data-stu-id="42b63-163">{1777F761-68AD-4D8A-87-BD-30-B7-59-FA-33-DD}</span></span> |
| <span data-ttu-id="42b63-164">Folderid- \_ Schriftarten</span><span class="sxs-lookup"><span data-stu-id="42b63-164">FOLDERID\_Fonts</span></span>                  | <span data-ttu-id="42b63-165">{FD228CB7-AE11-4AE3-86-4C-16-F3-91-0A-B8-FE}</span><span class="sxs-lookup"><span data-stu-id="42b63-165">{FD228CB7-AE11-4AE3-86-4C-16-F3-91-0A-B8-FE}</span></span> |
| <span data-ttu-id="42b63-166">Folderid- \_ Spiele</span><span class="sxs-lookup"><span data-stu-id="42b63-166">FOLDERID\_Games</span></span>                  | <span data-ttu-id="42b63-167">{cac52c1a-b53d-4edc-92-T7-6B-2E-8a-C1-94-34}</span><span class="sxs-lookup"><span data-stu-id="42b63-167">{cac52c1a-b53d-4edc-92-d7-6b-2e-8a-c1-94-34}</span></span> |
| <span data-ttu-id="42b63-168">Folderid- \_ gametasks</span><span class="sxs-lookup"><span data-stu-id="42b63-168">FOLDERID\_GameTasks</span></span>              | <span data-ttu-id="42b63-169">{54fae61-4dd8-4787 -80-B6-9-2 -20-C4-B7-0}</span><span class="sxs-lookup"><span data-stu-id="42b63-169">{54fae61-4dd8-4787-80-b6-9-2-20-c4-b7-0}</span></span>     |
| <span data-ttu-id="42b63-170">Folderid- \_ Verlauf</span><span class="sxs-lookup"><span data-stu-id="42b63-170">FOLDERID\_History</span></span>                | <span data-ttu-id="42b63-171">{D9DC8A3B-B784-432e-A7-81-5A-11-30-A7-59-63}</span><span class="sxs-lookup"><span data-stu-id="42b63-171">{D9DC8A3B-B784-432E-A7-81-5A-11-30-A7-59-63}</span></span> |
| <span data-ttu-id="42b63-172">Folderid- \_ Heim Netzgruppe</span><span class="sxs-lookup"><span data-stu-id="42b63-172">FOLDERID\_HomeGroup</span></span>              | <span data-ttu-id="42b63-173">{52528a6b-b9e3-4ADD-B6-d-58-8c-2D-BA-84-2D}</span><span class="sxs-lookup"><span data-stu-id="42b63-173">{52528a6b-b9e3-4add-b6-d-58-8c-2d-ba-84-2d}</span></span>  |
| <span data-ttu-id="42b63-174">Folderid \_ implicitappconnections</span><span class="sxs-lookup"><span data-stu-id="42b63-174">FOLDERID\_ImplicitAppShortcuts</span></span>   | <span data-ttu-id="42b63-175">{bcb5256f-79F 6-4cee-B7-25-DC-34-E4-2-FD-46}</span><span class="sxs-lookup"><span data-stu-id="42b63-175">{bcb5256f-79f6-4cee-b7-25-dc-34-e4-2-fd-46}</span></span>  |
| <span data-ttu-id="42b63-176">Folderid \_ Internetcache</span><span class="sxs-lookup"><span data-stu-id="42b63-176">FOLDERID\_InternetCache</span></span>          | <span data-ttu-id="42b63-177">{352481e8-33be-4251-BA-85-60-07-ca-Ed-CF-9d}</span><span class="sxs-lookup"><span data-stu-id="42b63-177">{352481E8-33BE-4251-BA-85-60-07-CA-ED-CF-9D}</span></span> |
| <span data-ttu-id="42b63-178">Ordner-ID \_ Internetordner</span><span class="sxs-lookup"><span data-stu-id="42b63-178">FOLDERID\_InternetFolder</span></span>         | <span data-ttu-id="42b63-179">{4d9f 7874-4e0c-4904-96-7B-40-B0-D2-0C-3E-4B}</span><span class="sxs-lookup"><span data-stu-id="42b63-179">{4D9F7874-4E0C-4904-96-7B-40-B0-D2-0C-3E-4B}</span></span> |
| <span data-ttu-id="42b63-180">Folderid- \_ Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="42b63-180">FOLDERID\_Libraries</span></span>              | <span data-ttu-id="42b63-181">{1b3ea5dc-B587-4786-B4-EF-BD-1D-C3-32-AE-AE}</span><span class="sxs-lookup"><span data-stu-id="42b63-181">{1b3ea5dc-b587-4786-b4-ef-bd-1d-c3-32-ae-ae}</span></span> |
| <span data-ttu-id="42b63-182">Folderid- \_ Links</span><span class="sxs-lookup"><span data-stu-id="42b63-182">FOLDERID\_Links</span></span>                  | <span data-ttu-id="42b63-183">{bfb9d5e0-c6a9-404C-B2-B2-AE-6D-B6-AF-49-68}</span><span class="sxs-lookup"><span data-stu-id="42b63-183">{bfb9d5e0-c6a9-404c-b2-b2-ae-6d-b6-af-49-68}</span></span> |
| <span data-ttu-id="42b63-184">Folderid \_ LocalAppData</span><span class="sxs-lookup"><span data-stu-id="42b63-184">FOLDERID\_LocalAppData</span></span>           | <span data-ttu-id="42b63-185">{F1B32785-6f-4bcf-9d-55-7B-8E-7F-15-70-91}</span><span class="sxs-lookup"><span data-stu-id="42b63-185">{F1B32785-6FBA-4FCF-9D-55-7B-8E-7F-15-70-91}</span></span> |
| <span data-ttu-id="42b63-186">Folderid \_ LocalAppDataLow</span><span class="sxs-lookup"><span data-stu-id="42b63-186">FOLDERID\_LocalAppDataLow</span></span>        | <span data-ttu-id="42b63-187">{A520A1A4-1780-4ff6-BD-18-16-73-43-C5-AF-16}</span><span class="sxs-lookup"><span data-stu-id="42b63-187">{A520A1A4-1780-4FF6-BD-18-16-73-43-C5-AF-16}</span></span> |
| <span data-ttu-id="42b63-188">Folderid \_ LocalizedResourcesDir</span><span class="sxs-lookup"><span data-stu-id="42b63-188">FOLDERID\_LocalizedResourcesDir</span></span>  | <span data-ttu-id="42b63-189">{2a00375e-224c-49DE-B8-D1-44-0d-F7-EF-3D-DC}</span><span class="sxs-lookup"><span data-stu-id="42b63-189">{2A00375E-224C-49DE-B8-D1-44-0D-F7-EF-3D-DC}</span></span> |
| <span data-ttu-id="42b63-190">Folderid- \_ Musik</span><span class="sxs-lookup"><span data-stu-id="42b63-190">FOLDERID\_Music</span></span>                  | <span data-ttu-id="42b63-191">{4bd8d571-6d19-48d3-be-97-42-22-20-08-0E-43}</span><span class="sxs-lookup"><span data-stu-id="42b63-191">{4BD8D571-6D19-48D3-BE-97-42-22-20-08-0E-43}</span></span> |
| <span data-ttu-id="42b63-192">Folderid \_ musiclibrary</span><span class="sxs-lookup"><span data-stu-id="42b63-192">FOLDERID\_MusicLibrary</span></span>           | <span data-ttu-id="42b63-193">{2112ab0a-c86a-4ffe-a3-68-d-E9-6E-47-1-2E}</span><span class="sxs-lookup"><span data-stu-id="42b63-193">{2112ab0a-c86a-4ffe-a3-68-d-e9-6e-47-1-2e}</span></span>   |
| <span data-ttu-id="42b63-194">Folderid- \_ nthood</span><span class="sxs-lookup"><span data-stu-id="42b63-194">FOLDERID\_NetHood</span></span>                | <span data-ttu-id="42b63-195">{C5ABBF53-E17F-4121-89-00-86-62-6f-C2-C9-73}</span><span class="sxs-lookup"><span data-stu-id="42b63-195">{C5ABBF53-E17F-4121-89-00-86-62-6F-C2-C9-73}</span></span> |
| <span data-ttu-id="42b63-196">Folderid \_ networkfolder</span><span class="sxs-lookup"><span data-stu-id="42b63-196">FOLDERID\_NetworkFolder</span></span>          | <span data-ttu-id="42b63-197">{D20BEEC4-5ca8-4905-AE-3B-BF-25-1E-a0-9B-53}</span><span class="sxs-lookup"><span data-stu-id="42b63-197">{D20BEEC4-5CA8-4905-AE-3B-BF-25-1E-A0-9B-53}</span></span> |
| <span data-ttu-id="42b63-198">Folderid \_ originalimages</span><span class="sxs-lookup"><span data-stu-id="42b63-198">FOLDERID\_OriginalImages</span></span>         | <span data-ttu-id="42b63-199">{2c36c0aa-5812-4b87-BF-D0-4C-D0-DF-B1-9B-39}</span><span class="sxs-lookup"><span data-stu-id="42b63-199">{2C36C0AA-5812-4b87-bf-d0-4c-d0-df-b1-9b-39}</span></span> |
| <span data-ttu-id="42b63-200">Folderid- \_ Photoalben</span><span class="sxs-lookup"><span data-stu-id="42b63-200">FOLDERID\_PhotoAlbums</span></span>            | <span data-ttu-id="42b63-201">{69d2cf90-FC33-4fb7-9a-0C-EB-B0-F0-FC-B4-3C}</span><span class="sxs-lookup"><span data-stu-id="42b63-201">{69D2CF90-FC33-4FB7-9A-0C-EB-B0-F0-FC-B4-3C}</span></span> |
| <span data-ttu-id="42b63-202">Folderid- \_ Bilder</span><span class="sxs-lookup"><span data-stu-id="42b63-202">FOLDERID\_Pictures</span></span>               | <span data-ttu-id="42b63-203">{33E28130-4E1E-4676-83-5A-98-39-5C-3B-C3-BB}</span><span class="sxs-lookup"><span data-stu-id="42b63-203">{33E28130-4E1E-4676-83-5A-98-39-5C-3B-C3-BB}</span></span> |
| <span data-ttu-id="42b63-204">Folderid \_ pictureslibrary</span><span class="sxs-lookup"><span data-stu-id="42b63-204">FOLDERID\_PicturesLibrary</span></span>        | <span data-ttu-id="42b63-205">{a990ae9f-a03b-4e80-94-BC-99-12-T7-50-41-4}</span><span class="sxs-lookup"><span data-stu-id="42b63-205">{a990ae9f-a03b-4e80-94-bc-99-12-d7-50-41-4}</span></span>  |
| <span data-ttu-id="42b63-206">Folderid- \_ Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="42b63-206">FOLDERID\_Playlists</span></span>              | <span data-ttu-id="42b63-207">{DE92C1C7-837f-4f 69-a3-BB-86-E6-31-20-4a-23}</span><span class="sxs-lookup"><span data-stu-id="42b63-207">{DE92C1C7-837F-4F69-A3-BB-86-E6-31-20-4A-23}</span></span> |
| <span data-ttu-id="42b63-208">Ordner-ID ( \_ Ordner)</span><span class="sxs-lookup"><span data-stu-id="42b63-208">FOLDERID\_PrintersFolder</span></span>         | <span data-ttu-id="42b63-209">{76fc4e2d-D6AD-4519-A6-63 -37-Bd-56-06-81-85}</span><span class="sxs-lookup"><span data-stu-id="42b63-209">{76FC4E2D-D6AD-4519-A6-63-37-BD-56-06-81-85}</span></span> |
| <span data-ttu-id="42b63-210">Folderid- \_ printhood</span><span class="sxs-lookup"><span data-stu-id="42b63-210">FOLDERID\_PrintHood</span></span>              | <span data-ttu-id="42b63-211">{9274bd8d-CFD1-41c3-B3-5E-B1-3F-55-A7-58-F4}</span><span class="sxs-lookup"><span data-stu-id="42b63-211">{9274BD8D-CFD1-41C3-B3-5E-B1-3F-55-A7-58-F4}</span></span> |
| <span data-ttu-id="42b63-212">Folderid- \_ Profil</span><span class="sxs-lookup"><span data-stu-id="42b63-212">FOLDERID\_Profile</span></span>                | <span data-ttu-id="42b63-213">{5e6c858f-0E22-4760-9a-FE-EA-33-17-B6-71-73}</span><span class="sxs-lookup"><span data-stu-id="42b63-213">{5E6C858F-0E22-4760-9A-FE-EA-33-17-B6-71-73}</span></span> |
| <span data-ttu-id="42b63-214">Folderid- \_ programmdata</span><span class="sxs-lookup"><span data-stu-id="42b63-214">FOLDERID\_ProgramData</span></span>            | <span data-ttu-id="42b63-215">{62ab5d82-FDC1-4dc3-A9-DD-07-0d-1D-49-5D-97}</span><span class="sxs-lookup"><span data-stu-id="42b63-215">{62AB5D82-FDC1-4DC3-A9-DD-07-0D-1D-49-5D-97}</span></span> |
| <span data-ttu-id="42b63-216">Folderid \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="42b63-216">FOLDERID\_ProgramFilesX86</span></span>        | <span data-ttu-id="42b63-217">{7c5a40ef-A0FB-4bfc-87-4a-C0-F2-E0-B9-FA-8E}</span><span class="sxs-lookup"><span data-stu-id="42b63-217">{7C5A40EF-A0FB-4BFC-87-4A-C0-F2-E0-B9-FA-8E}</span></span> |
| <span data-ttu-id="42b63-218">Folderid \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="42b63-218">FOLDERID\_ProgramFilesCommonX86</span></span>  | <span data-ttu-id="42b63-219">{DE974D24-D9C6-4d3e-BF-91-F4-45-51 -20-B9-17}</span><span class="sxs-lookup"><span data-stu-id="42b63-219">{DE974D24-D9C6-4D3E-BF-91-F4-45-51-20-B9-17}</span></span> |
| <span data-ttu-id="42b63-220">Folderid \_ ProgramFilesX64</span><span class="sxs-lookup"><span data-stu-id="42b63-220">FOLDERID\_ProgramFilesX64</span></span>        | <span data-ttu-id="42b63-221">{6d809377-6af0-444b-89-57-a3-77-3F-02-20-0E}</span><span class="sxs-lookup"><span data-stu-id="42b63-221">{6d809377-6af0-444b-89-57-a3-77-3f-02-20-0e}</span></span> |
| <span data-ttu-id="42b63-222">Folderid \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="42b63-222">FOLDERID\_ProgramFilesCommonX64</span></span>  | <span data-ttu-id="42b63-223">{6365d5a7-f0d-45e5-87-F6-d-A5-6B-6a-4f-7D}</span><span class="sxs-lookup"><span data-stu-id="42b63-223">{6365d5a7-f0d-45e5-87-f6-d-a5-6b-6a-4f-7d}</span></span>   |
| <span data-ttu-id="42b63-224">Folderid- \_ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="42b63-224">FOLDERID\_ProgramFiles</span></span>           | <span data-ttu-id="42b63-225">{905E63B6-C1BF-494E-B2-9c-65-B7-32-D3-D2-1a}</span><span class="sxs-lookup"><span data-stu-id="42b63-225">{905e63b6-c1bf-494e-b2-9c-65-b7-32-d3-d2-1a}</span></span> |
| <span data-ttu-id="42b63-226">Folderid \_ programfilescommon</span><span class="sxs-lookup"><span data-stu-id="42b63-226">FOLDERID\_ProgramFilesCommon</span></span>     | <span data-ttu-id="42b63-227">{F7F1ED05-9F 6D-47a2-AA-AE-29-D3-17-C6-F0-66}</span><span class="sxs-lookup"><span data-stu-id="42b63-227">{F7F1ED05-9F6D-47A2-AA-AE-29-D3-17-C6-F0-66}</span></span> |
| <span data-ttu-id="42b63-228">Folderid- \_ Programme</span><span class="sxs-lookup"><span data-stu-id="42b63-228">FOLDERID\_Programs</span></span>               | <span data-ttu-id="42b63-229">{A77F5D77-2e2b-44c3-A6-a2-ab-A6-01-05-4a-51}</span><span class="sxs-lookup"><span data-stu-id="42b63-229">{A77F5D77-2E2B-44C3-A6-A2-AB-A6-01-05-4A-51}</span></span> |
| <span data-ttu-id="42b63-230">Folderid \_ Public</span><span class="sxs-lookup"><span data-stu-id="42b63-230">FOLDERID\_Public</span></span>                 | <span data-ttu-id="42b63-231">{DFDF76A2-C82A-4d63-90-6a-56-44-AC-45-73-85}</span><span class="sxs-lookup"><span data-stu-id="42b63-231">{DFDF76A2-C82A-4D63-90-6A-56-44-AC-45-73-85}</span></span> |
| <span data-ttu-id="42b63-232">Folderid \_ publicdesktop</span><span class="sxs-lookup"><span data-stu-id="42b63-232">FOLDERID\_PublicDesktop</span></span>          | <span data-ttu-id="42b63-233">{C4AA340D-F20F-4863-AF-EF-F8-7e-F2-E6-BA-25}</span><span class="sxs-lookup"><span data-stu-id="42b63-233">{C4AA340D-F20F-4863-AF-EF-F8-7E-F2-E6-BA-25}</span></span> |
| <span data-ttu-id="42b63-234">Folderid \_ publicdocuments</span><span class="sxs-lookup"><span data-stu-id="42b63-234">FOLDERID\_PublicDocuments</span></span>        | <span data-ttu-id="42b63-235">{ED4824AF-DCE4-45a8-81-E2-FC-79-65-08-36-34}</span><span class="sxs-lookup"><span data-stu-id="42b63-235">{ED4824AF-DCE4-45A8-81-E2-FC-79-65-08-36-34}</span></span> |
| <span data-ttu-id="42b63-236">Ordner-ID \_ publicdownloads</span><span class="sxs-lookup"><span data-stu-id="42b63-236">FOLDERID\_PublicDownloads</span></span>        | <span data-ttu-id="42b63-237">{3d644c9b-1sb8-4f 30-9B-45-F6-70-23-5F-79-C0}</span><span class="sxs-lookup"><span data-stu-id="42b63-237">{3d644c9b-1fb8-4f30-9b-45-f6-70-23-5f-79-c0}</span></span> |
| <span data-ttu-id="42b63-238">Folderid \_ PublicGameTasks</span><span class="sxs-lookup"><span data-stu-id="42b63-238">FOLDERID\_PublicGameTasks</span></span>        | <span data-ttu-id="42b63-239">{debf2536-e1a8-4c59-B6-a2-41-45-86-47-6a-EA}</span><span class="sxs-lookup"><span data-stu-id="42b63-239">{debf2536-e1a8-4c59-b6-a2-41-45-86-47-6a-ea}</span></span> |
| <span data-ttu-id="42b63-240">Folderid \_ publicmusic</span><span class="sxs-lookup"><span data-stu-id="42b63-240">FOLDERID\_PublicMusic</span></span>            | <span data-ttu-id="42b63-241">{3214fab5-9757 -4298-BB-61-92-A9-de-AA-44-ff}</span><span class="sxs-lookup"><span data-stu-id="42b63-241">{3214FAB5-9757-4298-BB-61-92-A9-DE-AA-44-FF}</span></span> |
| <span data-ttu-id="42b63-242">Folderid \_ publicpictures</span><span class="sxs-lookup"><span data-stu-id="42b63-242">FOLDERID\_PublicPictures</span></span>         | <span data-ttu-id="42b63-243">{B6EBFB86-6907-413c-9a-F7-4f-C2-ab-F0-7C-C5}</span><span class="sxs-lookup"><span data-stu-id="42b63-243">{B6EBFB86-6907-413C-9A-F7-4F-C2-AB-F0-7C-C5}</span></span> |
| <span data-ttu-id="42b63-244">Folderid \_ publicringtones</span><span class="sxs-lookup"><span data-stu-id="42b63-244">FOLDERID\_PublicRingtones</span></span>        | <span data-ttu-id="42b63-245">{E555AB60-153b-4d17-9F-04-A5-FE-99-FC-15-EC}</span><span class="sxs-lookup"><span data-stu-id="42b63-245">{E555AB60-153B-4D17-9F-04-A5-FE-99-FC-15-EC}</span></span> |
| <span data-ttu-id="42b63-246">Folderid \_ publicvideos</span><span class="sxs-lookup"><span data-stu-id="42b63-246">FOLDERID\_PublicVideos</span></span>           | <span data-ttu-id="42b63-247">{2400183a-6185-49fb-a2-D8-4a-39-2a-60-2B-a3}</span><span class="sxs-lookup"><span data-stu-id="42b63-247">{2400183A-6185-49FB-A2-D8-4A-39-2A-60-2B-A3}</span></span> |
| <span data-ttu-id="42b63-248">Folderid- \_ Schnellstart</span><span class="sxs-lookup"><span data-stu-id="42b63-248">FOLDERID\_QuickLaunch</span></span>            | <span data-ttu-id="42b63-249">{52a4b021-7b75-48a9-9F-6B-4B-87-a2-10-BC-8F}</span><span class="sxs-lookup"><span data-stu-id="42b63-249">{52a4f021-7b75-48a9-9f-6b-4b-87-a2-10-bc-8f}</span></span> |
| <span data-ttu-id="42b63-250">Folderid \_ aktuell</span><span class="sxs-lookup"><span data-stu-id="42b63-250">FOLDERID\_Recent</span></span>                 | <span data-ttu-id="42b63-251">{AE50C081-EBD2-438a-86-55-8a-09-2E-34-98-7a}</span><span class="sxs-lookup"><span data-stu-id="42b63-251">{AE50C081-EBD2-438A-86-55-8A-09-2E-34-98-7A}</span></span> |
| <span data-ttu-id="42b63-252">Folderid \_ recordedtvlibrary</span><span class="sxs-lookup"><span data-stu-id="42b63-252">FOLDERID\_RecordedTVLibrary</span></span>      | <span data-ttu-id="42b63-253">{1a6f dba2-f42d-4358-A7-98-B7-4D-74-59-26-C5}</span><span class="sxs-lookup"><span data-stu-id="42b63-253">{1a6fdba2-f42d-4358-a7-98-b7-4d-74-59-26-c5}</span></span> |
| <span data-ttu-id="42b63-254">Folderid \_ recyclebinfolder</span><span class="sxs-lookup"><span data-stu-id="42b63-254">FOLDERID\_RecycleBinFolder</span></span>       | <span data-ttu-id="42b63-255">{B7534046-3ecb-4c18-be-4E-64-CD-4C-B7-D6-AC}</span><span class="sxs-lookup"><span data-stu-id="42b63-255">{B7534046-3ECB-4C18-BE-4E-64-CD-4C-B7-D6-AC}</span></span> |
| <span data-ttu-id="42b63-256">Folderid \_ resourceDir</span><span class="sxs-lookup"><span data-stu-id="42b63-256">FOLDERID\_ResourceDir</span></span>            | <span data-ttu-id="42b63-257">{8ad10c31-2adb-4296-A8-F7-E4-70-12 -32-C9-72}</span><span class="sxs-lookup"><span data-stu-id="42b63-257">{8AD10C31-2ADB-4296-A8-F7-E4-70-12-32-C9-72}</span></span> |
| <span data-ttu-id="42b63-258">Folderid- \_ Klingeltöne</span><span class="sxs-lookup"><span data-stu-id="42b63-258">FOLDERID\_Ringtones</span></span>              | <span data-ttu-id="42b63-259">{C870044B-F49E-4126-A9-C3-B5-2a-1F-F4-11-E8}</span><span class="sxs-lookup"><span data-stu-id="42b63-259">{C870044B-F49E-4126-A9-C3-B5-2A-1F-F4-11-E8}</span></span> |
| <span data-ttu-id="42b63-260">Folderid \_ roamingappdata</span><span class="sxs-lookup"><span data-stu-id="42b63-260">FOLDERID\_RoamingAppData</span></span>         | <span data-ttu-id="42b63-261">{3EB685DB-65F9-4CF6-a0-3a-E3-EF-65-72-9F-3D}</span><span class="sxs-lookup"><span data-stu-id="42b63-261">{3EB685DB-65F9-4CF6-A0-3A-E3-EF-65-72-9F-3D}</span></span> |
| <span data-ttu-id="42b63-262">Folderid \_ sampleplaylists</span><span class="sxs-lookup"><span data-stu-id="42b63-262">FOLDERID\_SamplePlaylists</span></span>        | <span data-ttu-id="42b63-263">{15ca69b3-30ee-49c1-AC-E1-6B-5E-C3-72-AF-B5}</span><span class="sxs-lookup"><span data-stu-id="42b63-263">{15CA69B3-30EE-49C1-AC-E1-6B-5E-C3-72-AF-B5}</span></span> |
| <span data-ttu-id="42b63-264">Folderid \_ samplemusic</span><span class="sxs-lookup"><span data-stu-id="42b63-264">FOLDERID\_SampleMusic</span></span>            | <span data-ttu-id="42b63-265">{B250C668-F57D-4ee1-A6-3C-29-0E-E7-D1-AA-1F}</span><span class="sxs-lookup"><span data-stu-id="42b63-265">{B250C668-F57D-4EE1-A6-3C-29-0E-E7-D1-AA-1F}</span></span> |
| <span data-ttu-id="42b63-266">Folderid \_ samplepictures</span><span class="sxs-lookup"><span data-stu-id="42b63-266">FOLDERID\_SamplePictures</span></span>         | <span data-ttu-id="42b63-267">{C4900540-2379-4c75-84-4B-64-E6-FA-F8-71-6B}</span><span class="sxs-lookup"><span data-stu-id="42b63-267">{C4900540-2379-4C75-84-4B-64-E6-FA-F8-71-6B}</span></span> |
| <span data-ttu-id="42b63-268">Folderid \_ samplevideos</span><span class="sxs-lookup"><span data-stu-id="42b63-268">FOLDERID\_SampleVideos</span></span>           | <span data-ttu-id="42b63-269">{859ead94-2e85-48ad-A7-1a-09-69-CB-56-A6-CD}</span><span class="sxs-lookup"><span data-stu-id="42b63-269">{859EAD94-2E85-48AD-A7-1A-09-69-CB-56-A6-CD}</span></span> |
| <span data-ttu-id="42b63-270">Folderid \_ savedgames</span><span class="sxs-lookup"><span data-stu-id="42b63-270">FOLDERID\_SavedGames</span></span>             | <span data-ttu-id="42b63-271">{4c5c32ff-bb9d-43b0-B5-B4-2D-72-E5-4E-AA-A4}</span><span class="sxs-lookup"><span data-stu-id="42b63-271">{4c5c32ff-bb9d-43b0-b5-b4-2d-72-e5-4e-aa-a4}</span></span> |
| <span data-ttu-id="42b63-272">Folderid \_ savedsuchen</span><span class="sxs-lookup"><span data-stu-id="42b63-272">FOLDERID\_SavedSearches</span></span>          | <span data-ttu-id="42b63-273">{7d1d3a04-Debb-4115-95-CF-2F-29-da-29-20-da}</span><span class="sxs-lookup"><span data-stu-id="42b63-273">{7d1d3a04-debb-4115-95-cf-2f-29-da-29-20-da}</span></span> |
| <span data-ttu-id="42b63-274">folderid- \_ Suche \_ csc</span><span class="sxs-lookup"><span data-stu-id="42b63-274">FOLDERID\_SEARCH\_CSC</span></span>            | <span data-ttu-id="42b63-275">{ee32e446-31ca-4aba-81-4f-A5-EB-D2-FD-6D-5E}</span><span class="sxs-lookup"><span data-stu-id="42b63-275">{ee32e446-31ca-4aba-81-4f-a5-eb-d2-fd-6d-5e}</span></span> |
| <span data-ttu-id="42b63-276">folderid \_ - \_ suchmapi</span><span class="sxs-lookup"><span data-stu-id="42b63-276">FOLDERID\_SEARCH\_MAPI</span></span>           | <span data-ttu-id="42b63-277">{98ec0e18-2098-4d44-86-44-66-97-93 -15-a2-81}</span><span class="sxs-lookup"><span data-stu-id="42b63-277">{98ec0e18-2098-4d44-86-44-66-97-93-15-a2-81}</span></span> |
| <span data-ttu-id="42b63-278">Folderid \_ searchhome</span><span class="sxs-lookup"><span data-stu-id="42b63-278">FOLDERID\_SearchHome</span></span>             | <span data-ttu-id="42b63-279">{190337d1-b8ca-4121-A6-39-6D-47-2D-16-97-2a}</span><span class="sxs-lookup"><span data-stu-id="42b63-279">{190337d1-b8ca-4121-a6-39-6d-47-2d-16-97-2a}</span></span> |
| <span data-ttu-id="42b63-280">Folderid \_ SendTo</span><span class="sxs-lookup"><span data-stu-id="42b63-280">FOLDERID\_SendTo</span></span>                 | <span data-ttu-id="42b63-281">{8983036c-27c0-404b-8F-08-10-2D-10-DC-FD-74}</span><span class="sxs-lookup"><span data-stu-id="42b63-281">{8983036C-27C0-404B-8F-08-10-2D-10-DC-FD-74}</span></span> |
| <span data-ttu-id="42b63-282">Folderid \_ Startmenü</span><span class="sxs-lookup"><span data-stu-id="42b63-282">FOLDERID\_StartMenu</span></span>              | <span data-ttu-id="42b63-283">{625b53c3-AB48-4ec1-BA-1F-a1-EF-41-46-FC-19}</span><span class="sxs-lookup"><span data-stu-id="42b63-283">{625B53C3-AB48-4EC1-BA-1F-A1-EF-41-46-FC-19}</span></span> |
| <span data-ttu-id="42b63-284">Folderid- \_ Start</span><span class="sxs-lookup"><span data-stu-id="42b63-284">FOLDERID\_Startup</span></span>                | <span data-ttu-id="42b63-285">{B97D20BB-F46A-4c97-BA-10-5E-36-08-43-08-54}</span><span class="sxs-lookup"><span data-stu-id="42b63-285">{B97D20BB-F46A-4C97-BA-10-5E-36-08-43-08-54}</span></span> |
| <span data-ttu-id="42b63-286">Folderid \_ syncmanagerfolder</span><span class="sxs-lookup"><span data-stu-id="42b63-286">FOLDERID\_SyncManagerFolder</span></span>      | <span data-ttu-id="42b63-287">{43668bf-C14E-49b2-97-C9-74-77 -84-T7-84-B7}</span><span class="sxs-lookup"><span data-stu-id="42b63-287">{43668BF8-C14E-49B2-97-C9-74-77-84-D7-84-B7}</span></span> |
| <span data-ttu-id="42b63-288">\_Ordnerid synkresultorfolder</span><span class="sxs-lookup"><span data-stu-id="42b63-288">FOLDERID\_SyncResultsFolder</span></span>      | <span data-ttu-id="42b63-289">{289a9a43-be44-4057-A4-1B-58-7a-76-T7-E7-F9}</span><span class="sxs-lookup"><span data-stu-id="42b63-289">{289a9a43-be44-4057-a4-1b-58-7a-76-d7-e7-f9}</span></span> |
| <span data-ttu-id="42b63-290">Folderid \_ SyncSetupFolder</span><span class="sxs-lookup"><span data-stu-id="42b63-290">FOLDERID\_SyncSetupFolder</span></span>        | <span data-ttu-id="42b63-291">{f214138-b1d3-4a90-BB-A9-27-CB-C0-C5-38-9a}</span><span class="sxs-lookup"><span data-stu-id="42b63-291">{f214138-b1d3-4a90-bb-a9-27-cb-c0-c5-38-9a}</span></span>  |
| <span data-ttu-id="42b63-292">Folderid- \_ System</span><span class="sxs-lookup"><span data-stu-id="42b63-292">FOLDERID\_System</span></span>                 | <span data-ttu-id="42b63-293">{1ac14e77-02e7-4e5d-B7-44-2E-B1-AE-51-98-B7}</span><span class="sxs-lookup"><span data-stu-id="42b63-293">{1AC14E77-02E7-4E5D-B7-44-2E-B1-AE-51-98-B7}</span></span> |
| <span data-ttu-id="42b63-294">Folderid \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="42b63-294">FOLDERID\_SystemX86</span></span>              | <span data-ttu-id="42b63-295">{D65231B0-B2F1-4857-A4-CE-A8-E7-C6-EA-7D-27}</span><span class="sxs-lookup"><span data-stu-id="42b63-295">{D65231B0-B2F1-4857-A4-CE-A8-E7-C6-EA-7D-27}</span></span> |
| <span data-ttu-id="42b63-296">Folderid- \_ Vorlagen</span><span class="sxs-lookup"><span data-stu-id="42b63-296">FOLDERID\_Templates</span></span>              | <span data-ttu-id="42b63-297">{A63293E8-664E-48dB-a0-79-DF-75-9E-05-09-F7}</span><span class="sxs-lookup"><span data-stu-id="42b63-297">{A63293E8-664E-48DB-A0-79-DF-75-9E-05-09-F7}</span></span> |
| <span data-ttu-id="42b63-298">Folderid \_ Benutzer festgelegt</span><span class="sxs-lookup"><span data-stu-id="42b63-298">FOLDERID\_UserPinned</span></span>             | <span data-ttu-id="42b63-299">{9e3995ab-1F 9c-4b13-B8-27 -48-B2-4B-6C-71-74}</span><span class="sxs-lookup"><span data-stu-id="42b63-299">{9e3995ab-1f9c-4f13-b8-27-48-b2-4b-6c-71-74}</span></span> |
| <span data-ttu-id="42b63-300">Folderid \_ usersfiles</span><span class="sxs-lookup"><span data-stu-id="42b63-300">FOLDERID\_UsersFiles</span></span>             | <span data-ttu-id="42b63-301">{f3ce0f7c-4901-4acc-86-48-D5-D4-4B-04-EF-8F}</span><span class="sxs-lookup"><span data-stu-id="42b63-301">{f3ce0f7c-4901-4acc-86-48-d5-d4-4b-04-ef-8f}</span></span> |
| <span data-ttu-id="42b63-302">Folderid \_ userslibraries</span><span class="sxs-lookup"><span data-stu-id="42b63-302">FOLDERID\_UsersLibraries</span></span>         | <span data-ttu-id="42b63-303">{a302545d-definitiv-464b-ab-E8-61-C8-64-8D-93-9B}</span><span class="sxs-lookup"><span data-stu-id="42b63-303">{a302545d-deff-464b-ab-e8-61-c8-64-8d-93-9b}</span></span> |
| <span data-ttu-id="42b63-304">Folderid \_ User Profiles</span><span class="sxs-lookup"><span data-stu-id="42b63-304">FOLDERID\_UserProfiles</span></span>           | <span data-ttu-id="42b63-305">{0762d272-C50A-4bb0-a3-82-69-7D-CD-72-9B-80}</span><span class="sxs-lookup"><span data-stu-id="42b63-305">{0762D272-C50A-4BB0-A3-82-69-7D-CD-72-9B-80}</span></span> |
| <span data-ttu-id="42b63-306">Folderid \_ userprogramfiles</span><span class="sxs-lookup"><span data-stu-id="42b63-306">FOLDERID\_UserProgramFiles</span></span>       | <span data-ttu-id="42b63-307">{5cd7aee2-2219-4a67-B8-5D-6C-9c-E1-56 -60-CB}</span><span class="sxs-lookup"><span data-stu-id="42b63-307">{5cd7aee2-2219-4a67-b8-5d-6c-9c-e1-56-60-cb}</span></span> |
| <span data-ttu-id="42b63-308">Folderid \_ userprogramfilescommon</span><span class="sxs-lookup"><span data-stu-id="42b63-308">FOLDERID\_UserProgramFilesCommon</span></span> | <span data-ttu-id="42b63-309">{bcbd3057-ca5c-4622-B4-2D-BC-56-dB-0A-E5-16}</span><span class="sxs-lookup"><span data-stu-id="42b63-309">{bcbd3057-ca5c-4622-b4-2d-bc-56-db-0a-e5-16}</span></span> |
| <span data-ttu-id="42b63-310">Folderid- \_ Videos</span><span class="sxs-lookup"><span data-stu-id="42b63-310">FOLDERID\_Videos</span></span>                 | <span data-ttu-id="42b63-311">{18989b1d-99 B5-455b-84-1C-ab-7C-74-E4-DD-FC}</span><span class="sxs-lookup"><span data-stu-id="42b63-311">{18989B1D-99B5-455B-84-1C-AB-7C-74-E4-DD-FC}</span></span> |
| <span data-ttu-id="42b63-312">Folderid \_ videoslibrary {</span><span class="sxs-lookup"><span data-stu-id="42b63-312">FOLDERID\_VideosLibrary {</span></span>        | <span data-ttu-id="42b63-313">491e922f-5643-4af4-A7-EB-4E-7a-13-8D-81-74}</span><span class="sxs-lookup"><span data-stu-id="42b63-313">491e922f-5643-4af4-a7-eb-4e-7a-13-8d-81-74}</span></span>  |
| <span data-ttu-id="42b63-314">Folderid \_ Windows {</span><span class="sxs-lookup"><span data-stu-id="42b63-314">FOLDERID\_Windows {</span></span>              | <span data-ttu-id="42b63-315">F38BF404-1d43-42f2-93-05 -67-de-0B-28-FC-23}</span><span class="sxs-lookup"><span data-stu-id="42b63-315">F38BF404-1D43-42F2-93-05-67-DE-0B-28-FC-23}</span></span>  |



 

## <a name="examples"></a><span data-ttu-id="42b63-316">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42b63-316">Examples</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```




```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



## <a name="related-topics"></a><span data-ttu-id="42b63-317">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="42b63-317">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42b63-318">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="42b63-318">KNOWNFOLDERID</span></span>](/windows/desktop/shell/knownfolderid)
</dt> </dl>

 

 
