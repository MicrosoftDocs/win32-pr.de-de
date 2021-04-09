---
title: Eigenschaften von ivmdvddrive ImageFile (vpccominterfaces. h)
description: Ruft den vollständigen Pfad der Bilddatei ab, die für dieses Gerät festgelegt ist.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- ImageFile-Eigenschaft virtueller PC
- ImageFile-Eigenschaft Virtual PC, ivmdvddrive-Schnittstelle
- Ivmdvddrive Interface Virtual PC, ImageFile-Eigenschaft
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859210"
---
# <a name="ivmdvddriveimagefile-property"></a>Ivmdvddrive:: ImageFile (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den vollständigen Pfad der Bilddatei ab, die für dieses Gerät festgelegt ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a>Eigenschaftswert

Der vollständige Pfad zur Bilddatei.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                            | Bedeutung                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | Der Vorgang wurde durchgeführt.<br/>                                  |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                 | Der-Parameter ist **null**.<br/>                                     |
| <dl> <dt>E \_ </dt> <dt>0x80004005</dt> fehlschlagen </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                              |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>         | Der virtuelle Computer wurde nicht gefunden.<br/>                        |
| <dl> <dt>VM \_ E \_ Laufwerk \_ ungültige</dt> <dt>0xa0040502</dt> </dl>      | Der Busstandort für dieses Laufwerk ist ungültig.<br/>                  |
| <dl> <dt>VM \_ E \_ Medien \_ falscher \_ Typ</dt> <dt>0xa00400728</dt> </dl> | Das von diesem DVD-Laufwerk erfasste Medium ist keine ISO-Abbild Datei.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>         | Ein unerwarteter Fehler ist aufgetreten.<br/>                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmdvddrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmdvddrive**](ivmdvddrive.md)
</dt> </dl>

 

