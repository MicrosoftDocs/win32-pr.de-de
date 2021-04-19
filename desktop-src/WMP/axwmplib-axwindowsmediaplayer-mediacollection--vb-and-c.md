---
title: AxWindowsMediaPlayer. mediacollection (Eigenschaft)
description: Die mediacollection-Eigenschaft ruft eine iwmpmediacollection-Schnittstelle ab, die eine Möglichkeit bietet, eine große Sammlung von Medien Elementen zu organisieren.
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- mediacollection-Eigenschaft, Windows-Media Player
- mediacollection-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, mediacollection (Eigenschaft)
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
ms.openlocfilehash: f6501dd5dda8e60b8ba1a5f2667f6b581cbdfd90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359746"
---
# <a name="axwindowsmediaplayermediacollection-property"></a>AxWindowsMediaPlayer. mediacollection (Eigenschaft)

Die mediacollection-Eigenschaft ruft eine **iwmpmediacollection** -Schnittstelle ab, die eine Möglichkeit bietet, eine große Sammlung von Medien Elementen zu organisieren.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a>Eigenschaftswert

Die WMPLib. iwmpmediacollection-Schnittstelle zu einer Auflistung von Medien Elementen.

## <a name="remarks"></a>Bemerkungen

Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**AxWindowsMediaPlayer-Objekt (VB und c#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Iwmpmediacollection-Schnittstelle (VB und c#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





