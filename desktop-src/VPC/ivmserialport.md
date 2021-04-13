---
title: Ivmserialport-Schnittstelle (vpccominterfaces. h)
description: Definiert einen seriellen Anschluss innerhalb eines virtuellen Computers.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Ivmserialport Interface Virtual PC
- Ivmserialport Interface Virtual PC, beschrieben
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
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518395"
---
# <a name="ivmserialport-interface"></a>Ivmserialport-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert einen seriellen Anschluss innerhalb eines virtuellen Computers. Diese Schnittstelle ermöglicht Ihnen das Konfigurieren von seriellen Anschlüssen innerhalb eines virtuellen Computers. Sie können ein **ivmserialport** -Objekt aus dem [**ivmserialportcollection**](ivmserialportcollection.md) -Objekt abrufen, das von der [**ivmvirtualmachine:: serialports**](ivmvirtualmachine-serialports.md) -Eigenschaft zurückgegeben wird.

## <a name="members"></a>Member

Die **ivmserialport** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmserialport** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmserialport** -Schnittstelle verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [**\_id**](ivmserialport--id.md)            | Ruft den internen Bezeichner des seriellen Anschlusses ab.<br/> |
| [**Konfigurieren**](ivmserialport-configure.md) | Konfiguriert den seriellen Anschluss.<br/>                           |



 

### <a name="properties"></a>Eigenschaften

Die **ivmserialport** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                  | Zugriffstyp          | BESCHREIBUNG                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [**Connectimmediately**](ivmserialport-connectimmediately.md)<br/> | Schreibgeschützt<br/> | Gibt an, ob der serielle Anschluss geöffnet werden soll, ohne darauf zu warten, dass ein Modem Befehl empfangen wird.<br/> |
| [**Name**](ivmserialport-name.md)<br/>                             | Schreibgeschützt<br/> | Der Name des seriellen Anschlusses.<br/>                                                                           |
| [**type**](ivmserialport-type.md)<br/>                             | Schreibgeschützt<br/> | Der Typ des seriellen Anschlusses.<br/>                                                                           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmserialport ist als 2ce4460d-1d3f-4458-bf8b-44084b816815 definiert.<br/>              |



 

