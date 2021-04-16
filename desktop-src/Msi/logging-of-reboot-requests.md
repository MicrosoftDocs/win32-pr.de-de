---
description: Wenn die InstallValidate-Aktion die Installation einer verwendeten Datei erkennt, wird das Dialog Feld FilesInUse angezeigt, und die folgenden Informationen werden protokolliert.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Protokollierung von Neustart Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530233"
---
# <a name="logging-of-reboot-requests"></a><span data-ttu-id="df1f3-103">Protokollierung von Neustart Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df1f3-103">Logging of Reboot Requests</span></span>

<span data-ttu-id="df1f3-104">Wenn die [InstallValidate-Aktion](installvalidate-action.md) die Installation einer verwendeten Datei erkennt, wird das [Dialog Feld FilesInUse](filesinuse-dialog.md) angezeigt, und die folgenden Informationen werden protokolliert.</span><span class="sxs-lookup"><span data-stu-id="df1f3-104">If the [InstallValidate action](installvalidate-action.md) detects the installation of a file in use it displays the [FilesInUse Dialog](filesinuse-dialog.md) and logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

<span data-ttu-id="df1f3-105">Wenn das Installationsprogramm erkennt, dass es im Begriff ist, eine Datei zu überschreiben, die verwendet wird, werden die folgenden Informationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="df1f3-105">If the installer detects that it is about to overwrite a file that is in use, it logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

<span data-ttu-id="df1f3-106">Das \[ filename- \] Token kann tatsächlich einen Pfad zu einer Datei mit der Erweiterung RBF enthalten.</span><span class="sxs-lookup"><span data-stu-id="df1f3-106">The \[filename\] token may actually contain a path to a file with an .rbf extension.</span></span> <span data-ttu-id="df1f3-107">In diesem Fall handelt es sich bei der RBF-Datei tatsächlich um die ursprüngliche Datei, die von der 1603-Nachricht protokolliert wurde, die in die RBF-Datei umbenannt wurde.</span><span class="sxs-lookup"><span data-stu-id="df1f3-107">In this case the .rbf file is actually the original file logged by the 1603 message which has been renamed to the .rbf file.</span></span> <span data-ttu-id="df1f3-108">Die verwendete Datei wird zuerst mit der Erweiterung RBF umbenannt und dann gelöscht.</span><span class="sxs-lookup"><span data-stu-id="df1f3-108">The file that's in use is first renamed with an .rbf extension and then deleted.</span></span>

<span data-ttu-id="df1f3-109">Wenn Sie weitere Informationen dazu erhalten möchten, warum das Installationsprogramm versucht, diese Datei zu überschreiben, können Sie die Option ausführliche Protokollierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="df1f3-109">To obtain more information about why the installer is attempting to overwrite this particular file, you can use the verbose logging option.</span></span> <span data-ttu-id="df1f3-110">Verwenden Sie den ausführlichen installlogmode- \_ Wert in einem [**msienablelog**](/windows/desktop/api/Msi/nf-msi-msienableloga) -aufrufswert, oder verwenden Sie die Option "ausführliche Output" der [Befehlszeilenoptionen](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="df1f3-110">Use the INSTALLLOGMODE\_VERBOSE value in a call to [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) or use the verbose output option of the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="df1f3-111">Hierdurch werden die folgenden Informationen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="df1f3-111">This logs the following information.</span></span>

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

<span data-ttu-id="df1f3-112">Das Protokoll enthält eine Nachricht, z. b. "vorhandene Datei ist eine niedrigere Version" oder "vorhandene Datei ist beschädigt (ungültige Prüfsumme)".</span><span class="sxs-lookup"><span data-stu-id="df1f3-112">The log will include a message such as "Existing file is a lower version" or "Existing file is corrupt (invalid checksum)"</span></span>

 

 



