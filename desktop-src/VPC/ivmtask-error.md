---
title: IVMTask Error-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft den für diese Aufgabe aufgezeichneten Fehler ab.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Fehlereigenschaft Virtueller PC
- Fehlereigenschaft Virtueller PC, IVMTask-Schnittstelle
- IVMTask-Schnittstelle Virtueller PC, Error-Eigenschaft
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
ms.openlocfilehash: 4d186f6a6fbdf9c27d3d2724715903baaa8a494261f19b2725f6bd009820aacb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117938366"
---
# <a name="ivmtaskerror-property"></a>IVMTask::Error-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

Instanzen von [**IVMTask,**](ivmtask.md) die von anderen Schnittstellen zurückgegeben werden, geben möglicherweise zusätzliche Werte zurück. Weitere Informationen finden Sie in der Dokumentation der Methoden, die eine **IVMTask-Instanz** zurückgeben.



| Name/Wert                                                                                                                                                                        | Bedeutung                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                           | Der Vorgang wurde durchgeführt.<br/>                              |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                             | Der Parameterwert ist **NULL.**<br/>                           |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                     | Ein unerwarteter Fehler ist aufgetreten.<br/>                          |
| <dl> <dt>VM \_ E \_ VMVIRTUALPC \_ ÄLTERE \_ VERSION</dt> <dt>0xA0040952</dt> </dl>     | Sowohl Virtual PC 2007 als auch Windows Virtual PC sind installiert.<br/> |
| <dl> <dt>VM \_ E \_ OTHER \_ VIRTUALIZATION \_ SOFTWARE</dt> <dt>0xA0040953</dt> </dl> | Andere Virtualisierungssoftware ist installiert.<br/>                |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask ist als ab72b222-6e9c-48ae-aa54-85e3e635767c definiert.<br/>                    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

