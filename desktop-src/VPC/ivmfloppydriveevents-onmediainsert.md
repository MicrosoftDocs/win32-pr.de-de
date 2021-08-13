---
title: IVMFloppyDriveEvents OnMediaInsert-Methode (VPCCOMInterfaces.h)
description: Empfängt die Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden. | IVMFloppyDriveEvents OnMediaInsert-Methode (VPCCOMInterfaces.h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- OnMediaInsert-Methode Virtueller PC
- OnMediaInsert-Methode Virtueller PC, IVMFloppyDriveEvents-Schnittstelle
- IVMFloppyDriveEvents-Schnittstelle Virtueller PC , OnMediaInsert-Methode
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30eb00222304168b30f6512b51f9d381fc4fbd61e7c5d254e0d53c3eb931a819
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594779"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a>IVMFloppyDriveEvents::OnMediaInsert-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt die Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnMediaInsert(
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

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn Medien (ein Diskettenimage oder eine Diskette auf einem Hostlaufwerk) eingefügt werden. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das onMediaInsert-Ereignis vmFloppyDriveEvent zu erhalten, \_ das von [**IVMFloppyDrive**](ivmfloppydrive.md)stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMFloppyDriveEvents ist als a9ed3401-4e09-4177-86ec-a13bf9fa7d4e definiert.<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)
</dt> </dl>

 

