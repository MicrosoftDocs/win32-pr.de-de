---
title: Bearbeiten von Arbeits Elementen
description: Die ischeduledworkitem-Schnittstelle stellt Methoden zum Abrufen und Festlegen von Arbeits Element Eigenschaften bereit. Erstellen, abrufen und Löschen von Triggern für Arbeitselemente (das Festlegen des Triggers muss mit der itasktrigger-settrigger-Methode erfolgen); und zum Ausführen, beenden und Löschen des Arbeits Elements. Beachten Sie für die Eigenschaften eines bestimmten Arbeits Elementtyps die-Schnittstelle für diesen Objekttyp. Beispielsweise können Sie die Prioritätsstufe eines Arbeits Elements nicht festlegen. Sie können jedoch die Methoden der ITask-Schnittstelle verwenden, um die Priorität einer Aufgabe abzurufen und festzulegen.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- Arbeitselemente Taskplaner, verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728545"
---
# <a name="manipulating-work-items"></a>Bearbeiten von Arbeits Elementen

Die [**ischeduledworkitem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) -Schnittstelle stellt Methoden zum Abrufen und Festlegen von Arbeits Element Eigenschaften bereit. Erstellen, abrufen und Löschen von Triggern für Arbeitselemente (das Festlegen des Triggers muss mit der [**itasktrigger:: settrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) -Methode erfolgen); und zum Ausführen, beenden und Löschen des Arbeits Elements.

> [!Note]  
> Informationen zu den Eigenschaften eines bestimmten Arbeits Elementtyps finden Sie in der-Schnittstelle für diesen Objekttyp. Beispielsweise können Sie die Prioritätsstufe eines Arbeits Elements nicht festlegen. Sie können jedoch die Methoden der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle verwenden, um die Priorität einer Aufgabe abzurufen und festzulegen.

 

Wenn Sie ein Arbeits Element ändern, müssen Sie das Objekt [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) abrufen, um das geänderte Arbeits Element auf dem Datenträger zu speichern. Die Schnittstelle [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) ist eine Standard-COM-Schnittstelle, die von der [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle unterstützt wird.

| Beispiele für                                                            | Siehe                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Abrufen von Eigenschaften, die für alle Typen von Arbeits Elementen gelten                | [Abrufen von Beispielen für Arbeits Element Eigenschaften](retrieving-work-item-property-examples.md) |
| Festlegen von Eigenschaften, die für alle Typen von Arbeits Elementen gelten                   | [Festlegen von Beispielen für Arbeits Element Eigenschaften](setting-work-item-property-examples.md)       |
| Ausführen einer bekannten Aufgabe                                                       | [Beispiel für das Starten einer Aufgabe](starting-a-task-example.md)                               |
| Beenden einer laufenden Aufgabe                                                 | [Beispiel für das Beenden einer Aufgabe](terminating-a-task-example.md)                         |
| Erstellen eines neuen-Auslösers für eine bekannte Aufgabe                                    | [Erstellen eines neuen-Auslösers](creating-a-new-trigger.md)                                 |
| Erstellen eines ereignisbasierten Leerlauf-Auslösers für eine bekannte Aufgabe                      | [Erstellen eines Beispiels für einen Leerlauf-Timeout](creating-an-idle-trigger-example.md)             |
| Abrufen der triggerzeichenfolge aller Trigger, die einer bekannten Aufgabe zugeordnet sind | [Beispiel für das Abrufen von Beispiel Zeichen folgen](retrieving-trigger-strings-example.md)         |



 

 

 