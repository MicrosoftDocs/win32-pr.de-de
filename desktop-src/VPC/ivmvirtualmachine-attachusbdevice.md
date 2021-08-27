---
title: IVMVirtualMachine AttachUSBDevice-Methode (VPCCOMInterfaces.h)
description: Fügt ein USB-Gerät an einen virtuellen Computer an.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- AttachUSBDevice-Methode Virtueller PC
- AttachUSBDevice-Methode Virtueller PC, IVMVirtualMachine-Schnittstelle
- IVMVirtualMachine-Schnittstelle Virtueller PC , AttachUSBDevice-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c62f3e6862e14a7faa70719d1238500ab5dfe1de10801e7aea390e24a07210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006900"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>IVMVirtualMachine::AttachUSBDevice-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Fügt ein USB-Gerät an einen virtuellen Computer (VM) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inUSBDevice* \[ In\]
</dt> <dd>

Ein [**IVMUSBDevice-Zeiger,**](ivmusbdevice.md) der das USB-Gerät darstellt, das mit dem Host verbunden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                             | BESCHREIBUNG                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                   | Der Vorgang wurde durchgeführt.<br/>                                           |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                     | Der Parameter ist **NULL.**<br/>                                              |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,**</dt> <dt>0xA0040206</dt> </dl>                        | Der virtuelle Computer wird nicht ausgeführt.<br/>                                                  |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                             | Die Konfiguration ist unbekannt.<br/>                                           |
| <dl> <dt>**VM \_ E \_ ADDITIONEN \_ NICHT \_ VERFÜGBAR**</dt> <dt>0XA0040504</dt> </dl>                   | Integrationskomponenten sind im Gastbetriebssystem nicht verfügbar.<br/> |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl>          | Das USB-Feature ist nicht verfügbar.<br/>                                       |
| <dl> <dt>**VM \_ E \_ USB CONNECTOR DRIVER \_ \_ \_ ERROR**</dt> <dt>0xA00400925</dt> </dl>          | Fehler beim USB-Connectortreiber.<br/>                                 |
| <dl> <dt>**VM \_ E \_ USB ATTACH FAILED MORE \_ \_ \_ \_ DEVICES**</dt> <dt>0xA00400931</dt> </dl>     | Es können keine weiteren Geräte an den virtuellen Computer angefügt werden.<br/>                                   |
| <dl> <dt>**VM \_ E \_ USB ATTACH FAILED GP \_ \_ \_ \_ ERROR**</dt> <dt>0xA00400932</dt> </dl>         | Eine Gruppenrichtlinieneinstellung verhindert die USB-Umleitung.<br/>               |
| <dl> <dt>**VM \_ \_E USB ATTACH FAILED ALREADY \_ \_ \_ \_ ASSIGNED**</dt> <dt>0XA00400933</dt> </dl> | Ein USB-Gerät wurde bereits von einem anderen Client angeschlossen.<br/>            |
| <dl> <dt>**VM \_ E \_ USB \_ ATTACH \_ FAILED**</dt> <dt>0xA00400926</dt> </dl>                    | Fehler beim Anfügen.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                             | Ein unerwarteter Fehler ist aufgetreten.<br/>                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

