---
description: Die AuthenticationLevel-Eigenschaft ist eine ganze Zahl, die die COM-Authentifizierungsebene definiert, die diesem Objekt zugewiesen ist.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: SWbemSecurity.AuthenticationLevel-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbb765241fabb86a14a5d74f7a839d5d81b017856b6da349b9ec04fd8535a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312714"
---
# <a name="swbemsecurityauthenticationlevel-property"></a>SWbemSecurity.AuthenticationLevel-Eigenschaft

Die **AuthenticationLevel-Eigenschaft** ist eine ganze Zahl, die die COM-Authentifizierungsebene definiert, die diesem Objekt zugewiesen ist. Diese Einstellung bestimmt, wie Sie von WMI gesendete Informationen schützen. Weitere Informationen zu Authentifizierungsebenen finden Sie unter [Setting Client Application Process \_ \_ Security](setting-client-application-process-security.md). Im Allgemeinen ist es nicht erforderlich, die Authentifizierungsebene festzulegen, wenn WMI-API-Aufrufe vorgenommen werden. Wenn Sie diese Eigenschaft nicht festlegen, wird die STANDARDMÄßIGE COM-Authentifizierungsebene für Ihr System verwendet.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Mit der Einstellung authenticationLevel können Sie die Ebene der DCOM-Authentifizierung und des Datenschutzes anfordern, die während einer Verbindung verwendet werden soll. Einstellungen reichen von keiner Authentifizierung bis hin zur paketbasierten verschlüsselten Authentifizierung.



| Wert        | Beschreibung                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine         | Verwendet keine Authentifizierung. Alle Sicherheitseinstellungen werden ignoriert.<br/>                                                                                                                                                                                                                                         |
| Standard      | Verwendet eine Standardsicherheitsaushandlung, um eine Authentifizierungsebene auszuwählen. Dies ist die empfohlene Einstellung, da der an der Transaktion beteiligte Client auf die vom Server angegebene Authentifizierungsebene ausgehandelt wird.<br/> DCOM wählt während einer Aushandlungssitzung nicht den Wert None aus.<br/> |
| Verbinden      | Authentifiziert die Anmeldeinformationen des Clients nur, wenn der Client versucht, eine Verbindung mit dem Server herzustellen. Nachdem eine Verbindung hergestellt wurde, werden keine weiteren Authentifizierungsüberprüfungen durchgeführt.<br/>                                                                                                                          |
| Aufruf         | Authentifiziert die Anmeldeinformationen des Clients nur zu Beginn jedes Aufrufs, wenn der Server die Anforderung empfängt. Die Paketheader werden signiert, aber die zwischen dem Client und dem Server ausgetauschten Datenpakete sind weder signiert noch verschlüsselt.<br/>                                                     |
| Pkt          | Authentifiziert, dass alle Datenpakete vom erwarteten Client empfangen werden. Ähnlich wie aufrufe; Paketheader werden signiert, aber nicht verschlüsselt. Pakete selbst sind weder signiert noch verschlüsselt.<br/>                                                                                                               |
| PktIntegrity | Authentifiziert und überprüft, ob keines der zwischen dem Client und dem Server übertragenen Datenpakete geändert wurde. Jedes Datenpaket wird signiert, um sicherzustellen, dass die Pakete während der Übertragung nicht geändert wurden. Keines der Datenpakete wird verschlüsselt.<br/>                                            |
| PktPrivacy   | Authentifiziert alle vorherigen Identitätswechselebenen und signiert und verschlüsselt jedes Datenpaket. Dadurch wird sichergestellt, dass die gesamte Kommunikation zwischen dem Client und dem Server vertraulich ist.<br/>                                                                                                                             |



 

Sie können die Authentifizierungsebene der [**Objekte SWbemServices,**](swbemservices.md) [**SWbemObject,**](swbemobject.md) [**SWbemObjectSet,**](swbemobjectset.md) [**SWbemObjectPath**](swbemobjectpath.md)und [**SwbemLocator**](swbemlocator.md) festlegen, indem Sie die **AuthenticationLevel-Eigenschaft** auf den gewünschten Wert festlegen.

Das folgende Beispiel zeigt, wie die Authentifizierungsebene für ein **SwbemObject-Objekt** festgelegt wird.


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



Sie können Authentifizierungsebenen auch als Teil eines Monikers angeben. Im folgenden Beispiel werden die Authentifizierungsebene und die Identitätswechselebene festgelegt und eine Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)abgerufen.


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Festlegen der \_ \_ Clientanwendungsprozesssicherheit](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> </dl>

 

