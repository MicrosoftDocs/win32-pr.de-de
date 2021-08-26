---
title: IWMPClosedCaption2 SAMILangCount (Eigenschaft)
description: Die SAMILangCount-Eigenschaft ruft die Anzahl der Sprachen ab, die von der aktuellen SAMI-Datei unterstützt werden.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- SAMILangCount-Windows Media Player
- SAMILangCount-Eigenschaft Windows Media Player , IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2-Schnittstelle Windows Media Player , SAMILangCount-Eigenschaft
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
ms.openlocfilehash: 23b85ce04bd672f0219b8dd96f91172241689a80042a37a7680e2f8e26b65c85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900000"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a>IWMPClosedCaption2::SAMILangCount (Eigenschaft)

Die **SAMILangCount-Eigenschaft** ruft die Anzahl der Sprachen ab, die von der aktuellen SAMI-Datei unterstützt werden.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** bei dem es sich um die Anzahl der unterstützten Sprachen handelt.

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

[**IWMPClosedCaption.SAMILang (VB und C#)**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2-Schnittstelle (VB und C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2.getSAMILangName (VB und C#)**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





