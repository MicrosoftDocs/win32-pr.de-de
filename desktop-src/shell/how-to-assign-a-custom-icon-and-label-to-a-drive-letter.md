---
description: Geben Sie ein benutzerdefiniertes Symbol und eine Bezeichnung für ein Laufwerk an.
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: Zuweisen eines benutzerdefinierten Symbols und einer Bezeichnung zu einem Laufwerk Buchstaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979632"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a>Zuweisen eines benutzerdefinierten Symbols und einer Bezeichnung zu einem Laufwerk Buchstaben

Geben Sie ein benutzerdefiniertes Symbol und eine Bezeichnung für ein Laufwerk an.

## <a name="instructions"></a>Instructions

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a>Schritt 1: Ersetzen des Standard-Laufwerk Symbols durch ein benutzerdefiniertes Symbol in Windows 2000

Um das Standard Laufwerk Symbol durch ein benutzerdefiniertes Symbol in Windows 2000 zu ersetzen, fügen Sie dem folgenden Schlüssel einen Unterschlüssel mit dem Namen für den Laufwerk Buchstaben hinzu.

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

Im folgenden Beispiel wird ein benutzerdefiniertes Symbol und eine Bezeichnung für das Laufwerk E: angegeben. Das Symbol befindet sich in der Datei "C: \\ mydir \\MyDrive.exe" mit einem NULL basierten Index von drei.

Für Windows 2000:

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a>Schritt 2: Ersetzen des Standard-Laufwerk Symbols durch ein benutzerdefiniertes Symbol in allen anderen Versionen von Windows

Um das Standard Laufwerk Symbol durch ein benutzerdefiniertes Symbol in allen Windows-Versionen außer Windows 2000 zu ersetzen, fügen Sie dem folgenden Schlüssel einen Unterschlüssel mit dem Namen für den Laufwerk Buchstaben hinzu.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

Im folgenden Beispiel wird ein benutzerdefiniertes Symbol und eine Bezeichnung für das Laufwerk E: angegeben. Das Symbol befindet sich in der Datei "C: \\ mydir \\MyDrive.exe" mit einem NULL basierten Index von drei.

Für alle anderen Versionen von Windows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a>Schritt 3: Aufrufen des shupdateimage-Ereignisses

Wenn Sie in allen Versionen von Windows einen Dateityp oder ein Laufwerk Symbol ändern, müssen Sie auch shupdateimage aufrufen, um die Shell zu benachrichtigen, dass derzeit angezeigte Symbole aktualisiert werden.

## <a name="remarks"></a>Bemerkungen

Auf den Laufwerk Buchstaben darf kein Doppelpunkt (:). Fügen Sie dem Unterschlüssel Laufwerksbuchstabe einen **DefaultIcon** -Unterschlüssel hinzu, und legen Sie dessen Standardwert auf eine Zeichenfolge fest, die den Speicherort des Symbols enthält. Der erste Teil der Zeichenfolge enthält den voll qualifizierten Pfad der Symbol Datei. Wenn in der Datei mehr als ein Symbol vorhanden ist, folgt der Pfad ein Komma und dann der null basierte Index des Symbols.

 

 



