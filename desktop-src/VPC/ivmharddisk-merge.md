---
title: Ivmharddisk-Merge-Methode (vpccominterfaces. h)
description: Führt eine differenzierende virtuelle Festplatte mit dem übergeordneten Datenträger Image zusammen.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Merge-Methode Virtual PC
- Merge-Methode Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Merge-Methode
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
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956662"
---
# <a name="ivmharddiskmerge-method"></a>Ivmharddisk:: Merge-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Führt eine differenzierende virtuelle Festplatte mit dem übergeordneten Datenträger Image zusammen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mergetask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss des Zusammenführungs Vorgangs zu verfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                          |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                      | Der-Parameter ist **null**.<br/>                                                                                                                                                                                             |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt> </dl> | Das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt referenzierte virtuelle Festplatten Abbild wird verwendet, oder das übergeordnete Element dieses virtuellen Festplatten Abbilds wird verwendet. Oder die Festplatten Abbilder können Teil eines gespeicherten Zustands sein.<br/> |
| <dl> <dt>**VM \_ E \_ falscher \_ HD \_ - \_ Abbildtyp**</dt> <dt>0xa004067b</dt> </dl>                   | Das Image der virtuellen Festplatte, auf das dieses [**ivmharddisk**](ivmharddisk.md) -Objekt verweist, muss ein differenzierender Datenträger Abbild sein.<br/>                                                                                            |
| <dl> <dt>**VM \_ E \_ - \_ Datei \_**</dt> schreibgeschützt <dt>0xa004067a</dt> </dl>                         | Das übergeordnete Element des virtuellen Festplatten Abbilds, auf das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt verwiesen wird, ist schreibgeschützt.<br/>                                                                                             |
| <dl> <dt>**VM \_ E über \_ geordneter \_ Pfad \_ nicht \_ gefunden**</dt> <dt>0xa0040677</dt> </dl>                 | Das übergeordnete Element der virtuellen Festplatte, auf die von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt verwiesen wird, ist nicht vorhanden.<br/>                                                                                                       |
| <dl> <dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt> </dl>                      | Das virtuelle Festplatten Abbild kann nicht zusammengeführt werden, da die Anwendung heruntergefahren wird.<br/>                                                                                                                                 |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmharddisk ist als ffa14ae6-48f5-42a4-8a22-186f2e5c7db0 definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmharddisk**](ivmharddisk.md)
</dt> </dl>

 

