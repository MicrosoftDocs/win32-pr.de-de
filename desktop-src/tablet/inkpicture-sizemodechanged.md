---
description: Tritt ein, nachdem die SizeMode-Eigenschaft des InkPicture-Steuerelements geändert wurde.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: InkPicture.SizeModeChanged-Ereignis (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebcd5a659894c6f70a87ea75f7a99321d94dba2826fd538530f7e6d060d5730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032028"
---
# <a name="inkpicturesizemodechanged-event"></a>InkPicture.SizeModeChanged-Ereignis

Tritt ein, nachdem die [**SizeMode-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) des [InkPicture-Steuerelements](inkpicture-control-reference.md) geändert wurde.

## <a name="syntax"></a>Syntax


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewMode* \[ In\]
</dt> <dd>

Der neue Zustand des [InkPicture-Steuerelements](inkpicture-control-reference.md) basierend auf dem neuen Wert der [**SizeMode-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)

</dd> <dt>

*OldMode* \[ In\]
</dt> <dd>

Der alte Zustand des [InkPicture-Steuerelements](inkpicture-control-reference.md) basierend auf dem alten Wert der [**SizeMode-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Ereignismethode wird in der **\_ IInkPictureEvents-Schnittstelle** definiert. Die **\_ IInkPictureEvents-Schnittstelle** implementiert die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) mit dem Bezeichner DISPID \_ IPESizeModeChanged.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Inkpicture](inkpicture-control-reference.md)
</dt> </dl>

 

