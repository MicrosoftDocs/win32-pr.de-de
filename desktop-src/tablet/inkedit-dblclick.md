---
description: Tritt auf, wenn auf das InkEdit-Steuerelement Doppel geklickt wird.
ms.assetid: 380499e4-8697-4823-8153-29f24b2f234c
title: InkEdit. DblClick-Ereignis (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fee0ec42171c9abbe0c99691f881b99db512869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369828"
---
# <a name="inkeditdblclick-event"></a>InkEdit. DblClick-Ereignis

Tritt auf, wenn auf das [InkEdit](inkedit-control-reference.md) -Steuerelement Doppel geklickt wird.

## <a name="syntax"></a>Syntax


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Abbrechen* \[ in, out\]
</dt> <dd>

**Variant \_ TRUE** , um das Ereignis für das übergeordnete Steuerelement abzubrechen. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Verwenden Sie das [**MouseDown**](inkedit-mousedown.md) -und das [**MouseUp**](inkedit-mouseup.md) -Ereignis, um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden. Wenn im [**Click**](inkedit-click.md) -Ereignis Code vorhanden ist, wird das **DblClick** -Ereignis nie auslöst.

 

Diese Ereignismethode wird in der **\_ iinkeditevents** -Schnittstelle definiert. Die **\_ iinkeditevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ ieedblclick**.

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

 

 




