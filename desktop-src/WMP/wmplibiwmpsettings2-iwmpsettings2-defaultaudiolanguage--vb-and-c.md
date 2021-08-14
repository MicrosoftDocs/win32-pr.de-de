---
title: IWMPSettings2 defaultAudioLanguage (Eigenschaft)
description: Die defaultAudioLanguage-Eigenschaft ruft den Locale Identifier (LCID) der Standardaudiosprache ab, die in der Windows Media Player.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- defaultAudioLanguage-Windows Media Player
- defaultAudioLanguage-Eigenschaft Windows Media Player , IWMPSettings2-Schnittstelle
- IWMPSettings2-Schnittstelle Windows Media Player , defaultAudioLanguage-Eigenschaft
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
ms.openlocfilehash: 4f09df11cc53e9b813de2e40e40eca1e31a88afeff0c16ce1f9c0c5ba4745277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331100"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a>IWMPSettings2::d efaultAudioLanguage (Eigenschaft)

Die **defaultAudioLanguage-Eigenschaft** ruft den Locale Identifier (LCID) der Standardaudiosprache ab, die in Windows Media Player.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System.Int32,** das die LCID ist.

## <a name="remarks"></a>Hinweise

Eine LCID identifiziert eindeutig einen bestimmten Sprachdialekt, der als "Locale" bezeichnet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPControls3.currentAudioLanguage (VB und C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[**IWMPSettings-Schnittstelle (VB und C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2-Schnittstelle (VB und C#)**](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





