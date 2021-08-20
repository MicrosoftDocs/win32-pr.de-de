---
title: IWMPClosedCaption2-SAMIStyleCount-Eigenschaft
description: Die SAMIStyleCount-Eigenschaft ruft die Anzahl der Stile ab, die von der aktuellen SAMI-Datei unterstützt werden.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- SAMIStyleCount-Eigenschaft Windows Media Player
- SAMIStyleCount-Eigenschaft Windows Media Player , IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2-Schnittstelle Windows Media Player , SAMIStyleCount-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMIStyleCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f73ab4e252386f790f74741053012239d0219b1e296e392146894f906e1556f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115917"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a>IWMPClosedCaption2::SAMIStyleCount-Eigenschaft

Die **SAMIStyleCount-Eigenschaft** ruft die Anzahl der Stile ab, die von der aktuellen SAMI-Datei unterstützt werden.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.Int32-Datei,** die der Anzahl von Formatvorlagen entspricht.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt 0 zurück, es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer.openState ist gleich 13).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**IWMPClosedCaption-Schnittstelle (VB und C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption.SAMIStyle (VB und C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2.getSAMIStyleName (VB und C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





