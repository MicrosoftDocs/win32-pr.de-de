---
description: Tritt ein, wenn ein Benutzer auf das InkPicture-Steuerelement klickt.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: InkPicture.Click-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08ebde47609a36a92eca211f597345a9784fca03f66076ebb4db6f04ee6f5936
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218539"
---
# <a name="inkpictureclick-event"></a>InkPicture.Click-Ereignis

Tritt ein, wenn ein Benutzer auf das [InkPicture-Steuerelement](inkpicture-control-reference.md) klickt.

## <a name="syntax"></a>Syntax


```C++
void Click();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn Sie auf ein Steuerelement klicken, werden zusätzlich zum Click-Ereignis [**MouseDown-**](inkpicture-mousedown.md) und [**MouseUp-Ereignisse**](inkpicture-mouseup.md) generiert.

> [!Note]  
> Um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden, verwenden Sie die [**MouseDown-**](inkpicture-mousedown.md) und [**MouseUp-Ereignisse.**](inkpicture-mouseup.md)

 

Wenn das **Click-Ereignis** Code enthält, wird das [**DblClick-Ereignis**](inkpicture-dblclick.md) nie ausgelöst, da das **Click-Ereignis** das erste Ereignis ist, das zwischen den beiden ausgelöst wird. Daher wird der Mausklick vom **Click-Ereignis** abgefangen, sodass das **DblClick-Ereignis** nicht auftritt.

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ IPEClick.**

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

 

 




