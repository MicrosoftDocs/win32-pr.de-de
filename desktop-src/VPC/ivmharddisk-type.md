---
title: Ivmharddisk-Typeigenschaft (vpccominterfaces. h)
description: Der Typ der virtuellen Festplatte.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Type-Eigenschaft Virtual PC
- Type-Eigenschaft Virtual PC, ivmharddisk-Schnittstelle
- Ivmharddisk Interface Virtual PC, Type-Eigenschaft
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040566"
---
# <a name="ivmharddisktype-property"></a>Ivmharddisk:: Type (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Typ der virtuellen Festplatte ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Typ des aktuellen Festplatten Bilds.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                               | Bedeutung                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                                  |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                                    | Der-Parameter ist **null**.<br/>                                                     |
| <dl> <dt>HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)</dt> <dt>0x80070002</dt> </dl> | Die aktuelle Festplatten Abbild Datei wurde nicht gefunden.<br/>                           |
| <dl> <dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt> </dl>                         | Der Typ des aktuellen Festplatten Abbilds ist ungültig.<br/>                            |
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

 

