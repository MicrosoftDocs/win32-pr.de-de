---
title: Ivmtask Error-Eigenschaft (vpccominterfaces. h)
description: Ruft den für diese Aufgabe aufgezeichneten Fehler ab.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Fehler Eigenschaft Virtual PC
- Fehler Eigenschaft Virtual PC, ivmtask-Schnittstelle
- Ivmtask Interface Virtual PC, Error-Eigenschaft
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338553"
---
# <a name="ivmtaskerror-property"></a>Ivmtask:: Error-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den für diese Aufgabe aufgezeichneten Fehler ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a>Eigenschaftswert

Der aufgezeichnete Fehler.

## <a name="error-codes"></a>Fehlercodes

Von anderen Schnittstellen zurückgegebene Instanzen von [**ivmtask**](ivmtask.md) können zusätzliche Werte zurückgeben. Weitere Informationen finden Sie in der Dokumentation der Methoden, die eine **ivmtask** -Instanz zurückgeben.



| Name/Wert                                                                                                                                                                        | Bedeutung                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                           | Der Vorgang wurde durchgeführt.<br/>                              |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                             | Der Parameterwert ist **null**.<br/>                           |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                     | Ein unerwarteter Fehler ist aufgetreten.<br/>                          |
| <dl> <dt>VM \_ E \_ vmvirtualpc, \_ ältere \_ Version</dt> <dt>0xa0040952</dt> </dl>     | Sowohl Virtual PC 2007 als auch Windows Virtual PC werden installiert.<br/> |
| <dl> <dt>VM \_ E \_ Weitere \_ Virtualisierungssoftware \_ </dt> <dt>0xa0040953</dt> </dl> | Andere Virtualisierungssoftware ist installiert.<br/>                |



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

 

