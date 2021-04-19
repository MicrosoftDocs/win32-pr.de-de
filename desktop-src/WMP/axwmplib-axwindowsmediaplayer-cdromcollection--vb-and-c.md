---
title: AxWindowsMediaPlayer. cdromcollection (Eigenschaft)
description: Die cdromcollection-Eigenschaft ruft eine iwmpcdromcollection-Schnittstelle ab, die den Zugriff auf eine Sammlung von CD-oder DVD-Laufwerken ermöglicht.
ms.assetid: 03f4e7d1-4376-4112-993e-943d29aca049
keywords:
- cdromcollection-Eigenschaft, Windows-Media Player
- cdromcollection-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, cdromcollection (Eigenschaft)
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.cdromCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4ba3bb5df95e9ee53e2a6c3aecbd1e9a355882
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367410"
---
# <a name="axwindowsmediaplayercdromcollection-property"></a>AxWindowsMediaPlayer. cdromcollection (Eigenschaft)

Die cdromcollection-Eigenschaft ruft eine **iwmpcdromcollection** -Schnittstelle ab, die den Zugriff auf eine Sammlung von CD-oder DVD-Laufwerken ermöglicht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public IWMPCdromCollection cdromCollection {get;}
```


```VB

Public ReadOnly Property cdromCollection As IWMPCdromCollection
```





## <a name="property-value"></a>Eigenschaftswert

Eine WMPLib. iwmpcdromcollection-Schnittstelle.

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

[**Iwmpcdromcollection-Schnittstelle (VB und c#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





