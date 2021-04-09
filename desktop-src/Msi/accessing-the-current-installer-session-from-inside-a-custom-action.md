---
description: Nicht verzögerte benutzerdefinierte Aktionen, die Dynamic Link Libraries oder Skripts aufrufen, können auf eine laufende Installation zugreifen, um die Attribute der aktuellen Installationssitzung abzufragen oder zu ändern.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Zugreifen auf die aktuelle Installer-Sitzung innerhalb einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959555"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a><span data-ttu-id="4a416-103">Zugreifen auf die aktuelle Installer-Sitzung innerhalb einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="4a416-103">Accessing the Current Installer Session from Inside a Custom Action</span></span>

<span data-ttu-id="4a416-104">Nicht verzögerte benutzerdefinierte Aktionen, die [Dynamic Link Libraries](dynamic-link-libraries.md) oder [Skripts](scripts.md) aufrufen, können auf eine laufende Installation zugreifen, um die Attribute der aktuellen Installationssitzung abzufragen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4a416-104">Nondeferred custom actions that call [dynamic-link libraries](dynamic-link-libraries.md) or [scripts](scripts.md) may access a running installation to query or modify the attributes of the current installation session.</span></span> <span data-ttu-id="4a416-105">Nur ein **Sitzungs** Objekt kann für jeden Prozess vorhanden sein, und benutzerdefinierte Aktions Skripts dürfen nicht versuchen, eine weitere Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a416-105">Only one **Session** object can exist for each process, and custom action scripts must not attempt to create another session.</span></span>

<span data-ttu-id="4a416-106">Benutzerdefinierte Aktionen können nur temporäre Zeilen, Spalten oder Tabellen aus einer Datenbank hinzufügen, ändern oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="4a416-106">Custom actions can only add, modify, or remove temporary rows, columns, or tables from a database.</span></span> <span data-ttu-id="4a416-107">Benutzerdefinierte Aktionen können keine persistenten Daten in einer Datenbank ändern, z. b. Daten, die Teil der Datenbank sind, die auf dem Datenträger gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4a416-107">Custom actions cannot modify persistent data in a database, for example, data that is a part of the database stored on disk.</span></span>

[<span data-ttu-id="4a416-108">Dynamic Link Libraries</span><span class="sxs-lookup"><span data-stu-id="4a416-108">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)

<span data-ttu-id="4a416-109">Für den Zugriff auf eine ausgeführte Installation werden benutzerdefinierte Aktionen, die dll (Dynamic Link Libraries) aufrufen, als einziges Argument des msihandle-Typs für die aktuelle Sitzung als einziges Argument für den DLL-Einstiegspunkt, der in der Ziel Spalte der [Tabelle CustomAction](customaction-table.md)benannt ist</span><span class="sxs-lookup"><span data-stu-id="4a416-109">To access a running installation, custom actions that call dynamic-link libraries (DLL) are passed a handle of the type MSIHANDLE for the current session as the only argument to the DLL entry point named in the Target column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="4a416-110">Da das Installationsprogramm dieses Handle bereitstellt, sollte es von der benutzerdefinierten Aktion nicht geschlossen werden, um z. b. das Handle *hinstall* vom Installationsprogramm zu empfangen, wird die benutzerdefinierte Action-Funktion wie folgt deklariert.</span><span class="sxs-lookup"><span data-stu-id="4a416-110">Because the installer provides this handle, the custom action should not close it, for example, to receive the handle *hInstall* from the installer, the custom action function is declared as follows.</span></span>


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="4a416-111">Für den schreibgeschützten Zugriff auf die aktuelle Datenbank erhalten Sie das Daten Bank Handle durch Aufrufen von [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span><span class="sxs-lookup"><span data-stu-id="4a416-111">For read-only access to the current database obtain the database handle by calling [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span></span> <span data-ttu-id="4a416-112">Weitere Informationen finden Sie unter Abrufen [eines Daten Bank Handles](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="4a416-112">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

[<span data-ttu-id="4a416-113">Skripts</span><span class="sxs-lookup"><span data-stu-id="4a416-113">Scripts</span></span>](scripts.md)

<span data-ttu-id="4a416-114">In VBScript oder JScript geschriebene benutzerdefinierte Aktionen können mithilfe des [**Session-Objekts**](session-object.md)auf die aktuelle Installationssitzung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4a416-114">Custom actions written in VBScript or JScript can access the current installation session by using the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="4a416-115">Das Installationsprogramm erstellt ein **Sitzungs** Objekt mit dem Namen "Session", das auf die aktuelle Installation verweist.</span><span class="sxs-lookup"><span data-stu-id="4a416-115">The installer creates a **Session** object named "Session" that references the current installation.</span></span> <span data-ttu-id="4a416-116">Verwenden Sie für den schreibgeschützten Zugriff auf die aktuelle Datenbank die [**Database**](session-database.md) -Eigenschaft des **Session** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="4a416-116">For read-only access to the current database use the [**Database**](session-database.md) property of the **Session** object.</span></span>

<span data-ttu-id="4a416-117">Da ein Skript aus dem Kontext des [**Session**](session-object.md) -Objekts ausgeführt wird, ist es nicht immer erforderlich, Eigenschaften und Methoden vollständig zu qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="4a416-117">Because a script is run from the context of the [**Session**](session-object.md) object, it is not always necessary to fully qualify properties and methods.</span></span> <span data-ttu-id="4a416-118">Im folgenden Beispiel kann die Me-Referenz beim Verwenden von VBScript das **Session** -Objekt ersetzen, z. b. sind die folgenden drei Zeilen gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="4a416-118">In the following example, when using VBScript, the Me reference can replace the **Session** object, for example, the following three lines are equivalent.</span></span>


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[<span data-ttu-id="4a416-119">Ausführbare Dateien</span><span class="sxs-lookup"><span data-stu-id="4a416-119">Executable Files</span></span>](executable-files.md)

<span data-ttu-id="4a416-120">Sie können nicht über benutzerdefinierte Aktionen auf die aktuelle Installer-Sitzung zugreifen, die ausführbare Dateien aufrufen, die mit einer Befehlszeile gestartet wurden, z. b. [benutzerdefinierter Aktionstyp 2](custom-action-type-2.md) und [benutzerdefinierter Aktionstyp 18](custom-action-type-18.md).</span><span class="sxs-lookup"><span data-stu-id="4a416-120">You cannot access the current installer session from custom actions that call executable files launched with a command-line, for example, [Custom Action Type 2](custom-action-type-2.md) and [Custom Action Type 18](custom-action-type-18.md).</span></span>

[<span data-ttu-id="4a416-121">Benutzerdefinierte Aktionen für verzögerte Ausführung</span><span class="sxs-lookup"><span data-stu-id="4a416-121">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)

<span data-ttu-id="4a416-122">Sie können nicht auf die aktuelle Installer-Sitzung oder auf alle Eigenschaften Daten aus einer benutzerdefinierten Aktion für eine verzögerte Ausführung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4a416-122">You cannot access the current installer session or all property data from a deferred execution custom action.</span></span> <span data-ttu-id="4a416-123">Weitere Informationen finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="4a416-123">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a416-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a416-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a416-125">Zugreifen auf eine Datenbank oder eine Sitzung innerhalb einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="4a416-125">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



