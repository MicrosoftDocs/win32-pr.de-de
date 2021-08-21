---
description: Identifiziert einen Eintrag in der Shimdatenbank.
ms.assetid: c092592d-a4f4-4b2f-9b03-c07951ed214a
title: TAG (Exposeenums2managed.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7e4df727245ead30ecefef0cd941148b8f4c76e2881ab19f41c3388934abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075794"
---
# <a name="tag"></a>TAG

Identifiziert einen Eintrag in der Shimdatenbank.

Die folgenden Einträge sind vom Typ **TAG \_ TYPE \_ LIST** (0x7000).



| Konstante/Wert                                                                                                                                                                                                                                                             | Beschreibung                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span id="TAG_DATABASE"></span><span id="tag_database"></span><dl> <dt>**TAG \_ DATABASE**</dt> <dt>(0x1 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                               | Datenbankeintrag.<br/>                                                |
| <span id="TAG_LIBRARY"></span><span id="tag_library"></span><dl> <dt>**TAG \_ LIBRARY**</dt> <dt>(0x2 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                  | Bibliothekseintrag.<br/>                                                 |
| <span id="TAG_INEXCLUDE"></span><span id="tag_inexclude"></span><dl> <dt>**TAG \_ INEXCLUDE**</dt> <dt>(0x3 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                            | Eintrag einschließen und ausschließen.<br/>                                     |
| <span id="TAG_SHIM"></span><span id="tag_shim"></span><dl> <dt>**TAG \_ SHIM**</dt> <dt>(0x4 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                           | Shimeintrag, der die Namens- und Zweckinformationen enthält.<br/>     |
| <span id="TAG_PATCH"></span><span id="tag_patch"></span><dl> <dt>**TAG \_ PATCH**</dt> <dt>(0x5 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                        | Patcheintrag, der die Informationen zum Patchen im Arbeitsspeicher enthält.<br/>  |
| <span id="TAG_APP"></span><span id="tag_app"></span><dl> <dt>**TAG \_ APP**</dt> <dt>(0x6 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                              | Anwendungseintrag.<br/>                                             |
| <span id="TAG_EXE"></span><span id="tag_exe"></span><dl> <dt>**TAG \_ EXE**</dt> <dt>(0x7 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                              | Ausführbarer Eintrag.<br/>                                              |
| <span id="TAG_MATCHING_FILE"></span><span id="tag_matching_file"></span><dl> <dt>**TAG \_ ÜBEREINSTIMMENDE \_ DATEI**</dt> <dt>(0x8 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>               | Übereinstimmender Dateieintrag.<br/>                                           |
| <span id="TAG_SHIM_REF"></span><span id="tag_shim_ref"></span><dl> <dt>**TAG \_ SHIM \_ REF**</dt> <dt>(0x9 \| \_ \_ TAGTYPLISTE)</dt> </dl>                                   | Shimdefinitionseintrag.<br/>                                         |
| <span id="TAG_PATCH_REF"></span><span id="tag_patch_ref"></span><dl> <dt>**TAG \_ PATCH \_ REF**</dt> <dt>(0xA \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                           | Patchdefinitionseintrag.<br/>                                        |
| <span id="TAG_LAYER"></span><span id="tag_layer"></span><dl> <dt>**TAG \_ LAYER**</dt> <dt>(0xB \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                        | Layer-Shimeintrag.<br/>                                              |
| <span id="TAG_FILE"></span><span id="tag_file"></span><dl> <dt>**TAG \_ FILE**</dt> <dt>(0xC \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                           | In einem Shimeintrag verwendetes Dateiattribut.<br/>                           |
| <span id="TAG_APPHELP"></span><span id="tag_apphelp"></span><dl> <dt>**TAG \_ APPHELP**</dt> <dt>(0xD \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                  | Apphelp-Informationseintrag.<br/>                                     |
| <span id="TAG_LINK"></span><span id="tag_link"></span><dl> <dt>**TAG \_ LINK**</dt> <dt>(0xE \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                           | Apphelp-Onlinelink-Informationseintrag.<br/>                         |
| <span id="TAG_DATA"></span><span id="tag_data"></span><dl> <dt>**TAG \_ DATA**</dt> <dt>(0xF \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                           | Name-Wert-Zuordnungseintrag.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM"></span><span id="tag_msi_transform"></span><dl> <dt>**TAG \_ MSI \_ TRANSFORM**</dt> <dt>(0x10 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>              | MSI-Transformationseintrag.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM_REF"></span><span id="tag_msi_transform_ref"></span><dl> <dt>**TAG \_ MSI \_ TRANSFORM \_ REF**</dt> <dt>(0x11 \| **\_ \_ TAGTYPLISTE**)</dt> </dl> | Msi-Transformationsdefinitionseintrag.<br/>                           |
| <span id="TAG_MSI_PACKAGE"></span><span id="tag_msi_package"></span><dl> <dt>**TAG \_ \_MSI-PAKET**</dt> <dt>(0x12 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                    | MSI-Paketeintrag.<br/>                                             |
| <span id="TAG_FLAG"></span><span id="tag_flag"></span><dl> <dt>**TAG \_ FLAG**</dt> <dt>(0x13 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                          | Flageintrag.<br/>                                                    |
| <span id="TAG_MSI_CUSTOM_ACTION"></span><span id="tag_msi_custom_action"></span><dl> <dt>**TAG \_ BENUTZERDEFINIERTE \_ \_ MSI-AKTION**</dt> <dt>(0x14 \| **\_ \_ TAGTYPLISTE)**</dt> </dl> | Benutzerdefinierter MSI-Aktionseintrag.<br/>                                       |
| <span id="TAG_FLAG_REF"></span><span id="tag_flag_ref"></span><dl> <dt>**TAG \_ FLAG \_ REF**</dt> <dt>(0x15 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                             | Flagdefinitionseintrag.<br/>                                         |
| <span id="TAG_ACTION"></span><span id="tag_action"></span><dl> <dt>**TAG \_ ACTION**</dt> <dt>(0x16 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                    | Nicht verwendet.<br/>                                                        |
| <span id="TAG_LOOKUP"></span><span id="tag_lookup"></span><dl> <dt>**TAG \_ LOOKUP**</dt> <dt>(0x17 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                    | Sucheintrag, der für die Suche in einer Treiberdatenbank verwendet wird.<br/>             |
| <span id="TAG_STRINGTABLE"></span><span id="tag_stringtable"></span><dl> <dt>**TAG \_ STRINGTABLE**</dt> <dt>(0x801 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                    | Zeichenfolgentabelleneintrag.<br/>                                            |
| <span id="TAG_INDEXES"></span><span id="tag_indexes"></span><dl> <dt>**TAG \_ INDIZES**</dt> <dt>(0x802 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                | Indexeintrag, der alle Indizes in einer Shimdatenbank definiert.<br/> |
| <span id="TAG_INDEX"></span><span id="tag_index"></span><dl> <dt>**TAG \_ INDEX**</dt> <dt>(0x803 \| **\_ \_ TAGTYPLISTE**)</dt> </dl>                                      | Indexeintrag, der einen Index in einer Shimdatenbank definiert.<br/>          |



Die folgenden Einträge sind vom Typ **TAG \_ TYPE \_ STRINGREF** (0x6000).



| Konstante/Wert                                                                                                                                                                                                                                                                     | Beschreibung                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="TAG_NAME"></span><span id="tag_name"></span><dl> <dt>**TAG \_ NAME**</dt> <dt>(0x1 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                                              | Name-Attribut.<br/>                                                                    |
| <span id="TAG_DESCRIPTION"></span><span id="tag_description"></span><dl> <dt>**TAG \_ DESCRIPTION**</dt> <dt>(0x2 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                         | Beschreibungseintrag.<br/>                                                                 |
| <span id="TAG_MODULE"></span><span id="tag_module"></span><dl> <dt>**TAG \_ MODULE**</dt> <dt>(0x3 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                                        | Modulattribut.<br/>                                                                  |
| <span id="TAG_API"></span><span id="tag_api"></span><dl> <dt>**TAG \_ API**</dt> <dt>(0x4 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                                                 | API-Eintrag.<br/>                                                                         |
| <span id="TAG_VENDOR"></span><span id="tag_vendor"></span><dl> <dt>**TAG \_ VENDOR**</dt> <dt>(0x5 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                                        | Attribut "Anbietername".<br/>                                                             |
| <span id="TAG_APP_NAME"></span><span id="tag_app_name"></span><dl> <dt>**TAG \_ \_APP-NAME**</dt> <dt>(0x6 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                                 | Anwendungsnamenattribut, das einen Anwendungseintrag in einer Shimdatenbank beschreibt.<br/> |
| <span id="TAG_COMMAND_LINE"></span><span id="tag_command_line"></span><dl> <dt>**TAG \_ \_BEFEHLSZEILE**</dt> <dt>(0x8 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                     | Befehlszeilenattribut, das z. B. beim Übergeben von Argumenten an einen Shim verwendet wird.<br/> |
| <span id="TAG_COMPANY_NAME"></span><span id="tag_company_name"></span><dl> <dt>**TAG \_ \_UNTERNEHMENSNAME**</dt> <dt>(0x9 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                     | Attribut "Unternehmensname".<br/>                                                            |
| <span id="TAG_DLLFILE"></span><span id="tag_dllfile"></span><dl> <dt>**TAG \_ DLLFILE**</dt> <dt>(0xA \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                                     | DLL-Dateiattribut für einen Shimeintrag.<br/>                                               |
| <span id="TAG_WILDCARD_NAME"></span><span id="tag_wildcard_name"></span><dl> <dt>**TAG \_ PLATZHALTERNAME \_**</dt> <dt>(0xB \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                  | Platzhalternamenattribut für einen ausführbaren Eintrag mit einem Platzhalter als Dateinamen.<br/>  |
| <span id="TAG_PRODUCT_NAME"></span><span id="tag_product_name"></span><dl> <dt>**TAG \_ \_PRODUKTNAME**</dt> <dt>(0x10 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                    | Attribut "Produktname".<br/>                                                            |
| <span id="TAG_PRODUCT_VERSION"></span><span id="tag_product_version"></span><dl> <dt>**TAG \_ \_PRODUKTVERSION**</dt> <dt>(0x11 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>           | Produktversionsattribut.<br/>                                                         |
| <span id="TAG_FILE_DESCRIPTION"></span><span id="tag_file_description"></span><dl> <dt>**TAG \_ \_DATEIBESCHREIBUNG**</dt> <dt>(0x12 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>        | Dateibeschreibungsattribut.<br/>                                                        |
| <span id="TAG_FILE_VERSION"></span><span id="tag_file_version"></span><dl> <dt>**TAG \_ \_DATEIVERSION**</dt> <dt>(0x13 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                    | Dateiversionsattribut.<br/>                                                            |
| <span id="TAG_ORIGINAL_FILENAME"></span><span id="tag_original_filename"></span><dl> <dt>**TAG \_ ORIGINAL \_ FILENAME**</dt> <dt>(0x14 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>     | Ursprüngliches Dateinamenattribut.<br/>                                                      |
| <span id="TAG_INTERNAL_NAME"></span><span id="tag_internal_name"></span><dl> <dt>**TAG \_ INTERNER \_ NAME**</dt> <dt>(0x15 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                 | Internes Dateinamenattribut.<br/>                                                      |
| <span id="TAG_LEGAL_COPYRIGHT"></span><span id="tag_legal_copyright"></span><dl> <dt>**TAG \_ RECHTLICHES \_ COPYRIGHT**</dt> <dt>(0x16 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>           | Copyrightattribut.<br/>                                                               |
| <span id="TAG_16BIT_DESCRIPTION"></span><span id="tag_16bit_description"></span><dl> <dt>**TAG \_ 16-BIT-BESCHREIBUNG \_**</dt> <dt>(0x17 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>     | 16-Bit-Beschreibungsattribut.<br/>                                                      |
| <span id="TAG_APPHELP_DETAILS"></span><span id="tag_apphelp_details"></span><dl> <dt>**TAG \_ APPHELP \_ DETAILS**</dt> <dt>(0x18 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>           | Apphelp details message information attribute (Attribut für AppHelp-Details zu Nachrichteninformationen).<br/>                                     |
| <span id="TAG_LINK_URL"></span><span id="tag_link_url"></span><dl> <dt>**TAG \_ \_LINK-URL**</dt> <dt>(0x19 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                                | Url-Attribut für Apphelp-Onlinelink.<br/>                                                 |
| <span id="TAG_LINK_TEXT"></span><span id="tag_link_text"></span><dl> <dt>**TAG \_ \_LINKTEXT**</dt> <dt>(0x1A \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                             | Apphelp-Onlinelink-Textattribut.<br/>                                                |
| <span id="TAG_APPHELP_TITLE"></span><span id="tag_apphelp_title"></span><dl> <dt>**TAG \_ APPHELP \_ TITLE**</dt> <dt>(0x1B \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                 | Apphelp-Titelattribut.<br/>                                                           |
| <span id="TAG_APPHELP_CONTACT"></span><span id="tag_apphelp_contact"></span><dl> <dt>**TAG \_ APPHELP \_ CONTACT**</dt> <dt>(0x1C \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>           | Kontaktattribut des AppHelp-Anbieters.<br/>                                                  |
| <span id="TAG_SXS_MANIFEST"></span><span id="tag_sxs_manifest"></span><dl> <dt>**TAG \_ \_SXS-MANIFEST**</dt> <dt>(0x1D \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                    | Eintrag des manifests nebeneinander.<br/>                                                       |
| <span id="TAG_DATA_STRING"></span><span id="tag_data_string"></span><dl> <dt>**TAG \_ DATA \_ STRING**</dt> <dt>(0x1E \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                       | Zeichenfolgenattribut für einen Dateneintrag.<br/>                                                 |
| <span id="TAG_MSI_TRANSFORM_FILE"></span><span id="tag_msi_transform_file"></span><dl> <dt>**TAG \_ MSI \_ TRANSFORM \_ FILE**</dt> <dt>(0x1F \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl> | Dateinamenattribut eines MSI-Transformationseintrags.<br/>                                |
| <span id="TAG_16BIT_MODULE_NAME"></span><span id="tag_16bit_module_name"></span><dl> <dt>**TAG \_ 16-BIT-MODULNAME \_ \_**</dt> <dt>(0x20 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>    | 16-Bit-Modulnamensattribut.<br/>                                                      |
| <span id="TAG_LAYER_DISPLAYNAME"></span><span id="tag_layer_displayname"></span><dl> <dt>**TAG \_ LAYER \_ DISPLAYNAME**</dt> <dt>(0x21 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>     | Nicht verwendet.<br/>                                                                            |
| <span id="TAG_COMPILER_VERSION"></span><span id="tag_compiler_version"></span><dl> <dt>**TAG \_ \_COMPILERVERSION**</dt> <dt>(0x22 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>        | Compilerversion der Shim-Datenbank.<br/>                                                    |
| <span id="TAG_ACTION_TYPE"></span><span id="tag_action_type"></span><dl> <dt>**TAG \_ \_AKTIONSTYP**</dt> <dt>(0x23 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                       | Nicht verwendet.<br/>                                                                            |
| <span id="TAG_EXPORT_NAME"></span><span id="tag_export_name"></span><dl> <dt>**TAG \_ EXPORT \_ NAME**</dt> <dt>(0x24 \| **\_ TAGTYP \_ STRINGREF**)</dt> </dl>                       | Exportieren Sie das Dateinamenattribut.<br/>                                                        |



Die folgenden Einträge sind vom Typ **TAG \_ TYPE \_ DWORD** (0x4000).



| Konstante/Wert                                                                                                                                                                                                                                                                    | Beschreibung                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| <span id="TAG_SIZE"></span><span id="tag_size"></span><dl> <dt>**TAG \_ SIZE**</dt> <dt>(0x1 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                                 | Dateigrößenattribut.<br/>                                                                                  |
| <span id="TAG_OFFSET"></span><span id="tag_offset"></span><dl> <dt>**TAG \_ OFFSET**</dt> <dt>(0x2 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                           | Nicht verwendet.<br/>                                                                                               |
| <span id="TAG_CHECKSUM"></span><span id="tag_checksum"></span><dl> <dt>**TAG \_ CHECKSUM**</dt> <dt>(0x3 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                     | Dateiprüfsummenattribut.<br/>                                                                              |
| <span id="TAG_SHIM_TAGID"></span><span id="tag_shim_tagid"></span><dl> <dt>**TAG \_ \_SHIM-TAGID**</dt> <dt>(0x4 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                              | **Shim-TAGID-Attribut.**<br/>                                                                             |
| <span id="TAG_PATCH_TAGID"></span><span id="tag_patch_tagid"></span><dl> <dt>**TAG \_ \_PATCH-TAGID**</dt> <dt>(0x5 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                           | **Patch-TAGID-Attribut.**<br/>                                                                            |
| <span id="TAG_MODULE_TYPE"></span><span id="tag_module_type"></span><dl> <dt>**TAG \_ \_MODULTYP**</dt> <dt>(0x6 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                           | Modultypattribut.<br/>                                                                                |
| <span id="TAG_VERDATEHI"></span><span id="tag_verdatehi"></span><dl> <dt>**TAG \_ VERDATEHI**</dt> <dt>(0x7 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                  | Höherer Teil des Datumsattributs der Dateiversion.<br/>                                                |
| <span id="TAG_VERDATELO"></span><span id="tag_verdatelo"></span><dl> <dt>**TAG \_ VERDATELO**</dt> <dt>(0x8 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                  | Niedriger Teil des Datumsattributs der Dateiversion.<br/>                                                 |
| <span id="TAG_VERFILEOS"></span><span id="tag_verfileos"></span><dl> <dt>**TAG \_ VERFILEOS**</dt> <dt>(0x9 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                  | Betriebssystemdateiversionsattribut.<br/>                                                              |
| <span id="TAG_VERFILETYPE"></span><span id="tag_verfiletype"></span><dl> <dt>**TAG \_ VERFILETYPE**</dt> <dt>(0xA \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                            | Dateitypattribut.<br/>                                                                                  |
| <span id="TAG_PE_CHECKSUM"></span><span id="tag_pe_checksum"></span><dl> <dt>**TAG \_ PE \_ CHECKSUM**</dt> <dt>(0xB \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                           | PE-Dateiprüfsummenattribut.<br/>                                                                           |
| <span id="TAG_PREVOSMAJORVER"></span><span id="tag_prevosmajorver"></span><dl> <dt>**TAG \_ PREVOSMAJORVER**</dt> <dt>(0xC \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                   | Hauptversionsattribut des Betriebssystems.<br/>                                                             |
| <span id="TAG_PREVOSMINORVER"></span><span id="tag_prevosminorver"></span><dl> <dt>**TAG \_ PREVOSMINORVER**</dt> <dt>(0xD \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                   | Nebenversionsattribut des Betriebssystems.<br/>                                                             |
| <span id="TAG_PREVOSPLATFORMID"></span><span id="tag_prevosplatformid"></span><dl> <dt>**TAG \_ PREVOSPLATFORMID**</dt> <dt>(0xE \| **\_ TAGTYP \_ DWORD**)</dt> </dl>             | Bezeichnerattribut der Betriebssystemplattform.<br/>                                                       |
| <span id="TAG_PREVOSBUILDNO"></span><span id="tag_prevosbuildno"></span><dl> <dt>**TAG \_ PREVOSBUILDNO**</dt> <dt>(0xF \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                      | Buildnummerattribut des Betriebssystems.<br/>                                                              |
| <span id="TAG_PROBLEMSEVERITY"></span><span id="tag_problemseverity"></span><dl> <dt>**TAG \_ PROBLEMSEVERITY**</dt> <dt>(0x10 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>               | Blockattribut eines Apphelp-Eintrags. Dadurch wird bestimmt, ob die Anwendung hart oder soft blockiert ist.<br/> |
| <span id="TAG_LANGID"></span><span id="tag_langid"></span><dl> <dt>**TAG \_ LANGID**</dt> <dt>(0x11 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                          | Sprachbezeichner eines Apphelp-Eintrags.<br/>                                                              |
| <span id="TAG_VER_LANGUAGE"></span><span id="tag_ver_language"></span><dl> <dt>**TAG \_ VER \_ LANGUAGE**</dt> <dt>(0x12 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                       | Sprachversionsattribut einer Datei.<br/>                                                                 |
| <span id="TAG_ENGINE"></span><span id="tag_engine"></span><dl> <dt>**TAG \_ ENGINE**</dt> <dt>(0x14 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                          | Nicht verwendet.<br/>                                                                                               |
| <span id="TAG_HTMLHELPID"></span><span id="tag_htmlhelpid"></span><dl> <dt>**TAG \_ HTMLHELPID**</dt> <dt>(0x15 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                              | Hilfebezeichnerattribut für einen Apphelp-Eintrag.<br/>                                                       |
| <span id="TAG_INDEX_FLAGS"></span><span id="tag_index_flags"></span><dl> <dt>**TAG \_ \_INDEXFLAGS**</dt> <dt>(0x16 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                          | Flags-Attribut für einen Indexeintrag.<br/>                                                                   |
| <span id="TAG_FLAGS"></span><span id="tag_flags"></span><dl> <dt>**TAG \_ FLAGS**</dt> <dt>(0x17 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                             | Flags-Attribut für einen Apphelp-Eintrag.<br/>                                                                 |
| <span id="TAG_DATA_VALUETYPE"></span><span id="tag_data_valuetype"></span><dl> <dt>**TAG \_ DATA \_ VALUETYPE**</dt> <dt>(0x18 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                 | Datentypattribut für einen Dateneintrag.<br/>                                                                 |
| <span id="TAG_DATA_DWORD"></span><span id="tag_data_dword"></span><dl> <dt>**TAG \_ DATA \_ DWORD**</dt> <dt>(0x19 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                             | **DWORD-Wertattribut** für einen Dateneintrag.<br/>                                                           |
| <span id="TAG_LAYER_TAGID"></span><span id="tag_layer_tagid"></span><dl> <dt>**TAG \_ LAYER \_ TAGID**</dt> <dt>(0x1A \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                          | **Tagid-Attribut** für Ebenens shim.<br/>                                                                       |
| <span id="TAG_MSI_TRANSFORM_TAGID"></span><span id="tag_msi_transform_tagid"></span><dl> <dt>**TAG \_ MSI \_ \_ TRANSFORM TAGID**</dt> <dt>(0x1B \| **\_ TAGTYP \_ DWORD**)</dt> </dl> | **TAGID-Attribut** für MSI-Transformation.<br/>                                                                    |
| <span id="TAG_LINKER_VERSION"></span><span id="tag_linker_version"></span><dl> <dt>**TAG \_ \_LINKERVERSION**</dt> <dt>(0x1C \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                 | Linkerversionsattribut einer Datei.<br/>                                                                   |
| <span id="TAG_LINK_DATE"></span><span id="tag_link_date"></span><dl> <dt>**TAG \_ \_LINKDATUM**</dt> <dt>(0x1D \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                | Linkdatumsattribut einer Datei.<br/>                                                                        |
| <span id="TAG_UPTO_LINK_DATE"></span><span id="tag_upto_link_date"></span><dl> <dt>**TAG \_ UPTO \_ LINK \_ DATE**</dt> <dt>(0x1E \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                | Linkdatumsattribut einer Datei. Der Abgleich erfolgt bis einschließlich dieses Linkdatums.<br/>                   |
| <span id="TAG_OS_SERVICE_PACK"></span><span id="tag_os_service_pack"></span><dl> <dt>**TAG \_ OS \_ SERVICE \_ PACK**</dt> <dt>(0x1F \| **\_ TAGTYP \_ DWORD**)</dt> </dl>             | Service Pack-Attribut des Betriebssystems für einen ausführbaren Eintrag.<br/>                                      |
| <span id="TAG_FLAG_TAGID"></span><span id="tag_flag_tagid"></span><dl> <dt>**TAG \_ FLAG \_ TAGID**</dt> <dt>(0x20 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                             | Kennzeichnet **das TAGID-Attribut.**<br/>                                                                            |
| <span id="TAG_RUNTIME_PLATFORM"></span><span id="tag_runtime_platform"></span><dl> <dt>**TAG \_ RUNTIME \_ PLATFORM**</dt> <dt>(0x21 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>           | Laufzeitplattformattribut einer Datei.<br/>                                                                |
| <span id="TAG_OS_SKU"></span><span id="tag_os_sku"></span><dl> <dt>**TAG \_ \_BETRIEBSSYSTEM-SKU**</dt> <dt>(0x22 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                         | Betriebssystem-SKU-Attribut für einen ausführbaren Eintrag.<br/>                                               |
| <span id="TAG_OS_PLATFORM"></span><span id="tag_os_platform"></span><dl> <dt>**TAG \_ \_BETRIEBSSYSTEMPLATTFORM**</dt> <dt>(0x23 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                          | Betriebssystemplattformattribut.<br/>                                                                  |
| <span id="TAG_APP_NAME_RC_ID"></span><span id="tag_app_name_rc_id"></span><dl> <dt>**TAG \_ \_APP-NAME \_ \_ RC-ID**</dt> <dt>(0x24 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>               | Ressourcenbezeichnerattribut des Anwendungsnamens für Apphelp-Einträge.<br/>                                   |
| <span id="TAG_VENDOR_NAME_RC_ID"></span><span id="tag_vendor_name_rc_id"></span><dl> <dt>**TAG \_ VENDOR \_ NAME \_ RC \_ ID**</dt> <dt>(0x25 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>      | Ressourcenbezeichnerattribut des Anbieternamens für Apphelp-Einträge.<br/>                                        |
| <span id="TAG_SUMMARY_MSG_RC_ID"></span><span id="tag_summary_msg_rc_id"></span><dl> <dt>**TAG \_ ZUSAMMENFASSUNG \_ MSG \_ RC \_ ID**</dt> <dt>(0x26 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>      | Ressourcenbezeichnerattribut der Zusammenfassungsmeldung für Apphelp-Einträge.<br/>                                    |
| <span id="TAG_VISTA_SKU"></span><span id="tag_vista_sku"></span><dl> <dt>**TAG \_ \_VISTA-SKU**</dt> <dt>(0x27 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                | Windows Vista-SKU-Attribut.<br/>                                                                          |
| <span id="TAG_DESCRIPTION_RC_ID"></span><span id="tag_description_rc_id"></span><dl> <dt>**TAG \_ DESCRIPTION \_ RC \_ ID**</dt> <dt>(0x28 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>       | Beschreibung des Ressourcenbezeichnerattributs für Apphelp-Einträge.<br/>                                        |
| <span id="TAG_PARAMETER1_RC_ID"></span><span id="tag_parameter1_rc_id"></span><dl> <dt>**TAG \_ PARAMETER1 \_ RC \_ ID**</dt> <dt>(0x29 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>          | Parameter1 Ressourcenbezeichnerattribut für Apphelp-Einträge.<br/>                                         |
| <span id="TAG_TAGID"></span><span id="tag_tagid"></span><dl> <dt>**TAG \_ TAGID**</dt> <dt>(0x801 \| **\_ TAGTYP \_ DWORD**)</dt> </dl>                                            | **TAGID-Attribut.**<br/>                                                                                  |



Der folgende Eintrag hat den Typ **TAG \_ TYPE \_ STRING** (0x8000).



| Konstante/Wert                                                                                                                                                                                                                                                            | Beschreibung                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|
| <span id="TAG_STRINGTABLE_ITEM"></span><span id="tag_stringtable_item"></span><dl> <dt>**TAG \_ STRINGTABLE \_ ITEM**</dt> <dt>(0x801 \| **\_ TAGTYP \_ ZEICHENFOLGE**)</dt> </dl> | Eintrag des Zeichenfolgentabellenelements.<br/> |



Die folgenden Einträge sind vom Typ **TAG \_ TYPE \_ NULL** (0x1000).



| Konstante/Wert                                                                                                                                                                                                                                                                            | Beschreibung                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span id="TAG_INCLUDE"></span><span id="tag_include"></span><dl> <dt>**TAG \_ INCLUDE**</dt> <dt>(0x1 \| **\_ TAGTYP \_ NULL**)</dt> </dl>                                                 | Listeneintrag einschließen.<br/>                           |
| <span id="TAG_GENERAL"></span><span id="tag_general"></span><dl> <dt>**TAG \_ ALLGEMEIN**</dt> <dt>(0x2 \| **\_ TAGTYP \_ NULL**)</dt> </dl>                                                 | Allgemeiner Shimeintrag.<br/>                   |
| <span id="TAG_MATCH_LOGIC_NOT"></span><span id="tag_match_logic_not"></span><dl> <dt>**TAG \_ MATCH \_ LOGIC \_ NOT**</dt> <dt>(0x3 \| **\_ TAGTYP \_ NULL**)</dt> </dl>                       | NICHT des übereinstimmenden Logikeintrags.<br/>                  |
| <span id="TAG_APPLY_ALL_SHIMS"></span><span id="tag_apply_all_shims"></span><dl> <dt>**TAG \_ APPLY \_ ALL \_ SHIMS**</dt> <dt>(0x4 \| **\_ TAGTYP \_ NULL**)</dt> </dl>                       | Nicht verwendet.<br/>                                       |
| <span id="TAG_USE_SERVICE_PACK_FILES"></span><span id="tag_use_service_pack_files"></span><dl> <dt>**TAG \_ VERWENDEN VON \_ SERVICE \_ \_ PACK-DATEIEN**</dt> <dt>(0x5 \| **\_ TAGTYP \_ NULL**)</dt> </dl> | Service Pack-Informationen für AppHelp-Einträge.<br/> |
| <span id="TAG_MITIGATION_OS"></span><span id="tag_mitigation_os"></span><dl> <dt>**TAG \_ \_ENTSCHÄRFUNGSBETRIEBSSYSTEM**</dt> <dt>(0x6 \| **\_ TAGTYP \_ NULL**)</dt> </dl>                              | Entschärfung beim Eintrag im Betriebssystembereich.<br/>   |
| <span id="TAG_BLOCK_UPGRADE"></span><span id="tag_block_upgrade"></span><dl> <dt>**TAG \_ BLOCK \_ UPGRADE**</dt> <dt>(0x7 \| **\_ TAGTYP \_ NULL**)</dt> </dl>                              | Upgradeblockeintrag.<br/>                          |
| <span id="TAG_INCLUDEEXCLUDEDLL"></span><span id="tag_includeexcludedll"></span><dl> <dt>**TAG \_ INCLUDEEXCLUDEDLL**</dt> <dt>(0x8 \| **\_ TAGTYP \_ NULL**)</dt> </dl>                   | DLL-Include/Exclude-Eintrag.<br/>                    |



Die folgenden Einträge sind vom Typ **TAG \_ TYPE \_ QWORD** (0x5000).



| Konstante/Wert                                                                                                                                                                                                                                                                                   | Beschreibung                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TAG_TIME"></span><span id="tag_time"></span><dl> <dt>**TAG \_ TIME**</dt> <dt>(0x1 \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                                                                | Zeitattribut.<br/>                                                                                     |
| <span id="TAG_BIN_FILE_VERSION"></span><span id="tag_bin_file_version"></span><dl> <dt>**TAG \_ BIN \_ FILE \_ VERSION**</dt> <dt>(0x2 \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                          | Bin-Dateiversionsattribut für Dateieinträge.<br/>                                                        |
| <span id="TAG_BIN_PRODUCT_VERSION"></span><span id="tag_bin_product_version"></span><dl> <dt>**TAG \_ BIN \_ PRODUCT \_ VERSION**</dt> <dt>(0x3 \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                 | Bin-Produktversionsattribut für Dateieinträge.<br/>                                                     |
| <span id="TAG_MODTIME"></span><span id="tag_modtime"></span><dl> <dt>**TAG \_ MODTIME**</dt> <dt>(0x4 \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                                                       | Nicht verwendet.<br/>                                                                                             |
| <span id="TAG_FLAG_MASK_KERNEL"></span><span id="tag_flag_mask_kernel"></span><dl> <dt>**TAG \_ FLAG \_ MASK \_ KERNEL**</dt> <dt>(0x5 \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                          | Kernelflag-Maskattribut.<br/>                                                                         |
| <span id="TAG_UPTO_BIN_PRODUCT_VERSION"></span><span id="tag_upto_bin_product_version"></span><dl> <dt>**TAG \_ UPTO \_ BIN \_ PRODUCT \_ VERSION**</dt> <dt>(0x6 \| **\_ TAGTYP \_ QWORD**)</dt> </dl> | Bin-Produktversionsattribut einer Datei. Der Abgleich erfolgt bis einschließlich dieser Produktversion.<br/> |
| <span id="TAG_DATA_QWORD"></span><span id="tag_data_qword"></span><dl> <dt>**TAG \_ DATA \_ QWORD**</dt> <dt>(0x7 \| **TAG \_ TYPE \_ QWORD**)</dt> </dl>                                             | **ULONGLONG-Wertattribut** für einen Dateneintrag.<br/>                                                     |
| <span id="TAG_FLAG_MASK_USER"></span><span id="tag_flag_mask_user"></span><dl> <dt>**TAG \_ FLAG \_ MASK \_ USER**</dt> <dt>(0x8 \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                                | Benutzerflagmaskenattribut.<br/>                                                                           |
| <span id="TAG_FLAGS_NTVDM1"></span><span id="tag_flags_ntvdm1"></span><dl> <dt>**TAG \_ FLAGS \_ NTVDM1**</dt> <dt>(0x9 \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                                       | NTVDM1-Flagmaskenattribut.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM2"></span><span id="tag_flags_ntvdm2"></span><dl> <dt>**TAG \_ FLAGS \_ NTVDM2**</dt> <dt>(0xA \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                                       | NTVDM2-Flagmaskenattribut.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM3"></span><span id="tag_flags_ntvdm3"></span><dl> <dt>**TAG \_ FLAGS \_ NTVDM3**</dt> <dt>(0xB \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                                       | NTVDM3-Flagmaskenattribut.<br/>                                                                         |
| <span id="TAG_FLAG_MASK_SHELL"></span><span id="tag_flag_mask_shell"></span><dl> <dt>**TAG \_ FLAG \_ MASK \_ SHELL**</dt> <dt>(0xC \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                             | Shell-Flagmaskenattribut.<br/>                                                                          |
| <span id="TAG_UPTO_BIN_FILE_VERSION"></span><span id="tag_upto_bin_file_version"></span><dl> <dt>**TAG \_ UPTO \_ BIN \_ FILE \_ VERSION**</dt> <dt>(0xD \| **\_ TAGTYP \_ QWORD**)</dt> </dl>          | Bin-Dateiversionsattribut einer Datei. Der Abgleich erfolgt bis einschließlich dieser Dateiversion.<br/>       |
| <span id="TAG_FLAG_MASK_FUSION"></span><span id="tag_flag_mask_fusion"></span><dl> <dt>**TAG \_ FLAG \_ MASK \_ FUSION**</dt> <dt>(0xE \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                          | Fusion-Flagmaskenattribut.<br/>                                                                         |
| <span id="TAG_FLAG_PROCESSPARAM"></span><span id="tag_flag_processparam"></span><dl> <dt>**TAG \_ FLAG \_ PROCESSPARAM**</dt> <dt>(0xF \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                        | Prozessparam-Flagattribut.<br/>                                                                       |
| <span id="TAG_FLAG_LUA"></span><span id="tag_flag_lua"></span><dl> <dt>**TAG \_ FLAG \_ LUA**</dt> <dt>(0x10 \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                                                  | LUA-Flagattribut.<br/>                                                                                 |
| <span id="TAG_FLAG_INSTALL"></span><span id="tag_flag_install"></span><dl> <dt>**TAG \_ \_FLAGINSTALLATION**</dt> <dt>(0x11 \| **\_ TAGTYP \_ QWORD**)</dt> </dl>                                      | Installieren Sie das Flagattribut.<br/>                                                                             |



Die folgenden Einträge sind vom Typ **TAG \_ TYPE \_ BINARY** (0x9000).



| Konstante/Wert                                                                                                                                                                                                                                                     | Beschreibung                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="TAG_PATCH_BITS"></span><span id="tag_patch_bits"></span><dl> <dt>**TAG \_ PATCH \_ BITS**</dt> <dt>(0x2 \| **\_ TAGTYP \_ BINARY**)</dt> </dl>              | Patchdatei-Bits-Attribut.<br/>                          |
| <span id="TAG_FILE_BITS"></span><span id="tag_file_bits"></span><dl> <dt>**TAG \_ FILE \_ BITS**</dt> <dt>(0x3 \| **\_ TAGTYP \_ BINARY**)</dt> </dl>                 | Dateibitattribut.<br/>                                |
| <span id="TAG_EXE_ID"></span><span id="tag_exe_id"></span><dl> <dt>**TAG \_ \_EXE-ID**</dt> <dt>(0x4 \| **\_ TAGTYP \_ BINARY**)</dt> </dl>                          | **GUID-Attribut** eines ausführbaren Eintrags.<br/>          |
| <span id="TAG_DATA_BITS"></span><span id="tag_data_bits"></span><dl> <dt>**TAG \_ DATA \_ BITS**</dt> <dt>(0x5 \| **\_ TAGTYP \_ BINARY**)</dt> </dl>                 | Data bits-Attribut.<br/>                                |
| <span id="TAG_MSI_PACKAGE_ID"></span><span id="tag_msi_package_id"></span><dl> <dt>**TAG \_ \_ \_ MSI-PAKET-ID**</dt> <dt>(0x6 \| **\_ TAGTYP \_ BINARY**)</dt> </dl> | MSI-Paketbezeichnerattribut eines MSI-Pakets.<br/> |
| <span id="TAG_DATABASE_ID"></span><span id="tag_database_id"></span><dl> <dt>**TAG \_ DATABASE \_ ID**</dt> <dt>(0x7 \| **\_ TAGTYP \_ BINARY**)</dt> </dl>           | **GUID-Attribut** einer Datenbank.<br/>                   |
| <span id="TAG_INDEX_BITS"></span><span id="tag_index_bits"></span><dl> <dt>**TAG \_ \_INDEXBITS**</dt> <dt>(0x801 \| **\_ TAGTYP \_ BINARY**)</dt> </dl>            | Indexbits-Attribut.<br/>                               |



Die folgenden Einträge sind vom Typ **TAG \_ TYPE \_ WORD** (0x3000).



| Konstante/Wert                                                                                                                                                                                                                                      | Beschreibung                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="TAG_MATCH_MODE"></span><span id="tag_match_mode"></span><dl> <dt>**TAG \_ \_ÜBEREINSTIMMUNGSMODUS**</dt> <dt>(0x1 \| **\_ TAGTYP \_ WORD**)</dt> </dl> | Übereinstimmungsmodusattribut.<br/>                   |
| <span id="TAG_TAG"></span><span id="tag_tag"></span><dl> <dt>**TAG \_ TAG**</dt> <dt>(0x801 \| **\_ TAGTYP \_ WORD**)</dt> </dl>                     | TAG-Eintrag.<br/>                              |
| <span id="TAG_INDEX_TAG"></span><span id="tag_index_tag"></span><dl> <dt>**TAG \_ \_INDEXTAG**</dt> <dt>(0x802 \| **\_ TAGTYP \_ WORD**)</dt> </dl>  | IndexTAG-Attribut für einen Indexeintrag.<br/> |
| <span id="TAG_INDEX_KEY"></span><span id="tag_index_key"></span><dl> <dt>**TAG \_ \_INDEXSCHLÜSSEL**</dt> <dt>(0x803 \| **\_ TAGTYP \_ WORD**)</dt> </dl>  | Indexschlüsselattribut für einen Indexeintrag.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Exposeenums2managed.h (include Axextendenums.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[TAG-Typen](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




