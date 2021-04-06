---
title: Undvtaskpluginnotifysink-Schnittstelle
description: Die Schnittstelle "" wird vom Task-Agent verwendet, um mit dem auslöseragent zu kommunizieren.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste
- Undvtaskpluginnotifysink-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742072"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>Undvtaskpluginnotifysink-Schnittstelle

Die **Schnittstelle** "" wird vom Task-Agent verwendet, um mit dem auslöseragent zu kommunizieren. Ein Zeiger auf diese Schnittstelle wird in der Methode " [**iridvtaskplugin:: Initialize**](irdvtaskplugin-initialize.md) " an den Task-Agent übermittelt.

## <a name="members"></a>Member

Die " **iridvtaskpluginnotifysink** "-Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. " **Iridvtaskpluginnotifysink** " verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die " **iridvtaskpluginnotifysink** "-Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | Wird vom Task-Agent aufgerufen, um einen geplanten Task zu löschen.<br/>                   |
| [**Ontaskstatechange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | Wird verwendet, um den Agent zu benachrichtigen, dass sich der Zustand einer Aufgabe geändert hat.<br/> |
| [**Onterminiert**](irdvtaskpluginnotifysink-onterminated.md)           | Wird vom Task-Agent aufgerufen, um anzufordern, dass der Task-Agent heruntergefahren wird.<br/>  |
| [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md)           | Wird vom Task-Agent zum Planen einer Aufgabe aufgerufen.<br/>                           |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wird zwar von den in den folgenden Anforderungen identifizierten Betriebssystemen unterstützt, Sie wird jedoch nur verwendet, wenn der virtuelle Computer unter Windows Server 2012 gehostet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 Enterprise<br/>   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/> |



 

