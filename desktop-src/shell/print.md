---
description: Die Shell-API stellt Funktionen bereit, die Sie zum Verwalten von Netzwerkdruckern verwenden können. Wenn einer Datei das Druck Verb zugeordnet ist, können Sie den Befehl ShellExecuteEx verwenden, um Sie zu drucken.
ms.assetid: b94fca60-237a-43b1-a75a-faccf9dc63fb
title: Verwalten von Druckern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e9625fbe17c0dd350a10c0c71dcd5332fb9154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979953"
---
# <a name="managing-printers"></a><span data-ttu-id="bdca6-104">Verwalten von Druckern</span><span class="sxs-lookup"><span data-stu-id="bdca6-104">Managing Printers</span></span>

<span data-ttu-id="bdca6-105">Die Shell-API stellt Funktionen bereit, die Sie zum Verwalten von Netzwerkdruckern verwenden können.</span><span class="sxs-lookup"><span data-stu-id="bdca6-105">The Shell API provides functions that you can use to manage networked printers.</span></span> <span data-ttu-id="bdca6-106">Wenn einer Datei das **Druck** Verb zugeordnet ist, können Sie den Befehl [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) verwenden, um Sie zu drucken.</span><span class="sxs-lookup"><span data-stu-id="bdca6-106">If a file has the **print** verb associated with it, you can use the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) command to print it.</span></span>

-   [<span data-ttu-id="bdca6-107">Druckerverwaltung</span><span class="sxs-lookup"><span data-stu-id="bdca6-107">Printer Management</span></span>](#printer-management)
-   [<span data-ttu-id="bdca6-108">Drucken von Dateien mit ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="bdca6-108">Printing Files with ShellExecuteEx</span></span>](#printing-files-with-shellexecuteex)

## <a name="printer-management"></a><span data-ttu-id="bdca6-109">Druckerverwaltung</span><span class="sxs-lookup"><span data-stu-id="bdca6-109">Printer Management</span></span>

<span data-ttu-id="bdca6-110">Sie können Drucker auf einem System mit der [**shinvokeprintercommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) -Funktion verwalten.</span><span class="sxs-lookup"><span data-stu-id="bdca6-110">You can manage printers on a system with the [**SHInvokePrinterCommand**](/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda) function.</span></span> <span data-ttu-id="bdca6-111">Diese Funktion ermöglicht Ihnen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bdca6-111">This function allows you to:</span></span>

-   <span data-ttu-id="bdca6-112">Installieren Sie Drucker.</span><span class="sxs-lookup"><span data-stu-id="bdca6-112">Install printers.</span></span>
-   <span data-ttu-id="bdca6-113">Öffnen Sie Drucker.</span><span class="sxs-lookup"><span data-stu-id="bdca6-113">Open printers.</span></span>
-   <span data-ttu-id="bdca6-114">Druckereigenschaften erhalten.</span><span class="sxs-lookup"><span data-stu-id="bdca6-114">Get printer properties.</span></span>
-   <span data-ttu-id="bdca6-115">Erstellen Sie Drucker Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="bdca6-115">Create printer links.</span></span>
-   <span data-ttu-id="bdca6-116">Drucken Sie eine Testseite.</span><span class="sxs-lookup"><span data-stu-id="bdca6-116">Print a test page.</span></span>

## <a name="printing-files-with-shellexecuteex"></a><span data-ttu-id="bdca6-117">Drucken von Dateien mit ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="bdca6-117">Printing Files with ShellExecuteEx</span></span>

<span data-ttu-id="bdca6-118">Wenn einem Dateityp ein Druckbefehl zugeordnet ist, können Sie die Datei drucken, indem Sie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) mit dem Wert " **Print** " als Verb aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bdca6-118">If a file type has a print command associated with it, you can print the file by calling [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) with **print** as the verb.</span></span> <span data-ttu-id="bdca6-119">Dieser Befehl ist häufig identisch mit dem, der für das **geöffnete** Verb verwendet wurde, mit dem Hinzufügen eines Flags, um der Anwendung mitzuteilen, dass die Datei gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bdca6-119">This command is often the same as that used for the **open** verb, with the addition of a flag to tell the application to print the file.</span></span> <span data-ttu-id="bdca6-120">Beispielsweise können txt-Dateien von Microsoft WordPad gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="bdca6-120">For instance, .txt files can be printed by Microsoft WordPad.</span></span> <span data-ttu-id="bdca6-121">Das **geöffnete** Verb für eine txt-Datei entspricht daher etwa dem folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="bdca6-121">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
"C:\Program Files\Windows NT\Accessories\Wordpad.exe" /p "%1"
```



<span data-ttu-id="bdca6-122">Wenn Sie [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) zum Drucken einer txt-Datei verwenden, wird die Datei von WordPad geöffnet, gedruckt und dann geschlossen, und die Steuerung wird an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bdca6-122">When you use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to print a .txt file, WordPad opens the file, prints it, and then closes, returning control to the application.</span></span> <span data-ttu-id="bdca6-123">Die folgende Beispiel Funktion verwendet einen voll qualifizierten Pfad und verwendet **ShellExecuteEx** , um Sie zu drucken, wobei der der Dateinamenerweiterung zugeordnete Print-Befehl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bdca6-123">The following sample function takes a fully qualified path, and uses **ShellExecuteEx** to print it, using the print command associated with its file name extension.</span></span>


```C++
#include <shlobj.h>

HINSTANCE PrintFile(LPCTSTR pszFileName)
{
    SHELLEXECUTEINFO ShExecInfo;
    HINSTANCE hInst;

    // Fill the SHELLEXECUTEINFO array.

    ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
    ShExecInfo.fMask = NULL;
    ShExecInfo.hwnd = NULL;
    ShExecInfo.lpVerb = "print";
    ShExecInfo.lpFile = pszFileName;  // a fully qualified path
    ShExecInfo.lpParameters = NULL;
    ShExecInfo.lpDirectory = NULL;    
    ShExecInfo.nShow = SW_MAXIMIZE;
    ShExecInfo.hInstApp = NULL;

    hInst = ShellExecuteEx(&ShExecInfo);
    
    return hInst;
}
```



 

 



