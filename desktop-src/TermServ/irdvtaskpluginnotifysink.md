---
title: IRDVTaskPluginNotifySink-Schnittstelle
description: Die IRDVTaskPluginNotifySink-Schnittstelle wird vom Task-Agent für die Kommunikation mit dem Trigger-Agent verwendet.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- IRDVTaskPluginNotifySink-Schnittstelle Remotedesktopdienste
- IRDVTaskPluginNotifySink-Schnittstelle Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88692175fedbad4faf5b2755ce92897cff25fe9d588e6fb446d8174407aa6b5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072390"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>IRDVTaskPluginNotifySink-Schnittstelle

Die **IRDVTaskPluginNotifySink-Schnittstelle** wird vom Task-Agent für die Kommunikation mit dem Trigger-Agent verwendet. Ein Zeiger auf diese Schnittstelle wird an den Task-Agent in der [**IRDVTaskPlugin::Initialize-Methode**](irdvtaskplugin-initialize.md) übergeben.

## <a name="members"></a>Member

Die **IRDVTaskPluginNotifySink-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRDVTaskPluginNotifySink** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IRDVTaskPluginNotifySink-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | Wird vom Task-Agent aufgerufen, um einen geplanten Task zu löschen.<br/>                   |
| [**OnTaskStateChange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | Wird verwendet, um den Trigger-Agent zu benachrichtigen, dass sich der Status eines Tasks geändert hat.<br/> |
| [**Am Ende**](irdvtaskpluginnotifysink-onterminated.md)           | Wird vom Task-Agent aufgerufen, um anzufordern, dass der Task-Agent heruntergefahren wird.<br/>  |
| [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md)           | Wird vom Task-Agent aufgerufen, um eine Aufgabe zu planen.<br/>                           |



 

## <a name="remarks"></a>Hinweise

Obwohl diese Schnittstelle unter den in den unten aufgeführten Anforderungen angegebenen Betriebssystemen unterstützt wird, wird sie nur verwendet, wenn der virtuelle Computer auf Windows Server 2012 gehostet wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



 

