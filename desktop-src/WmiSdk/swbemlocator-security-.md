---
description: Die Security-Eigenschaft des SWbemLocator-Objekts wird zum Lesen oder Festlegen der Sicherheitseinstellungen für ein \_ SWbemLocator-Objekt verwendet. Diese Eigenschaft ist ein SWbemSecurity-Objekt.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: SWbemLocator.Security_ -Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6c5fa2ba102de1135c0019e2dcfb291f55672cabb00cea1c59d8a655f21c882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955170"
---
# <a name="swbemlocatorsecurity_-property"></a>SWbemLocator.Security \_ (Eigenschaft)

Die **\_ Security-Eigenschaft** des [**SWbemLocator-Objekts**](swbemlocator.md) wird zum Lesen oder Festlegen der Sicherheitseinstellungen für ein **SWbemLocator-Objekt** verwendet. Diese Eigenschaft ist ein [**SWbemSecurity-Objekt.**](swbemsecurity.md)

> [!Note]  
> Durch Festlegen **der \_ Security-Eigenschaft** eines [**SWbemLocator-Objekts**](swbemlocator.md) auf **NULL** wird jedem jederzeit unbegrenzter Zugriff gewährt. Weitere Informationen finden Sie unter [**SWbemSecurity**](swbemsecurity.md).

 

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Die Eigenschaften eines **SWbemLocator.Security-Objekts \_** haben keine Standardwerte. Wenn Sie versuchen, den Wert [**von SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) oder [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) für ein [**SWbemLocator-Objekt**](swbemlocator.md) zu erhalten, bevor Sie es festgelegt haben, wird ein [wbemErrFailed-Fehler](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) ausgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Festlegen der Sicherheit \_ des \_ Clientanwendungsprozesses](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity-Objekt**](swbemsecurity.md)
</dt> <dt>

[Sichern einer WMI-Remoteverbindung](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




