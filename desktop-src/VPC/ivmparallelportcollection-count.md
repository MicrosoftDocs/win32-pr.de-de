---
title: Ivmparallelportcollection-Anzahl (Eigenschaft) (vpccominterfaces. h)
description: Anzahl paralleler Ports in dieser Sammlung.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Count-Eigenschaft virtueller PC
- Count-Eigenschaft Virtual PC, ivmparallelportcollection-Schnittstelle
- Ivmparallelportcollection-Schnittstelle Virtual PC, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956560"
---
# <a name="ivmparallelportcollectioncount-property"></a>Ivmparallelportcollection:: Count-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Anzahl paralleler Ports in dieser Auflistung ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Anzahl paralleler Ports.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                            | Bedeutung                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | Der Vorgang wurde durchgeführt.<br/> |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl> | Der-Parameter ist **null**.<br/>    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmparallelportcollection ist als 27c3e036-198l-430c-8735-6e652f 7203fd definiert.<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmparallelportcollection**](ivmparallelportcollection.md)
</dt> </dl>

 

