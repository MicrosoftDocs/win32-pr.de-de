---
title: Ivmguestos ProductType-Eigenschaft (vpccominterfaces. h)
description: Hiermit wird der Produkttyp des Gast Betriebssystems abgerufen, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- ProductType-Eigenschaft virtueller PC
- ProductType-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, ProductType-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337320"
---
# <a name="ivmguestosproducttype-property"></a>Ivmguestos::P roducttype-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Hiermit wird der Produkttyp des Gast Betriebssystems abgerufen, das auf dem virtuellen Computer ausgeführt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Produkttyp. Die folgenden Zeichen folgen Werte werden unterstützt.



| Wert                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"0x0000002"</dt> </dl> | Das System ist ein Domänen Controller, und das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.<br/>                                                                                                   |
| <dl> <dt>"0x0000003"</dt> </dl> | Das Betriebssystem ist Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 oder Windows 2000 Server.<br/> Beachten Sie, dass ein Server, der auch ein Domänen Controller ist, als **ver- \_ NT- \_ Domänen \_ Controller**, nicht als **ver-NT- \_ \_ Server** gemeldet<br/> |
| <dl> <dt>"0x0000001"</dt> </dl> | Das Betriebssystem ist Windows 7, Windows Vista, Windows XP oder Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmguestos**](ivmguestos.md)
</dt> </dl>

 

