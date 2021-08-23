---
description: Die ImpersonationLevel-Eigenschaft ist eine ganze Zahl, die die COM-Identitätswechselebene definiert, die diesem Objekt zugewiesen ist.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: SWbemSecurity.ImpersonationLevel (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cde6bca09198d6e05f1ae0143ee07d1aedd465df68258303f1d6ca2b4b7699f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639580"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>SWbemSecurity.ImpersonationLevel (Eigenschaft)

Die **ImpersonationLevel-Eigenschaft** ist eine ganze Zahl, die die COM-Identitätswechselebene definiert, die diesem Objekt zugewiesen ist. Diese Einstellung bestimmt, ob Prozesse, die sich im Besitz der Windows Management Instrumentation (WMI) befinden, Ihre Sicherheitsanmeldeinformationen erkennen oder verwenden können, wenn Sie Aufrufe an andere Prozesse tätigen. Weitere Informationen zu Identitätswechselebenen finden Sie unter [Setting Client Application Process \_ \_ Security](setting-client-application-process-security.md).

Wenn Sie die Identitätswechselebene nicht speziell in einem Moniker oder durch Festlegen der **SWBemSecurity.ImpersonationLevel-Eigenschaft** für ein sicherungsfähiges Objekt festlegen, legt WMI die Standard-Identitätswechselebene auf den Wert fest, der im Standardregistrierungsschlüssel der Identitätswechselebene angegeben [ist.](setting-the-default-process-security-level-using-vbscript.md) Wenn diese Einstellung nicht ausreicht, stellt der Anbieter Ihre Anforderung nicht bereit, und der Aufruf der WMI-API kann mit dem Fehlercode **wbemErrAccessDenied** (2147749891/0x80041003) fehlschlagen.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Als DCOM-Identitätswechselebene kann diese Eigenschaft auf einen der folgenden Werte festgelegt werden:



| Wert           | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anonym**   | Verbirgt die Anmeldeinformationen des Aufrufers. WMI unterstützt diese Identitätswechselebene nicht. Wenn ein Skript impersonationLevel=Anonymous angibt, aktualisiert WMI automatisch die Identitätswechselebene auf Identify. Dies ist jedoch in irgendeiner Weise eine bedeutungslose Übung, da Skripts, die die Identify-Ebene verwenden, wahrscheinlich fehlschlagen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Identifizieren**    | Ermöglicht Objekten das Abfragen der Anmeldeinformationen des Aufrufers. Skripts, die diese Identitätswechselebene verwenden, können wahrscheinlich fehlschlagen. Mit der Ebene Identifizieren können Sie in der Regel nur Zugriffssteuerungslisten überprüfen. Sie können keine Skripts für Remotecomputer mithilfe von Identifizieren ausführen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | Ermöglicht Objekten die Verwendung der Anmeldeinformationen des Aufrufers. Es wird empfohlen, diese Identitätswechselebene mit WMI-Skripts zu verwenden. Wenn Sie dies tun, verwendet das WMI-Skript Ihre Benutzeranmeldeinformationen. Dadurch kann er alle Aufgaben ausführen, die Sie ausführen können.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Delegat**    | Ermöglicht Es -Objekten, anderen Objekten die Verwendung der Anmeldeinformationen des Aufrufers zu erlauben. Die Delegierung ermöglicht es einem Skript, Ihre Anmeldeinformationen auf einem Remotecomputer zu verwenden, und ermöglicht es diesem Remotecomputer dann, Ihre Anmeldeinformationen auf einem anderen Remotecomputer zu verwenden. Obwohl Sie diese Identitätswechselebene in WMI-Skripts verwenden können, sollten Sie dies nur bei Bedarf tun, da dies ein Sicherheitsrisiko darstellen kann.<br/> Sie können die Identitätswechselebene "Delegieren" nur verwenden, wenn alle Benutzerkonten und Computerkonten, die an der Transaktion beteiligt sind, als Vertrauenswürdig für delegierung in Active Directory markiert wurden. Dies trägt zur Minimierung der Sicherheitsrisiken bei. Obwohl ein Remotecomputer Ihre Anmeldeinformationen verwenden kann, ist dies nur dann der Fall, wenn sowohl er als auch alle anderen computer, die an der Transaktion beteiligt sind, für die Delegierung vertrauenswürdig sind.<br/> |



 

Wie bereits erwähnt, blendet der anonyme Identitätswechsel Ihre Anmeldeinformationen aus, und Identifizieren ermöglicht es einem Remoteobjekt, Ihre Anmeldeinformationen abfragt, aber das Remoteobjekt kann die Identität Ihres Sicherheitskontexts nicht imitieren. (Anders ausgedrückt: Obwohl das Remoteobjekt weiß, wer Sie sind, kann es sich nicht "vorgeben", Sie zu sein.) WMI-Skripts, die über eine dieser beiden Einstellungen auf Remotecomputer zugreifen, führen im Allgemeinen zu einem Fehler. Tatsächlich können die meisten Skripts, die mit einer dieser beiden Einstellungen auf dem lokalen Computer ausgeführt werden, ebenfalls fehlschlagen.

Der Identitätswechsel ermöglicht es dem WMI-Remotedienst, Ihren Sicherheitskontext zum Ausführen des angeforderten Vorgangs zu verwenden. Eine WMI-Remoteanforderung, die die Einstellung Identitätswechsel verwendet, ist in der Regel erfolgreich, vorausgesetzt, Ihre Anmeldeinformationen verfügen über ausreichende Berechtigungen, um den beabsichtigten Vorgang durchzuführen. Anders ausgedrückt: Sie können WMI nicht verwenden, um eine Aktion (remote oder anderweitig) durchzuführen, für die Sie außerhalb von WMI nicht berechtigt sind.

Wenn Sie impersonationLevel auf Delegate festlegen, kann der WMI-Remotedienst Ihre Anmeldeinformationen an andere Objekte übergeben und wird im Allgemeinen als Sicherheitsrisiko angesehen.

Sie können die Identitätswechselebene eines [**SWbemServices-,**](swbemservices.md) [**SWbemObject-,**](swbemobject.md) [**SWbemObjectSet-,**](swbemobjectset.md) [**SWbemObjectPath-**](swbemobjectpath.md)und [**SwbemLocator-Objekts**](swbemlocator.md) festlegen, indem Sie die **ImpersonationLevel-Eigenschaft** auf den gewünschten Wert festlegen. Das folgende Beispiel zeigt, wie Sie die Identitätswechselebene für ein **SWbemObject-Objekt** festlegen:


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



Sie können Identitätswechselebenen auch als Teil eines Monikers angeben. Im folgenden Beispiel werden die Authentifizierungsebene und die Identitätswechselebene und eine Instanz des [**Win32-Diensts \_ abgerufen.**](/windows/desktop/CIMWin32Prov/win32-service)


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Festlegen der Sicherheit \_ des \_ Clientanwendungsprozesses](setting-client-application-process-security.md)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

