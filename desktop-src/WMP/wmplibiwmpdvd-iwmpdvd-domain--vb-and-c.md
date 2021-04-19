---
title: Iwmpdvd-Domänen Eigenschaft
description: Die Domänen Eigenschaft ruft die aktuelle Domäne der DVD ab.
ms.assetid: 0b7b39fe-2b04-44e2-aa5e-cab7be9a06b1
keywords:
- Domänen Eigenschaften Fenster Media Player
- Domänen Eigenschaft Windows Media Player, iwmpdvd-Schnittstelle
- Iwmpdvd-Schnittstelle, Windows Media Player, Domäne (Eigenschaft)
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
ms.openlocfilehash: 6546a8288160fe80f7df4a7c41ea79a0edc905f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367792"
---
# <a name="iwmpdvddomain-property"></a>Iwmpdvd::d omain-Eigenschaft

Die **Domänen** Eigenschaft ruft die aktuelle Domäne der DVD ab.

## <a name="syntax"></a>Syntax


```CSharp
public System.String domain {get; set;}
```


```VB

Public ReadOnly Property domain As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. String** -Wert, der einem der folgenden Werte entspricht.



| Wert                                                                                        | Bedeutung                                                                                                                                          |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>FirstPlay</dt> </dl>         | Die Standard Initialisierung einer DVD-CD wird durchgeführt.<br/>                                                                                      |
| <dl> <dt>videomanagermenu</dt> </dl>  | Anzeigen von Menüs für die gesamte Festplatte. Wird auch als "topmenu" für Windows-Media Player bezeichnet. Wird üblicherweise als Titelmenü oder im oberen Menü bezeichnet.<br/> |
| <dl> <dt>videotitlesetmenu</dt> </dl> | Anzeigen von Menüs für den aktuellen Titel Satz. Wird auch als titlemenu für Windows-Media Player bezeichnet. Wird üblicherweise als Stamm Menü bezeichnet.<br/>          |
| <dl> <dt>title</dt> </dl>             | Normalerweise zeigt den aktuellen Titel an.<br/>                                                                                                |
| <dl> <dt>stop</dt> </dl>              | Der DVD-Navigator befindet sich in der DVD-stoppdomäne.<br/>                                                                                          |
| <dl> <dt>definiert</dt> </dl>         | Windows Media Player befindet sich nicht in einer DVD-Domäne.<br/>                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Jede DVD wird unterschiedlich verfasst. Einige DVDs enthalten nicht die Domänen FirstPlay, videomanagermenu oder videotitlesetmenu.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpdvd-Schnittstelle (VB und c#)**](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





