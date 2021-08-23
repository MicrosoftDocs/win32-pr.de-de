---
description: Sie können die Registrierung verwenden, um anzugeben, dass beim Navigieren zu einem Verbindungspunkt eine Stammansicht anstelle der Standardansicht des Inhalts der zugeordneten Erweiterung geöffnet wird.
title: Öffnen einer Stammansicht eines Verbindungspunkts über die Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f575d4265a207e97c20f0c2a42456ddbf55cebbe5a0d42664c1fdfa9f5986d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593160"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a>Öffnen einer Stammansicht eines Verbindungspunkts über die Registrierung

Sie können die Registrierung verwenden, um anzugeben, dass beim Navigieren zu einem Verbindungspunkt eine Stammansicht anstelle der Standardansicht des Inhalts der zugeordneten Erweiterung geöffnet wird.

## <a name="instructions"></a>Anweisungen


Um anzugeben, dass beim Durchsuchen eines Verbindungspunkts eine Stammansicht geöffnet werden soll, fügen Sie dem  \\   \\ **CLSID-Unterschlüssel** Ihrer Erweiterung die Unterschlüssel Befehl öffnen und **Befehl** durchsuchen hinzu, wobei die Standardwerte den hier gezeigten Befehlszeilen zugewiesen sind:

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

Nachdem Sie diese Werte hinzugefügt haben, wird eine Instanz von Explorer.exe gestartet, um den Inhalt der Erweiterung als Rootansicht anzuzeigen, wenn der Benutzer den Verbindungspunkt auswählt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Angeben des Speicherorts einer Namespaceerweiterung](nse-junction.md)
</dt> <dt>

[Öffnen einer Stammansicht eines Verbindungspunkts durch eine Verknüpfungsdatei](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



