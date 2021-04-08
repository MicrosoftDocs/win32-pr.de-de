---
description: Tritt auf, wenn ein Benutzer auf das InkPicture-Steuerelement klickt.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: InkPicture. Click-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867728"
---
# <a name="inkpictureclick-event"></a>InkPicture. Click-Ereignis

Tritt auf, wenn ein Benutzer auf das [InkPicture](inkpicture-control-reference.md) -Steuerelement klickt.

## <a name="syntax"></a>Syntax


```C++
void Click();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie auf ein Steuerelement klicken, werden zusätzlich zum Click-Ereignis [**mousdown**](inkpicture-mousedown.md) -und [**mousup**](inkpicture-mouseup.md) -Ereignisse generiert.

> [!Note]  
> Verwenden Sie das [**MouseDown**](inkpicture-mousedown.md) -und das [**MouseUp**](inkpicture-mouseup.md) -Ereignis, um zwischen den linken, rechten und mittleren Maustasten zu unterscheiden.

 

Wenn im **Click** -Ereignis Code vorhanden ist, wird das [**DblClick**](inkpicture-dblclick.md) -Ereignis nie auslöst, da das **Click** -Ereignis das erste Ereignis ist, das zwischen beiden angezeigt wird. Folglich wird der Maus Klick von dem **Click** -Ereignis abgefangen, sodass das **DblClick** -Ereignis nicht auftritt.

Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert. Die **\_ iinkpictureevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner **DISPID \_ ipeclick**.

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

 

 




