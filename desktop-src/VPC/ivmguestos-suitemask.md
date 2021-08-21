---
title: IVMGuestOS SuiteMask-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die SuiteMask des Gastbetriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- SuiteMask-Eigenschaft Virtueller PC
- SuiteMask-Eigenschaft Virtueller PC, IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC, SuiteMask (Eigenschaft)
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
ms.openlocfilehash: 22075c68ef30fda7360f25e76c84dbffbf7e306335a0ef20bda45559cb6dac09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472294"
---
# <a name="ivmguestossuitemask-property"></a>IVMGuestOS::SuiteMask (Eigenschaft)

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die SuiteMask des Gastbetriebssystems ab, das auf dem virtuellen Computer ausgeführt wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Suitemaske. Die folgenden Zeichenfolgenwerte werden unterstützt.



| Wert                                                                                   | Bedeutung                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"0x00000004"</dt> </dl> | Microsoft BackOffice-Komponenten werden installiert.<br/>                                                                                                              |
| <dl> <dt>"0x00000400"</dt> </dl> | Windows Server 2003, Web Edition ist installiert.<br/>                                                                                                              |
| <dl> <dt>"0x00004000"</dt> </dl> | Windows Server 2003, Compute Cluster Edition ist installiert.<br/>                                                                                                  |
| <dl> <dt>"0x00000080"</dt> </dl> | Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition oder Windows 2000 Datacenter Server ist installiert.<br/> |
| <dl> <dt>"0x00000002"</dt> </dl> | Windows Server 2008 R2 Enterprise ist Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition oder Windows 2000 Advanced Server installiert.<br/>   |
| <dl> <dt>"0x00000040"</dt> </dl> | Windows XP Embedded ist installiert.<br/>                                                                                                                           |
| <dl> <dt>"0x00000200"</dt> </dl> | Windows Vista Home Premium, Windows Vista Home Basic oder Windows XP Home Edition ist installiert.<br/>                                                              |
| <dl> <dt>"0x00000100"</dt> </dl> | Remotedesktop wird unterstützt, aber nur eine interaktive Sitzung wird unterstützt.<br/>                                                                                 |
| <dl> <dt>"0x00000001"</dt> </dl> | Microsoft Small Business Server wurde einmal auf dem System installiert, wurde aber möglicherweise auf eine andere Version von Windows.<br/>                                 |
| <dl> <dt>"0x00000020"</dt> </dl> | Microsoft Small Business Server wird mit der restriktiven Clientlizenz installiert.<br/>                                                                  |
| <dl> <dt>"0x00002000"</dt> </dl> | Windows Storage Server 2003 R2 oder Windows Storage Server 2003 ist installiert.<br/>                                                                                 |
| <dl> <dt>"0x00000010"</dt> </dl> | Remotedesktopdienste ist installiert. Dieser Wert wird immer festgelegt.<br/>                                                                                             |
| <dl> <dt>"0x00008000"</dt> </dl> | Windows Home Server ist installiert.<br/>                                                                                                                           |



 

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                                       | Bedeutung                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | Der Vorgang wurde durchgeführt.<br/>                        |
| <dl> <dt>E \_ ZEIGER 0X80004003</dt> <dt></dt> </dl>                            | Der Parameter ist **NULL.**<br/>                           |
| <dl> <dt>VM \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | Der virtuelle Computer wird nicht ausgeführt.<br/>                               |
| <dl> <dt>VM \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0XA0040505</dt> </dl> | Integrationskomponenten sind auf diesem virtuellen Computer nicht installiert.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ein unerwarteter Fehler ist aufgetreten.<br/>                    |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

