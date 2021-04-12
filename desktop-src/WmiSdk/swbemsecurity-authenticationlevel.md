---
description: Die AuthenticationLevel-Eigenschaft ist eine ganze Zahl, die die com-Authentifizierungs Ebene definiert, die diesem Objekt zugewiesen ist.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: Taubemsecurity. AuthenticationLevel-Eigenschaft
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
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344709"
---
# <a name="swbemsecurityauthenticationlevel-property"></a>Taubemsecurity. AuthenticationLevel-Eigenschaft

Die **AuthenticationLevel** -Eigenschaft ist eine ganze Zahl, die die com-Authentifizierungs Ebene definiert, die diesem Objekt zugewiesen ist. Mit dieser Einstellung wird bestimmt, wie die von WMI gesendeten Informationen geschützt werden. Weitere Informationen zu Authentifizierungs Ebenen finden Sie unter [Festlegen der \_ \_ Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md). Im Allgemeinen ist es nicht notwendig, die Authentifizierungs Ebene beim Ausführen von WMI-API-aufrufen festzulegen. Wenn Sie diese Eigenschaft nicht festlegen, wird die Standard-com-Authentifizierungs Ebene für das System verwendet.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Mithilfe der AuthenticationLevel-Einstellung können Sie die Ebene der DCOM-Authentifizierung und des Datenschutzes anfordern, die während der gesamten Verbindung verwendet werden soll. Die Einstellungen reichen von der Authentifizierung über die verschlüsselte Authentifizierung per Paket.



| Wert        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Keine         | Verwendet keine Authentifizierung. Alle Sicherheitseinstellungen werden ignoriert.<br/>                                                                                                                                                                                                                                         |
| Standard      | Verwendet eine Standard-Sicherheitsaus Handlung, um eine Authentifizierungs Ebene auszuwählen. Dies ist die empfohlene Einstellung, da der an der Transaktion beteiligte Client mit der vom Server angegebenen Authentifizierungs Ebene ausgehandelt wird.<br/> Der Wert None während einer Aushandlungs Sitzung wird von DCOM nicht ausgewählt.<br/> |
| Verbinden      | Authentifiziert die Anmelde Informationen des Clients nur, wenn der Client versucht, eine Verbindung mit dem Server herzustellen. Nachdem eine Verbindung hergestellt wurde, werden keine weiteren Authentifizierungsprüfungen durchgeführt.<br/>                                                                                                                          |
| Aufruf         | Authentifiziert die Anmelde Informationen des Clients nur zu Beginn jedes Aufrufes, wenn der Server die Anforderung empfängt. Die Paket Header sind signiert, aber die zwischen Client und Server ausgetauschten Datenpakete sind weder signiert noch verschlüsselt.<br/>                                                     |
| Pkt          | Authentifiziert, dass alle Datenpakete vom erwarteten Client empfangen werden. Vergleichbar mit "Call;" Paket Header sind signiert, aber nicht verschlüsselt. Pakete selbst sind weder signiert noch verschlüsselt.<br/>                                                                                                               |
| PktIntegrity | Authentifiziert und überprüft, ob keines der Datenpakete, die zwischen dem Client und dem Server übertragen wurden, geändert wurde. Jedes Datenpaket wird signiert und stellt sicher, dass die Pakete während der Übertragung nicht geändert wurden. Keines der Datenpakete ist verschlüsselt.<br/>                                            |
| PKTPRIVACY   | Authentifiziert alle vorherigen Identitätswechsel Ebenen und signiert und verschlüsselt jedes Datenpaket. Dadurch wird sichergestellt, dass die gesamte Kommunikation zwischen dem Client und dem Server vertraulich ist.<br/>                                                                                                                             |



 

Sie können die Authentifizierungs Ebene der Objekte " [**Swap Services**](swbemservices.md)", " [**errbewbject**](swbemobject.md)", " [**errbewbjectset**](swbemobjectset.md)", " [**errbewbjectpath**](swbemobjectpath.md)" und " [**taubemlocator**](swbemlocator.md) " festlegen, indem Sie die Eigenschaft " **AuthenticationLevel** " auf den gewünschten Wert festlegen.

Im folgenden Beispiel wird gezeigt, wie Sie die Authentifizierungs Ebene für ein " **errbemubject** "-Objekt festlegen.


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



Sie können auch Authentifizierungs Ebenen als Teil eines Monikers angeben. Im folgenden Beispiel werden die Authentifizierungs Ebene und die Identitätswechsel Ebene festgelegt, und es wird eine Instanz von [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)abgerufen.


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Sicherheit<br/>                                                         |
| IID<br/>                      | IID \_ iswbemsecurity<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Festlegen der \_ Prozesssicherheit für Client Anwendungen \_](setting-client-application-process-security.md)
</dt> <dt>

[**Wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**Austausch Sicherheit**](swbemsecurity.md)
</dt> </dl>

 

