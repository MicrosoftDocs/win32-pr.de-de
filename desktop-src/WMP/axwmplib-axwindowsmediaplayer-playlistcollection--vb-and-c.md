---
title: AxWindowsMediaPlayer. playlistcollection (Eigenschaft)
description: Die playlistcollection-Eigenschaft ruft eine iwmpplaylistcollection-Schnittstelle ab.
ms.assetid: f3c65f70-b58f-41c1-afe0-3a9d9c95561c
keywords:
- playlistcollection-Eigenschaft, Windows-Media Player
- playlistcollection-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, playlistcollection (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.playlistCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a01ca41d194a6321e02d34280241cd5701597e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365638"
---
# <a name="axwindowsmediaplayerplaylistcollection-property"></a>AxWindowsMediaPlayer. playlistcollection (Eigenschaft)

Die playlistcollection-Eigenschaft ruft eine **iwmpplaylistcollection** -Schnittstelle ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPPlaylistCollection playlistCollection {get;}
```


```VB

Public ReadOnly Property playlistCollection As IWMPPlaylistCollection
```





## <a name="property-value"></a>Eigenschaftswert

WMPLib. **Iwmpplaylistcollection** -Schnittstelle.

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

[**Iwmpplaylistcollection-Schnittstelle (VB und c#)**](iwmpplaylistcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





