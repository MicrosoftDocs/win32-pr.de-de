---
description: Tritt auf, wenn der InkStrokes-Auflistung mindestens ein IInkStrokeDisp-Objekt hinzugefügt wird.
ms.assetid: 577ad52b-ecd3-4a49-8997-481ebdb47203
title: InkPicture.StrokesAdded-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5f9418289ac996b2c2248c2cf1696e7d45b4548dbafa4dff9494e76cbedc30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717403"
---
# <a name="inkpicturestrokesadded-event"></a>InkPicture.StrokesAdded-Ereignis

Tritt auf, wenn der [InkStrokes-Auflistung mindestens ein IInkStrokeDisp-Objekt hinzugefügt](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) wird. [](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)

## <a name="syntax"></a>Syntax


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StrokeIds* \[ In\]
</dt> <dd>

Das ganzzahlige Array von Bezeichnern für jedes [**IInkStrokeDisp-Objekt,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) das hinzugefügt wird, wenn dieses Ereignis eintritt.

Weitere Informationen zur VARIANT-Struktur finden Sie unter [Verwenden der COM-Bibliothek](using-the-com-library.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkStrokesEvents-Schnittstelle** definiert. Die **\_ IInkStrokesEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ SEStrokesAdded.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

