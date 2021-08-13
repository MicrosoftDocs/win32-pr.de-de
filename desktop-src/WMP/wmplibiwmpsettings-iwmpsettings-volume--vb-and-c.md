---
title: IWMPSettings-Volumeeigenschaft
description: Die Volumeeigenschaft ruft das aktuelle Wiedergabevolumen ab oder legt es fest.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Volumeeigenschafts-Windows Media Player
- Volumeeigenschaft Windows Media Player , IWMPSettings-Schnittstelle
- IWMPSettings-Schnittstelle Windows Media Player , Volumeeigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings.volume
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2077547dd00b5c75b6ca77a966190db2bb3bb1bcde61d1f5c5b84c794af84e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568397"
---
# <a name="iwmpsettingsvolume-property"></a>IWMPSettings::volume-Eigenschaft

Die **Volumeeigenschaft** ruft das aktuelle Wiedergabevolumen ab oder legt es fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** bei dem es sich um die Volumeebene handelt, die zwischen 0 und 100 liegt.

## <a name="remarks"></a>Hinweise

Der Wert 0 gibt an, dass kein Volume (stummgeschaltet) ist. Der Wert 100 gibt das vollständige Volume an. Wenn für diese Eigenschaft kein Wert angegeben wird, wird standardmäßig die letzte Volumeeinstellung verwendet, die für die Windows Media Player.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





