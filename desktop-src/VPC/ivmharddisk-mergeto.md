---
title: Ivmharddisk mergeto-Methode (vpccominterfaces. h)
description: Führt eine differenzierende virtuelle Festplatte mit allen übergeordneten Elementen zusammen.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Mergeto-Methode virtueller PC
- Mergeto-Methode Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, mergeto-Methode
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103965"
---
# <a name="ivmharddiskmergeto-method"></a>Ivmharddisk:: mergeto-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Führt eine differenzierende virtuelle Festplatte mit allen übergeordneten Elementen (bis einschließlich der übergeordneten virtuellen Festplatte) einer neuen Festplatten Datei zusammen.

## <a name="syntax"></a>Syntax


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newdiskimagepath* \[ in\]
</dt> <dd>

Der Pfad zum neuen Ziel Datenträger Image, in dem die ausgewählten Datenträger Images zusammengeführt werden.

</dd> <dt>

*newdiskimagetype* \[ in\]
</dt> <dd>

Der Typ des neuen Ziel datenträgerbilds. Die für das neue Ziel Datenträgerabbild zulässigen Abbild Typen sind " **vmdisktype \_ Dynamic** " und " **vmdisktype \_ FixedSize**". Weitere Informationen finden Sie unter [**vmharddisktype**](vmharddisktype.md).

</dd> <dt>

*mergetask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss des Zusammenführungs Vorgangs zu verfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                                                                                                                                                                                      |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                      | Ein Parameter ist **null**.<br/>                                                                                                                                                                                                                                                                           |
| <dl> <dt>**E \_ InvalidArg**</dt> <dt>0x80000003</dt> </dl>                                   | Der *newdiskimagepath* -Parameter ist leer.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt> </dl>   | Das System kann die durch den Parameter " *newdiskimagepath* " angegebene Datei nicht finden.<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Fehler \_ Pfad \_ nicht \_ gefunden)**</dt> <dt>0x80070003</dt> </dl>   | Das System kann den durch den *newdiskimagepath* -Parameter angegebenen Pfad nicht finden.<br/>                                                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ Von \_ Win32 ( \_ ungültiger \_ Name)**</dt> <dt>0x8007007b</dt> </dl>      | Der *newdiskimagepath* -Parameter enthält ein ungültiges Zeichen (eines der folgenden Zeichen: " \* ? <>/ \| ": ").<br/>                                                                                                                                                                                         |
| <dl> <dt>**HRESULT \_ FROM \_ Win32 (Error ungültiger \_ \_ Pfadname)**</dt> <dt>0x800700a1</dt> </dl>      | Der *newdiskimagepath* -Parameter gibt einen leeren oder relativen Pfad an. Ein absoluter Pfad ist erforderlich.<br/>                                                                                                                                                                                                |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Puffer \_ Überlauf)**</dt> <dt>0x8007006f</dt> </dl>   | Der durch den *newdiskimagepath* -Parameter angegebene Pfad ist zu lang. Der Pfad muss weniger als 260 Zeichen umfassen.<br/>                                                                                                                                                                                     |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt> </dl> | Entweder wird die virtuelle Festplatte verwendet, auf die von diesem Objekt verwiesen wird, oder das übergeordnete Element dieser virtuellen Festplatte wird verwendet.<br/>                                                                                                                                                                                |
| <dl> <dt>**VM \_ E \_ falscher \_ HD \_ - \_ Abbildtyp**</dt> <dt>0xa004067b</dt> </dl>                   | Dieser Fehler ist darauf zurückzuführen, dass es sich bei dem virtuellen Festplatten Image, auf das dieses [**ivmharddisk**](ivmharddisk.md) -Objekt verweist, nicht um ein differenzierender Datenträger Image handelt oder weil der *newdiskimagetype* -Parameter nicht zu den zulässigen Werten, **vmdisktype \_ Dynamic** oder **vmdisktype \_ FixedSize** gehört.<br/> |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ bereits \_ vorhanden)**</dt> <dt>0x800700b7</dt> </dl>    | Die Datei, auf die der *newdiskimagepath* -Parameter verweist, ist bereits vorhanden.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt> </dl>         | Auf dem Host Volume ist nicht genügend Speicherplatz vorhanden, um diese virtuelle Festplatte zusammenzuführen.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**VM \_ E über \_ geordneter \_ Pfad \_ nicht \_ gefunden**</dt> <dt>0xa0040677</dt> </dl>                 | Das übergeordnete Element der virtuellen Festplatte, auf die von diesem Objekt verwiesen wird, ist nicht vorhanden.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt> </dl>                      | Das virtuelle Festplatten Abbild kann nicht zusammengeführt werden, da die Anwendung heruntergefahren wird.<br/>                                                                                                                                                                                                             |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                                                                                                                                                                                  |



 

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

 

