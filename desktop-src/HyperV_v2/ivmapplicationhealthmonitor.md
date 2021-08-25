---
description: Meldet den Integritätsstatus einer Anwendung, die auf einem virtuellen Computer ausgeführt wird, an die Hyper-V-Integrationskomponenten, die auf demselben virtuellen Computer ausgeführt werden.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: IVmApplicationHealthMonitor-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 3cc565c43fd61ebed6183cbfa2f4fdf7ece7d39872f23718fb1a12a3b591d531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694320"
---
# <a name="ivmapplicationhealthmonitor-interface"></a>IVmApplicationHealthMonitor-Schnittstelle

Meldet den Integritätsstatus einer Anwendung, die auf einem virtuellen Computer ausgeführt wird, an die Hyper-V-Integrationskomponenten, die auf demselben virtuellen Computer ausgeführt werden. Der Status der Anwendungen, die auf dem virtuellen Computer ausgeführt werden, wird im **OperationalStatus** \[ 1-Eigenschaftswert \] der [**Msvm \_ HeartbeatComponent-Klasse widergespiegelt.**](msvm-heartbeatcomponent.md) Diese Schnittstelle bietet auch eine Möglichkeit, den gesamten in Hyper-V gesammelten Anwendungszustand zurückzusetzen.

Diese Schnittstelle wird von den Windows 8 Hyper-V-Integrationskomponenten implementiert. Eine Instanz dieser Schnittstelle wird durch Erstellen einer Instanz der CLSID **397a2e5f-348c-482d-b9a3-57d383b483cd** abgerufen.

## <a name="members"></a>Member

Die **IVmApplicationHealthMonitor-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVmApplicationHealthMonitor** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IVmApplicationHealthMonitor-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                   | Beschreibung                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ResetAllApplicationState**](ivmapplicationhealthmonitor-resetallapplicationstate.md) | Setzt den Integritätsstatus für alle Anwendungen auf einem virtuellen Computer zurück.<br/>            |
| [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)           | Legt den Integritätsstatus einer Anwendung fest, die auf einem virtuellen Computer ausgeführt wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Um dieses Programmierelement zu verwenden, müssen die Windows 8 Integrationskomponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                                                                                                     |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                                                                                           |
| Version<br/>                  | Integrationskomponenten für Windows 8<br/>                                                                                                                                |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl>                                                                      |
| IID<br/>                      | IID \_ IVmApplicationHealthMonitor ist als 267a0284-848f-447e-a096-5e10a1a76bca definiert.<br/> Der Objektbezeichner ist als 397a2e5f-348c-482d-b9a3-57d383b483cd definiert.<br/> |



 

