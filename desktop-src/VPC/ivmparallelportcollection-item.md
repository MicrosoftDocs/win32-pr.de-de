---
title: IVMParallelPortCollection-Elementeigenschaft (VPCCOMInterfaces.h)
description: Ruft das parallele Portobjekt ab, das dem angegebenen Index entspricht.
ms.assetid: f67a4224-ca96-4d68-9f0f-4977ffff859e
keywords:
- Item-Eigenschaft Virtueller PC
- Item-Eigenschaft Virtual PC, IVMParallelPortCollection-Schnittstelle
- IVMParallelPortCollection-Schnittstelle Virtueller PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Item
- IVMParallelPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a28aec3fbe9585185f61cc7941d5de8033b73019354ca480f72fe4b3b7be793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007000"
---
# <a name="ivmparallelportcollectionitem-property"></a>IVMParallelPortCollection::Item-Eigenschaft

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft das parallele Portobjekt ab, das dem angegebenen Index entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]          long            index,
  [out, retval] IVMParallelPort **vmParallelPort
);
```



## <a name="property-value"></a>Eigenschaftswert

Das [**IVMParallelPort-Objekt.**](ivmparallelport.md)

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt. <br/>                                                      |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>         | Der *vmParallelPort-Parameter* ist **NULL.** <br/>                                        |
| <dl> <dt>DISP \_ E \_ BADINDEX-0x8002000B</dt> <dt></dt> </dl>  | Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung. <br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>                                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection ist als 27c3e036-198f-430c-8735-6e652f7203fd definiert.<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> <dt>

[**IVMParallelPortCollection**](ivmparallelportcollection.md)
</dt> </dl>

 

