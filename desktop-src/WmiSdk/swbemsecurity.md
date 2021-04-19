---
description: Das Swap Security-Objekt ruft Sicherheitseinstellungen ab oder legt diese fest, z. b. Berechtigungen, com-Identitätswechsel und Authentifizierungs Stufen, die einem Objekt zugewiesen sind.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Swap Security-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359985"
---
# <a name="swbemsecurity-object"></a>Swap Security-Objekt

Das **Swap Security** -Objekt ruft Sicherheitseinstellungen ab oder legt diese fest, z. b. Berechtigungen, com-Identitätswechsel und Authentifizierungs Stufen, die einem Objekt zugewiesen sind. Die Objekte " [**errbemlocator**](swbemlocator.md)", " [**Swap Services**](swbemservices.md)", " [**errbeapbject**](swbemobject.md)", " [**errbeapbjectset**](swbemobjectset.md)", " [**errbeapbjectpath**](swbemobjectpath.md)", " [**errbemlasterror**](swbemlasterror.md)" und " [**errbemeventsource**](swbemeventsource.md) " verfügen über eine **Sicherheits \_** Eigenschaft, die das Objekt " **Swap Security** " ist Wenn Sie eine Instanz von abrufen oder das WMI-Sicherheitsprotokoll anzeigen, müssen Sie möglicherweise die Eigenschaften des **Sicherheits \_** Objekts festlegen.

Der VBScript-Befehl zum Erstellen von [Objekten](/previous-versions//xzysf6hc(v=vs.85)) kann das Sicherheits Objekt nicht erstellen. Die Sicherheitseinstellungen in diesem Objekt identifizieren nicht die Authentifizierungs-, Identitäts-oder Berechtigungseinstellungen für eine Verbindung mit WMI oder die Sicherheit, die für den Proxy wirksam ist, wenn ein Objekt in einem asynchronen-Befehl an eine Senke übermittelt wird. Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

## <a name="members"></a>Member

Das **taubemsecurity** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Swap Security** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                    | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)<br/> | Lesen/Schreiben<br/> | Numerischer Wert, der die com-Authentifizierungs Ebene definiert, die diesem-Objekt zugewiesen ist. Mit dieser Einstellung wird bestimmt, wie die von WMI gesendeten Informationen geschützt werden.<br/>                                                                 |
| [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)<br/>   | Lesen/Schreiben<br/> | Numerischer Wert, der die Ebene des com-Identitäts Wechsels definiert, die diesem-Objekt zugewiesen ist. Mit dieser Einstellung wird festgelegt, ob von WMI gehörende Prozesse ihre Sicherheits Anmelde Informationen erkennen oder verwenden können, wenn Sie Aufrufe an andere Prozesse ausführen.<br/> |
| [**Rechte**](swbemsecurity-privileges.md)<br/>                   | Schreibgeschützt<br/>  | Ein " [**taubemprivilegeset**](swbemprivilegeset.md) "-Objekt, das Berechtigungen für dieses Objekt definiert. Weitere Informationen finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).<br/>                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Sicherheit<br/>                                                         |
| IID<br/>                      | IID \_ iswbemsecurity<br/>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[API-Skript Objekte](scripting-api-objects.md)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> <dt>

[Festlegen der \_ Prozesssicherheit für Client Anwendungen \_](setting-client-application-process-security.md)
</dt> <dt>

[**Wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**Wbemimpersonationlevelenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**Wbemprivilegeumum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

