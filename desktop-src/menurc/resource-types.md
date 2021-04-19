---
title: Ressourcentypen (Winuser. h)
description: Im folgenden finden Sie die vordefinierten Ressourcentypen.
ms.assetid: 8d27f79a-8165-4565-a975-f25b2344efdc
topic_type:
- apiref
api_name:
- RT_ACCELERATOR
- RT_ANICURSOR
- RT_ANIICON
- RT_BITMAP
- RT_CURSOR
- RT_DIALOG
- RT_DLGINCLUDE
- RT_FONT
- RT_FONTDIR
- RT_GROUP_CURSOR
- RT_GROUP_ICON
- RT_HTML
- RT_ICON
- RT_MANIFEST
- RT_MENU
- RT_MESSAGETABLE
- RT_PLUGPLAY
- RT_RCDATA
- RT_STRING
- RT_VERSION
- RT_VXD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595f1d459f645d26014a644d0e2b7cb608f4c6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372710"
---
# <a name="resource-types"></a>Ressourcentypen

Im folgenden finden Sie die vordefinierten Ressourcentypen.



| Konstante/Wert                                                                                                                                                                                                                                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RT_ACCELERATOR"></span><span id="rt_accelerator"></span><dl> <dt>**RT \_**</dt>Zugriffstaste <dt>makeintresource (9)</dt> </dl>                                 | Zugriffstasten Tabelle.<br/>                                                                                                                                                                                                                                                                    |
| <span id="RT_ANICURSOR"></span><span id="rt_anicursor"></span><dl> <dt>**RT \_ Anicursor**</dt> <dt>makeintresource (21)</dt> </dl>                                      | Animierter Cursor.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_ANIICON"></span><span id="rt_aniicon"></span><dl> <dt>**RT \_ Aniicon**</dt> <dt>makeintresource (22)</dt> </dl>                                            | Animiertes Symbol.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_BITMAP"></span><span id="rt_bitmap"></span><dl> <dt>**RT \_ Bitmap**</dt> <dt>makeintresource (2)</dt> </dl>                                                | Bitmap-Ressource.<br/>                                                                                                                                                                                                                                                                      |
| <span id="RT_CURSOR"></span><span id="rt_cursor"></span><dl> <dt>**RT \_ Cursor**</dt> <dt>makeintresource (1)</dt> </dl>                                                | Hardware abhängige Cursor Ressource.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_DIALOG"></span><span id="rt_dialog"></span><dl> <dt>**RT \_ Dialog**</dt> <dt>makeintresource (5)</dt> </dl>                                                | (Dialog Feld).<br/>                                                                                                                                                                                                                                                                           |
| <span id="RT_DLGINCLUDE"></span><span id="rt_dlginclude"></span><dl> <dt>**RT \_ DLGINCLUDE**</dt> <dt>makeintresource (17)</dt> </dl>                                   | Ermöglicht einem Tool zur Ressourcen Bearbeitung, eine Zeichenfolge einer RC-Datei zuzuordnen. In der Regel ist die Zeichenfolge der Name der Header Datei, die symbolische Namen bereitstellt. Der Ressourcen Compiler analysiert die Zeichenfolge, ignoriert aber andernfalls den Wert. Beispiel: <br/> `1 DLGINCLUDE "MyFile.h"`<br/> |
| <span id="RT_FONT"></span><span id="rt_font"></span><dl> <dt>**RT \_ Schriftart**</dt> <dt>makeintresource (8)</dt> </dl>                                                      | Schriftart Ressource.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_FONTDIR"></span><span id="rt_fontdir"></span><dl> <dt>**RT \_ Fontdir**</dt> <dt>makeintresource (7)</dt> </dl>                                             | Schriftart Verzeichnis Ressource.<br/>                                                                                                                                                                                                                                                              |
| <span id="RT_GROUP_CURSOR"></span><span id="rt_group_cursor"></span><dl> <dt>**RT \_ Gruppen \_ Cursor**</dt> <dt>makeintresource ((ULONG \_ PTR) (RT- \_ Cursor) + 11)</dt> </dl> | Hardware unabhängige Cursor Ressource.<br/>                                                                                                                                                                                                                                                 |
| <span id="RT_GROUP_ICON"></span><span id="rt_group_icon"></span><dl> <dt>**RT \_ Gruppen \_ Symbol**</dt> <dt>makeintresource ((ULONG \_ PTR) (RT- \_ Symbol) + 11)</dt> </dl>         | Hardware unabhängige Symbol Ressource.<br/>                                                                                                                                                                                                                                                   |
| <span id="RT_HTML"></span><span id="rt_html"></span><dl> <dt>**RT \_ HTML**</dt> - <dt>makeintresource (23)</dt> </dl>                                                     | HTML-Ressource.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_ICON"></span><span id="rt_icon"></span><dl> <dt>**RT \_ Symbol**</dt> " <dt>makeintresource" (3)</dt> </dl>                                                      | Hardware abhängige Symbol Ressource.<br/>                                                                                                                                                                                                                                                     |
| <span id="RT_MANIFEST"></span><span id="rt_manifest"></span><dl> <dt>**RT \_ Manifest**</dt> <dt>makeintresource (24)</dt> </dl>                                         | Paralleles Assemblymanifest.<br/>                                                                                                                                                                                                                                                       |
| <span id="RT_MENU"></span><span id="rt_menu"></span><dl> <dt>**RT \_ Menü**</dt> " <dt>makeintresource" (4)</dt> </dl>                                                      | Menü Ressource.<br/>                                                                                                                                                                                                                                                                        |
| <span id="RT_MESSAGETABLE"></span><span id="rt_messagetable"></span><dl> <dt>**RT \_ Messagetable**</dt> <dt>makeintresource (11)</dt> </dl>                             | Nachrichten Tabelleneintrag.<br/>                                                                                                                                                                                                                                                                  |
| <span id="RT_PLUGPLAY"></span><span id="rt_plugplay"></span><dl> <dt>**RT \_ Plugplay**</dt> <dt>makeintresource (19)</dt> </dl>                                         | Plug & Play Ressource.<br/>                                                                                                                                                                                                                                                               |
| <span id="RT_RCDATA"></span><span id="rt_rcdata"></span><dl> <dt>**RT \_ RCDATA**</dt> <dt>makeintresource (10)</dt> </dl>                                               | Anwendungs definierte Ressource (Rohdaten).<br/>                                                                                                                                                                                                                                              |
| <span id="RT_STRING"></span><span id="rt_string"></span><dl> <dt>**RT \_ String**</dt> <dt>makeintresource (6)</dt> </dl>                                                | Zeichen folgen Tabelleneintrag.<br/>                                                                                                                                                                                                                                                                   |
| <span id="RT_VERSION"></span><span id="rt_version"></span><dl> <dt>**RT \_ Version**</dt> <dt>makeintresource (16)</dt> </dl>                                            | Versions Ressource.<br/>                                                                                                                                                                                                                                                                     |
| <span id="RT_VXD"></span><span id="rt_vxd"></span><dl> <dt>**RT \_ VXD**</dt> <dt>makeintresource (20)</dt> </dl>                                                        | VXD.<br/>                                                                                                                                                                                                                                                                                  |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

 





