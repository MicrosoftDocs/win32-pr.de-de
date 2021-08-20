---
title: IVMSerialPort_ID Methode (VPCCOMInterfaces.h)
description: Interner Bezeichner des seriellen Anschlusses.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- _ID-Methode Virtueller PC
- _ID Virtual PC, IVMSerialPort-Schnittstelle
- IVMSerialPort-Schnittstelle Virtueller PC , _ID-Methode
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b55974319e4af48ae1a6f3554ae79557feaa5c8455e47b66e82e4d4cf02a801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123734"
---
# <a name="ivmserialport_id-method"></a>IVMSerialPort:: \_ ID-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den internen Bezeichner des seriellen Anschlusses ab.

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

Der Bezeichner des seriellen Anschlusses.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                 | Beschreibung                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                            |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>                               |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                        |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration für diesen virtuellen Computer ist ungültig.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann von Skriptsprachen nicht verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

