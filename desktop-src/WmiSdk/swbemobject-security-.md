---
description: Die Security- \_ Eigenschaft des-Objekts mit dem-Objekt wird zum Lesen oder Festlegen der Sicherheitseinstellungen für ein-Objekt vom typaustausch verwendet.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: SWbemObject.Security_-Eigenschaft (wbemdisp. h)
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
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349219"
---
# <a name="swbemobjectsecurity_-property"></a>Errbemubject. Security ( \_ Eigenschaft)

Die **Security \_** -Eigenschaft des [**-Objekts mit**](swbemobject.md) dem-Objekt wird zum Lesen oder Festlegen der Sicherheitseinstellungen für ein-Objekt vom **typaustausch** verwendet. Diese Eigenschaft ist ein [**Swap Security**](swbemsecurity.md) -Objekt. Die Sicherheitseinstellungen in diesem Objekt geben nicht die Authentifizierung, den Identitätswechsel oder die Berechtigungseinstellungen an, die für eine Verbindung mit Windows-Verwaltungsinstrumentation (WMI) vorgenommen wurden, oder die für den Proxy geltenden Sicherheit, wenn ein Objekt in einem asynchronen-Befehl an eine Senke übermittelt wird. Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).

> [!Note]  
> Das Festlegen **der \_ Security** -Eigenschaft eines " [**errbemubject**](swbemobject.md) "-Objekts auf **null** gewährt allen Benutzern uneingeschränkten Zugriff. Weitere Informationen finden Sie unter [**Swap Security**](swbemsecurity.md).

 

Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Austausch Objekt<br/>                                                           |
| IID<br/>                      | IID \_ iswbemujekt<br/>                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Austausch Objekt**](swbemobject.md)
</dt> <dt>

[Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Festlegen der \_ Prozesssicherheit für Client Anwendungen \_](setting-client-application-process-security.md)
</dt> <dt>

[**Austausch Sicherheit**](swbemsecurity.md)
</dt> <dt>

[**Wbemauthenticationlevelerum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**Wbemimpersonationlevelenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**Wbemprivilegeumum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Berechtigungs Konstanten**](privilege-constants.md)
</dt> </dl>

 

 




