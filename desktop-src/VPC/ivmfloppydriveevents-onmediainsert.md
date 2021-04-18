---
title: Ivmfloppydriveevents onmediainsert-Methode (vpccominterfaces. h)
description: Empfängt eine Benachrichtigung, dass Medien in das Laufwerk eingefügt wurden. | Ivmfloppydriveevents onmediainsert-Methode (vpccominterfaces. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Onmediainsert-Methode Virtual PC
- Onmediainsert-Methode Virtual PC, ivmfloppydriveevents-Schnittstelle
- Ivmfloppydriveevents Interface Virtual PC, onmediainsert-Methode
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
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106351911"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a>Ivmfloppydriveevents:: onmediainsert-Methode

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

Der Buchstabe des Host Laufwerks bzw. der Pfad des Disketten Bilds.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird aufgerufen, wenn Medien (ein Disketten Image oder eine Diskette in einem Host Laufwerk) eingefügt werden. Das Client Programm muss diese Schnittstellen Methode implementieren, um Benachrichtigungen über das vmfloppydriveevent \_ onmediainsert-Ereignis zu erhalten, das von [**ivmfloppydrive**](ivmfloppydrive.md)stammt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | Diid \_ ivmfloppydriveevents ist als a9ed3401-4e09-4177-86ec-a13bf9fa7d4e definiert.<br/>      |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmfloppydriveevents**](ivmfloppydriveevents.md)
</dt> </dl>

 

