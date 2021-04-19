---
title: IWMPSettings2 defaultaudiolanguage (Eigenschaft)
description: Die defaultaudiolanguage-Eigenschaft ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) der in Windows Media Player angegebenen Standard Audiosprache ab.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- defaultaudiolanguage-Eigenschaft, Windows Media Player
- defaultaudiolanguage-Eigenschaft, Windows Media Player, IWMPSettings2-Schnittstelle
- IWMPSettings2 Interface Windows Media Player, defaultaudiolanguage-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356451"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>IWMPSettings2::d efaultaudiolanguage-Eigenschaft

Die **defaultaudiolanguage** -Eigenschaft ruft den Gebiets Schema Bezeichner (Locale Identifier, LCID) der in Windows Media Player angegebenen Standard Audiosprache ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. Int32** -Wert, der die LCID ist.

## <a name="remarks"></a>Bemerkungen

Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPControls3. currentaudiolanguage (VB und c#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**Iwmpsettings-Schnittstelle (VB und c#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2-Schnittstelle (VB und c#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





