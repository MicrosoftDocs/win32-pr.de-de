---
title: IVMHardDiskConnectionCollection Count-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die Anzahl der Festplattenverbindungen in dieser Auflistung ab.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Count-Eigenschaft Virtueller PC
- Count-Eigenschaft Virtual PC, IVMHardDiskConnectionCollection-Schnittstelle
- IVMHardDiskConnectionCollection-Schnittstelle Virtueller PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fccb00cf2388db8a971f5da2f726030b3f793ac878f4a59df2646195eb41ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974324"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a>IVMHardDiskConnectionCollection::Count (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Anzahl der Festplattenverbindungen in dieser Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl der Festplattenverbindungen.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der Parameter ist **NULL.**<br/>        |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                          |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                               |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                      |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection ist als b9f2caf4-0aeb-4085-b105-ceddb90dbf62 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

