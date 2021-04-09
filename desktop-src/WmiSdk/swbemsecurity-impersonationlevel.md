---
description: Die Eigenschaft "Identitätswechsel Ebene" ist eine ganze Zahl, die die Ebene des com-Identitäts Wechsels definiert, die diesem Objekt zugewiesen ist.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Swap Security. Identitäts ationlevel-Eigenschaft
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
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868743"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>Swap Security. Identitäts ationlevel-Eigenschaft

Die Eigenschaft "Identitätswechsel **Ebene** " ist eine ganze Zahl, die die Ebene des com-Identitäts Wechsels definiert, die diesem Objekt zugewiesen ist. Mit dieser Einstellung wird festgelegt, ob Prozesse im Besitz von Windows-Verwaltungsinstrumentation (WMI) Ihre Sicherheits Anmelde Informationen erkennen oder verwenden können, wenn Sie Aufrufe an andere Prozesse ausführen. Weitere Informationen zu Identitätswechsel Ebenen finden Sie unter [Festlegen der \_ \_ Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md).

Wenn Sie die Identitätswechsel Ebene nicht speziell in einem Moniker oder durch Festlegen der Eigenschaft " **Swap Security. Identitäts ationlevel** " für ein Sicherungs fähiges Objekt festlegen, wird die standardmäßige Identitätswechsel Ebene von WMI auf den Wert festgelegt, der im [Standard Registrierungsschlüssel](setting-the-default-process-security-level-using-vbscript.md)der Identitätswechsel Ebene angegeben ist. Wenn diese Einstellung nicht ausreicht, wird Ihre Anforderung vom Anbieter nicht unterstützt, und der WMI-API-Aufrufe kann mit dem Fehlercode **wbemErrAccessDenied** (2147749891/0x80041003) fehlschlagen.

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Als DCOM-Identitätswechsel Ebene kann diese Eigenschaft auf einen der folgenden Werte festgelegt werden:



| Wert           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anonym**   | Verbirgt die Anmeldeinformationen des Aufrufers. WMI unterstützt diese Identitätswechsel Ebene nicht. Wenn ein Skript "Identitätswechsel Ebene = anonym" angibt, führt WMI eine automatische Aktualisierung der Identitätswechsel Ebene durch, um zu identifizieren. Dies ist jedoch in gewisser Weise eine bedeutungslose Übung, da Skripts, die die identifizebene verwenden, wahrscheinlich fehlschlagen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Identifizieren**    | Ermöglicht es Objekten, die Anmelde Informationen des Aufrufers abzufragen. Skripts, die diese Identitätswechsel Ebene verwenden, schlagen wahrscheinlich fehl. in der Regel können Sie mit der Ebene "identifizieren" in der Regel keine Zugriffs Steuerungs Listen überprüfen. Skripts können nicht auf Remote Computern mit identifiziert werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | Ermöglicht es Objekten, die Anmelde Informationen des Aufrufers zu verwenden. Es wird empfohlen, diese Identitätswechsel Ebene mit WMI-Skripts zu verwenden. Wenn Sie dies tun, verwendet das WMI-Skript Ihre Benutzer Anmelde Informationen. Dadurch können alle Aufgaben ausgeführt werden, die Sie ausführen können.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Delegat**    | Ermöglicht es Objekten, anderen Objekten die Verwendung der Anmelde Informationen des Aufrufers zu gestatten. Die Delegierung ermöglicht es einem Skript, Ihre Anmelde Informationen auf einem Remote Computer zu verwenden, und ermöglicht diesem Remote Computer dann die Verwendung Ihrer Anmelde Informationen auf einem anderen Remote Computer. Obwohl Sie diese Identitätswechsel Ebene innerhalb von WMI-Skripts verwenden können, sollten Sie dies nur bei Bedarf tun, da Sie ein Sicherheitsrisiko darstellen könnte.<br/> Die Identitätswechsel Ebene des Delegaten kann nur verwendet werden, wenn alle Benutzerkonten und Computer Konten, die an der Transaktion beteiligt sind, als vertrauenswürdig für die Delegierung in Active Directory gekennzeichnet wurden. Dies trägt dazu bei, die Sicherheitsrisiken zu minimieren. Zwar können von einem Remote Computer Ihre Anmelde Informationen verwendet werden, dies ist jedoch nur möglich, wenn sowohl dieser als auch andere an der Transaktion beteiligte Computer für die Delegierung vertrauenswürdig sind.<br/> |



 

Wie bereits erwähnt, blendet der anonyme Identitätswechsel Ihre Anmelde Informationen aus und identifiziert das Remote Objekt, um Ihre Anmelde Informationen abzufragen, aber das Remote Objekt kann die Identität des Sicherheits Kontexts nicht annehmen. (Mit anderen Worten: Obwohl das Remote Objekt weiß, wer Sie sind, kann es nicht "vorgeben", Sie zu sein.) WMI-Skripts, die mit einer dieser beiden Einstellungen auf Remote Computer zugreifen, schlagen in der Regel fehl. Tatsächlich können die meisten Skripts, die auf dem lokalen Computer ausgeführt werden, mit einer dieser beiden Einstellungen auch fehlschlagen.

Durch den Identitätswechsel wird dem WMI-Remote Dienst ermöglicht, den angeforderten Vorgang mithilfe Ihres Sicherheits Kontexts auszuführen. Eine Remote-WMI-Anforderung, die die Einstellung Identität verwenden verwendet, ist in der Regel erfolgreich, sofern Ihre Anmelde Informationen über ausreichende Berechtigungen verfügen, um den beabsichtigten Vorgang auszuführen Anders ausgedrückt: Sie können WMI nicht zum Ausführen einer Aktion (Remote oder anderweitig) verwenden, für die Sie keine Berechtigung außerhalb von WMI haben.

Wenn Sie "Identitätswechsel Ebene" auf "delegieren" festlegen, kann der Remote-WMI-Dienst ihre Anmelde Informationen an andere Objekte übergeben und wird in der Regel als Sicherheitsrisiko eingestuft.

Sie können die Identitätswechsel Ebene des Objekts " [**Swap Services**](swbemservices.md)", " [**errbewbject**](swbemobject.md)", " [**errbewbjectset**](swbemobjectset.md)", " [**errbewbjectpath**](swbemobjectpath.md)" und " [**taubemlocator**](swbemlocator.md) " festlegen, indem Sie die Eigenschaft "Identitätswechsel **Ebene** " auf den gewünschten Wert festlegen. Im folgenden Beispiel wird gezeigt, wie Sie die Identitätswechsel Ebene für ein " **errbemubject** "-Objekt festlegen:


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



Sie können auch Identitätswechsel Ebenen als Teil eines Monikers angeben. Im folgenden Beispiel werden die Authentifizierungs Ebene und die Ebene des Identitäts Wechsels festgelegt, und eine Instanz des [**Win32- \_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/win32-service)wird abgerufen.


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
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Sicherheit<br/>                                                         |
| IID<br/>                      | IID \_ iswbemsecurity<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austausch Sicherheit**](swbemsecurity.md)
</dt> <dt>

[Festlegen der \_ Prozesssicherheit für Client Anwendungen \_](setting-client-application-process-security.md)
</dt> <dt>

[**Wbemimpersonationlevelenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

