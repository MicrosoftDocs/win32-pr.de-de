---
title: IVMHardDiskConnection UndoHardDisk-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft ein Festplattenobjekt ab, das dem Rückgängig-Datenträgerimage dieser Verbindung entspricht.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- UndoHardDisk-Eigenschaft Virtueller PC
- UndoHardDisk-Eigenschaft Virtueller PC, IVMHardDiskConnection-Schnittstelle
- IVMHardDiskConnection-Schnittstelle Virtueller PC, UndoHardDisk-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba90d72aeab4fae618c3113796de1335d005670369de514b4e0650fead75d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998920"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a>IVMHardDiskConnection::UndoHardDisk -Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft ein Festplattenobjekt ab, das dem Rückgängig-Datenträgerimage dieser Verbindung entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a>Eigenschaftswert

Ein [**IVMHardDisk-Objekt,**](ivmharddisk.md) das die rückgängig gemachte Festplatte beschreibt, die dieser Verbindung zugeordnet ist.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                                                                    |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                                    | Der -Parameter ist **NULL** oder ungültig.<br/>                                                                                          |
| <dl> <dt>HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)</dt> <dt>0X80070002</dt> </dl> | Der Rückgängig-Datenträger für diese Verbindung wurde nicht gefunden.<br/>                                                                                 |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>                            | Die aktuelle Konfiguration des virtuellen Computers ist ungültig.<br/>                                                                          |
| <dl> <dt>VM \_ E \_ DRIVE \_ INVALID</dt> <dt>0xA0040502</dt> </dl>                         | Der Busstandort für diese Verbindung wurde nicht ordnungsgemäß initialisiert, oder das Gerät an diesem Standort ist keine gültige Festplatte.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection ist als aefa36a5-463a-46ae-9e6c-a1fb4e12e671 definiert.<br/>      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

