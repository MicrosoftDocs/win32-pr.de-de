---
title: Ivmguestos-suitemask-Eigenschaft (vpccominterfaces. h)
description: Ruft den suitemask des Gast Betriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- Suitemask-Eigenschaft virtueller PC
- Suitemask-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, suitemask-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743592"
---
# <a name="ivmguestossuitemask-property"></a>Ivmguestos:: suitemask-Eigenschaft

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft den suitemask des Gast Betriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Sammlungs Maske. Die folgenden Zeichen folgen Werte werden unterstützt.



| Wert                                                                                   | Bedeutung                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x00000004</dt> </dl> | Microsoft BackOffice-Komponenten werden installiert.<br/>                                                                                                              |
| <dl> <dt>"0x00000400"</dt> </dl> | Windows Server 2003, Web Edition ist installiert.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows Server 2003, Compute Cluster Edition ist installiert.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition oder Windows 2000 Datacenter Server ist installiert.<br/> |
| <dl> <dt>0x00000002</dt> </dl> | Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition oder Windows 2000 Advanced Server ist installiert.<br/>   |
| <dl> <dt>0x00000040</dt> </dl> | Windows XP Embedded ist installiert.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Windows Vista Home Premium, Windows Vista Home Basic oder Windows XP Home Edition ist installiert.<br/>                                                              |
| <dl> <dt>0x00000100</dt> </dl> | Remotedesktop wird unterstützt, es wird jedoch nur eine interaktive Sitzung unterstützt.<br/>                                                                                 |
| <dl> <dt>0x00000001</dt> </dl> | Microsoft Small Business Server wurde auf dem System installiert, kann jedoch auf eine andere Version von Windows aktualisiert werden.<br/>                                 |
| <dl> <dt>0x00000020</dt> </dl> | Microsoft Small Business Server wird mit der eingeschränkten Client Lizenz in Kraft installiert.<br/>                                                                  |
| <dl> <dt>0x00002000</dt> </dl> | Windows Storage Server 2003 R2 oder Windows Storage Server 2003 ist installiert.<br/>                                                                                 |
| <dl> <dt>0x00000010</dt> </dl> | Remotedesktopdienste ist installiert. Dieser Wert ist immer festgelegt.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Windows Home Server ist installiert.<br/>                                                                                                                           |



 

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                        |
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                            | Der-Parameter ist **null**.<br/>                           |
| <dl> <dt>VM \_ E \_ - \_ VM \_ führt</dt> <dt>0xa0040206</dt> nicht aus </dl>               | Der virtuelle Computer wird nicht ausgeführt.<br/>                               |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ - \_ Funktion \_ nicht</dt> " <dt>uxa0040505</dt> " </dl> | Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmguestos ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ivmguestos**](ivmguestos.md)
</dt> </dl>

 

