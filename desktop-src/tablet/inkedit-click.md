---
description: Tritt ein, wenn ein Benutzer auf das InkEdit-Steuerelement klickt.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: InkEdit.Click-Ereignis (Inked.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f126035319c5d225da3fe57e075044c50f91f928277de89fce8e516e4723c701
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718138"
---
# <a name="inkeditclick-event"></a>InkEdit.Click-Ereignis

Tritt ein, wenn ein Benutzer auf das [InkEdit-Steuerelement](inkedit-control-reference.md) klickt.

## <a name="syntax"></a>Syntax


```C++
void Click();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn Sie auf ein Steuerelement klicken, werden zusätzlich zum Click-Ereignis [**MouseDown-**](inkedit-mousedown.md) und [**MouseUp-Ereignisse**](inkedit-mouseup.md) generiert.

> [!Note]  
> Verwenden Sie die [**MouseDown-**](inkedit-mousedown.md) und MouseUp-Ereignisse, um zwischen den linken, rechten und mittleren [**Maustasten zu**](inkedit-mouseup.md) unterscheiden.

 

Wenn das Click-Ereignis Code enthält, wird das [**DblClick-Ereignis**](inkedit-dblclick.md) nie ausgelöst, da das  **Click-Ereignis** das erste Ereignis ist, das zwischen den beiden ausgelöst wird. Daher wird der Mausklick vom **Click-Ereignis** abgefangen, sodass das **DblClick-Ereignis** nicht auftritt.

Diese Ereignismethode wird in der **\_ IInkEditEvents-Schnittstelle** definiert. Die **\_ IInkEditEvents-Schnittstelle** implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ IeeClick.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Inked.h (erfordert auch inked \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Inkedit](inkedit-control-reference.md)
</dt> </dl>

 

 




