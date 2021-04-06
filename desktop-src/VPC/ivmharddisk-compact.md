---
title: Ivmharddisk Compact-Methode (vpccominterfaces. h)
description: Komprimiert eine dynamisch erweiterbare virtuelle Festplatten Abbild.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Compact-Methode Virtual PC
- Compact-Methode Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Compact-Methode
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743248"
---
# <a name="ivmharddiskcompact-method"></a>Ivmharddisk:: Compact-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Komprimiert eine dynamisch erweiterbare virtuelle Festplatten Abbild.

## <a name="syntax"></a>Syntax


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*kompakttask* \[ Out, retval\]
</dt> <dd>

Ein [**ivmtask**](ivmtask.md) -Objekt, das verwendet wird, um den Abschluss des Komprimierungsprozesses zu verfolgen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                    | Der Vorgang wurde durchgeführt.<br/>                                                                                                        |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                              | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                                                                    |
| <dl> <dt>**E \_ Zeiger**</dt> <dt>0x80004003</dt> </dl>                                      | Der-Parameter ist **null**.<br/>                                                                                                           |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Freigabe \_ Verletzung)**</dt> <dt>0x80070020</dt> </dl> | Das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt referenzierte virtuelle Festplatten Abbild wird verwendet.<br/>                                  |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ \_**</dt> Datenträger voll) <dt>0x80070070</dt> </dl>         | Auf dem Host Volume ist nicht genügend Speicherplatz vorhanden, um eine temporäre Datei zu erstellen, die für die Komprimierung dieses virtuellen Festplatten Abbilds erforderlich ist.<br/>     |
| <dl> <dt>**VM \_ E \_ App \_ \_ herunter**</dt> fahren <dt>0xa0040209</dt> </dl>                      | Das Image der virtuellen Festplatte kann nicht komprimiert werden, da die Anwendung heruntergefahren wird.<br/>                                            |
| <dl> <dt>**VM \_ E \_ - \_ Datei \_**</dt> schreibgeschützt <dt>0xa004067a</dt> </dl>                         | Das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt referenzierte virtuelle Festplatten Abbild ist als schreibgeschützt gekennzeichnet.<br/>                     |
| <dl> <dt>**VM \_ E \_ falscher \_ HD \_ - \_ Abbildtyp**</dt> <dt>0xa004067b</dt> </dl>                   | Das von diesem [**ivmharddisk**](ivmharddisk.md) -Objekt referenzierte virtuelle Festplatten Abbild muss ein **vmdisktypedynamic** -Bildtyp sein.<br/> |
| <dl> <dt>**VM \_ E \_ ungültige \_ HD- \_ Datei**</dt> <dt>0xa0040682</dt> </dl>                        | Das Image der virtuellen Festplatte, auf das dieses [**ivmharddisk**](ivmharddisk.md) -Objekt verweist, scheint kein gültiges Image zu sein.<br/>          |



 

## <a name="remarks"></a>Bemerkungen

Zum Komprimieren eines dynamisch erweiterbaren Festplatten Abbilds sollte der freie Speicherplatz auf dem Datenträger Abbild zuerst nulfiert werden.

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

 

