---
title: IVMGuestOS Restart-Methode (VPCCOMInterfaces.h)
description: Startet das Gastbetriebssystem neu.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Neustartmethode Virtueller PC
- Neustartmethode Virtual PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, Restart-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b25d5fc2bec8c8a0a10425f63b6abc7c6363e8562b84376af4d053ec710e709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594008"
---
# <a name="ivmguestosrestart-method"></a>IVMGuestOS::Restart-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Startet das Gastbetriebssystem neu.

## <a name="syntax"></a>Syntax


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inForced* \[ In\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn ein erzwungener Neustart erforderlich ist, **andernfalls VARIANT \_ FALSE.**

</dd> <dt>

*outRestartTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) das zum Nachverfolgen des Abschlussfortschritts der Neustartsequenz verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                    | BESCHREIBUNG                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                                   |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                            | Der *outRestartTask-Parameter* ist **NULL.**<br/>                     |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                               |
| <dl> <dt>**VM \_ E \_ TIMED \_ OUT**</dt> <dt>0xA0040202</dt> </dl>                     | Der Vorgang wurde nicht rechtzeitig abgeschlossen.<br/>              |
| <dl> <dt>**VM \_ E \_ VM \_ NOT \_ RUNNING**</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer (VM) muss für diesen Vorgang ausgeführt werden.<br/>    |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                    | Die Konfiguration ist unbekannt.<br/>                                   |
| <dl> <dt>**VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL**</dt> <dt>0XA0040505</dt> </dl> | Die Integrationskomponentenfunktion ist auf diesem virtuellen Computer nicht installiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Werte können über die [**Error-Eigenschaft**](ivmtask-error.md) des zurückgegebenen [**IVMTask-Objekts zurückgegeben**](ivmtask.md) werden.



| [](ivmtask-error.md) Fehlercode/-wert                                                                                                                                                                                                                                                                          | BESCHREIBUNG                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)<br/>                             | Der Aufrufer muss über Ausführungszugriffsberechtigungen für diesen virtuellen Computer verfügen.<br/>             |
| <span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)<br/>                         | Der Computer ist gesperrt und kann nicht ohne die Force-Option heruntergefahren werden.<br/> |
| <span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)<br/>                                             | Das Gerät ist nicht bereit.<br/>                                                 |
| <span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)<br/> | Das System wird heruntergefahren.<br/>                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

