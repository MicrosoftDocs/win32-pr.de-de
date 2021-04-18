---
description: Tritt auf, wenn ein Benutzer auf das InkEdit-Steuerelement klickt.
ms.assetid: 99fd7ef0-02cf-4390-9026-00ef2bbc1e37
title: InkEdit. Click-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55df62807ee78e0f083a301c83a756b4cffb729d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350855"
---
# <a name="inkeditclick-event"></a>InkEdit. Click-Ereignis

Tritt auf, wenn ein Benutzer auf das [InkEdit](inkedit-control-reference.md) -Steuerelement klickt.

## <a name="syntax"></a>Syntax


```C++
void Click();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie auf ein Steuerelement klicken, werden zusätzlich zum Click-Ereignis [**mousdown**](inkedit-mousedown.md) -und [**mousup**](inkedit-mouseup.md) -Ereignisse generiert.

> [!Note]  
> Verwenden Sie das [**MouseDown**](inkedit-mousedown.md) -und das [**MouseUp**](inkedit-mouseup.md) -Ereignis, um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden.

 

Wenn im **Click** -Ereignis Code vorhanden ist, wird das [**DblClick**](inkedit-dblclick.md) -Ereignis nie auslöst, da das **Click** -Ereignis das erste Ereignis ist, das zwischen beiden angezeigt wird. Folglich wird der Maus Klick von dem **Click** -Ereignis abgefangen, sodass das **DblClick** -Ereignis nicht auftritt.

Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert. Die **\_ iinkeditevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ ieeclick**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>In "-. h" (auch als "gezeichneten \_ i. c" erforderlich)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkEd.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[InkEdit](inkedit-control-reference.md)
</dt> </dl>

 

 




