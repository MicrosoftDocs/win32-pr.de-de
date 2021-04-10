---
title: Ivmdvddriveevents onmediainsert-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden. | Ivmdvddriveevents onmediainsert-Methode (vpccominterfaces. h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Onmediainsert-Methode Virtual PC
- Onmediainsert-Methode Virtual PC, ivmdvddriveevents-Schnittstelle
- Ivmdvddriveevents Interface Virtual PC, onmediainsert-Methode
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
ms.openlocfilehash: 883f7990de17a9d1dbb21db9651e0f5ad4ec74aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961310"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a>Ivmdvddriveevents:: onmediainsert-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnMediaInsert(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mediapath* \[ in\]
</dt> <dd>

Der Buchstabe des Host Laufwerks bzw. der Pfad zum ISO-Abbild.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn Medien (ein ISO-Image oder ein Laufwerk auf einem Host Laufwerk) eingefügt werden. Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das vmdvddriveevent OnInsert-Ereignis zu erhalten, das \_ von [**ivmdvddrive**](ivmdvddrive.md)stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | Diid \_ ivmdvddriveevents ist als c2a7d8e9-e76c-4eb8-94f7-71a5122d249b definiert.<br/>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmdvddriveevents**](ivmdvddriveevents.md)
</dt> </dl>

 

