---
title: Ivmvirtualmachine startcommunicationchannel-Methode (vpccominterfaces. h)
description: Richtet einen Kommunikationskanal zwischen dem Host und dem Gast Betriebssystem ein.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- Startcommunicationchannel-Methode Virtual PC
- Startcommunicationchannel-Methode Virtual PC, ivmvirtualmachine-Schnittstelle
- Ivmvirtualmachine Interface Virtual PC, startcommunicationchannel-Methode
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478324"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a>Ivmvirtualmachine:: startcommunicationchannel-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Richtet einen Kommunikationskanal zwischen dem Host und dem Gast Betriebssystem ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*inhostendpointtype* \[ in\]
</dt> <dd>

Dieser Parameter muss **vmendpoint \_ NamedPipe** (0) sein.

</dd> <dt>

*inhostendpointname* \[ in\]
</dt> <dd>

Der eindeutige Pipename. Diese Zeichenfolge muss folgende Form aufweisen: " \\ \\ . \\ Pipe \\ *Pipename*". Der *pitzame* -Teil des Namens kann ein beliebiges Zeichen enthalten, das kein umgekehrter Schrägstrich ist, einschließlich Ziffern und Sonderzeichen. Die Zeichenfolge für den gesamten Pipenamen kann bis zu 256 Zeichen lang sein. Bei Pipenamen wird die Groß-/Kleinschreibung nicht beachtet

</dd> <dt>

*inguestendpointtype* \[ in\]
</dt> <dd>

Dieser Parameter muss **vmendpoint \_ tcpip** (1) sein.

</dd> <dt>

*inguestendpointname* \[ in\]
</dt> <dd>

Die Portnummer, die der TCP-Server im Gast abhört.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                        | Der Vorgang wurde durchgeführt.<br/>                                                                                                                    |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                                       | Der *inhostendpointtype* -Parameter ist nicht **vmendpoint \_ NamedPipe** (0), oder der *inguestendpointtype* -Parameter ist nicht **vmendpoint \_ tcpip** (1).<br/> |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                          | Der *inhostendpointname* -Parameter oder der *inguestendpointname* -Parameter ist **null** oder kein gültiger Wert.<br/>                                                    |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                                  | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ ungültiges \_ handle)**</dt> <dt>0x80070006</dt> </dl>        | Ein Handle ist ungültig.<br/>                                                                                                                           |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Error \_ outo-Memory)**</dt> <dt>0x8007000E</dt> </dl>            | Es ist nicht genügend Arbeitsspeicher verfügbar, um diese Anforderung abzuschließen.<br/>                                                                                   |
| <dl> <dt>**HRESULT \_ Aus \_ Win32 (Fehler \_ nicht \_ bereit)**</dt> <dt>0x80070015</dt> </dl>             | Das zugrunde liegende System, das für die Bereitstellung von Netzwerkdiensten verwendet wird, wird zurzeit initialisiert.<br/>                                                        |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt> </dl>        | Der Pipename wird bereits verwendet.<br/>                                                                                                                 |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Pipe \_ ausgelastet)**</dt> <dt>0x800700e7</dt> </dl>             | Ein oder mehrere Kanäle werden herunterlaufen und werden möglicherweise in Kürze verfügbar.<br/>                                                                          |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler bei \_ maximalen \_ Sitzungen \_ erreicht)**</dt> <dt>0x80070161</dt> </dl> | Die maximale Anzahl verfügbarer Kommunikationskanäle ist in Gebrauch. Ein anderer Kanal kann zu diesem Zeitpunkt nicht gestartet werden.<br/>                              |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Revisions Konflikt \_ )**</dt> <dt>0x8007051a</dt> </dl>     | Die Version des Host-und Gast Subsystems stimmt nicht überein. Weitere Details finden Sie im Windows-Ereignisprotokoll.<br/>                             |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>                             | Der virtuelle Computer wird nicht ausgeführt.<br/>                                                                                                                           |



 

## <a name="remarks"></a>Bemerkungen

Die aktuelle Implementierung unterstützt nur Named Pipe-Schnittstelle auf dem Host und die TCP/IP-Schnittstelle auf dem Gast Betriebssystem.

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
</dt> <dt>

[**Vmendpointtype**](vmendpointtype.md)
</dt> </dl>

 

