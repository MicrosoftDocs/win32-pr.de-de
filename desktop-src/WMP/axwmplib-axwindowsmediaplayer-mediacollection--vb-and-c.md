---
title: AxWindowsMediaPlayer.mediaCollection -Eigenschaft
description: Die mediaCollection-Eigenschaft ruft eine IWMPMediaCollection-Schnittstelle ab, die eine Möglichkeit bietet, eine große Sammlung von Medienelementen zu organisieren.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- mediaCollection-Windows Media Player
- mediaCollection-Eigenschaft Windows Media Player , AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse Windows Media Player , mediaCollection-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ad0cc720c49926ddbd75fe71d47738a9e8af43fa97670a0b9915a50716ed0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902630"
---
# <a name="axwindowsmediaplayermediacollection-property"></a>AxWindowsMediaPlayer.mediaCollection -Eigenschaft

Die mediaCollection-Eigenschaft ruft eine **IWMPMediaCollection-Schnittstelle** ab, die eine Möglichkeit bietet, eine große Sammlung von Medienelementen zu organisieren.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a>Eigenschaftswert

Die WMPLib.IWMPMediaCollection-Schnittstelle für eine Sammlung von Medienelementen.

## <a name="remarks"></a>Hinweise

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection-Schnittstelle (VB und C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





