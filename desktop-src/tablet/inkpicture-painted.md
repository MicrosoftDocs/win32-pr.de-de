---
description: Tritt auf, wenn das InkPicture-Steuerelement das erneute zeichnen selbst abgeschlossen hat.
ms.assetid: a8194cff-ed94-402e-8564-08d370f958b4
title: InkPicture. gezeichnet-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60188ef87d88ba7412a07300e708718bedc947fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348687"
---
# <a name="inkpicturepainted-event"></a>InkPicture. gezeichnet-Ereignis

Tritt auf, wenn das [InkPicture](inkpicture-control-reference.md) -Steuerelement das erneute zeichnen selbst abgeschlossen hat.

## <a name="syntax"></a>Syntax


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdc* \[ in\]
</dt> <dd>

Der Gerätekontext, in dem das Ereignis aufgetreten ist.

</dd> <dt>

*Rect* \[ in\]
</dt> <dd>

Das [**inkrechteck**](inkrectangle-class.md) , das neu gezeichnet wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in den **\_ iinkoverlayevents** -und **\_ iinkpictureevents** -DISP mit der ID DISPID \_ ioegezeichnet definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkPicture](inkpicture-control-reference.md)
</dt> </dl>

 

 




