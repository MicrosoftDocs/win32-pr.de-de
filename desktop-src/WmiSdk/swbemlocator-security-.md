---
description: Die Security- \_ Eigenschaft des Objekts "Swap-Locator" wird verwendet, um die Sicherheitseinstellungen für ein "Swap"-Objekt zu lesen oder festzulegen. Diese Eigenschaft ist ein Swap Security-Objekt.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: SWbemLocator.Security_-Eigenschaft (wbemdisp. h)
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
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755025"
---
# <a name="swbemlocatorsecurity_-property"></a>"Swap-Locator. Security"- \_ Eigenschaft

Die **Security \_** -Eigenschaft des Objekts " [**Swap-Locator**](swbemlocator.md) " wird verwendet, um die Sicherheitseinstellungen für ein " **Swap** "-Objekt zu lesen oder festzulegen. Diese Eigenschaft ist ein [**Swap Security**](swbemsecurity.md) -Objekt.

> [!Note]  
> Das Festlegen **der \_ Security** -Eigenschaft eines " [**Swap**](swbemlocator.md) "-Objekts auf **null** gewährt allen Personen jederzeit uneingeschränkten Zugriff. Weitere Informationen finden Sie unter [**Swap Security**](swbemsecurity.md).

 

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Die Eigenschaften eines " **taubemlocator. Security \_** "-Objekts haben keine Standardwerte. Wenn Sie versuchen, den Wert von " [**Swap Security. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) " oder " [**taubemsecurity. Identitäts ationlevel**](swbemsecurity-impersonationlevel.md) " für ein " [**taubemlocator**](swbemlocator.md) "-Objekt zu erhalten, bevor Sie es festgelegt haben, wird ein [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) -Fehler ausgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch<br/>                                                          |
| IID<br/>                      | IID \_ iswbemlocator<br/>                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Ausführen privilegierter Vorgänge mit VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Festlegen der \_ Prozesssicherheit für Client Anwendungen \_](setting-client-application-process-security.md)
</dt> <dt>

[**Swap Security-Objekt**](swbemsecurity.md)
</dt> <dt>

[Sichern einer Remote-WMI-Verbindung](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




