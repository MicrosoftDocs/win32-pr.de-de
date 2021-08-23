---
title: IVMGuestOS IntegrationComponentsVersion-Eigenschaft (VPCCOMInterfaces.h)
description: Ruft die Version der Integrationskomponenten ab, die im Gastbetriebssystem installiert sind.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- IntegrationComponentsVersion-Eigenschaft Virtueller PC
- IntegrationComponentsVersion-Eigenschaft Virtual PC , IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC , IntegrationComponentsVersion-Eigenschaft
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854cb86817f461085c72a437fa962649e50ab11b65a847d0756dc8e9c7b18177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999050"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a>IVMGuestOS::IntegrationComponentsVersion-Eigenschaft

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft die Version der Integrationskomponenten ab, die im Gastbetriebssystem installiert sind.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Version.

## <a name="error-codes"></a>Fehlercodes



| Name/Wert                                                                                                                                                              | Bedeutung                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | Der Vorgang wurde durchgeführt.<br/>                                                     |
| <dl> <dt>E \_ POINTER</dt> <dt>0x80004003</dt> </dl>                   | Der Parameter ist **NULL.**<br/>                                                        |
| <dl> <dt>VM \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>           | Der virtuelle Computer (VM) wurde nicht gefunden.<br/>                                      |
| <dl> <dt>VM \_ \_E ADDITIONEN \_ NICHT \_ VERFÜGBAR</dt> <dt>0xA0040504</dt> </dl> | Integrationskomponenten sind auf diesem virtuellen Computer nicht installiert, oder der virtuelle Computer wurde nie gestartet.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                 |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

