---
title: AxWindowsMediaPlayer.stretchToFit-Eigenschaft
description: Die stretchToFit-Eigenschaft ruft einen Wert ab, der angibt, ob das vom Windows Media Player-Steuerelement angezeigte Video automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Videobilds ist, oder legt diesen fest.
ms.assetid: 02e2bcba-4975-4ddd-996b-9bd40774ebc1
keywords:
- stretchToFit-Eigenschaft Windows Media Player
- stretchToFit-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , stretchToFit-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.stretchToFit
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3090889207e0631fbc2f35613398b4c979f4c907cfe240e9f0a7374c74b00b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581510"
---
# <a name="axwindowsmediaplayerstretchtofit-property"></a>AxWindowsMediaPlayer.stretchToFit-Eigenschaft

Die stretchToFit-Eigenschaft ruft einen Wert ab, der angibt, ob das vom Windows Media Player-Steuerelement angezeigte Video automatisch an das Videofenster angepasst wird, wenn das Videofenster größer als die Abmessungen des Videobilds ist, oder legt diesen fest.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean stretchToFit {get; set;}
```


```VB

Public Property stretchToFit As System.Boolean
```





## <a name="property-value"></a>Eigenschaftswert

Der System.Boolean-Wert, der angibt, ob das Video gestreckt wird, um an das Fenster anzupassen. Der Standardwert ist „FALSE“.

## <a name="remarks"></a>Hinweise

Wenn **stretchToFit** auf TRUE festgelegt ist, behält das Windows Media Player-Steuerelement das ursprüngliche Seitenverhältnis des Videos bei. Wenn das Seitenverhältnis des Videos nicht mit dem Seitenverhältnis des Videofensters übereinstimmt, können schwarze Maskierungsbereiche entweder oben und unten oder links und rechts des Videobilds angezeigt werden.

Diese Eigenschaft gilt nur für das Windows Media Player Steuerelement, wenn es in eine Webseite eingebettet ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





