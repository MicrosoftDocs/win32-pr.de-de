---
description: Tritt auf, nachdem die SizeMode-Eigenschaft des InkPicture-Steuer Elements geändert wurde.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: InkPicture. SizeModeChanged-Ereignis (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348658"
---
# <a name="inkpicturesizemodechanged-event"></a>InkPicture. SizeModeChanged-Ereignis

Tritt auf, nachdem die [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) -Eigenschaft des [InkPicture](inkpicture-control-reference.md) -Steuer Elements geändert wurde.

## <a name="syntax"></a>Syntax


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NEWMODE* \[ in\]
</dt> <dd>

Der neue Zustand des [InkPicture](inkpicture-control-reference.md) -Steuer Elements, basierend auf dem neuen Wert der [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) -Eigenschaft.

</dd> <dt>

*Oldmode* \[ in\]
</dt> <dd>

Der alte Zustand des [InkPicture](inkpicture-control-reference.md) -Steuer Elements, basierend auf dem alten Wert der [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) -Eigenschaft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Ereignismethode wird in der **\_ iinkpictureevents** -Schnittstelle definiert. Die **\_ iinkpictureevents** -Schnittstelle implementiert die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle mit dem Bezeichner "DISPID \_ iPeer SizeModeChanged".

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

 

