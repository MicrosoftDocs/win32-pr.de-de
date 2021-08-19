---
title: IVMDVDDriveEvents OnMediaEject-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausjiziert wurden. | IVMDVDDriveEvents OnMediaEject-Methode (VPCCOMInterfaces.h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- 'OnMediaEject-Methode : Virtueller PC'
- OnMediaEject-Methode Virtual PC, IVMDVDDriveEvents-Schnittstelle
- IVMDVDDriveEvents-Schnittstelle Virtueller PC, OnMediaEject-Methode
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2fbf9ffe589597e1baab7c0b503cf94384cfa540749cfe49e083286f743370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117753751"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a>IVMDVDDriveEvents::OnMediaEject-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt eine Benachrichtigung, dass Medien vom Laufwerk ausjiziert wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mediaPath* \[ In\]
</dt> <dd>

Der Buchstabe oder Pfad des Hostlaufwerks zum ISO-Image.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird aufgerufen, wenn Medien (ein ISO-Image oder ein Datenträger auf einem Hostlaufwerk) ausjiziert werden. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das Ereignis vmDVDDriveEvent OnEject zu erhalten, das von \_ [**IVMDVDDrive stammt.**](ivmdvddrive.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents ist als c2a7d8e9-e76c-4eb8-94f7-71a5122d249b definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

