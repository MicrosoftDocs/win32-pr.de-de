---
title: Ivmtask ErrorDescription-Eigenschaft (vpccominterfaces. h)
description: Ruft die lokalisierte Fehlerbeschreibung ab, die für diese Aufgabe aufgezeichnet wurde.
ms.assetid: 85728775-14b6-4031-9ccd-4c4f8c410705
keywords:
- ErrorDescription-Eigenschaft virtueller PC
- ErrorDescription-Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, ErrorDescription (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMTask.ErrorDescription
- IVMTask.get_ErrorDescription
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5c95eac383d8e071832fdbf7843c01345278c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743097"
---
# <a name="ivmtaskerrordescription-property"></a>Ivmtask:: ErrorDescription-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die lokalisierte Fehlerbeschreibung ab, die für diese Aufgabe aufgezeichnet wurde.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ErrorDescription(
  [out, retval] BSTR *outErrorDesc
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Fehlerbeschreibung.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>     |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der Parameterwert ist **null**.<br/>  |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmtask ist als ab72b222-6e9c-48ae-AA54-85e3e635767c definiert.<br/>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmtask**](ivmtask.md)
</dt> </dl>

 

