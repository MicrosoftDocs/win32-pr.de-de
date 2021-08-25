---
title: IVMSerialPortCollection-Elementeigenschaft (VPCCOMInterfaces.h)
description: Ruft das serielle Portobjekt ab, das dem angegebenen Index entspricht.
ms.assetid: 24ce1404-d7aa-4125-b1f9-9c54418ea205
keywords:
- Elementeigenschaft Virtueller PC
- Item-Eigenschaft Virtueller PC, IVMSerialPortCollection-Schnittstelle
- IVMSerialPortCollection-Schnittstelle Virtueller PC, Item-Eigenschaft
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Item
- IVMSerialPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48ebe4e8775abdb9bec3206cd4fd908caad0a35d503c12c528123a005e726f5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973800"
---
# <a name="ivmserialportcollectionitem-property"></a>IVMSerialPortCollection::Item-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft das serielle Portobjekt ab, das dem angegebenen Index entspricht.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Item(
  [in]          long          index,
  [out, retval] IVMSerialPort **serialPort
);
```



## <a name="property-value"></a>Eigenschaftswert

Das [**IVMSerialPort-Objekt.**](ivmserialport.md)

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt. <br/>                                                      |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>         | Der *serialPort-Parameter* ist NULL. <br/>                                                |
| <dl> <dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | Der Index des angeforderten Elements entspricht keinem Element in dieser Auflistung. <br/> |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl> | Die Konfiguration ist unbekannt.<br/>                                                       |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection ist als dd3c6175-1f04-4341-9f85-104074880289 definiert.<br/>    |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> <dt>

[**IVMSerialPortCollection**](ivmserialportcollection.md)
</dt> </dl>

 

