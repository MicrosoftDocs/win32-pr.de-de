---
title: Ivmharddisk sizone Guest-Eigenschaft (vpccominterfaces. h)
description: Ruft die Größe der virtuellen Festplatte im Gast Betriebssystem ab.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- Sizone Guest-Eigenschaft virtueller PC
- Sizeingeguest-Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, sizone Guest (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104918"
---
# <a name="ivmharddisksizeinguest-property"></a>Ivmharddisk:: sizone Guest-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Größe der virtuellen Festplatte im Gast Betriebssystem ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Größe (in Bytes) des Festplatten Abbilds. Dieser Wert ist eine **Variante** vom Typ VT \_ Decimal.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                  |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                                    | Der-Parameter ist **null**.<br/>                                                     |
| <dl> <dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt> </dl> | Die aktuelle Datei der virtuellen Festplatte konnte nicht gefunden werden.<br/>                         |
| <dl> <dt>VM \_ E \_ HD- \_ Abbild \_ Öffnen \_ fehlschlagen</dt> <dt>0xa004067c</dt> </dl>                  | Fehler beim Öffnen der aktuellen Festplatten Abbild Datei.<br/>   |
| <dl> <dt>VM \_ E \_ HD- \_ Abbild \_ Zugriff</dt> <dt>0xa0040681</dt> </dl>                      | Fehler beim Zugriff auf die aktuelle Festplatten Abbild Datei.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                              |



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

 

