---
title: Undvtaskplugin-Schnittstelle
description: Die Schnittstelle "iridvtaskplugin" wird von einem Task-Agent für virtuelle Computer Updates implementiert, damit der Task-Agent Systemupdates für einen virtuellen Computer verwalten kann.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Undvtaskplugin-Schnittstelle Remotedesktopdienste
- Undvtaskplugin-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957153"
---
# <a name="irdvtaskplugin-interface"></a>Undvtaskplugin-Schnittstelle

Die Schnittstelle " **iridvtaskplugin** " wird von einem *Task-Agent* für virtuelle Computer Updates implementiert, damit der Task-Agent Systemupdates für einen virtuellen Computer verwalten kann. Diese Schnittstelle wird vom- *Agent* verwendet, der vom Host System implementiert wird.

## <a name="members"></a>Member

Die Schnittstelle " **iridvtaskplugin** " erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. " **Iridvtaskplugin** " verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Schnittstelle " **iridvtaskplugin** " verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [**Initialisieren**](irdvtaskplugin-initialize.md) | Wird aufgerufen, um den Task-Agent zu initialisieren.<br/>                    |
| [**StartTask**](irdvtaskplugin-starttask.md)   | Wird aufgerufen, um den Aktualisierungs Task auf dem virtuellen Computer zu starten.<br/> |
| [**Terminate**](irdvtaskplugin-terminate.md)   | Wird aufgerufen, wenn der Task-Agent heruntergefahren wird.<br/>          |



 

### <a name="properties"></a>Eigenschaften

Die Schnittstelle " **iridvtaskplugin** " verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp          | BESCHREIBUNG                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [**PluginName**](irdvtaskplugin-pluginname.md)<br/> | Schreibgeschützt<br/> | Enthält den anzeigen amen des Task-Agents.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Task-Agent wird auf dem virtuellen Computer ausgeführt, wenn der virtuelle Computer für ein System Update geplant ist. Der Task-Agent aktualisiert die virtuelle Maschine, wenn die [**Starttask**](irdvtaskplugin-starttask.md) -Methode aufgerufen wird.

Fügen Sie der Registrierung des virtuellen Computers den folgenden Schlüssel hinzu, um den Task-Agent zu registrieren:

**HKEY \_ Lokale \_ Computer** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\ **Task** \\ **Plugins** \\ **taskagentname**

Fügen Sie unter diesem Registrierungsschlüssel die folgenden Werte hinzu:



| Name                     | type                      | BESCHREIBUNG                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **CLSID**<br/>     | **REG- \_ SZ**<br/>    | Eine Zeichenfolge, die die **CLSID** des Task-Agents darstellt.<br/>          |
| **IsEnabled**<br/> | **REG \_ DWORD**<br/> | 0, wenn der Task-Agent deaktiviert ist, oder 1, wenn der Task-Agent aktiviert ist.<br/> |



 

> [!Note]  
> Es können mehr als ein Task-Agent registriert werden, es wird jedoch nur ein Task-Agent verwendet. Wenn mehr als ein Task-Agent aktiviert ist, wird nur der erste gefundene verwendet.

 

Diese Schnittstelle wird zwar von den in den folgenden Anforderungen identifizierten Betriebssystemen unterstützt, Sie wird jedoch nur verwendet, wenn der virtuelle Computer unter Windows Server 2012 gehostet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



 

