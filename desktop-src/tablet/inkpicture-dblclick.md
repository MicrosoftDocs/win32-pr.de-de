---
description: Tritt ein, wenn auf das InkPicture-Steuerelement doppelklickt wird.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: InkPicture.DblClick-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 515d16d16fb585771a8e2e06e642476b6be7a29851b750add4d6de2ca1a89bda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717329"
---
# <a name="inkpicturedblclick-event"></a>InkPicture.DblClick-Ereignis

Tritt ein, wenn auf das [InkPicture-Steuerelement](inkpicture-control-reference.md) doppelklickt wird.

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

Gibt an, ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden, verwenden Sie die [**MouseDown-**](inkpicture-mousedown.md) und [**MouseUp-Ereignisse.**](inkpicture-mouseup.md) Wenn das [**Click-Ereignis**](inkpicture-click.md) Code enthält, wird das **DblClick-Ereignis** nie ausgelöst.

 

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ IPEDblClick.**

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

 

 




