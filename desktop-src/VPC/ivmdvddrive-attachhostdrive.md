---
title: IVMDVDDrive AttachHostDrive-Methode (VPCCOMInterfaces.h)
description: Anfügen eines Hostlaufwerks an das DVD-Laufwerk auf dem virtuellen Computer.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- AttachHostDrive-Methode Virtueller PC
- AttachHostDrive-Methode Virtueller PC, IVMDVDDrive-Schnittstelle
- IVMDVDDrive-Schnittstelle Virtueller PC, AttachHostDrive-Methode
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c82229488ebb705cab1a684a207f973356d2d43177c4123ae4f456b55fbe6840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136853"
---
# <a name="ivmdvddriveattachhostdrive-method"></a>IVMDVDDrive::AttachHostDrive-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Anfügen eines Hostlaufwerks an das DVD-Laufwerk auf dem virtuellen Computer.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*driveLetter* \[ In\]
</dt> <dd>

Der Buchstabe des Hostlaufwerks, das angefügt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                    | Beschreibung                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                          | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>         | Es wurde kein Laufwerkbuchstaben angegeben, oder der angegebene Laufwerkbuchstaben ist ungültig.<br/>                                                                                                  |
| <dl> <dt>**E \_ FEHLER**</dt> <dt>0x80004005</dt> </dl>               | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                         |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>    | Der virtuelle Computer wurde nicht gefunden.<br/>                                                                                                                                   |
| <dl> <dt>**VM \_ \_VERWENDETES \_ \_ E-LAUFWERK**</dt> <dt>0XA0040727</dt> </dl> | Ein Host-DVD-Laufwerk oder ISO-Image ist bereits auf dem virtuellen Computer an dieses Laufwerk angefügt, oder das angegebene Hostlaufwerk wird bereits auf einem anderen virtuellen Computer verwendet.<br/> |
| <dl> <dt>**VM \_ E \_ DRIVE \_ INVALID**</dt> <dt>0xA0040502</dt> </dl> | Der Busspeicherort für dieses Laufwerk ist ungültig, oder das Laufwerk scheint kein gültiges DVD-Laufwerk zu sein.<br/>                                                                         |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>    | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

