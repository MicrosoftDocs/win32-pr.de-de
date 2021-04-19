---
description: Identifiziert einen Eintrag in der Shimdatenbank.
ms.assetid: c092592d-a4f4-4b2f-9b03-c07951ed214a
title: Tag (Exposeenums2managed. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacbd3c8d29e1f41d7aaabc989848c561415ae4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361441"
---
# <a name="tag"></a>TAG

Identifiziert einen Eintrag in der Shimdatenbank.

Die folgenden Einträge sind vom Typ " **Tag \_ Type \_ List** (0x7000)".



| Konstante/Wert                                                                                                                                                                                                                                                             | BESCHREIBUNG                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span id="TAG_DATABASE"></span><span id="tag_database"></span><dl> <dt>**Tag \_ Database**</dt> <dt>(0x1- \| **\_ Tagtyp \_ Liste**)</dt> </dl>                               | Datenbankeintrag.<br/>                                                |
| <span id="TAG_LIBRARY"></span><span id="tag_library"></span><dl> <dt>**Tag \_ Bibliothek**</dt> <dt>(0x2- \| **\_ Tagtyp \_ Liste**)</dt> </dl>                                  | Bibliotheks Eintrag.<br/>                                                 |
| <span id="TAG_INEXCLUDE"></span><span id="tag_inexclude"></span><dl> <dt>**Tag \_ Inexclude**</dt> <dt>(0x3- \| **\_ Tagtyp \_ Liste**)</dt> </dl>                            | Schließt einen Eintrag ein und aus.<br/>                                     |
| <span id="TAG_SHIM"></span><span id="tag_shim"></span><dl> <dt>**Tag \_ Shim**</dt> <dt>(Liste der 0x4- \| **\_ Tagtypen \_**)</dt> </dl>                                           | Der Shim-Eintrag, der die Informationen zu Name und Zweck enthält.<br/>     |
| <span id="TAG_PATCH"></span><span id="tag_patch"></span><dl> <dt>**Tag \_ Patch**</dt> <dt>(0x5- \| **\_ Tagtyp \_ Liste**)</dt> </dl>                                        | Patch-Eintrag, der die in-Memory-Patchinformationen enthält.<br/>  |
| <span id="TAG_APP"></span><span id="tag_app"></span><dl> <dt>**Tag \_ App**</dt> <dt>(0x6- \| **\_ Tagtyp \_ Liste**)</dt> </dl>                                              | Anwendungs Eintrag.<br/>                                             |
| <span id="TAG_EXE"></span><span id="tag_exe"></span><dl> <dt>**Tag \_ EXE**</dt> <dt>(0x7- \| **\_ Tagtyp \_ Liste**)</dt> </dl>                                              | Ausführbarer Eintrag.<br/>                                              |
| <span id="TAG_MATCHING_FILE"></span><span id="tag_matching_file"></span><dl> <dt>**Tag \_ Übereinstimmende \_ Datei**</dt> <dt>(0x8- \| **\_ Tagtyp \_ Liste**)</dt> </dl>               | Übereinstimmender Datei Eintrag.<br/>                                           |
| <span id="TAG_SHIM_REF"></span><span id="tag_shim_ref"></span><dl> <dt>**Tag \_ Shim- \_ ref**</dt> <dt>(0x9- \| \_ Tagtyp \_ Liste)</dt> </dl>                                   | Der Shim-Definitions Eintrag.<br/>                                         |
| <span id="TAG_PATCH_REF"></span><span id="tag_patch_ref"></span><dl> <dt>**Tag \_ Patchverweis \_**</dt> <dt>(Liste 0xa- \| **\_ \_ Tagtyp**)</dt> </dl>                           | Patch-Definitions Eintrag.<br/>                                        |
| <span id="TAG_LAYER"></span><span id="tag_layer"></span><dl> <dt>**Tag \_ Ebene**</dt> <dt>(Liste der 0xB- \| **\_ \_ Tagtypen**)</dt> </dl>                                        | Ebenenshim-Eintrag.<br/>                                              |
| <span id="TAG_FILE"></span><span id="tag_file"></span><dl> <dt>**Tag \_ Datei**</dt> <dt>(Liste 0xc- \| **\_ Tagtyp \_**)</dt> </dl>                                           | Das in einem shimeintrag verwendete Datei Attribut.<br/>                           |
| <span id="TAG_APPHELP"></span><span id="tag_apphelp"></span><dl> <dt>**Tag \_ AppHelp**</dt> <dt>(0xD \| **\_ Tagtyp \_ Liste**)</dt> </dl>                                  | Der AppHelp-Informations Eintrag.<br/>                                     |
| <span id="TAG_LINK"></span><span id="tag_link"></span><dl> <dt>**Tag \_ Link**</dt> <dt>(Liste der 0xe- \| **\_ Tagtypen \_**)</dt> </dl>                                           | Eintrag für AppHelp Online Link Information.<br/>                         |
| <span id="TAG_DATA"></span><span id="tag_data"></span><dl> <dt>**Tag \_ Daten**</dt> <dt>(Liste 0xF- \| **\_ Tagtyp \_**)</dt> </dl>                                           | Name-Wert-Zuordnungseintrag.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM"></span><span id="tag_msi_transform"></span><dl> <dt>**Tag \_ MSI- \_ Transformation**</dt> <dt>(0x10- \| **\_ Tagtyp \_ Liste**)</dt> </dl>              | MSI-Transformations Eintrag.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM_REF"></span><span id="tag_msi_transform_ref"></span><dl> <dt>**Tag \_ MSI \_ - \_ Transformations**</dt> Verweis <dt>(0x11- \| **\_ Tagtyp \_ Liste**)</dt> </dl> | Definitions Eintrag für MSI-Transformation.<br/>                           |
| <span id="TAG_MSI_PACKAGE"></span><span id="tag_msi_package"></span><dl> <dt>**Tag \_ MSI- \_ Paket**</dt> <dt>(Liste 0x12- \| **\_ Tagtyp \_**)</dt> </dl>                    | MSI-Paket Eintrag.<br/>                                             |
| <span id="TAG_FLAG"></span><span id="tag_flag"></span><dl> <dt>**Tag \_ Flag**</dt> <dt>(0x13- \| **\_ Tagtyp \_ Liste**)</dt> </dl>                                          | Flag-Eintrag.<br/>                                                    |
| <span id="TAG_MSI_CUSTOM_ACTION"></span><span id="tag_msi_custom_action"></span><dl> <dt>**Tag \_ \_Benutzerdefinierte \_ MSI-Aktion**</dt> <dt>(Liste 0x14- \| **\_ Tagtyp \_**)</dt> </dl> | Benutzerdefinierter MSI-Aktions Eintrag.<br/>                                       |
| <span id="TAG_FLAG_REF"></span><span id="tag_flag_ref"></span><dl> <dt>**Tag \_ Flag \_ ref**</dt> <dt>(0x15 \| **Tag \_ Type \_ List**)</dt> </dl>                             | Definitions Eintrag markieren.<br/>                                         |
| <span id="TAG_ACTION"></span><span id="tag_action"></span><dl> <dt>**Tag \_ Aktion**</dt> <dt>(0x16- \| **\_ Tagtyp \_ Liste**)</dt> </dl>                                    | Nicht verwendet.<br/>                                                        |
| <span id="TAG_LOOKUP"></span><span id="tag_lookup"></span><dl> <dt>**Tag \_ Suche**</dt> <dt>(Liste der 0x17- \| **\_ \_ Tagtypen**)</dt> </dl>                                    | Sucheintrag, der für die Suche in einer Treiberdatenbank verwendet wird.<br/>             |
| <span id="TAG_STRINGTABLE"></span><span id="tag_stringtable"></span><dl> <dt>**Tag \_ STRINGTABLE**</dt> <dt>(0x801- \| **\_ Tagtyp \_ Liste**)</dt> </dl>                    | Zeichen folgen Tabelleneintrag.<br/>                                            |
| <span id="TAG_INDEXES"></span><span id="tag_indexes"></span><dl> <dt>**Tag \_ Indizes**</dt> <dt>(Liste 0x802- \| **\_ \_ Tagtyp**)</dt> </dl>                                | Index Eintrag, der alle Indizes in einer Shimdatenbank definiert.<br/> |
| <span id="TAG_INDEX"></span><span id="tag_index"></span><dl> <dt>**Tag \_ Index**</dt> <dt>(Liste 0x803- \| **\_ \_ Tagtyp**)</dt> </dl>                                      | Index Eintrag, der einen Index in einer Shimdatenbank definiert.<br/>          |



Die folgenden Einträge sind vom Typ **" \_ Tagtyp \_** " ("") "".



| Konstante/Wert                                                                                                                                                                                                                                                                     | BESCHREIBUNG                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="TAG_NAME"></span><span id="tag_name"></span><dl> <dt>**Tag \_ Name**</dt> <dt>(0x1- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                                              | Name-Attribut.<br/>                                                                    |
| <span id="TAG_DESCRIPTION"></span><span id="tag_description"></span><dl> <dt>**Tag \_ Beschreibung**</dt> <dt>(0x2- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                         | Der Beschreibungs Eintrag.<br/>                                                                 |
| <span id="TAG_MODULE"></span><span id="tag_module"></span><dl> <dt>**Tag \_ Module**</dt> <dt>(0x3- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                                        | Modul Attribut.<br/>                                                                  |
| <span id="TAG_API"></span><span id="tag_api"></span><dl> <dt>**Tag \_ API**</dt> <dt>(0x4- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                                                 | API-Eintrag.<br/>                                                                         |
| <span id="TAG_VENDOR"></span><span id="tag_vendor"></span><dl> <dt>**Tag \_ Hersteller**</dt> <dt>(0x5- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                                        | Name-Attribut des Anbieters.<br/>                                                             |
| <span id="TAG_APP_NAME"></span><span id="tag_app_name"></span><dl> <dt>**Tag \_ APP- \_ Name**</dt> <dt>(0x6- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                                 | Das Anwendungs Namensattribut, das einen Anwendungs Eintrag in einer Shimdatenbank beschreibt.<br/> |
| <span id="TAG_COMMAND_LINE"></span><span id="tag_command_line"></span><dl> <dt>**Tag \_ Befehls \_ Zeile**</dt> <dt>(0x8- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                     | Das Befehlszeilen Attribut, das verwendet wird, wenn Argumente an einen Shim übergeben werden, z. b..<br/> |
| <span id="TAG_COMPANY_NAME"></span><span id="tag_company_name"></span><dl> <dt>**Tag \_ Firmen \_ Name**</dt> <dt>(0x9- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                     | Company Name-Attribut.<br/>                                                            |
| <span id="TAG_DLLFILE"></span><span id="tag_dllfile"></span><dl> <dt>**Tag \_ Dllfile**</dt> <dt>(0xa- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                                     | DLL-Datei Attribut für einen shimeintrag.<br/>                                               |
| <span id="TAG_WILDCARD_NAME"></span><span id="tag_wildcard_name"></span><dl> <dt>**Tag \_ Platzhalter \_ Name**</dt> <dt>(0xB- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                  | Platzhalter Namensattribut für einen ausführbaren Eintrag mit einem Platzhalter als Dateinamen.<br/>  |
| <span id="TAG_PRODUCT_NAME"></span><span id="tag_product_name"></span><dl> <dt>**Tag \_ Produkt \_ Name**</dt> <dt>(0x10- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                    | Product Name-Attribut.<br/>                                                            |
| <span id="TAG_PRODUCT_VERSION"></span><span id="tag_product_version"></span><dl> <dt>**Tag \_ Produkt \_ Version**</dt> <dt>(0x11- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>           | Produkt Versions Attribut.<br/>                                                         |
| <span id="TAG_FILE_DESCRIPTION"></span><span id="tag_file_description"></span><dl> <dt>**Tag \_ Datei \_ Beschreibung**</dt> <dt>(0x12- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>        | Dateibeschreibungs-Attribut.<br/>                                                        |
| <span id="TAG_FILE_VERSION"></span><span id="tag_file_version"></span><dl> <dt>**Tag \_ Datei \_ Version**</dt> <dt>(0x13- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                    | Datei Versions Attribut.<br/>                                                            |
| <span id="TAG_ORIGINAL_FILENAME"></span><span id="tag_original_filename"></span><dl> <dt>**Tag \_ Ursprünglicher \_ Dateiname**</dt> <dt>(0x14- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>     | Ursprüngliches Dateiname-Attribut.<br/>                                                      |
| <span id="TAG_INTERNAL_NAME"></span><span id="tag_internal_name"></span><dl> <dt>**Tag \_ Interner \_ Name**</dt> <dt>(0x15- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                 | Internes Dateiname-Attribut.<br/>                                                      |
| <span id="TAG_LEGAL_COPYRIGHT"></span><span id="tag_legal_copyright"></span><dl> <dt>**Tag \_ Rechts \_ Copyright**</dt> <dt>(0x16- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>           | Copyright-Attribut.<br/>                                                               |
| <span id="TAG_16BIT_DESCRIPTION"></span><span id="tag_16bit_description"></span><dl> Transponder- <dt>**\_ 16-Bit- \_ Beschreibung**</dt> <dt>(0x17- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>     | 16-Bit-Beschreibungs Attribut.<br/>                                                      |
| <span id="TAG_APPHELP_DETAILS"></span><span id="tag_apphelp_details"></span><dl> <dt>**Tag \_ AppHelp- \_ Details**</dt> <dt>(0x18- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>           | Das AppHelp Details-Nachrichten Attribut.<br/>                                     |
| <span id="TAG_LINK_URL"></span><span id="tag_link_url"></span><dl> <dt>**Tag \_ Link- \_ URL**</dt> <dt>(0x19- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                                | URL-Attribut für AppHelp Online-Link.<br/>                                                 |
| <span id="TAG_LINK_TEXT"></span><span id="tag_link_text"></span><dl> <dt>**Tag \_ \_Linktext**</dt> <dt>(0x1A \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                             | AppHelp Online Link Text-Attribut.<br/>                                                |
| <span id="TAG_APPHELP_TITLE"></span><span id="tag_apphelp_title"></span><dl> <dt>**Tag \_ AppHelp- \_ Titel**</dt> <dt>(0x1B- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                 | AppHelp-Titel Attribut.<br/>                                                           |
| <span id="TAG_APPHELP_CONTACT"></span><span id="tag_apphelp_contact"></span><dl> <dt>**Tag \_ AppHelp- \_ Kontakt**</dt> <dt>(0x1C- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>           | Kontakt Attribut des AppHelp-Herstellers.<br/>                                                  |
| <span id="TAG_SXS_MANIFEST"></span><span id="tag_sxs_manifest"></span><dl> <dt>**Tag \_ SxS- \_ Manifest**</dt> <dt>(0x1D- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                    | Seite-an-Seite-Manifest-Eintrag.<br/>                                                       |
| <span id="TAG_DATA_STRING"></span><span id="tag_data_string"></span><dl> <dt>**Tag \_ Daten \_ Zeichenfolge**</dt> <dt>(0x1E \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                       | Zeichen folgen Attribut für einen Dateneintrag.<br/>                                                 |
| <span id="TAG_MSI_TRANSFORM_FILE"></span><span id="tag_msi_transform_file"></span><dl> <dt>**Tag \_ MSI- \_ Transformations \_ Datei**</dt> <dt>(0x1F- \| **\_ Tagtyp \_ stringref**)</dt> </dl> | Dateiname-Attribut eines MSI-Transformations Eintrags.<br/>                                |
| <span id="TAG_16BIT_MODULE_NAME"></span><span id="tag_16bit_module_name"></span><dl> <dt>**Tag- \_ 16-Bit- \_ \_ Modulname**</dt> <dt>(0x20- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>    | das 16-Bit-Modul Namensattribut.<br/>                                                      |
| <span id="TAG_LAYER_DISPLAYNAME"></span><span id="tag_layer_displayname"></span><dl> <dt>**Tag \_ \_Ebenendisplay Name**</dt> <dt>(0x21- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>     | Nicht verwendet.<br/>                                                                            |
| <span id="TAG_COMPILER_VERSION"></span><span id="tag_compiler_version"></span><dl> <dt>**Tag \_ \_Compilerversion**</dt> <dt>(0x22- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>        | Compilerversion der Shimdatenbank.<br/>                                                    |
| <span id="TAG_ACTION_TYPE"></span><span id="tag_action_type"></span><dl> <dt>**Tag \_ \_Aktionstyp**</dt> <dt>(0x23- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                       | Nicht verwendet.<br/>                                                                            |
| <span id="TAG_EXPORT_NAME"></span><span id="tag_export_name"></span><dl> <dt>**Tag \_ Export \_ Name**</dt> <dt>(0x24- \| **\_ Tagtyp " \_ strauf**")</dt> </dl>                       | Exportieren Sie das Dateinamen Attribut.<br/>                                                        |



Die folgenden Einträge sind vom Typ **\_ Tagtyp \_ DWORD** (0x4000).



| Konstante/Wert                                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| <span id="TAG_SIZE"></span><span id="tag_size"></span><dl> <dt>**Tag \_ Größe**</dt> <dt>(0x1- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                                 | Dateigrößen Attribut.<br/>                                                                                  |
| <span id="TAG_OFFSET"></span><span id="tag_offset"></span><dl> <dt>**Tag \_ Offset**</dt> <dt>(0x2- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                           | Nicht verwendet.<br/>                                                                                               |
| <span id="TAG_CHECKSUM"></span><span id="tag_checksum"></span><dl> <dt>**Tag \_ Prüfsumme**</dt> <dt>(0x3- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                     | File Prüfsumme-Attribut.<br/>                                                                              |
| <span id="TAG_SHIM_TAGID"></span><span id="tag_shim_tagid"></span><dl> <dt>**Tag \_ Shim- \_ TagID**</dt> <dt>(0x4- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                              | Shim- **TagID** -Attribut.<br/>                                                                             |
| <span id="TAG_PATCH_TAGID"></span><span id="tag_patch_tagid"></span><dl> <dt>**Tag \_ \_Patchtagid**</dt> <dt>(0x5- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                           | Patch- **TagID** -Attribut.<br/>                                                                            |
| <span id="TAG_MODULE_TYPE"></span><span id="tag_module_type"></span><dl> <dt>**Tag \_ \_Modultyp**</dt> <dt>(0x6- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                           | Modultyp Attribut.<br/>                                                                                |
| <span id="TAG_VERDATEHI"></span><span id="tag_verdatehi"></span><dl> <dt>**Tag \_ Verdatehi**</dt> <dt>(0x7- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                  | Der hochwertige Teil des Dateiversions-Date-Attributs.<br/>                                                |
| <span id="TAG_VERDATELO"></span><span id="tag_verdatelo"></span><dl> <dt>**Tag \_ Verdatelo**</dt> <dt>(0x8- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                  | Niedriger Anordnungs Anteil des Dateiversions-Datums Attributs.<br/>                                                 |
| <span id="TAG_VERFILEOS"></span><span id="tag_verfileos"></span><dl> <dt>**Tag \_ Verfileos**</dt> <dt>(0x9- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                  | Datei Versions Attribut des Betriebssystems.<br/>                                                              |
| <span id="TAG_VERFILETYPE"></span><span id="tag_verfiletype"></span><dl> <dt>**Tag \_ Verfiletype**</dt> <dt>(0xa- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                            | Dateityp Attribut.<br/>                                                                                  |
| <span id="TAG_PE_CHECKSUM"></span><span id="tag_pe_checksum"></span><dl> <dt>**Tag \_ PE- \_ Prüfsumme**</dt> <dt>(0xB- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                           | Prüfsummen Attribut der PE-Datei.<br/>                                                                           |
| <span id="TAG_PREVOSMAJORVER"></span><span id="tag_prevosmajorver"></span><dl> <dt>**Tag \_ Prevosmajorver**</dt> <dt>(0xc- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                   | Das Attribut für die Hauptversion des Betriebssystems.<br/>                                                             |
| <span id="TAG_PREVOSMINORVER"></span><span id="tag_prevosminorver"></span><dl> <dt>**Tag \_ Prevosminorver**</dt> <dt>(0xD \| **Tag \_ Type \_ DWORD**)</dt> </dl>                   | Neben Versions Attribut des Betriebssystems.<br/>                                                             |
| <span id="TAG_PREVOSPLATFORMID"></span><span id="tag_prevosplatformid"></span><dl> <dt>**Tag \_ Prevosplatformid**</dt> <dt>(0xe- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>             | Bezeichnerattribut für die Betriebssystem Plattform.<br/>                                                       |
| <span id="TAG_PREVOSBUILDNO"></span><span id="tag_prevosbuildno"></span><dl> <dt>**Tag \_ Prevosbuildno**</dt> <dt>(0xF- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                      | Attribut für die Buildnummer des Betriebssystems.<br/>                                                              |
| <span id="TAG_PROBLEMSEVERITY"></span><span id="tag_problemseverity"></span><dl> <dt>**Tag \_ Problemschwere Grad**</dt> <dt>(0x10- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>               | Block-Attribut eines AppHelp-Eintrags. Hiermit wird bestimmt, ob die Anwendung hart oder vorläufig blockiert ist.<br/> |
| <span id="TAG_LANGID"></span><span id="tag_langid"></span><dl> <dt>**Tag \_ Langid**</dt> <dt>(0x11- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                          | Der sprach Bezeichner eines AppHelp-Eintrags.<br/>                                                              |
| <span id="TAG_VER_LANGUAGE"></span><span id="tag_ver_language"></span><dl> <dt>**Tag \_ Ver- \_ Sprache**</dt> <dt>(0x12- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                       | Sprach Versions Attribut einer Datei.<br/>                                                                 |
| <span id="TAG_ENGINE"></span><span id="tag_engine"></span><dl> <dt>**Tag \_ Engine**</dt> <dt>(0x14 \| **Tag \_ Type \_ DWORD**)</dt> </dl>                                          | Nicht verwendet.<br/>                                                                                               |
| <span id="TAG_HTMLHELPID"></span><span id="tag_htmlhelpid"></span><dl> <dt>**Tag \_ Htmlhelpid**</dt> <dt>(0x15 \| **Tag \_ Type \_ DWORD**)</dt> </dl>                              | Hilfe-Bezeichnerattribut für einen AppHelp-Eintrag.<br/>                                                       |
| <span id="TAG_INDEX_FLAGS"></span><span id="tag_index_flags"></span><dl> <dt>**Tag \_ \_Indexflags**</dt> <dt>(0x16- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                          | Flags-Attribut für einen Index Eintrag.<br/>                                                                   |
| <span id="TAG_FLAGS"></span><span id="tag_flags"></span><dl> <dt>**Tag \_ Flags**</dt> <dt>(0x17- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                             | Flags-Attribut für einen AppHelp-Eintrag.<br/>                                                                 |
| <span id="TAG_DATA_VALUETYPE"></span><span id="tag_data_valuetype"></span><dl> <dt>**Tag \_ \_Datenvaluetype**</dt> <dt>(0x18- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                 | Datentyp Attribut für einen Dateneintrag.<br/>                                                                 |
| <span id="TAG_DATA_DWORD"></span><span id="tag_data_dword"></span><dl> <dt>**Tag \_ Data \_ DWORD**</dt> <dt>(0x19- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                             | **DWORD** -Wert Attribut für einen Dateneintrag.<br/>                                                           |
| <span id="TAG_LAYER_TAGID"></span><span id="tag_layer_tagid"></span><dl> <dt>**Tag \_ \_Ebenentagid**</dt> <dt>(0x1A- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                          | Das **TagID** -Attribut für die Layer-Shim.<br/>                                                                       |
| <span id="TAG_MSI_TRANSFORM_TAGID"></span><span id="tag_msi_transform_tagid"></span><dl> <dt>**Tag \_ MSI- \_ Transformations- \_ TagID**</dt> <dt>(0x1B- \| **\_ Tagtyp \_ DWORD**)</dt> </dl> | MSI- **transformierentagid** -Attribut.<br/>                                                                    |
| <span id="TAG_LINKER_VERSION"></span><span id="tag_linker_version"></span><dl> <dt>**Tag \_ Linker- \_ Version**</dt> <dt>(0x1C- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                 | Das Linker-Versions Attribut einer Datei.<br/>                                                                   |
| <span id="TAG_LINK_DATE"></span><span id="tag_link_date"></span><dl> <dt>**Tag \_ Verknüpfungs \_ Datum**</dt> <dt>(0x1D \| **Tag \_ Type \_ DWORD**)</dt> </dl>                                | Link Date-Attribut einer Datei.<br/>                                                                        |
| <span id="TAG_UPTO_LINK_DATE"></span><span id="tag_upto_link_date"></span><dl> <dt>**Tag \_ \_ \_ Datum des bis zu Links**</dt> <dt>(0x1E \| **Tag \_ Type \_ DWORD**)</dt> </dl>                | Link Date-Attribut einer Datei. Die Übereinstimmung wird bis einschließlich dieses Verknüpfungs Datums erreicht.<br/>                   |
| <span id="TAG_OS_SERVICE_PACK"></span><span id="tag_os_service_pack"></span><dl> <dt>**Tag \_ Betriebssystem \_ Service \_ Pack**</dt> <dt>(0x1F- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>             | Service Pack Attribut des Betriebssystems für einen ausführbaren Eintrag.<br/>                                      |
| <span id="TAG_FLAG_TAGID"></span><span id="tag_flag_tagid"></span><dl> <dt>**Tag \_ Markieren Sie \_ TagID**</dt> <dt>(0x20- \| **\_ Tagtyp \_ DWORD**)</dt> . </dl>                             | Flags- **TagID** -Attribut.<br/>                                                                            |
| <span id="TAG_RUNTIME_PLATFORM"></span><span id="tag_runtime_platform"></span><dl> <dt>**Tag \_ Lauf Zeit \_ Plattform**</dt> <dt>(0x21- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>           | Lauf Zeit Platt Form Attribut einer Datei.<br/>                                                                |
| <span id="TAG_OS_SKU"></span><span id="tag_os_sku"></span><dl> <dt>**Tag \_ Betriebssystem- \_ SKU**</dt> <dt>(0x22- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                         | SKU-Attribut des Betriebssystems für einen ausführbaren Eintrag.<br/>                                               |
| <span id="TAG_OS_PLATFORM"></span><span id="tag_os_platform"></span><dl> <dt>**Tag \_ Betriebssystem \_ Plattform**</dt> <dt>(0x23- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                          | Attribut der Betriebssystem Plattform.<br/>                                                                  |
| <span id="TAG_APP_NAME_RC_ID"></span><span id="tag_app_name_rc_id"></span><dl> <dt>**Tag \_ APP- \_ Name \_ RC- \_ ID**</dt> <dt>(0x24 \| **Tag \_ Type \_ DWORD**)</dt> </dl>               | Das Ressourcen Bezeichnerattribut für den Anwendungsnamen für AppHelp-Einträge.<br/>                                   |
| <span id="TAG_VENDOR_NAME_RC_ID"></span><span id="tag_vendor_name_rc_id"></span><dl> <dt>**Tag \_ Anbieter \_ Name \_ RC- \_ ID**</dt> <dt>(0x25 \| **Tag \_ Type \_ DWORD**)</dt> </dl>      | Attribut Name ressourcenbezeichnerattribut für AppHelp-Einträge.<br/>                                        |
| <span id="TAG_SUMMARY_MSG_RC_ID"></span><span id="tag_summary_msg_rc_id"></span><dl> <dt>**Tag \_ Zusammenfassungs Meldung \_ \_ RC- \_ ID**</dt> <dt>(0x26 \| **Tag \_ Type \_ DWORD**)</dt> </dl>      | Zusammenfassungs Nachrichten-ressourcenbezeichnerattribut für AppHelp-Einträge.<br/>                                    |
| <span id="TAG_VISTA_SKU"></span><span id="tag_vista_sku"></span><dl> <dt>**Tag \_ Vista- \_ SKU**</dt> <dt>(0x27- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                | Windows Vista-SKU-Attribut.<br/>                                                                          |
| <span id="TAG_DESCRIPTION_RC_ID"></span><span id="tag_description_rc_id"></span><dl> <dt>**Tag \_ Beschreibung der \_ RC- \_ ID**</dt> <dt>(0x28 \| **Tag \_ Type \_ DWORD**)</dt> </dl>       | Description ressourcenbezeichnerattribut für AppHelp-Einträge.<br/>                                        |
| <span id="TAG_PARAMETER1_RC_ID"></span><span id="tag_parameter1_rc_id"></span><dl> <dt>**Tag \_ PARAMETER1 \_ RC- \_ ID**</dt> <dt>(0x29 \| **Tag \_ Type \_ DWORD**)</dt> </dl>          | Parameter1 ressourcenbezeichnerattribut für AppHelp-Einträge.<br/>                                         |
| <span id="TAG_TAGID"></span><span id="tag_tagid"></span><dl> <dt>**Tag \_ TagID**</dt> <dt>(0x801- \| **\_ Tagtyp \_ DWORD**)</dt> </dl>                                            | **TagID** -Attribut.<br/>                                                                                  |



Der folgende Eintrag ist vom Typ **" \_ Tagtyp \_ Zeichenfolge** (0X8000)".



| Konstante/Wert                                                                                                                                                                                                                                                            | BESCHREIBUNG                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|
| <span id="TAG_STRINGTABLE_ITEM"></span><span id="tag_stringtable_item"></span><dl> <dt>**Tag \_ STRINGTABLE- \_ Element**</dt> <dt>(0x801- \| **\_ Tagtyp \_ Zeichenfolge**)</dt> </dl> | Zeichen folgen-Tabellen Element Eintrag.<br/> |



Die folgenden Einträge sind vom Typ **\_ Tagtyp \_ null** (0x1000).



| Konstante/Wert                                                                                                                                                                                                                                                                            | BESCHREIBUNG                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span id="TAG_INCLUDE"></span><span id="tag_include"></span><dl> <dt>**Tag \_ INCLUDE**</dt> <dt>(0x1- \| **\_ Tagtyp \_ null**)</dt> </dl>                                                 | Listeneintrag einschließen.<br/>                           |
| <span id="TAG_GENERAL"></span><span id="tag_general"></span><dl> <dt>**Tag \_ Allgemein**</dt> <dt>(0x2- \| **\_ Tagtyp \_ null**)</dt> </dl>                                                 | Allgemeine Shim-Eintrag.<br/>                   |
| <span id="TAG_MATCH_LOGIC_NOT"></span><span id="tag_match_logic_not"></span><dl> <dt>**Tag \_ Übereinstimmungs \_ Logik \_ nicht**</dt> <dt>(0x3- \| **\_ Tagtyp \_ null**)</dt> </dl>                       | Nicht übereinstimmender Logik Eintrag.<br/>                  |
| <span id="TAG_APPLY_ALL_SHIMS"></span><span id="tag_apply_all_shims"></span><dl> <dt>**Tag \_ \_Alle \_ Shims anwenden**</dt> <dt>(0x4- \| **\_ Tagtyp \_ null**)</dt> </dl>                       | Nicht verwendet.<br/>                                       |
| <span id="TAG_USE_SERVICE_PACK_FILES"></span><span id="tag_use_service_pack_files"></span><dl> <dt>**Tag \_ \_Service \_ Pack- \_ Dateien verwenden**</dt> <dt>(0x5- \| **\_ Tagtyp \_ null**)</dt> </dl> | Service Pack-Informationen für AppHelp-Einträge.<br/> |
| <span id="TAG_MITIGATION_OS"></span><span id="tag_mitigation_os"></span><dl> <dt>**Tag \_ Entschärfungs \_ Betriebssystem**</dt> <dt>(0x6- \| **\_ Tagtyp \_ null**)</dt> </dl>                              | Entschärfung bei Betriebssystem-Bereichs Eintrag.<br/>   |
| <span id="TAG_BLOCK_UPGRADE"></span><span id="tag_block_upgrade"></span><dl> <dt>**Tag \_ Block \_ Upgrade**</dt> <dt>(0x7- \| **\_ Tagtyp \_ null**)</dt> </dl>                              | Aktualisierungs Block Eintrag.<br/>                          |
| <span id="TAG_INCLUDEEXCLUDEDLL"></span><span id="tag_includeexcludedll"></span><dl> <dt>**Tag \_ Includeexcludedll**</dt> <dt>(0x8- \| **\_ Tagtyp \_ null**)</dt> </dl>                   | DLL-include/Ausschluss-Eintrag.<br/>                    |



Die folgenden Einträge sind vom Typ **" \_ Tagtyp \_ QWORD** (0x5.000)".



| Konstante/Wert                                                                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TAG_TIME"></span><span id="tag_time"></span><dl> <dt>**Tag \_ Uhrzeit**</dt> <dt>(0x1- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                                                                | Zeit Attribut.<br/>                                                                                     |
| <span id="TAG_BIN_FILE_VERSION"></span><span id="tag_bin_file_version"></span><dl> <dt>**Tag \_ BIN- \_ Datei \_ Version**</dt> <dt>(0x2- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                          | Attribut der Klassendatei Version für Datei Einträge.<br/>                                                        |
| <span id="TAG_BIN_PRODUCT_VERSION"></span><span id="tag_bin_product_version"></span><dl> <dt>**Tag \_ BIN- \_ Produkt \_ Version**</dt> <dt>(0x3- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                 | Bin-Produkt Versions Attribut für Datei Einträge.<br/>                                                     |
| <span id="TAG_MODTIME"></span><span id="tag_modtime"></span><dl> <dt>**Tag \_ Modtime**</dt> <dt>(0x4- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                                                       | Nicht verwendet.<br/>                                                                                             |
| <span id="TAG_FLAG_MASK_KERNEL"></span><span id="tag_flag_mask_kernel"></span><dl> <dt>**Tag \_ Flag \_ für \_ flagmaske**</dt> <dt>(0x5- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                          | Kernel Flag Mask-Attribut.<br/>                                                                         |
| <span id="TAG_UPTO_BIN_PRODUCT_VERSION"></span><span id="tag_upto_bin_product_version"></span><dl> <dt>**Tag \_ Upto \_ bin- \_ Produkt \_ Version**</dt> <dt>(0x6- \| **\_ Tagtyp \_ QWORD**)</dt> </dl> | Bin-Produkt Versions Attribut einer Datei. Der Abgleich erfolgt bis einschließlich dieser Produktversion.<br/> |
| <span id="TAG_DATA_QWORD"></span><span id="tag_data_qword"></span><dl> <dt>**Tag \_ Data \_ QWORD**</dt> <dt>(0x7- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                                             | **ULONGLONG** -Wert Attribut für einen Dateneintrag.<br/>                                                     |
| <span id="TAG_FLAG_MASK_USER"></span><span id="tag_flag_mask_user"></span><dl> <dt>**Tag \_ Flag \_ mask- \_ Benutzer**</dt> <dt>(0x8- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                                | Benutzerflag Maske-Attribut.<br/>                                                                           |
| <span id="TAG_FLAGS_NTVDM1"></span><span id="tag_flags_ntvdm1"></span><dl> <dt>**Tag \_ Flags \_ NTVDM1**</dt> <dt>(0x9- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                                       | NTVDM1 Flag Mask-Attribut.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM2"></span><span id="tag_flags_ntvdm2"></span><dl> <dt>**Tag \_ Flags \_ NTVDM2**</dt> <dt>(0xa- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                                       | NTVDM2 Flag Mask-Attribut.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM3"></span><span id="tag_flags_ntvdm3"></span><dl> <dt>**Tag \_ Flags \_ NTVDM3**</dt> <dt>(0xB- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                                       | NTVDM3 Flag Mask-Attribut.<br/>                                                                         |
| <span id="TAG_FLAG_MASK_SHELL"></span><span id="tag_flag_mask_shell"></span><dl> <dt>**Tag \_ Flagmaske- \_ \_ Shell**</dt> <dt>(0xc- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                             | Shellflag Mask-Attribut.<br/>                                                                          |
| <span id="TAG_UPTO_BIN_FILE_VERSION"></span><span id="tag_upto_bin_file_version"></span><dl> <dt>**Tag \_ Bis zur \_ bin- \_ Datei \_ Version**</dt> <dt>(0xD \| **Tag \_ Type \_ QWORD**)</dt> </dl>          | Datei Versions Attribut der Datei. Die Übereinstimmung wird bis einschließlich dieser Dateiversion erreicht.<br/>       |
| <span id="TAG_FLAG_MASK_FUSION"></span><span id="tag_flag_mask_fusion"></span><dl> <dt>**Tag \_ \_ \_ Fusion der flagmaske**</dt> <dt>(0xe- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                          | Fusion Flag Mask-Attribut.<br/>                                                                         |
| <span id="TAG_FLAG_PROCESSPARAM"></span><span id="tag_flag_processparam"></span><dl> <dt>**Tag \_ Flag \_ processparam**</dt> <dt>(0xF- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                        | Process param Flag-Attribut.<br/>                                                                       |
| <span id="TAG_FLAG_LUA"></span><span id="tag_flag_lua"></span><dl> <dt>**Tag \_ Flag \_ Lua**</dt> <dt>(0x10- \| **\_ Tagtyp \_ QWORD**)</dt> </dl>                                                  | Lua-Flag-Attribut.<br/>                                                                                 |
| <span id="TAG_FLAG_INSTALL"></span><span id="tag_flag_install"></span><dl> <dt>**Tag \_ Flag \_ Installieren**</dt> <dt>(0x11 \| **Tag \_ Type \_ QWORD**)</dt> </dl>                                      | Installationsflag-Attribut.<br/>                                                                             |



Die folgenden Einträge sind vom Typ " **Tag \_ Type \_ Binary** (0x9000)".



| Konstante/Wert                                                                                                                                                                                                                                                     | BESCHREIBUNG                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="TAG_PATCH_BITS"></span><span id="tag_patch_bits"></span><dl> <dt>**Tag \_ \_Patchbits**</dt> <dt>(0x2- \| **\_ Tagtyp \_ Binär**)</dt> </dl>              | Bits-Attribut der Patchdatei.<br/>                          |
| <span id="TAG_FILE_BITS"></span><span id="tag_file_bits"></span><dl> <dt>**Tag \_ \_Dateibits**</dt> <dt>(0x3- \| **\_ Tagtyp \_ Binär**)</dt> </dl>                 | Dateibits-Attribut.<br/>                                |
| <span id="TAG_EXE_ID"></span><span id="tag_exe_id"></span><dl> <dt>**Tag \_ EXE- \_ ID**</dt> <dt>(0x4- \| **\_ Tagtyp \_ Binär**)</dt> </dl>                          | **GUID** -Attribut eines ausführbaren Eintrags.<br/>          |
| <span id="TAG_DATA_BITS"></span><span id="tag_data_bits"></span><dl> <dt>**Tag \_ \_Datenbits**</dt> <dt>(0x5- \| **\_ Tagtyp \_ Binär**)</dt> </dl>                 | Datenbits-Attribut.<br/>                                |
| <span id="TAG_MSI_PACKAGE_ID"></span><span id="tag_msi_package_id"></span><dl> <dt>**Tag \_ MSI- \_ Paket- \_ ID**</dt> <dt>(0x6- \| **\_ Tagtyp \_ Binär**)</dt> </dl> | MSI-paketbezeichnerattribut eines MSI-Pakets.<br/> |
| <span id="TAG_DATABASE_ID"></span><span id="tag_database_id"></span><dl> <dt>**Tag \_ Datenbank- \_ ID**</dt> <dt>(0x7- \| **\_ Tagtyp \_ Binär**)</dt> </dl>           | **GUID** -Attribut einer Datenbank.<br/>                   |
| <span id="TAG_INDEX_BITS"></span><span id="tag_index_bits"></span><dl> <dt>**Tag \_ Index \_ Bits**</dt> <dt>(0x801- \| **\_ Tagtyp \_ Binär**)</dt> </dl>            | Index Bits-Attribut.<br/>                               |



Die folgenden Einträge sind vom Typ **\_ Tagtyp \_ Word** (0x3000).



| Konstante/Wert                                                                                                                                                                                                                                      | BESCHREIBUNG                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="TAG_MATCH_MODE"></span><span id="tag_match_mode"></span><dl> <dt>**Tag \_ \_**</dt> Übereinstimmungs Modus <dt>(0x1- \| **\_ Tagtyp \_ Wort**)</dt> </dl> | Übereinstimmungs Modus-Attribut.<br/>                   |
| <span id="TAG_TAG"></span><span id="tag_tag"></span><dl> <dt>**Tag \_ Tag**</dt> <dt>(0x801- \| **\_ Tagtyp \_ Wort**)</dt> </dl>                     | Tageintrag.<br/>                              |
| <span id="TAG_INDEX_TAG"></span><span id="tag_index_tag"></span><dl> <dt>**Tag \_ \_Indextag**</dt> <dt>(0x802- \| **\_ Tagtyp \_ Wort**)</dt> </dl>  | Indextagattribut für einen Index Eintrag.<br/> |
| <span id="TAG_INDEX_KEY"></span><span id="tag_index_key"></span><dl> <dt>**Tag \_ Index \_ Schlüssel**</dt> <dt>(0x803- \| **\_ Tagtyp \_ Wort**)</dt> </dl>  | Index Schlüssel Attribut für einen Index Eintrag.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Exposeenums2managed. h ("axextendenums. h" einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Tagtypen](tag-types.md)
</dt> <dt>

[**TagID**](tagid.md)
</dt> <dt>

[**Tagref**](tagref.md)
</dt> </dl>

 

 




