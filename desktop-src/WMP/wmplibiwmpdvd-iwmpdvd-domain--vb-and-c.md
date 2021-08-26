---
title: IWMPDVD-Domäneneigenschaft
description: Die Domäneneigenschaft ruft die aktuelle Domäne der DVD ab.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Domain Property Windows Media Player
- Domäneneigenschaft Windows Media Player , IWMPDVD-Schnittstelle
- IWMPDVD-Schnittstelle Windows Media Player , Domäneneigenschaft
topic_type:
- apiref
api_name:
- IWMPDVD.domain
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b5f382d7c1db820905b45b924105225c0c5b55a569f85707e4e9f729e59596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000470"
---
# <a name="iwmpdvddomain-property"></a>IWMPDVD::d omain-Eigenschaft

Die **Domäneneigenschaft** ruft die aktuelle Domäne der DVD ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.String,die** einer der folgenden Werte ist.



| Wert                                                                                        | Bedeutung                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>firstPlay</dt> </dl>         | Ausführen der Standardinitialisierung eines DVD-Datenträgers.<br/>                                                                                      |
| <dl> <dt>videoManagerMenu</dt> </dl>  | Anzeigen von Menüs für den gesamten Datenträger. Wird auch als topMenu für Windows Media Player bezeichnet. Wird häufig als Titelmenü oder oberes Menü bezeichnet.<br/> |
| <dl> <dt>videoTitleSetMenu</dt> </dl> | Anzeigen von Menüs für den aktuellen Titelsatz. Wird auch als titleMenu für Windows Media Player bezeichnet. Wird häufig als Stammmenü bezeichnet.<br/>          |
| <dl> <dt>title</dt> </dl>             | In der Regel wird der aktuelle Titel angezeigt.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | Der DVD-Navigator befindet sich in der Domäne DVD-Beenden.<br/>                                                                                          |
| <dl> <dt>Undefined</dt> </dl>         | Windows Media Player befindet sich nicht in einer DVD-Domäne.<br/>                                                                                        |



 

## <a name="remarks"></a>Hinweise

Jede DVD wird anders erstellt. Einige DVDs enthalten nicht die Domänen firstPlay, videoManagerMenu oder videoTitleSetMenu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPDVD-Schnittstelle (VB und C#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





