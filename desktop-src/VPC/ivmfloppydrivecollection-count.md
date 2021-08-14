---
title: IVMFloppyDriveCollection Count-Eigenschaft (VPCCOMInterfaces.h)
description: Anzahl der Diskettenlaufwerke in dieser Auflistung.
ms.assetid: d430e5ae-9782-4f88-a5a4-744e79545c7a
keywords:
- Count-Eigenschaft Virtueller PC
- Count-Eigenschaft Virtual PC , IVMFloppyDriveCollection-Schnittstelle
- IVMFloppyDriveCollection-Schnittstelle Virtueller PC , Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Count
- IVMFloppyDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1688a157b4352c1d2d1eba12701633e61ae6097b358737b1c9593a8ff16d122c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594836"
---
# <a name="ivmfloppydrivecollectioncount-property"></a>IVMFloppyDriveCollection::Count-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Anzahl der Diskettenlaufwerke in dieser Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der Diskettenmedienlaufwerke.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection ist als 8ba70a25-f698-4ee5-85ce-3cc93a925516 definiert.<br/>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)
</dt> </dl>

 

