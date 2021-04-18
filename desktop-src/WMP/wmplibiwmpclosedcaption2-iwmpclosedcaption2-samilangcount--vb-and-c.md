---
title: IWMPClosedCaption2 samilangcount (Eigenschaft)
description: Die samilangcount-Eigenschaft ruft die Anzahl der Sprachen ab, die von der aktuellen Sami-Datei unterstützt werden.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Samilangcount-Eigenschaften Fenster Media Player
- Samilangcount-Eigenschaft, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface Windows Media Player, samilangcount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354773"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a>IWMPClosedCaption2:: samilangcount (Eigenschaft)

Die **samilangcount** -Eigenschaft ruft die Anzahl der Sprachen ab, die von der aktuellen Sami-Datei unterstützt werden.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die Anzahl der unterstützten Sprachen ist.

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

[**Iwmpclosedcaption. samilang (VB und c#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und c#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2. getsamilangname (VB und c#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





