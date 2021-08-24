---
title: IVMFloppyDriveEvents OnMediaEject-Methode (VPCCOMInterfaces.h)
description: Empfängt die Benachrichtigung, dass Medien vom Laufwerk ausgesendet wurden. | IVMFloppyDriveEvents OnMediaEject-Methode (VPCCOMInterfaces.h)
ms.assetid: 3e9c0b5d-8fec-4f34-93d2-c5975403798b
keywords:
- OnMediaEject-Methode Virtueller PC
- OnMediaEject-Methode Virtual PC , IVMFloppyDriveEvents-Schnittstelle
- IVMFloppyDriveEvents-Schnittstelle Virtueller PC, OnMediaEject-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e624dcbf028caf58a2f50109789e5f89cd34d1d70c4679333b8b742c3b071ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653600"
---
# <a name="ivmfloppydriveeventsonmediaeject-method"></a>IVMFloppyDriveEvents::OnMediaEject-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt die Benachrichtigung, dass Medien vom Laufwerk ausgesendet wurden.

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

Der Laufwerkbuchstabe des Hosts oder der Pfad zum Diskettenimage.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode wird aufgerufen, wenn Medien (ein Diskettenimage oder ein Diskettendatenträger auf einem Hostlaufwerk) eingefügt werden. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um Benachrichtigungen über das onMediaEject-Ereignis vmFloppyDriveEvent zu erhalten, das \_ von [**IVMFloppyDrive**](ivmfloppydrive.md)stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents ist als a9ed3401-4e09-4177-86ec-a13bf9fa7d4e definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

