---
description: In Windows 7 und höher können Sie den Eintrag Unterbefehle in der Registrierung verwenden, um Kaskadierende Menüs mithilfe der in diesem Thema beschriebenen Prozedur zu erstellen.
title: Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag Unterbefehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994694"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "Unterbefehle"

In Windows 7 und höher können Sie den Eintrag Unterbefehle in der Registrierung verwenden, um Kaskadierende Menüs mithilfe der in diesem Thema beschriebenen Prozedur zu erstellen.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Erstellen Sie einen neuen Unterschlüssel unter **HKEY \_ Classes \_ root** \\ *ProgID* \\ **Shell**, wobei *ProgID* der Dateityp ist, für den Sie ein Cascading-Menü hinzufügen möchten. Sie können den neuen Unterschlüssel beliebig benennen. Im restlichen Teil dieses Themas nennen wir es *cascademenu*, wie im folgenden Beispiel gezeigt.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>Schritt 2:

Fügen Sie dem Unterschlüssel *cascademenu* einen Eintrag mit dem Namen "MUIVerb", dem Typ " **reg \_ SZ** " oder " **reg \_ Expand \_ SZ**", hinzu. Weisen Sie diesem Eintrag einen Zeichen folgen Wert zu, z. b. "Menü" Test Cascade " Normalerweise wird diese Zeichenfolge als Ressourcen Verweis in der Form " @file , Resource" bereitgestellt. Der (standardmäßige) Wert für den Unterschlüssel *caskadetten Menu* darf nicht festgelegt werden.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>Schritt 3:

Fügen Sie dem Unterschlüssel *caskadetten Menu* einen Eintrag mit dem Namen "Unterbefehle" vom Typ " **reg \_ SZ** " oder " **reg \_ Expand \_ SZ**" hinzu. Weisen Sie diesem Eintrag eine durch Semikolons getrennte Liste der Verben zu, die im Menü in der gewünschten Reihenfolge angezeigt werden sollen.

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>Schritt 4:

Füllen Sie den **commandstore** -Unterschlüssel mit Verb-Implementierungen für alle benutzerdefinierten statischen Verb-Implementierungs Methoden aus, die Sie im Eintrag für die Unterbefehle verwendet haben. Zum Beispiel:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von statischen kaskadierenden Menüs](creating-static-cascading-menus.md)
</dt> </dl>

 

 



