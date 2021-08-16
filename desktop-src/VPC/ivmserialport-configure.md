---
title: IVMSerialPort Configure-Methode (VPCCOMInterfaces.h)
description: Konfiguriert den seriellen Anschluss.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Konfigurieren der Methode "Virtueller PC"
- Konfigurieren der Methode Virtual PC, IVMSerialPort-Schnittstelle
- IVMSerialPort-Schnittstelle Virtueller PC, Methode konfigurieren
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e67d84239f7b672b5b8c47346d1dde73de6a35c1e99a3ba231b8425fe8b7d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136623"
---
# <a name="ivmserialportconfigure-method"></a>IVMSerialPort::Configure-Methode

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Konfiguriert den seriellen Anschluss.

## <a name="syntax"></a>Syntax


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*portType* \[ In\]
</dt> <dd>

Der Typ des seriellen Anschlusses. Eine Liste der Werte finden Sie unter [**VMSerialPortType**](vmserialporttype.md).

</dd> <dt>

*portName* \[ In\]
</dt> <dd>

Der Name des seriellen Anschlusses. Beispiel: "COM1" für **vmSerialPort \_ HostPort,**"C:SerialPort.txt" für \\ **vmSerialPort \_ TextFile** oder " \\ \\ *servername* \\ pipe \\ *pipename*" für **vmSerialPort \_ NamedPipe**.

</dd> <dt>

*vmConnectImmediately* \[ In\]
</dt> <dd>

**TRUE,** wenn der serielle Hostport sofort geöffnet werden soll, wenn der virtuelle Computer gestartet wird, **andernfalls FALSE.** Wird ignoriert, *wenn portType* nicht **vmSerialPort \_ HostPort ist.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | Beschreibung                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                          |
| <dl> <dt>**E \_ INVALIDARG-0x80000003**</dt> <dt></dt> </dl>                                 | Der *portType-Parameter* ist ungültig.<br/>                                                                                 |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                      |
| <dl> <dt>**E \_ ZEIGER 0X80004003**</dt> <dt></dt> </dl>                                    | Der *portName-Parameter* ist **NULL.**<br/>                                                                                  |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | Zum Abschließen dieser Anforderung ist nicht genügend Arbeitsspeicher verfügbar.<br/>                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BUFFER \_ OVERFLOW)**</dt> <dt>0x8007006f</dt> </dl> | Der durch den *portName-Parameter angegebene Pfad* ist zu lang. Der Pfad muss kleiner als **MAX \_ PATH** -Zeichen (260) sein.<br/> |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ INVALID \_ NAME)**</dt> <dt>0x8007007b</dt> </dl>    | Der *portName-Parameter* enthält ein ungültiges Zeichen (eines von " \* ?<>/ \| ":").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ BAD \_ PATHNAME)**</dt> <dt>0x800700a1</dt> </dl>    | Der *portName-Parameter* gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                            |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | Die Konfiguration für diesen virtuellen Computer ist ungültig.<br/>                                                               |
| <dl> <dt>**VM \_ E \_ PREF \_ \_ UNGÜLTIGER**</dt> <dt>0XA0040301</dt> </dl>                   | Der angegebene Port wird bereits verwendet.<br/>                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.<br/>              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

