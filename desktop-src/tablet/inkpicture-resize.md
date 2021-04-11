---
description: Tritt auf, wenn die Größe des InkPicture-Steuer Elements geändert wird (wenn sich die Eigenschaftswerte für Breite und/oder Höhe ändern).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: InkPicture. Resize-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042720"
---
# <a name="inkpictureresize-event"></a>InkPicture. Resize-Ereignis

Tritt auf, wenn die Größe des [InkPicture](inkpicture-control-reference.md) -Steuer Elements geändert wird (wenn sich die Eigenschaftswerte für Breite und/oder Höhe ändern).

## <a name="syntax"></a>Syntax


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Left* 
</dt> <dd>

Die Anzahl der Pixel von der linken Seite des Fensters, das das Steuerelement auf der linken Seite des-Steuer Elements enthält.

</dd> <dt>

*Top* 
</dt> <dd>

Die Anzahl der Pixel vom oberen Rand des Fensters, das das Steuerelement am oberen Rand des-Steuer Elements enthält.

</dd> <dt>

*Right* 
</dt> <dd>

Die Anzahl der Pixel von der linken Seite des Fensters, das das Steuerelement auf der rechten Seite des-Steuer Elements enthält.

</dd> <dt>

*bottom* 
</dt> <dd>

Die Anzahl der Pixel vom oberen Rand des Fensters, das das Steuerelement am unteren Rand des Steuer Elements enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die neue Breite des Steuer Elements in Pixel entspricht der Differenz zwischen dem *rechten* und dem *linken* Parameter. Ebenso ist die neue Höhe gleich der Differenz zwischen *unten* und *oben*.

Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert. Die **\_ iinkpictureevents** -Schnittstelle implementiert die IDispatch-Schnittstelle mit dem Bezeichner " **DISPID \_ iperesize**".

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

 

 




