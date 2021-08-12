---
title: IVMParallelPort_ID Methode (VPCCOMInterfaces.h)
description: Ruft den internen Bezeichner des parallelen Ports ab.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- _ID-Methode Virtueller PC
- _ID Virtual PC, IVMParallelPort-Schnittstelle
- IVMParallelPort-Schnittstelle Virtueller PC , _ID-Methode
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
ms.openlocfilehash: df0c7b3eab7de47d182c94aa9b5fb35aef04e98495ef3e7b39d4547967f3438b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593218"
---
# <a name="ivmparallelport_id-method"></a>IVMParallelPort:: \_ ID-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den internen Bezeichner des parallelen Ports ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*portID* \[ out\]
</dt> <dd>

Der Bezeichner des parallelen Ports.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | BESCHREIBUNG                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                            |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>                               |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                        |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration für diesen virtuellen Computer ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann von Skriptsprachen nicht verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort ist als 097beecb-0a02-474f-abd6-298b22293fc6 definiert.<br/>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

