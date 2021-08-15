---
description: Die \_ Security-Eigenschaft des SWbemObject-Objekts wird verwendet, um die Sicherheitseinstellungen für ein SWbemObject-Objekt zu lesen oder festzulegen.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: SWbemObject.Security_-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d83a155057e445848e727615978c3414e96f63334ffc70c78d5f055a396b53f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313784"
---
# <a name="swbemobjectsecurity_-property"></a>SWbemObject.Security-Eigenschaft \_

Die **\_ Security-Eigenschaft** des [**SWbemObject-Objekts**](swbemobject.md) wird verwendet, um die Sicherheitseinstellungen für ein **SWbemObject-Objekt** zu lesen oder festzulegen. Diese Eigenschaft ist ein [**SWbemSecurity-Objekt.**](swbemsecurity.md) Die Sicherheitseinstellungen in diesem Objekt geben weder die Authentifizierungs-, Identitätswechsel- oder Berechtigungseinstellungen an, die für eine Verbindung mit Windows Management Instrumentation (WMI) vorgenommen wurden, noch die sicherheit, die für den Proxy gilt, wenn ein Objekt in einem asynchronen Aufruf an eine Senke übermittelt wird. Weitere Informationen finden Sie unter [Verwalten der WMI-Sicherheit.](maintaining-wmi-security.md)

> [!Note]  
> Wenn Sie die **Security-Eigenschaft \_** eines [**SWbemObject-Objekts**](swbemobject.md) auf **NULL** festlegen, wird jedem jederzeit unbegrenzter Zugriff gewährt. Weitere Informationen finden Sie unter [**SWbemSecurity**](swbemsecurity.md).

 

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[Erstellen einer WMI-Anwendung oder eines WMI-Skripts](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Festlegen der \_ \_ Clientanwendungsprozesssicherheit](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Berechtigungskonstanten**](privilege-constants.md)
</dt> </dl>

 

 




