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
# <a name="simplelocation-url-element-search-connector-schema"></a>simpleloation-URL-Element (Suchconnector-Schema)

Das- <url> Element gibt eine URL für den Speicherort für diesen Suchconnector an. Bei diesem Wert kann es sich um eine reguläre file://-URL handeln, die in RFC 1738 definiert ist ( https://www.ietf.org/rfc/rfc1738.txt) Dokument oder oder eine URL, die das KnownFolders:-Protokoll verwendet. Dieses Element hat keine untergeordneten Elemente und keine Attribute.

## <a name="syntax"></a>Syntax


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



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                                             | Untergeordnete Elemente |
|--------------------------------------------------------------------------------------------|----------------|
| [simpleloation-Element (Suchconnector-Schema)](search-schema-sconn-simplelocation.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Eine Liste bekannter Ordner-GUIDs finden Sie unter [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid) . Verwenden Sie das folgende Format für den Wert dieses Elements, wenn Sie das knownfolder:-Protokoll verwenden.


```
<url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
```



In der folgenden Tabelle werden die Windows 7-GUIDs für bekannte Ordner angezeigt.



| Bekannter Ordner                     | GUID                                         |
|----------------------------------|----------------------------------------------|
| Folderid \_ admintools             | {724ef170-A42D-4fef-9F-26-B6-0E-84-6f-BA-4f} |
| Folderid \_ appupdates             | {a305ce99-F527-492b-8B-1a-7e-76-FA-98-D6-E4} |
| Folderid \_ addnewprograms         | {de61d971-5ebc-4f 02-a3-A9-6C-82-89-5E-5C-04} |
| Folderid \_ cdburning              | {9e52ab10-F80D-49df-AC-B8-43 00-F5-68-78-55} |
| Folderid \_ changeremuveprograms   | {df7266ac-9274-4867-8D-55-3B-D6-61-de-87-2D} |
| Folderid \_ commonadmintools       | {D0384E7D-BAC3-4797-8F-14-CB-a2-29-B3-92-B5} |
| Folderid \_ commonoemlinks         | {C1BAE2D0-10df-4334-be-DD-7a-a2-0B-22-7a-9d} |
| Folderid \_ commonprograms         | {0139d44e-6afe-49F 2-86-90-3D-AF-ca-E6-FF-B8} |
| Folderid \_ commonstartmenu        | {A4115719-D62E-491d-AA-7C-E7-4B-8B-E3-B0-67} |
| Folderid \_ commonstartup          | {82a5ea35-D9CD-47c5-96 -29-E1-5D-2F-71-4E-6E} |
| Folderid \_ commontemplates        | {B94237E7-57ac-4347-91-51-B0-8c-6C-32-D1-F7} |
| Ordner "folderid \_ Computer"         | {0ac0837c-BBF8-452A-85-0d-79-D0-8E-66-7C-A7} |
| Ordner-ID \_ conflictfolder         | {4bfef B45-347d-4006-A5-be-AC-0C-B0-56-71-92} |
| \_Ordnerid ConnectionsFolder      | {6f 0cd92b-2e97-45D1-88-FF-B0-D1-86-B8-de-DD} |
| Folderid- \_ Kontakte               | {56784854-C6CB-462b-81-69-88-E3-50-AC-B8-82} |
| Folderid \_ ControlPanelFolder     | {82a74aeb-AEB4-465c-a0-14-D0-97-EE-34-6D-63} |
| Folderid- \_ Cookies                | {2b0f 765D-C0E9-4171-90-8E-08-A6-11-B8-4f-F6} |
| Folderid \_ Desktop                | {B4BFCC3A-DB2C-424C-B0-29-7F-E9-9a-87-C6-41} |
| Folderid \_ DeviceMetadataStore    | {5ce4a5e9-e4eb-479d-B8-9F-13-0C-02-88-61-55} |
| Folderid- \_ Dokumente              | {FDD39AD0-238f-46af-AD-B4-6C-85-48-03-69-C7} |
| Folderid \_ documentslibrary       | {7b0db17d-9cd2-4A93-97-33 -46-CC-89-02-2E-7C} |
| Folderid- \_ Downloads              | {374de 290-123f-4565-91-64-39-C4-92-5E-46-7B} |
| Folderid- \_ Favoriten              | {1777f-68-68AD-4D8A-87-Bd-30-B7-59-FA-33-DD} |
| Folderid- \_ Schriftarten                  | {FD228CB7-AE11-4AE3-86-4C-16-F3-91-0A-B8-FE} |
| Folderid- \_ Spiele                  | {cac52c1a-b53d-4edc-92-T7-6B-2E-8a-C1-94-34} |
| Folderid- \_ gametasks              | {54fae61-4dd8-4787 -80-B6-9-2 -20-C4-B7-0}     |
| Folderid- \_ Verlauf                | {D9DC8A3B-B784-432e-A7-81-5A-11-30-A7-59-63} |
| Folderid- \_ Heim Netzgruppe              | {52528a6b-b9e3-4ADD-B6-d-58-8c-2D-BA-84-2D}  |
| Folderid \_ implicitappconnections   | {bcb5256f-79F 6-4cee-B7-25-DC-34-E4-2-FD-46}  |
| Folderid \_ Internetcache          | {352481e8-33be-4251-BA-85-60-07-ca-Ed-CF-9d} |
| Ordner-ID \_ Internetordner         | {4d9f 7874-4e0c-4904-96-7B-40-B0-D2-0C-3E-4B} |
| Folderid- \_ Bibliotheken              | {1b3ea5dc-B587-4786-B4-EF-BD-1D-C3-32-AE-AE} |
| Folderid- \_ Links                  | {bfb9d5e0-c6a9-404C-B2-B2-AE-6D-B6-AF-49-68} |
| Folderid \_ LocalAppData           | {F1B32785-6f-4bcf-9d-55-7B-8E-7F-15-70-91} |
| Folderid \_ LocalAppDataLow        | {A520A1A4-1780-4ff6-BD-18-16-73-43-C5-AF-16} |
| Folderid \_ LocalizedResourcesDir  | {2a00375e-224c-49DE-B8-D1-44-0d-F7-EF-3D-DC} |
| Folderid- \_ Musik                  | {4bd8d571-6d19-48d3-be-97-42-22-20-08-0E-43} |
| Folderid \_ musiclibrary           | {2112ab0a-c86a-4ffe-a3-68-d-E9-6E-47-1-2E}   |
| Folderid- \_ nthood                | {C5ABBF53-E17F-4121-89-00-86-62-6f-C2-C9-73} |
| Folderid \_ networkfolder          | {D20BEEC4-5ca8-4905-AE-3B-BF-25-1E-a0-9B-53} |
| Folderid \_ originalimages         | {2c36c0aa-5812-4b87-BF-D0-4C-D0-DF-B1-9B-39} |
| Folderid- \_ Photoalben            | {69d2cf90-FC33-4fb7-9a-0C-EB-B0-F0-FC-B4-3C} |
| Folderid- \_ Bilder               | {33E28130-4E1E-4676-83-5A-98-39-5C-3B-C3-BB} |
| Folderid \_ pictureslibrary        | {a990ae9f-a03b-4e80-94-BC-99-12-T7-50-41-4}  |
| Folderid- \_ Wiedergabelisten              | {DE92C1C7-837f-4f 69-a3-BB-86-E6-31-20-4a-23} |
| Ordner-ID ( \_ Ordner)         | {76fc4e2d-D6AD-4519-A6-63 -37-Bd-56-06-81-85} |
| Folderid- \_ printhood              | {9274bd8d-CFD1-41c3-B3-5E-B1-3F-55-A7-58-F4} |
| Folderid- \_ Profil                | {5e6c858f-0E22-4760-9a-FE-EA-33-17-B6-71-73} |
| Folderid- \_ programmdata            | {62ab5d82-FDC1-4dc3-A9-DD-07-0d-1D-49-5D-97} |
| Folderid \_ ProgramFilesX86        | {7c5a40ef-A0FB-4bfc-87-4a-C0-F2-E0-B9-FA-8E} |
| Folderid \_ ProgramFilesCommonX86  | {DE974D24-D9C6-4d3e-BF-91-F4-45-51 -20-B9-17} |
| Folderid \_ ProgramFilesX64        | {6d809377-6af0-444b-89-57-a3-77-3F-02-20-0E} |
| Folderid \_ ProgramFilesCommonX64  | {6365d5a7-f0d-45e5-87-F6-d-A5-6B-6a-4f-7D}   |
| Folderid- \_ Programmdateien           | {905E63B6-C1BF-494E-B2-9c-65-B7-32-D3-D2-1a} |
| Folderid \_ programfilescommon     | {F7F1ED05-9F 6D-47a2-AA-AE-29-D3-17-C6-F0-66} |
| Folderid- \_ Programme               | {A77F5D77-2e2b-44c3-A6-a2-ab-A6-01-05-4a-51} |
| Folderid \_ Public                 | {DFDF76A2-C82A-4d63-90-6a-56-44-AC-45-73-85} |
| Folderid \_ publicdesktop          | {C4AA340D-F20F-4863-AF-EF-F8-7e-F2-E6-BA-25} |
| Folderid \_ publicdocuments        | {ED4824AF-DCE4-45a8-81-E2-FC-79-65-08-36-34} |
| Ordner-ID \_ publicdownloads        | {3d644c9b-1sb8-4f 30-9B-45-F6-70-23-5F-79-C0} |
| Folderid \_ PublicGameTasks        | {debf2536-e1a8-4c59-B6-a2-41-45-86-47-6a-EA} |
| Folderid \_ publicmusic            | {3214fab5-9757 -4298-BB-61-92-A9-de-AA-44-ff} |
| Folderid \_ publicpictures         | {B6EBFB86-6907-413c-9a-F7-4f-C2-ab-F0-7C-C5} |
| Folderid \_ publicringtones        | {E555AB60-153b-4d17-9F-04-A5-FE-99-FC-15-EC} |
| Folderid \_ publicvideos           | {2400183a-6185-49fb-a2-D8-4a-39-2a-60-2B-a3} |
| Folderid- \_ Schnellstart            | {52a4b021-7b75-48a9-9F-6B-4B-87-a2-10-BC-8F} |
| Folderid \_ aktuell                 | {AE50C081-EBD2-438a-86-55-8a-09-2E-34-98-7a} |
| Folderid \_ recordedtvlibrary      | {1a6f dba2-f42d-4358-A7-98-B7-4D-74-59-26-C5} |
| Folderid \_ recyclebinfolder       | {B7534046-3ecb-4c18-be-4E-64-CD-4C-B7-D6-AC} |
| Folderid \_ resourceDir            | {8ad10c31-2adb-4296-A8-F7-E4-70-12 -32-C9-72} |
| Folderid- \_ Klingeltöne              | {C870044B-F49E-4126-A9-C3-B5-2a-1F-F4-11-E8} |
| Folderid \_ roamingappdata         | {3EB685DB-65F9-4CF6-a0-3a-E3-EF-65-72-9F-3D} |
| Folderid \_ sampleplaylists        | {15ca69b3-30ee-49c1-AC-E1-6B-5E-C3-72-AF-B5} |
| Folderid \_ samplemusic            | {B250C668-F57D-4ee1-A6-3C-29-0E-E7-D1-AA-1F} |
| Folderid \_ samplepictures         | {C4900540-2379-4c75-84-4B-64-E6-FA-F8-71-6B} |
| Folderid \_ samplevideos           | {859ead94-2e85-48ad-A7-1a-09-69-CB-56-A6-CD} |
| Folderid \_ savedgames             | {4c5c32ff-bb9d-43b0-B5-B4-2D-72-E5-4E-AA-A4} |
| Folderid \_ savedsuchen          | {7d1d3a04-Debb-4115-95-CF-2F-29-da-29-20-da} |
| folderid- \_ Suche \_ csc            | {ee32e446-31ca-4aba-81-4f-A5-EB-D2-FD-6D-5E} |
| folderid \_ - \_ suchmapi           | {98ec0e18-2098-4d44-86-44-66-97-93 -15-a2-81} |
| Folderid \_ searchhome             | {190337d1-b8ca-4121-A6-39-6D-47-2D-16-97-2a} |
| Folderid \_ SendTo                 | {8983036c-27c0-404b-8F-08-10-2D-10-DC-FD-74} |
| Folderid \_ Startmenü              | {625b53c3-AB48-4ec1-BA-1F-a1-EF-41-46-FC-19} |
| Folderid- \_ Start                | {B97D20BB-F46A-4c97-BA-10-5E-36-08-43-08-54} |
| Folderid \_ syncmanagerfolder      | {43668bf-C14E-49b2-97-C9-74-77 -84-T7-84-B7} |
| \_Ordnerid synkresultorfolder      | {289a9a43-be44-4057-A4-1B-58-7a-76-T7-E7-F9} |
| Folderid \_ SyncSetupFolder        | {f214138-b1d3-4a90-BB-A9-27-CB-C0-C5-38-9a}  |
| Folderid- \_ System                 | {1ac14e77-02e7-4e5d-B7-44-2E-B1-AE-51-98-B7} |
| Folderid \_ SystemX86              | {D65231B0-B2F1-4857-A4-CE-A8-E7-C6-EA-7D-27} |
| Folderid- \_ Vorlagen              | {A63293E8-664E-48dB-a0-79-DF-75-9E-05-09-F7} |
| Folderid \_ Benutzer festgelegt             | {9e3995ab-1F 9c-4b13-B8-27 -48-B2-4B-6C-71-74} |
| Folderid \_ usersfiles             | {f3ce0f7c-4901-4acc-86-48-D5-D4-4B-04-EF-8F} |
| Folderid \_ userslibraries         | {a302545d-definitiv-464b-ab-E8-61-C8-64-8D-93-9B} |
| Folderid \_ User Profiles           | {0762d272-C50A-4bb0-a3-82-69-7D-CD-72-9B-80} |
| Folderid \_ userprogramfiles       | {5cd7aee2-2219-4a67-B8-5D-6C-9c-E1-56 -60-CB} |
| Folderid \_ userprogramfilescommon | {bcbd3057-ca5c-4622-B4-2D-BC-56-dB-0A-E5-16} |
| Folderid- \_ Videos                 | {18989b1d-99 B5-455b-84-1C-ab-7C-74-E4-DD-FC} |
| Folderid \_ videoslibrary {        | 491e922f-5643-4af4-A7-EB-4E-7a-13-8D-81-74}  |
| Folderid \_ Windows {              | F38BF404-1d43-42f2-93-05 -67-de-0B-28-FC-23}  |



 

## <a name="examples"></a>Beispiele


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)
</dt> </dl>

 

 
