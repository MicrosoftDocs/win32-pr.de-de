---
title: Ivmguestos integrationcomponentsversion-Eigenschaft (vpccominterfaces. h)
description: Ruft die Version der Integrations Komponenten ab, die im Gast Betriebssystem installiert sind.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- Integrationcomponentsversion-Eigenschaft virtueller PC
- Integrationcomponentsversion-Eigenschaft Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, integrationcomponentsversion (Eigenschaft)
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
ms.openlocfilehash: f85352614b89ab208377fe44fe3b970c693d60dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740168"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a>Ivmguestos:: integrationcomponentsversion (Eigenschaft)

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft die Version der Integrations Komponenten ab, die im Gast Betriebssystem installiert sind.

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
| <dl> <dt>E \_ Zeiger</dt> <dt>0x80004003</dt> </dl>                   | Der-Parameter ist **null**.<br/>                                                        |
| <dl> <dt>VM \_ E \_ VM \_ unbekannt</dt> <dt>0xa0040207</dt> </dl>           | Der virtuelle Computer (VM) wurde nicht gefunden.<br/>                                      |
| <dl> <dt>VM \_ E- \_ Ergänzungen \_ nicht in \_ Anspruch</dt> nehmen <dt>0xa0040504</dt> </dl> | Integrations Komponenten sind auf diesem virtuellen Computer nicht installiert, oder der virtuelle Computer wurde nie gestartet.<br/> |
| <dl> <dt>DISP \_ E- \_ Ausnahme</dt> <dt>0x80020009</dt> </dl>           | Ein unerwarteter Fehler ist aufgetreten.<br/>                                                 |



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

 

