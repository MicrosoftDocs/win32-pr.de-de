---
description: Die Security-Eigenschaft des Objekts "errbewbjectpath" wird verwendet, um die Sicherheitskomponenten eines Objekt Pfads zu erhalten oder festzulegen.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: SWbemObjectPath.Security_-Eigenschaft (wbemdisp. h)
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
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215317"
---
# <a name="swbemobjectpathsecurity_-property"></a>Errbemubjectpath. Security- \_ Eigenschaft

Die **Security** -Eigenschaft des Objekts " [**errbewbjectpath**](swbemobjectpath.md) " wird verwendet, um die Sicherheitskomponenten eines Objekt Pfads zu erhalten oder festzulegen. Beachten Sie, dass es nicht verwendet wird, um Sicherheits Attribute des Objekts " **errbemubjectpath** " selbst festzulegen. Sie wird nur verwendet, um die Sicherheitskomponenten des Pfads für ein Objekt vom Typ " [**Swap**](swbemlocator.md) " darzustellen. Diese Eigenschaft ist ein [**Swap Security**](swbemsecurity.md) -Objekt.

> [!Note]  
> Durch das Festlegen der [**\_ Sicherheits**](swbemobject-security-.md) Eigenschaft eines " [**errbemubjectpath**](swbemobjectset.md) "-Objekts auf **null** wird allen Benutzern jederzeit uneingeschränkter Zugriff gewährt. Weitere Informationen finden Sie unter [**Swap Security**](swbemsecurity.md).

 

Weitere Informationen finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).

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
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID- \_ Swap-Austausch Pfad<br/>                                                       |
| IID<br/>                      | IID \_ iswbemubjectpath<br/>                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Errbemubjectpath**](swbemobjectpath.md)
</dt> <dt>

[Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Festlegen der \_ Prozesssicherheit für Client Anwendungen \_](setting-client-application-process-security.md)
</dt> </dl>

 

 




