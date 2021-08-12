---
title: IVMDVDDriveEvents OnMediaInsert-Methode (VPCCOMInterfaces.h)
description: Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden. | IVMDVDDriveEvents OnMediaInsert-Methode (VPCCOMInterfaces.h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- 'OnMediaInsert-Methode : Virtueller PC'
- OnMediaInsert-Methode Virtueller PC, IVMDVDDriveEvents-Schnittstelle
- IVMDVDDriveEvents-Schnittstelle Virtueller PC, OnMediaInsert-Methode
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b19beabfcc4cab182af850d27d3d45ea565b266e8bcaa8fa2488aa145f43fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595734"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a>IVMDVDDriveEvents::OnMediaInsert-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.

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

Der Buchstabe oder Pfad des Hostlaufwerks zum ISO-Image.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn Medien (ein ISO-Image oder ein Datenträger auf einem Hostlaufwerk) eingefügt werden. Das Clientprogramm muss diese Schnittstellenmethode implementieren, um eine Benachrichtigung über das ereignis vmDVDDriveEvent OnInsert zu erhalten, das \_ von [**IVMDVDDrive stammt.**](ivmdvddrive.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMDVDDriveEvents ist als c2a7d8e9-e76c-4eb8-94f7-71a5122d249b definiert.<br/>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDVDDriveEvents**](ivmdvddriveevents.md)
</dt> </dl>

 

