---
title: Ivmharddiskconnectioncollection-Element Eigenschaft (vpccominterfaces. h)
description: Ruft das Festplatten Verbindungs Objekt ab, das dem angegebenen Index entspricht.
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- Element Eigenschaft virtueller PC
- Item-Eigenschaft Virtual PC, ivmharddiskconnectioncollection-Schnittstelle
- Ivmharddiskconnectioncollection-Schnittstelle Virtual PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338314"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a>Ivmharddiskconnectioncollection:: Item (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft das Festplatten Verbindungs Objekt ab, das dem angegebenen Index entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a>Eigenschaftswert

Das [**ivmharddiskconnection**](ivmharddiskconnection.md) -Objekt.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt. <br/>                                                      |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der *harddiskconnection* -Parameter ist **null**. <br/>                                    |
| <dl> <dt>DISP \_ E \_ badindex</dt> <dt>0x8002000B</dt> </dl>  | Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung. <br/> |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>                                                       |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                          |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                               |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                      |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl>      |
| IID<br/>                      | IID \_ ivmharddiskconnectioncollection ist definiert als b9f2caf4-0aeb-4085-B105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmharddiskconnection**](ivmharddiskconnection.md)
</dt> <dt>

[**Ivmharddiskconnectioncollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

