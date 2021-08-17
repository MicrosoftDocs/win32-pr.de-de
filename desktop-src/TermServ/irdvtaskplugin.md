---
title: IRDVTaskPlugin-Schnittstelle
description: Die IRDVTaskPlugin-Schnittstelle wird von einem Task-Agent für die Aktualisierung virtueller Computer implementiert, damit der Task-Agent Systemupdates für einen virtuellen Computer verwalten kann.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- IRDVTaskPlugin-Remotedesktopdienste
- IRDVTaskPlugin-Schnittstelle Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe76f0b0b92286d5a4b7db5126706fd55bdb6f580c11fda1dcaa55a47be4678c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129169"
---
# <a name="irdvtaskplugin-interface"></a>IRDVTaskPlugin-Schnittstelle

Die **IRDVTaskPlugin-Schnittstelle** wird von  einem Task-Agent für die Aktualisierung virtueller Computer implementiert, damit der Task-Agent Systemupdates für einen virtuellen Computer verwalten kann. Diese Schnittstelle wird vom *Trigger-Agent verwendet,* der vom Hostsystem implementiert wird.

## <a name="members"></a>Member

Die **IRDVTaskPlugin-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRDVTaskPlugin** verfügt auch über diese Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IRDVTaskPlugin-Schnittstelle** verfügt über diese Methoden.



| Methode                                          | Beschreibung                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [**Initialisieren**](irdvtaskplugin-initialize.md) | Wird aufgerufen, um den Task-Agent zu initialisieren.<br/>                    |
| [**StartTask**](irdvtaskplugin-starttask.md)   | Wird aufgerufen, um die Updateaufgabe auf dem virtuellen Computer zu starten.<br/> |
| [**Terminate**](irdvtaskplugin-terminate.md)   | Wird aufgerufen, wenn der Task-Agent heruntergefahren wird.<br/>          |



 

### <a name="properties"></a>Eigenschaften

Die **IRDVTaskPlugin-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp          | Beschreibung                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [**PluginName**](irdvtaskplugin-pluginname.md)<br/> | Schreibgeschützt<br/> | Enthält den Anzeigenamen des Task-Agents.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Task-Agent wird auf dem virtuellen Computer ausgeführt, wenn für diesen virtuellen Computer ein Systemupdate geplant ist. Der Task-Agent aktualisiert den virtuellen Computer, wenn die [**StartTask-Methode**](irdvtaskplugin-starttask.md) aufgerufen wird.

Um den Task-Agent zu registrieren, fügen Sie der Registrierung des virtuellen Computers den folgenden Schlüssel hinzu:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** Terminal \\ **Server** Task \\  \\ **Plugins** \\ **TaskAgentName**

Fügen Sie unter diesem Registrierungsschlüssel die folgenden Werte hinzu:



| Name                     | type                      | Beschreibung                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **Clsid**<br/>     | **REG \_ SZ**<br/>    | Eine Zeichenfolge, die die **CLSID** des Task-Agents darstellt.<br/>          |
| **IsEnabled**<br/> | **REG \_ DWORD**<br/> | 0, wenn der Task-Agent deaktiviert ist, oder 1, wenn der Task-Agent aktiviert ist.<br/> |



 

> [!Note]  
> Es können mehrere Task-Agents registriert werden, es wird jedoch nur ein Task-Agent verwendet. Wenn mehr als ein Task-Agent aktiviert ist, wird nur der erste gefundene verwendet.

 

Obwohl diese Schnittstelle unter den in den folgenden Anforderungen angegebenen Betriebssystemen unterstützt wird, wird sie nur verwendet, wenn der virtuelle Computer auf der Windows Server 2012.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



 

