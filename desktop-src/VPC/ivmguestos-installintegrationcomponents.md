---
title: Ivmguestos installintegrationcomponents-Methode (vpccominterfaces. h)
description: Hiermit werden die aktuellen Integrations Komponenten in das Gast Betriebssystem eingecheckt und installiert.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- Installintegrationcomponents-Methode Virtual PC
- Installintegrationcomponents-Methode Virtual PC, ivmguestos-Schnittstelle
- Ivmguestos Interface Virtual PC, installintegrationcomponents-Methode
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879ded1464ebd310e1d1da4e3a952dc086600350
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391556"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a>Ivmguestos:: installintegrationcomponents-Methode

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Hiermit werden die aktuellen Integrations Komponenten in das Gast Betriebssystem eingecheckt und installiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                               |
| <dl> <dt>**VM \_ E \_ - \_ VM \_ führt**</dt> <dt>0xa0040206</dt> nicht aus </dl>                       | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>                     |
| <dl> <dt>**VM \_ E \_ VM \_ unbekannt**</dt> <dt>0xa0040207</dt> </dl>                            | Der virtuelle Computer wurde nicht gefunden.<br/>                                     |
| <dl> <dt>**VM \_ E \_ Laufwerk \_ ungültige**</dt> <dt>0xa0040502</dt> </dl>                         | Der virtuelle Computer verfügt über kein leeres DVD-Laufwerk.<br/>                       |
| <dl> <dt>**VM \_ E-of-Media-Bereitstellung \_ \_ \_ fehl**</dt> geschlagen <dt>0xa0040508</dt> </dl>                   | Fehler beim Versuch, die Bereitstellung des Mediums auf dem DVD-Laufwerk des virtuellen Computers aufzunehmen.<br/> |
| <dl> <dt>**DISP \_ E- \_ Ausnahme**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                           |
| <dl> <dt>**HRESULT \_ Von \_ Win32 (Fehler \_ Datei \_ nicht \_ gefunden)**</dt> <dt>0x80070002</dt> </dl> | Das System kann die ISO-Datei für die Integrations Komponenten nicht finden.<br/>         |



 

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

 

