---
title: Ivmfloppydrive-Anlage Eigenschaft (vpccominterfaces. h)
description: Ruft den Medientyp ab, der mit dem Diskettenlaufwerk auf dem virtuellen Computer verbunden ist.
ms.assetid: 0b7e43ac-de56-4c4b-82e6-75877aea06f2
keywords:
- Anlage Eigenschaft virtueller PC
- Anlage Eigenschaft Virtual PC, ivmfloppydrive-Schnittstelle
- Ivmfloppydrive Interface Virtual PC, Anlage (Eigenschaft)
topic_type:
- apiref
api_name:
- IVMFloppyDrive.Attachment
- IVMFloppyDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44814148baf27672f30b8e3c5015d841aaaba4b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340339"
---
# <a name="ivmfloppydriveattachment-property"></a>Ivmfloppydrive:: Attachment-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den Medientyp ab, der an das Diskettenlaufwerk im virtuellen Computer (VM) angefügt ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Attachment(
  [out, retval] VMFloppyDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a>Eigenschaftswert

Der Medientyp. Eine Liste der Werte finden Sie unter [**vmfloppydriveattachmenttype**](vmfloppydriveattachmenttype.md).

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                    | Bedeutung                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | Der Vorgang wurde durchgeführt.<br/>                                  |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>         | Der-Parameter ist **null**.<br/>                                     |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl> | Die Konfiguration für diese VM ist ungültig oder wurde nicht gefunden.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl> | Ein unerwarteter Fehler ist aufgetreten.<br/>                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmfloppydrive ist als 661abee6-112a-4ed9-BABF -3c874969s10e definiert.<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmfloppydrive**](ivmfloppydrive.md)
</dt> </dl>

 

