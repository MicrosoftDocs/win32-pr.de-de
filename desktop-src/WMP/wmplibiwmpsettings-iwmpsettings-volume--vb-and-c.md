---
title: Iwmpsettings-volumenschaft
description: Mit der Volume-Eigenschaft wird das aktuelle Wiedergabe Volume abgerufen oder festgelegt.
ms.assetid: cff4fe70-9ca2-4419-bfc3-d622e8c72756
keywords:
- Volumeeigenschaft (Windows Media Player)
- Volumeeigenschaft Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows-Media Player, Volume-Eigenschaft
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
ms.openlocfilehash: b21e50c9d3c52b7ce117d6c2ab681e592571c0f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370007"
---
# <a name="iwmpsettingsvolume-property"></a>Iwmpsettings:: Volume-Eigenschaft

Mit der **Volume** -Eigenschaft wird das aktuelle Wiedergabe Volume abgerufen oder festgelegt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 volume {get; set;}
```


```VB

Public Property volume As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Volumeebene zwischen 0 und 100 ist.

## <a name="remarks"></a>Bemerkungen

Der Wert 0 (null) gibt kein Volume (stumm) an. Der Wert 100 gibt das vollständige Volume an. Wenn für diese Eigenschaft kein Wert angegeben wird, wird standardmäßig die letzte für Windows Media Player festgelegte volumeeinstellung verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





