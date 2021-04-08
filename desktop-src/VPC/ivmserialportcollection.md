---
title: Ivmserialportcollection-Schnittstelle (vpccominterfaces. h)
description: Definiert die Sammlung von seriellen Anschlüssen innerhalb des virtuellen Computers. Zum Abrufen eines ivmserialportcollection-Objekts verwenden Sie die Eigenschaft "ivmvirtualmachine serialports".
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Ivmserialportcollection-Schnittstelle virtueller PC
- Ivmserialportcollection Interface Virtual PC, beschrieben
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741737"
---
# <a name="ivmserialportcollection-interface"></a>Ivmserialportcollection-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definiert die Sammlung von seriellen Anschlüssen innerhalb des virtuellen Computers. Zum Abrufen eines **ivmserialportcollection** -Objekts verwenden Sie die [**ivmvirtualmachine:: serialports**](ivmvirtualmachine-serialports.md) -Eigenschaft.

## <a name="members"></a>Member

Die **ivmserialportcollection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmserialportcollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmserialportcollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                         | Zugriffstyp          | BESCHREIBUNG                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [**\_"Netwenum"**](ivmserialportcollection--newenum.md)<br/> | Schreibgeschützt<br/> | Ein Enumerator für die Auflistung.<br/>                               |
| [**Countdown**](ivmserialportcollection-count.md)<br/>        | Schreibgeschützt<br/> | Die Anzahl der seriellen Anschlüsse in dieser Sammlung.<br/>                  |
| [**Element**](ivmserialportcollection-item.md)<br/>          | Schreibgeschützt<br/> | Das serielle Port Objekt, das dem angegebenen Index entspricht.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmserialportcollection ist als dd3c6175-1F04-4341-9f85-104074880289 definiert.<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmserialport**](ivmserialport.md)
</dt> <dt>

[**Ivmvirtualmachine:: serialports**](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

