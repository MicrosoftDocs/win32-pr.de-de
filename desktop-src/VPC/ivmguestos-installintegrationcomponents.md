---
title: IVMGuestOS InstallIntegrationComponents-Methode (VPCCOMInterfaces.h)
description: Sucht und installiert die neuesten Integrationskomponenten im Gastbetriebssystem.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- InstallIntegrationComponents-Methode Virtueller PC
- InstallIntegrationComponents-Methode Virtual PC , IVMGuestOS-Schnittstelle
- IVMGuestOS-Schnittstelle Virtueller PC , InstallIntegrationComponents-Methode
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
ms.openlocfilehash: c61ade15736cec16976566f464573b30df7fd918f0f2be84f2f4ebd56e5db514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007190"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a>IVMGuestOS::InstallIntegrationComponents-Methode

\[Windows Der virtuelle PC ist ab Windows 8 nicht mehr für die Verwendung verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Sucht und installiert die neuesten Integrationskomponenten im Gastbetriebssystem.

## <a name="syntax"></a>Syntax


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode/-wert                                                                                                                                                                            | Beschreibung                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | Der Vorgang wurde durchgeführt.<br/>                                               |
| <dl> <dt>**VM \_ E \_ VM WIRD NICHT \_ \_ AUSGEFÜHRT,**</dt> <dt>0xA0040206</dt> </dl>                       | Der virtuelle Computer muss für diesen Vorgang ausgeführt werden.<br/>                     |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                            | Der virtuelle Computer wurde nicht gefunden.<br/>                                     |
| <dl> <dt>**VM \_ E \_ LAUFWERK \_ UNGÜLTIGE**</dt> <dt>0xA0040502</dt> </dl>                         | Der virtuelle Computer verfügt nicht über ein leeres DVD-Laufwerk.<br/>                       |
| <dl> <dt>**VM \_ E \_ MEDIA \_ UNMOUNT \_ FAIL**</dt> <dt>0xA0040508</dt> </dl>                   | Fehler beim Aufheben der Bereitstellung des Mediums vom VM-DVD-Laufwerk.<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                            | Ein unerwarteter Fehler ist aufgetreten.<br/>                                           |
| <dl> <dt>**HRESULT \_ FROM \_ WIN32(ERROR \_ FILE NOT \_ \_ FOUND)**</dt> <dt>0x80070002</dt> </dl> | Das System kann die ISO-Datei für die Integrationskomponenten nicht finden.<br/>         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS ist als 99fea0db-4880-499a-b6d8-73dff9bc91be definiert.<br/>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

