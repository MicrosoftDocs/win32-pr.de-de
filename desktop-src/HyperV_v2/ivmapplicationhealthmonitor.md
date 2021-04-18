---
description: Meldet den Integritäts Status einer Anwendung, die auf einem virtuellen Computer ausgeführt wird, an die Hyper-V-Integrations Komponenten, die auf demselben virtuellen Computer ausgeführt werden.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Ivmapplicationhealthmonitor-Schnittstelle
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
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354595"
---
# <a name="ivmapplicationhealthmonitor-interface"></a>Ivmapplicationhealthmonitor-Schnittstelle

Meldet den Integritäts Status einer Anwendung, die auf einem virtuellen Computer ausgeführt wird, an die Hyper-V-Integrations Komponenten, die auf demselben virtuellen Computer ausgeführt werden. Der Status der Anwendungen, die auf dem virtuellen Computer ausgeführt werden, wird im Eigenschafts Wert **OperationalStatus** \[ 1 \] der [**MSVM-Klasse \_ heartbeatcomponent**](msvm-heartbeatcomponent.md) widergespiegelt. Diese Schnittstelle bietet auch eine Möglichkeit zum Zurücksetzen des gesamten Anwendungs Zustands, der in Hyper-V akkumuliert wurde.

Diese Schnittstelle wird von den Hyper-V-Integrations Komponenten von Windows 8 implementiert. Eine Instanz dieser Schnittstelle wird abgerufen, indem eine Instanz der **397a2e5f -348c-482d-b9a3-57d383b483cd** CLSID erstellt wird.

## <a name="members"></a>Member

Die **ivmapplicationhealthmonitor** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmapplicationhealthmonitor** verfügt auch über die folgenden Typen von Mitgliedern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ivmapplicationhealthmonitor** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**Resetallapplicationstate**](ivmapplicationhealthmonitor-resetallapplicationstate.md) | Setzt den Integritäts Status aller Anwendungen auf einem virtuellen Computer zurück.<br/>            |
| [**"Standort Status"**](ivmapplicationhealthmonitor-setapplicationstate.md)           | Legt den Integritäts Status einer Anwendung fest, die auf einem virtuellen Computer ausgeführt wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um dieses Programmier Element zu verwenden, müssen die Windows 8-Integrations Komponenten auf dem virtuellen Computer installiert sein, auf dem die Anwendung ausgeführt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                                                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                                                                                           |
| Version<br/>                  | Integrations Komponenten für Windows 8<br/>                                                                                                                                |
| IDL<br/>                      | <dl> <dt>Vmapplicationhealthmonitor. idl</dt> </dl>                                                                      |
| IID<br/>                      | IID \_ ivmapplicationhealthmonitor ist als 267a0284-848f -447e-A096-5e10a1a76bca definiert.<br/> Der Objekt Bezeichner ist als 397a2e5f -348c-482d-b9a3-57d383b483cd definiert.<br/> |



 

