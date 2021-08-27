---
description: In Windows 7 und höher können Sie den Eintrag SubCommands in der Registrierung verwenden, um kaskadierende Menüs mithilfe der in diesem Thema beschriebenen Prozedur zu erstellen.
title: Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag "SubCommands"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f12eb473d45a3d3aef1b7cf8e7f6cc51a0d97aa5b9e60ee39681c80af459988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111800"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>Erstellen von kaskadierenden Menüs mit dem Registrierungseintrag "SubCommands"

In Windows 7 und höher können Sie den Eintrag SubCommands in der Registrierung verwenden, um kaskadierende Menüs mithilfe der in diesem Thema beschriebenen Prozedur zu erstellen.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Erstellen Sie unter **HKEY \_ CLASSES \_ ROOT** ProgID shell einen neuen Unterschlüssel, wobei \\  \\  *ProgID* der Dateityp ist, für den Sie ein kaskadierendes Menü hinzufügen möchten. Sie können diesen neuen Unterschlüssel beliebig benennen. Im weiteren Verlauf dieses Themas wird es *CascadeMenu* genannt, wie im folgenden Beispiel gezeigt.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>Schritt 2:

Fügen Sie dem *CascadeMenu-Unterschlüssel* einen Eintrag mit dem Namen "MICVerb" vom Typ **REG \_ SZ** oder **REG EXPAND \_ \_ SZ** hinzu. Weisen Sie diesem Eintrag einen Zeichenfolgenwert wie "Test Cascade Menu" zu. Normalerweise wird diese Zeichenfolge als Ressourcenverweis im Format " @file , resource" bereitgestellt. Der (Standard)-Wert für den *CascadeMenu-Unterschlüssel* sollte nicht festgelegt werden.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>Schritt 3:

Fügen Sie dem *CascadeMenu-Unterschlüssel* einen Eintrag namens "SubCommands" vom Typ **REG \_ SZ** oder **REG EXPAND \_ \_ SZ** hinzu. Weisen Sie diesem Eintrag eine durch Semikolons getrennte Liste der Verben zu, die im Menü in der gewünschten Reihenfolge angezeigt werden sollen.

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>Schritt 4:

Füllen Sie den **CommandStore-Unterschlüssel** mit Verbimplementierungen für alle benutzerdefinierten statischen Verbimplementierungen auf, die Sie in Ihrem SubCommands-Eintrag verwendet haben. Zum Beispiel:

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

[Erstellen statischer kaskadierender Menüs](creating-static-cascading-menus.md)
</dt> </dl>

 

 



