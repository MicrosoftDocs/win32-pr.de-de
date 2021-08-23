---
description: Die Security-Eigenschaft des SWbemObjectPath-Objekts wird verwendet, um die Sicherheitskomponenten eines Objektpfads zu erhalten oder zu festlegen.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: SWbemObjectPath.Security_ -Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ed473049de6973da077b1ccfabdd3fe752ff4e5edd13f4a49a7c5589309ae81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639970"
---
# <a name="swbemobjectpathsecurity_-property"></a>SWbemObjectPath.Security \_ (Eigenschaft)

Die **Security-Eigenschaft** des [**SWbemObjectPath-Objekts**](swbemobjectpath.md) wird verwendet, um die Sicherheitskomponenten eines Objektpfads zu erhalten oder zu festlegen. Beachten Sie, dass es nicht zum Festlegen von Sicherheitsattributen des **SWbemObjectPath-Objekts** selbst verwendet wird. Es wird nur verwendet, um die Sicherheitskomponenten des Pfads für ein [**SWbemLocator-Objekt**](swbemlocator.md) zu darstellen. Diese Eigenschaft ist ein [**SWbemSecurity-Objekt.**](swbemsecurity.md)

> [!Note]  
> Durch festlegen [**der \_ Security-Eigenschaft**](swbemobject-security-.md) eines [**SWbemObjectPath-Objekts**](swbemobjectset.md) auf **NULL** wird jedem jederzeit unbegrenzter Zugriff gewährt. Weitere Informationen finden Sie unter [**SWbemSecurity**](swbemsecurity.md).

 

Weitere Informationen finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Security_ As Object
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
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> <dt>

[Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Festlegen der Sicherheit \_ des \_ Clientanwendungsprozesses](setting-client-application-process-security.md)
</dt> </dl>

 

 




