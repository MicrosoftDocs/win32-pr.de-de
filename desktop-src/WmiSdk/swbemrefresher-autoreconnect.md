---
description: Die AutoReconnect-Eigenschaft des SWbemRefresher-Objekts ist ein boolescher Wert, der angibt, ob die Aktualisierung automatisch wieder eine Verbindung mit einem Remoteanbieter herstellen soll, wenn die Verbindung unterbrochen wird.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: SWbemRefresher.AutoReconnect-Eigenschaft (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b1ad11c4362276d5714e54ef3196b246a40de1e26bf8f311f41fb5b5834bab0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312812"
---
# <a name="swbemrefresherautoreconnect-property"></a>SWbemRefresher.AutoReconnect-Eigenschaft

Die **AutoReconnect-Eigenschaft** des [**SWbemRefresher-Objekts**](swbemrefresher.md) ist ein boolescher Wert, der angibt, ob die Aktualisierung automatisch wieder eine Verbindung mit einem Remoteanbieter herstellen soll, wenn die Verbindung unterbrochen wird.

Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Das Ändern dieser Eigenschaft wirkt sich nur auf Objekte in der Aktualisierung aus, die von einem Hochleistungsanbieter unterstützt werden. Wenn der Anbieter kein Hochleistungsanbieter ist, hat das Festlegen der **AutoReconnect-Eigenschaft** auf **TRUE** keine Auswirkungen, da das [**SWbemRefresher-Objekt**](swbemrefresher.md) nie wieder eine Verbindung herstellen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Typbibliothek<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




