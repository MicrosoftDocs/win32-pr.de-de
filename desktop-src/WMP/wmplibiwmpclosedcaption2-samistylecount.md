---
title: IWMPClosedCaption2 samistylecount (Eigenschaft)
description: Die samistylecount-Eigenschaft ruft die Anzahl der Stile ab, die von der aktuellen Sami-Datei unterstützt werden.
ms.assetid: e2a0d194-6fa2-48c9-9fc7-0b60029d2e5d
keywords:
- Samistylecount-Eigenschaften Fenster Media Player
- Samistylecount-Eigenschaft, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface, Windows Media Player, samistylecount (Eigenschaft)
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
ms.openlocfilehash: ff361b4c6d34f63e86e3d8458bff4d3308cae29f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372460"
---
# <a name="iwmpclosedcaption2samistylecount-property"></a>IWMPClosedCaption2:: samistylecount (Eigenschaft)

Die **samistylecount** -Eigenschaft ruft die Anzahl der Stile ab, die von der aktuellen Sami-Datei unterstützt werden.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 SAMIStyleCount {get; set;}
```


```VB

Public ReadOnly Property SAMIStyleCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Anzahl der Stile ist.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt 0 (null) zurück, es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer. openstate ist gleich 13).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Untertiteln zu digitalen Medien**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Iwmpclosedcaption-Schnittstelle (VB und c#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Iwmpclosedcaption. samistyle (VB und c#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und c#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2. getsamistylename (VB und c#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md)
</dt> </dl>

 

 





