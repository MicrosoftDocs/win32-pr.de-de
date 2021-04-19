---
title: AxWindowsMediaPlayer. Status (Eigenschaft)
description: Die Status-Eigenschaft ruft einen Wert ab, der den Status von Windows Media Player angibt.
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- Status Eigenschaften Fenster Media Player
- Status-Eigenschaft, Windows Media Player, AxWindowsMediaPlayer-Klasse
- AxWindowsMediaPlayer-Klasse, Windows Media Player, Status-Eigenschaft
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea7e8c36ad05e2f9a4573d8e2433d705f354239
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372062"
---
# <a name="axwindowsmediaplayerstatus-property"></a>AxWindowsMediaPlayer. Status (Eigenschaft)

Die Status-Eigenschaft ruft einen Wert ab, der den Status von Windows Media Player angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Die System. String-Wert, der den Status hat.

## <a name="remarks"></a>Bemerkungen

Die in dieser Eigenschaft enthaltenen Werte können jederzeit geändert werden und sollten nur zu Anzeige Zwecken verwendet werden.

Der AxWindowsMediaPlayer. Das **statusChange** -Ereignis wird ausgelöst, wenn der Wert dieser Eigenschaft geändert wird.

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

[**AxWindowsMediaPlayer. statusChange-Ereignis (VB und c#)**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





