---
title: Erstellen einer Aufgabe mit NewWorkItem-Beispiel
description: Wenn Sie einen Task erstellen, verwenden Sie die beiden Taskplaner-Schnittstellen itaskscheduler und ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- Erstellen von Arbeits Elementen Taskplaner
- Arbeitselemente Taskplaner, Erstellen von Aufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315819"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Erstellen einer Aufgabe mit NewWorkItem-Beispiel

Beim Erstellen einer Aufgabe verwenden Sie zwei Taskplaner Schnittstellen: [**itaskscheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) und [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). Sie müssen einen eindeutigen Namen für den Task, den Klassen Bezeichner des Task-Objekts und den Schnittstellen Bezeichner " **ITask**" angeben. Der Klassen Bezeichner und der Schnittstellen Bezeichner werden im folgenden Codebeispiel gezeigt:

> [!Note]  
> Sie können auch einen Task erstellen, indem Sie [**itaskscheduler:: addworkitem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem)aufrufen. Wenn Sie diese Route verwenden, liegt es in ihrer Verantwortung, eine Instanz des **Task** -Objekts (das die [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle unterstützt) zu erstellen und dann die Aufgabe mit dem Namen hinzuzufügen, den Sie angeben.

 

> [!Note]  
> Standardmäßig können nur Mitglieder der Gruppe "Administratoren", "Sicherungs-Operatoren" oder "Server Operatoren" auf Windows Server 2003 Aufgaben erstellen. Ein Mitglied der Gruppe "Administratoren" kann die Sicherheits Beschreibung des Windows- \\ Task Ordners ändern, damit andere Aufgaben erstellen können.

 

Der Name, den Sie für die Aufgabe angeben, muss innerhalb des Ordners für geplante Aufgaben eindeutig sein. Wenn bereits eine Aufgabe mit dem gleichen Namen vorhanden ist, gibt [**itaskscheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) eine Fehler \_ Datei \_ vorhanden. Wenn Sie diesen Rückgabewert erhalten, geben Sie einen anderen Namen an, und versuchen Sie erneut, die Aufgabe zu erstellen.

Im folgenden Verfahren wird beschrieben, wie eine neue Arbeits Element Aufgabe erstellt wird.

**So erstellen Sie eine neue Arbeits Element Aufgabe**

1.  Aufrufen von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) zum Initialisieren der com-Bibliothek und von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) zum Abrufen eines Taskplaner Objekts. (In diesem Beispiel wird davon ausgegangen, dass der Taskplaner-Dienst ausgeführt wird.)
2.  Rufen Sie [**itaskscheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) auf, um eine neue Aufgabe zu erstellen. (Diese Methode gibt einen Zeiger auf eine [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) -Schnittstelle zurück.)
3.  Speichern Sie die neue Aufgabe auf einem Datenträger, indem Sie [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)aufrufen. (Die [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle ist eine von der **ITask** -Schnittstelle unterstützte Standard-COM-Schnittstelle.)
4.  Wenden Sie **ITask:: Release** an, um alle Ressourcen freizugeben. (Beachten Sie, dass [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) eine [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Methode ist, die von [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)geerbt wird.)



| Ein Codebeispiel für  | Siehe                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Erstellen einer einzelnen Aufgabe | [C/C++-Code Beispiel: Erstellen einer Aufgabe mit NewWorkItem](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Taskplaner 1,0-Beispiele](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 