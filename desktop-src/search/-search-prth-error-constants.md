---
description: 'Von Protokollhandlern zurückgegebene Fehlermeldungen:'
ms.assetid: b5e99ad1-1698-483c-8173-796af33085c4
title: Search Protocol Handler Error Messages (Searchapi.h) (Fehlermeldungen des Suchprotokollhandlers (Searchapi.h))
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4473e3e235641e5b4bb5d86313b4154cd00ec029fe96d42d8964dab51f33780f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969729"
---
# <a name="search-protocol-handler-error-messages"></a>Fehlermeldungen des Suchprotokollhandlers

Von Protokollhandlern zurückgegebene Fehlermeldungen:



| Konstante/Wert                                                                                                                                                                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRTH_E_ACCESS_DENIED"></span><span id="prth_e_access_denied"></span><dl> <dt>**PRTH \_ E \_ ACCESS \_ DENIED**</dt> <dt>0x80041205L</dt> </dl>             | Der Zugriff wurde verweigert. Wenn dies während einer inkrementellen Durchforstung auftritt, wird die Datei aus der URL-Warteschlange des Gatherers gelöscht.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_IS_READ_NONE"></span><span id="prth_e_acl_is_read_none"></span><dl> <dt>**PRTH \_ E \_ ACL \_ IS READ \_ \_ NONE**</dt> <dt>0x80041211L</dt> </dl>  | Das Element wird nicht indiziert. Die ACL ermöglicht es niemanden, das Element zu lesen.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_TOO_BIG"></span><span id="prth_e_acl_too_big"></span><dl> <dt>**PRTH \_ E \_ ACL \_ TOO \_ BIG**</dt> <dt>0x80041212L</dt> </dl>                  | Die ACL hat 64 KB überschritten. Die Suche indiziert das Element nicht.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_BAD_REQUEST"></span><span id="prth_e_bad_request"></span><dl> <dt>**PRTH \_ E \_ BAD \_ REQUEST**</dt> <dt>0x80041208L</dt> </dl>                   | Die Anforderung war aufgrund eines Fehlers in der URL ungültig.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_COMM_ERROR"></span><span id="prth_e_comm_error"></span><dl> <dt>**PRTH \_ E \_ \_ COMM-FEHLER**</dt> <dt>0x80041200L</dt> </dl>                      | Gibt einen Kommunikations- oder Serverfehler an. Wenn zu viele dieser Fehler für einen bestimmten Server vorhanden sind, markiert der Gatherer den Server als nicht verfügbar.<br/>                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_NOT_REDIRECTED"></span><span id="prth_e_not_redirected"></span><dl> <dt>**PRTH \_ E \_ NOT \_ REDIRECTED**</dt> <dt>0x80041207L</dt> </dl>          | Die umgeleitete URL ist nicht vorhanden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_E_OBJ_NOT_FOUND"></span><span id="prth_e_obj_not_found"></span><dl> <dt>**PRTH \_ E \_ OBJ \_ NOT \_ FOUND**</dt> <dt>0x80041201L</dt> </dl>            | Objekt konnte nicht gefunden werden. Gibt an, dass der Gatherer das Dokument aus der Warteschlange löschen soll, wenn es während einer inkrementellen Durchforstung nicht gefunden wird.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_REQUEST_ERROR"></span><span id="prth_e_request_error"></span><dl> <dt>**PRTH \_ E \_ REQUEST \_ ERROR**</dt> <dt>0x80041202L</dt> </dl>             | Verwendete Optionen werden nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="PRTH_E_SERVER_ERROR"></span><span id="prth_e_server_error"></span><dl> <dt>**PRTH \_ E \_ \_ SERVER-FEHLER**</dt> <dt>0x80041206L</dt> </dl>                | Kommunikations- oder Serverfehler. Wenn zu viele dieser Fehler für einen bestimmten Server vorhanden sind, markiert der Gatherer den Server als nicht verfügbar.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PRTH_S_NOT_ALL_PARTS"></span><span id="prth_s_not_all_parts"></span><dl> <dt>**PRTH \_ S \_ NOT \_ ALL \_ PARTS**</dt> <dt>0x8004121BL</dt> </dl>            | Auf Teile eines Elements kann nicht zugegriffen werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PRTH_S_NOT_MODIFIED"></span><span id="prth_s_not_modified"></span><dl> <dt>**PRTH \_ S \_ NICHT \_ GEÄNDERT**</dt> <dt>0x00041203L</dt> </dl>                | Der Elementinhalt wurde nicht geändert. Wenn dieser Fehler während einer inkrementellen Durchforstung auftritt, überspringt der Gatherer dieses Element, da das Element nicht geändert wurde.<br/>                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_S_TRY_IMPERSONATING"></span><span id="prth_s_try_impersonating"></span><dl> <dt>**PRTH \_ S \_ \_ VERSUCHEN, DIE IDENTITÄT VON**</dt> <dt>0x00041225L ZU IMITIEREN</dt> </dl> | Beim Identitätswechsel eines Benutzers sollte auf das Element zugegriffen werden. Vom Protokollhandler wird erwartet, dass er [**IUrlAccessor3::GetImpersonationSidBlobs**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs) implementiert, sodass der Suchprotokollhost eine Liste von SIDs abrufen kann, die für den Identitätswechsel verwendet werden sollen, und zur Verwendung von [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2)zurückwechseln kann. Dabei wird beim Öffnen des Elements die Identität eines der zulässigen Benutzer angenommen. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>                                            |
| Header<br/>                   | <dl> <dt>Searchapi.h</dt> </dl> |



 

 




