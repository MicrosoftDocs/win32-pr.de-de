---
title: IVMHardDisk Merge-Methode (VPCCOMInterfaces.h)
description: Führt eine differenzierende virtuelle Festplatte mit dem übergeordneten Datenträgerimage zusammen.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Mergemethode Virtueller PC
- Mergemethode Virtual PC , IVMHardDisk-Schnittstelle
- IVMHardDisk-Schnittstelle Virtueller PC, Merge-Methode
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b1683b5a44d8418dc247dddcfde52b369c293484e5c3b19c139fe25521ac6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998940"
---
# <a name="ivmharddiskmerge-method"></a>IVMHardDisk::Merge-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Führt eine differenzierende virtuelle Festplatte mit dem übergeordneten Datenträgerimage zusammen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mergeTask* \[ out, retval\]
</dt> <dd>

Ein [**IVMTask-Objekt,**](ivmtask.md) mit dem der Abschluss des Zusammenführungsprozesses nachverfolgt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                          |
| <dl> <dt>**E \_ POINTER**</dt> <dt>0x80004003</dt> </dl>                                      | Der Parameter ist **NULL.**<br/>                                                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ SHARING \_ VIOLATION)**</dt> <dt>0x80070020</dt> </dl> | Das virtuelle Festplattenimage, auf das dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, wird verwendet, oder das übergeordnete Image dieses virtuellen Festplattenimages wird verwendet. Oder diese Festplattenimages können Teil eines gespeicherten Zustands sein.<br/> |
| <dl> <dt>**VM \_ E \_ WRONG HD IMAGE \_ \_ \_ TYPE**</dt> <dt>0xA004067B</dt> </dl>                   | Das virtuelle Festplattenimage, auf das dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, muss ein differenzierendes Datenträgerimage sein.<br/>                                                                                            |
| <dl> <dt>**VM \_ E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt> </dl>                         | Das übergeordnete Image der virtuellen Festplatte, auf das dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, ist als schreibgeschützt markiert.<br/>                                                                                             |
| <dl> <dt>**VM \_ \_E \_ ÜBERGEORDNETER PFAD \_ NICHT \_ GEFUNDEN**</dt> <dt>0xA0040677</dt> </dl>                 | Das übergeordnete Element der virtuellen Festplatte, auf die dieses [**IVMHardDisk-Objekt**](ivmharddisk.md) verweist, ist nicht vorhanden.<br/>                                                                                                       |
| <dl> <dt>**VM \_ HERUNTERFAHREN \_ \_ DER \_ E-APP**</dt> <dt>0xA0040209</dt> </dl>                      | Das image der virtuellen Festplatte kann nicht zusammengeführt werden, da die Anwendung heruntergefahren wird.<br/>                                                                                                                                 |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMHardDisk**](ivmharddisk.md)
</dt> </dl>

 

