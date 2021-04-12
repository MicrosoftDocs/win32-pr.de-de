---
description: Tritt auf, wenn auf das InkPicture-Steuerelement Doppel geklickt wird.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: InkPicture. DblClick-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347888"
---
# <a name="inkpicturedblclick-event"></a>InkPicture. DblClick-Ereignis

Tritt auf, wenn auf das [InkPicture](inkpicture-control-reference.md) -Steuerelement Doppel geklickt wird.

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

Ob das Ereignis für das übergeordnete Steuerelement abgebrochen werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Verwenden Sie das [**MouseDown**](inkpicture-mousedown.md) -und das [**MouseUp**](inkpicture-mouseup.md) -Ereignis, um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden. Wenn im [**Click**](inkpicture-click.md) -Ereignis Code vorhanden ist, wird das **DblClick** -Ereignis nie auslöst.

 

Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert. Die **\_ iinkpictureevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ ipedblclick**.

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

 

 




