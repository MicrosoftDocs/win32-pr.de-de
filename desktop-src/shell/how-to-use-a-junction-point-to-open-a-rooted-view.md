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
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a>Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch die Registrierung

Sie können die Registrierung verwenden, um anzugeben, dass durch das Durchsuchen eines Verknüpfungs Punkts anstelle der Standardansicht des Inhalts der zugeordneten Erweiterung eine Stamm Ansicht geöffnet wird.

## <a name="instructions"></a>Instructions


Um anzugeben, dass durch das Durchsuchen eines Verknüpfungs Punkts eine rootansicht geöffnet werden soll, fügen Sie \\ dem CLSID-Unterschlüssel ihrer Erweiterung **den Befehl "** öffnen" und "unter **Suchen**" unter \\  Schlüssel hinzu, wobei die Standardwerte den hier gezeigten Befehlszeilen zugewiesen sind: 

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

Nachdem Sie diese Werte hinzugefügt haben, wird eine Instanz von Explorer.exe gestartet, um den Inhalt der Erweiterung als rootansicht anzuzeigen, wenn der Benutzer den Verknüpfungs Punkt auswählt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben des Speicher Orts der Namespace Erweiterung](nse-junction.md)
</dt> <dt>

[Öffnen einer Stamm Ansicht eines Verknüpfungs Punkts durch eine Verknüpfungs Datei](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



