---
title: IVMDVDDrive ImageFile-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft den vollständigen Pfad des Imagedateisets für dieses Gerät ab.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- ImageFile-Eigenschaft Virtueller PC
- ImageFile-Eigenschaft Virtueller PC, IVMDVDDrive-Schnittstelle
- IVMDVDDrive-Schnittstelle Virtueller PC, ImageFile-Eigenschaft
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
ms.openlocfilehash: 275826aaea8dcb4f40427f2448a5edc86a992aefa4dc81648703a5f0a2948604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123755"
---
# <a name="ivmdvddriveimagefile-property"></a>IVMDVDDrive::ImageFile (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft den vollständigen Pfad des Imagedateisets für dieses Gerät ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a>Eigenschaftswert

Der vollständige Pfad zur Imagedatei.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                            | Bedeutung                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                               | Der Vorgang wurde durchgeführt.<br/>                                  |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                 | Der Parameter ist **NULL.**<br/>                                     |
| <dl> <dt>E \_ FEHLER</dt> <dt>0x80004005</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                              |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>         | Der virtuelle Computer wurde nicht gefunden.<br/>                        |
| <dl> <dt>VM \_ E \_ DRIVE \_ INVALID</dt> <dt>0xA0040502</dt> </dl>      | Der Busstandort für dieses Laufwerk ist ungültig.<br/>                  |
| <dl> <dt>VM \_ E \_ MEDIA WRONG TYPE \_ \_ 0XA00400728</dt> <dt></dt> </dl> | Das von diesem DVD-Laufwerk erfasste Medium ist keine ISO-Imagedatei.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>         | Ein unerwarteter Fehler ist aufgetreten.<br/>                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive ist als b96328f6-6732-437d-a00d-ffa47e43971c definiert.<br/>                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

