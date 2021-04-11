---
title: Methode zum Konfigurieren von ivmserialport (vpccominterfaces. h)
description: Konfiguriert den seriellen Anschluss.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Konfigurieren des virtuellen Computers für die Methode
- Konfigurieren Sie die Methode Virtual PC, ivmserialport Interface.
- Ivmserialport Interface Virtual PC, Methode konfigurieren
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
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040678"
---
# <a name="ivmserialportconfigure-method"></a>Ivmserialport:: Configure-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

*portType* \[ in\]
</dt> <dd>

Der Typ des seriellen Anschlusses. Eine Liste der Werte finden Sie unter [**vmserialporttype**](vmserialporttype.md).

</dd> <dt>

*Portname* \[ in\]
</dt> <dd>

Der Name des seriellen Anschlusses. Beispiel: "COM1" for **vmserialport \_ hostport**, "C: \\SerialPort.txt" for **vmserialport \_ Textfile** oder " \\ \\ *Servername* \\ Pipe \\ *Pipename*" für **vmserialport \_ NamedPipe**.

</dd> <dt>

*vmconnectimmediately* \[ in\]
</dt> <dd>

**True** , wenn der serielle Host-Port sofort geöffnet werden soll, wenn der virtuelle Computer gestartet wird, andernfalls **false** . Wird ignoriert, wenn der *portType* nicht der **vmserialport- \_ hostport** ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                          |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                                 | Der *portType* -Parameter ist ungültig.<br/>                                                                                 |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                      |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                    | Der *Portname* -Parameter ist **null**.<br/>                                                                                  |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt> </dl>      | Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.<br/>                                                         |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl> | Der vom *Portname* -Parameter angegebene Pfad ist zu lang. Der Pfad muss kleiner als der **Maximale \_ Pfad** (260) sein.<br/> |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>    | Der *Portname* -Parameter enthält ein ungültiges Zeichen (eines der " \* ? <>/ \| ": ").<br/>                                    |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>    | Der *Portname* -Parameter gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                            |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                            | Die Konfiguration für diesen virtuellen Computer ist ungültig.<br/>                                                               |
| <dl> <dt>**VM \_ E \_ Pref \_ \_**</dt> unzulässiger Wert <dt>0xa0040301</dt> </dl>                   | Der angegebene Port wird bereits verwendet.<br/>                                                                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmserialport ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.<br/>              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmserialport**](ivmserialport.md)
</dt> </dl>

 

