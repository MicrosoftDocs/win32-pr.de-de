---
description: Sie können eine Namespace Erweiterung verwenden, um Benutzern zu ermöglichen, den Inhalt einer Datei zu durchsuchen, anstatt Sie als Ordner zu verwenden. Erweiterungen dieser Art werden normalerweise verwendet, um den Inhalt der Member eines Dateityps anzuzeigen.
title: Anzeigen einer rootansicht einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864928"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a><span data-ttu-id="17ef7-104">Anzeigen einer rootansicht einer Datei</span><span class="sxs-lookup"><span data-stu-id="17ef7-104">How to Display a Rooted View of a File</span></span>

<span data-ttu-id="17ef7-105">Sie können eine Namespace Erweiterung verwenden, um Benutzern zu ermöglichen, den Inhalt einer Datei zu durchsuchen, anstatt Sie als Ordner zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="17ef7-105">You can use a namespace extension to allow users to browse the contents of a file rather than have it presented as a folder.</span></span> <span data-ttu-id="17ef7-106">Erweiterungen dieser Art werden normalerweise verwendet, um den Inhalt der Member eines [Dateityps](fa-file-types.md)anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="17ef7-106">Extensions of this sort are typically used to display the contents of the members of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="17ef7-107">Beispielsweise können die Member eines Dateityps mehrere komprimierte Dateien oder Bilder enthalten, die in einer Hierarchie organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="17ef7-107">For instance, the members of a file type might contain multiple compressed files or images, organized in a hierarchy.</span></span> <span data-ttu-id="17ef7-108">Anstatt eine Anwendung zu schreiben, die es dem Benutzer ermöglicht, den Inhalt einer solchen Datei anzuzeigen, können Sie stattdessen eine Namespace Erweiterung schreiben und Windows-Explorer die Anzeige verarbeiten lassen.</span><span class="sxs-lookup"><span data-stu-id="17ef7-108">Rather than write an application to allow the user to view the contents of such a file, you can instead write a namespace extension and let Windows Explorer handle the display.</span></span>

<span data-ttu-id="17ef7-109">Sie müssen eine rootansicht verwenden, damit eine Erweiterung den Inhalt einer Datei anzeigen darf.</span><span class="sxs-lookup"><span data-stu-id="17ef7-109">You must use a rooted view in order to have an extension display the contents of a file.</span></span> <span data-ttu-id="17ef7-110">Die gängigste Methode, um eine rootansicht der Member eines Dateityps bereitzustellen, ist das Definieren eines Kontext [Menü Verbs](context.md) , das eine Instanz von Explorer.exe gestartet.</span><span class="sxs-lookup"><span data-stu-id="17ef7-110">The most common way to provide a rooted view of the members of a file type is to define a [shortcut menu verb](context.md) that launches an instance of Explorer.exe.</span></span> <span data-ttu-id="17ef7-111">Wenn Sie dieses Verb als Standard Verb festlegen, wird mit einem Doppelklick auch eine rootansicht der Datei geöffnet.</span><span class="sxs-lookup"><span data-stu-id="17ef7-111">By making this verb the default verb, a double-click will also open a rooted view of the file.</span></span> <span data-ttu-id="17ef7-112">Sie können entweder ein Verb für alle Elemente des Dateityps definieren, indem Sie [die Registrierung ändern](context.md), oder Sie können die Verben auf Datei Basis durch Implementieren eines Kontext [Menü Handlers](context-menu-handlers.md)dynamisch definieren.</span><span class="sxs-lookup"><span data-stu-id="17ef7-112">You can either define a verb for all members of the file type by [modifying the registry](context.md), or dynamically define verbs on a file-by-file basis by implementing a [shortcut menu handler](context-menu-handlers.md).</span></span>

## <a name="instructions"></a><span data-ttu-id="17ef7-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="17ef7-113">Instructions</span></span>


<span data-ttu-id="17ef7-114">Im folgenden Beispiel wird veranschaulicht, wie die Registrierung verwendet wird, um eine rootansicht der Member eines Dateityps durch Ändern der Registrierung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="17ef7-114">The following example illustrates how to use the registry to provide a rooted view of the members of a file type by modifying the registry.</span></span> <span data-ttu-id="17ef7-115">Der Beispiel Registrierungs Eintrag ist eine Änderung eines der Beispiele in Erweitern von Kontext [Menüs](context.md).</span><span class="sxs-lookup"><span data-stu-id="17ef7-115">The sample registry entry is a modification of one of the examples in [Extending Shortcut Menus](context.md).</span></span> <span data-ttu-id="17ef7-116">In den Registrierungs Einträgen werden Dateien mit der Dateinamenerweiterung MYP als Dateityp definiert, und mit dem **Browse** -Verb wird eine rootansicht von Membern dieses Typs gestartet.</span><span class="sxs-lookup"><span data-stu-id="17ef7-116">The registry entries define files with an .myp file name extension as a file type, and use the **browse** verb to launch a rooted view of members of that type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

<span data-ttu-id="17ef7-117">Sie können das gleiche Verb verwenden, um eine rootansicht eines Members des Dateityps Programm gesteuert zu starten, indem Sie die [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="17ef7-117">You can use the same verb to programmatically launch a rooted view of a member of the file type by calling the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17ef7-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="17ef7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17ef7-119">Angeben des Speicher Orts der Namespace Erweiterung</span><span class="sxs-lookup"><span data-stu-id="17ef7-119">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="17ef7-120">Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch die Registrierung</span><span class="sxs-lookup"><span data-stu-id="17ef7-120">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="17ef7-121">Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch eine Verknüpfungs Datei</span><span class="sxs-lookup"><span data-stu-id="17ef7-121">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="17ef7-122">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="17ef7-122">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



