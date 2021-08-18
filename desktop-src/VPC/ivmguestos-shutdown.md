---
title: IVMGuestOS Shutdown-Methode (VPCCOMInterfaces.h)
description: Fährt das Gastbetriebssystem auf dem virtuellen Computer herunter.
ms.assetid: a1453ad1-c4c2-47bb-a612-d203a6ee8c18
keywords:
- Shutdown-Methode Virtueller PC
- Shutdown-Methode Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC , Shutdown-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.Shutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759986fce07c0f974a18169fbece355902e5a9a82fd1434e78d5eb2b79b51fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998990"
---
# <a name="ivmguestosshutdown-method"></a>IVMGuestOS::Shutdown-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Fährt das Gastbetriebssystem auf dem virtuellen Computer herunter.

## <a name="syntax"></a>Syntax


```C++
HRESULT Shutdown(
  [in]          VARIANT_BOOL isForced,
  [out, retval] IVMTask      **outShutdownTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isForced* \[ In\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn das Herunterfahren erzwungen werden soll, **andernfalls VARIANT \_ FALSE.**

</dd> <dt>

*outShutdownTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) mit dem der Abschluss des Herunterfahrens nachverfolgt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                          | BESCHREIBUNG                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                | Der Vorgang wurde durchgeführt.<br/>                                   |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                  | Der *outShutdownTask-Parameter* ist **NULL.**<br/>                    |
| <dl> <dt>**VM \_ E \_ \_ TIMED OUT**</dt> <dt>0xA0040202</dt> </dl>                           | Der Vorgang wurde nicht rechtzeitig abgeschlossen.<br/>              |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                          | Der virtuelle Computer wurde nicht gefunden.<br/>                                      |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,**</dt> <dt>0xA0040206</dt> </dl>                     | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>                      |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ ACCESS \_ DENIED)**</dt> <dt>0x80070005</dt> </dl> | Der Aufrufer muss über Ausführungszugriffsberechtigungen für diesen virtuellen Computer verfügen.<br/>    |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl>       | Die Integrationskomponentenfunktion ist auf diesem virtuellen Computer nicht installiert.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                          | Ein unerwarteter Fehler ist aufgetreten.<br/>                               |



 

## <a name="remarks"></a>Hinweise

Der virtuelle Computer muss ausgeführt werden, und die Integrationskomponentenfunktion muss installiert werden, wenn diese Methode aufgerufen wird. Diese Methode wird nur für Windows-basierte Gastbetriebssysteme unterstützt.

Die folgenden Werte können über die [**Error-Eigenschaft**](ivmtask-error.md) des zurückgegebenen [**IVMTask-Objekts**](ivmtask.md) zurückgegeben werden.



| [](ivmtask-error.md) Fehlercode/-wert                                                                                                                                                                                                                                                                          | BESCHREIBUNG                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)<br/>                             | Der Aufrufer muss über Ausführungszugriffsberechtigungen für diesen virtuellen Computer verfügen.<br/>             |
| <span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)<br/>                         | Der Computer ist gesperrt und kann ohne die Option Force nicht heruntergefahren werden.<br/> |
| <span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)<br/>                                             | Das Gerät ist nicht bereit.<br/>                                                 |
| <span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)<br/> | Das Herunterfahren des Systems wird ausgeführt.<br/>                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

