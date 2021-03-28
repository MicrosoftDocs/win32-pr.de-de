---
description: Sie können die Registrierung verwenden, um anzugeben, dass durch das Durchsuchen eines Verknüpfungs Punkts anstelle der Standardansicht des Inhalts der zugeordneten Erweiterung eine Stamm Ansicht geöffnet wird.
title: Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch die Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51e87ccb541e995300cb010f82c79e33112e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215937"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a><span data-ttu-id="e7165-103">Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch die Registrierung</span><span class="sxs-lookup"><span data-stu-id="e7165-103">How to Open a Rooted View of a Junction Point Through the Registry</span></span>

<span data-ttu-id="e7165-104">Sie können die Registrierung verwenden, um anzugeben, dass durch das Durchsuchen eines Verknüpfungs Punkts anstelle der Standardansicht des Inhalts der zugeordneten Erweiterung eine Stamm Ansicht geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e7165-104">You can use the registry to specify that browsing into a junction point will open a rooted view rather than the default view of the contents of the associated extension.</span></span>

## <a name="instructions"></a><span data-ttu-id="e7165-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="e7165-105">Instructions</span></span>


<span data-ttu-id="e7165-106">Um anzugeben, dass durch das Durchsuchen eines Verknüpfungs Punkts eine rootansicht geöffnet werden soll, fügen Sie \\ dem CLSID-Unterschlüssel ihrer Erweiterung **den Befehl "** öffnen" und "unter **Suchen**" unter \\  Schlüssel hinzu, wobei die Standardwerte den hier gezeigten Befehlszeilen zugewiesen sind: </span><span class="sxs-lookup"><span data-stu-id="e7165-106">To specify that browsing into a junction point should open a rooted view, add **Open**\\**Command** and **Explore**\\**Command** subkeys to your extension's **CLSID** subkey, with their default values assigned to the command lines shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         Shell
            Open
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
            Explore
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
```

<span data-ttu-id="e7165-107">Nachdem Sie diese Werte hinzugefügt haben, wird eine Instanz von Explorer.exe gestartet, um den Inhalt der Erweiterung als rootansicht anzuzeigen, wenn der Benutzer den Verknüpfungs Punkt auswählt.</span><span class="sxs-lookup"><span data-stu-id="e7165-107">Once you've added those values, an instance of Explorer.exe is launched to display the contents of the extension as a rooted view when the user selects the junction point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7165-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7165-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7165-109">Angeben des Speicher Orts der Namespace Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e7165-109">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="e7165-110">Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch eine Verknüpfungs Datei</span><span class="sxs-lookup"><span data-stu-id="e7165-110">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



