---
description: 'Von Protokoll Handlern zurückgegebene Fehlermeldungen:'
ms.assetid: b5e99ad1-1698-483c-8173-796af33085c4
title: Protokoll Handler-Fehlermeldungen suchen (searchapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297ea44c367069a5558355cf6fe81cd9db57ee53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128560"
---
# <a name="search-protocol-handler-error-messages"></a>Protokoll Handler-Fehlermeldungen suchen

Von Protokoll Handlern zurückgegebene Fehlermeldungen:



| Konstante/Wert                                                                                                                                                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRTH_E_ACCESS_DENIED"></span><span id="prth_e_access_denied"></span><dl> <dt>**Prth \_ E \_ Access \_ verweigert**</dt> <dt>0x80041205l</dt> </dl>             | Der Zugriff wurde verweigert. Wenn dies während eines inkrementellen Crawls auftritt, wird die Datei aus der URL-Warteschlange des gatherers gelöscht.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_IS_READ_NONE"></span><span id="prth_e_acl_is_read_none"></span><dl> <dt>**Prth \_ E \_ ACL \_ ist \_ Read \_ None**</dt> <dt>0x80041211l</dt> </dl>  | Das Element wird nicht indiziert. Die ACL ermöglicht nicht, das Element zu lesen.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_TOO_BIG"></span><span id="prth_e_acl_too_big"></span><dl> <dt>**Prth \_ E \_ ACL \_ zu \_ groß**</dt> <dt>0x80041212l</dt> </dl>                  | Die ACL hat 64 KB überschritten. Bei der Suche wird das Element nicht indiziert.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_BAD_REQUEST"></span><span id="prth_e_bad_request"></span><dl> <dt>**Prth \_ E ungültige \_ \_ Anforderung**</dt> <dt>0x80041208l</dt> </dl>                   | Die Anforderung war aufgrund eines Fehlers in der URL ungültig.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_COMM_ERROR"></span><span id="prth_e_comm_error"></span><dl> <dt>**Prth \_ E- \_ comm- \_ Fehler**</dt> <dt>0x80041200l</dt> </dl>                      | Gibt einen Kommunikations-oder Server Fehler an. Wenn für einen bestimmten Server zu viele dieser Fehler vorhanden sind, kennzeichnet der Gatherer den Server als nicht verfügbar.<br/>                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_NOT_REDIRECTED"></span><span id="prth_e_not_redirected"></span><dl> <dt>**Prth \_ E \_ nicht \_ umgeleitet**</dt> <dt>0x80041207l</dt> </dl>          | Die umgeleitete URL ist nicht vorhanden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_E_OBJ_NOT_FOUND"></span><span id="prth_e_obj_not_found"></span><dl> <dt>**Prth \_ E \_ obj \_ nicht \_ gefunden**</dt> <dt>0x80041201l</dt> </dl>            | Objekt konnte nicht gefunden werden. Gibt an, dass der Gatherer das Dokument aus der Warteschlange löschen soll, wenn es während eines inkrementellen Crawls nicht gefunden wurde.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_REQUEST_ERROR"></span><span id="prth_e_request_error"></span><dl> <dt>**Prth \_ E- \_ Anforderungs \_ Fehler**</dt> <dt>0x80041202l</dt> </dl>             | Die verwendeten Optionen werden nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="PRTH_E_SERVER_ERROR"></span><span id="prth_e_server_error"></span><dl> <dt>**Prth \_ E- \_ Server \_ Fehler**</dt> <dt>0x80041206l</dt> </dl>                | Kommunikations-oder Server Fehler. Wenn für einen bestimmten Server zu viele dieser Fehler vorhanden sind, kennzeichnet der Gatherer den Server als nicht verfügbar.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PRTH_S_NOT_ALL_PARTS"></span><span id="prth_s_not_all_parts"></span><dl> <dt>**Prth \_ S \_ nicht \_ alle \_ Teile**</dt> <dt>0x8004121bl</dt> </dl>            | Auf Teile eines Elements kann nicht zugegriffen werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PRTH_S_NOT_MODIFIED"></span><span id="prth_s_not_modified"></span><dl> <dt>**Prth \_ S \_ nicht \_ geändert**</dt> <dt>0x00041203l</dt> </dl>                | Der Element Inhalt wurde nicht geändert. Wenn dieser Fehler während eines inkrementellen Crawls auftritt, überspringt der Gatherer dieses Element, da das Element nicht geändert wurde.<br/>                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_S_TRY_IMPERSONATING"></span><span id="prth_s_try_impersonating"></span><dl> <dt>**Prth \_ S \_ versuchen \_ Sie**</dt> , die Identität <dt>0x00041225l</dt> anzunehmen. </dl> | Auf das Element sollte während der Identität eines Benutzers zugegriffen werden. Es wird erwartet, dass der Protokollhandler [**IUrlAccessor3:: getimpersonationsidblosb**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs) implementiert, damit der Such Protokoll Host eine Liste von SIDs abrufen kann, die für den Identitätswechsel verwendet werden können, und die Verwendung von [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2)wiederherstellen und dabei die Identität eines der zulässigen Benutzer annehmen, wenn das Element geöffnet wird. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>                                            |
| Header<br/>                   | <dl> <dt>Searchapi. h</dt> </dl> |



 

 




