---
title: IVMSerialPort-Schnittstelle (VPCCOMInterfaces.h)
description: Definiert einen seriellen Port innerhalb eines virtuellen Computers.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- IVMSerialPort-Schnittstelle Virtueller PC
- IVMSerialPort-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385f22caf7b843a91987eea01a7713544475c24be741bbb56d59610cb2cd521d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752825"
---
# <a name="ivmserialport-interface"></a>IVMSerialPort-Schnittstelle

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definiert einen seriellen Port innerhalb eines virtuellen Computers. Mit dieser Schnittstelle können Sie serielle Ports innerhalb eines virtuellen Computers konfigurieren. Sie können ein **IVMSerialPort-Objekt** aus dem [**IVMSerialPortCollection-Objekt**](ivmserialportcollection.md) abrufen, das von der [**IVMVirtualMachine::SerialPorts-Eigenschaft**](ivmvirtualmachine-serialports.md) zurückgegeben wird.

## <a name="members"></a>Member

Die **IVMSerialPort-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMSerialPort** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMSerialPort-Schnittstelle** verfügt über diese Methoden.



| Methode                                       | Beschreibung                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [**\_Id**](ivmserialport--id.md)            | Ruft den internen Bezeichner des seriellen Anschlusses ab.<br/> |
| [**Konfigurieren**](ivmserialport-configure.md) | Konfiguriert den seriellen Anschluss.<br/>                           |



 

### <a name="properties"></a>Eigenschaften

Die **IVMSerialPort-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                  | Zugriffstyp          | Beschreibung                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [**ConnectImmediately**](ivmserialport-connectimmediately.md)<br/> | Schreibgeschützt<br/> | Gibt an, ob der serielle Anschluss geöffnet werden soll, ohne auf den Empfang eines Modembefehls zu warten.<br/> |
| [**Name**](ivmserialport-name.md)<br/>                             | Schreibgeschützt<br/> | Der Name des seriellen Anschlusses.<br/>                                                                           |
| [**type**](ivmserialport-type.md)<br/>                             | Schreibgeschützt<br/> | Der Typ des seriellen Anschlusses.<br/>                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.<br/>              |



 

