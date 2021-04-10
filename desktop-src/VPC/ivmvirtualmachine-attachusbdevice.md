---
title: Ivmvirtualmachine attachingbdevice-Methode (vpccominterfaces. h)
description: Fügt ein USB-Gerät an einen virtuellen Computer an.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Attachingbdevice-Methode Virtual PC
- Attachingbdevice-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, attachingbdevice-Methode
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
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040738"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a>Ivmvirtualmachine:: attachingbdevice-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fügt ein USB-Gerät an einen virtuellen Computer (VM) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*in-bdevice* \[ in\]
</dt> <dd>

Ein [**ivmusbdevice**](ivmusbdevice.md) -Zeiger, der das USB-Gerät darstellt, das mit dem Host verbunden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                             | BESCHREIBUNG                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                   | Der Vorgang wurde durchgeführt.<br/>                                           |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                     | Der-Parameter ist **null**.<br/>                                              |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>                        | Der virtuelle Computer wird nicht ausgeführt.<br/>                                                  |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                             | Die Konfiguration ist unbekannt.<br/>                                           |
| <dl> <dt>**VM \_ E- \_ Ergänzungen \_ nicht in \_ Anspruch**</dt> nehmen <dt>0xa0040504</dt> </dl>                   | Integrations Komponenten sind im Gast Betriebssystem nicht verfügbar.<br/> |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht**</dt> " <dt>uxa0040505</dt> " </dl>          | Das USB-Feature ist nicht verfügbar.<br/>                                       |
| <dl> <dt>**VM \_ E \_ USB- \_ Connector- \_ Treiber \_ Fehler**</dt> <dt>0xa00400925</dt> </dl>          | Fehler beim USB-Connector-Treiber.<br/>                                 |
| <dl> <dt>**VM \_ E \_ USB- \_ Anfüge Fehler \_ \_ Weitere \_ Geräte**</dt> <dt>0xa00400931</dt> </dl>     | Weitere Geräte können nicht an die VM angefügt werden.<br/>                                   |
| <dl> <dt>**VM \_ \_ \_ \_ \_ \_ Fehler beim Anfügen des USB-**</dt> Anfügens. <dt></dt> </dl>         | Die USB-Umleitung wird von einer Gruppenrichtlinien Einstellung verhindert.<br/>               |
| <dl> <dt>**VM \_ Fehler beim E \_ -USB- \_ Anfügen \_ \_ \_**</dt> mit <dt>0xa00400933</dt> . </dl> | Ein USB-Gerät wurde bereits von einem anderen Client angefügt.<br/>            |
| <dl> <dt>**VM \_ E \_ USB \_ - \_ Anfüge**</dt> Fehler <dt>0xa00400926</dt> </dl>                    | Der Anfüge Vorgang ist fehlgeschlagen.<br/>                                            |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                             | Ein unerwarteter Fehler ist aufgetreten.<br/>                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmvirtualmachine ist als f7092aa1-33ed-4f78-a59f-c00adfc2edd7 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmvirtualmachine**](ivmvirtualmachine.md)
</dt> </dl>

 

