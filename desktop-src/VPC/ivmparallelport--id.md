---
title: Ivmparallelport-_ID Methode (vpccominterfaces. h)
description: Ruft den internen Bezeichner des parallelen Ports ab.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- _ID-Methode Virtual PC
- _ID-Methode Virtual PC, ivmparallelport-Schnittstelle
- Ivmparallelport Interface Virtual PC, _ID-Methode
topic_type:
- apiref
api_name:
- IVMParallelPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267061204ea92dd8f5cae37fc5cb279e7dc2b010
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338519"
---
# <a name="ivmparallelport_id-method"></a>Ivmparallelport:: \_ ID-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den internen Bezeichner des parallelen Ports ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*portid* \[ vorgenommen\]
</dt> <dd>

Der parallele Port Bezeichner.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                            |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>                               |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                        |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration für diesen virtuellen Computer ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann nicht von Skriptsprachen verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmparallelport ist als 097beecb-0a02-474b-abd6-298b22293fc6 definiert.<br/>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmparallelport**](ivmparallelport.md)
</dt> </dl>

 

