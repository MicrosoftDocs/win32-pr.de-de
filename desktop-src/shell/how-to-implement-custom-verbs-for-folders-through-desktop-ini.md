---
description: In Windows 7 und höher können Sie mit Desktop.ini Verben zu einem Ordner hinzufügen. Weitere Informationen zu Desktop.ini Dateien finden Sie unter Anpassen von Ordnern mit Desktop.ini.
ms.assetid: F03AB35D-FBFE-46C2-A37F-F70C18219B9A
title: So implementieren Sie benutzerdefinierte Verben für Ordner über Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133726133abe884863a0b4d2abc0cc76aab1310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979545"
---
# <a name="how-to-implement-custom-verbs-for-folders-through-desktopini"></a>So implementieren Sie benutzerdefinierte Verben für Ordner über Desktop.ini

In Windows 7 und höher können Sie mit Desktop.ini Verben zu einem Ordner hinzufügen. Weitere Informationen zu Desktop.ini Dateien finden Sie unter [Anpassen von Ordnern mit Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini Dateien sollten immer als ausgeblendet **markiert werden**  +   , damit Sie Benutzern nicht angezeigt werden.

 

Um benutzerdefinierte Verben für Ordner über eine Desktop.ini Datei hinzuzufügen, führen Sie die folgenden Schritte aus.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Erstellen **Sie** einen Ordner, der als schreibgeschützt oder als **System** markiert ist.

### <a name="step-2"></a>Schritt 2:

Erstellen Sie eine Desktop.ini-Datei, die eine enthält \[ . Shellclassinfo \] directoryclass = Ordner ProgID.

### <a name="step-3"></a>Schritt 3:

Erstellen Sie in der Registrierung **HKEY \_ - \_ Klassen** \\ **Stamm Ordner ProgID** mit dem Wert "canusefordirectory". Der Wert von "canusefordirectory" vermeidet den Missbrauch von ProgIDs, die nicht an der Implementierung benutzerdefinierter Verben für Ordner durch Desktop.ini beteiligt sind.

### <a name="step-4"></a>Schritt 4:

Fügen Sie unter dem **Ordner** ProgID Unterschlüssel Verben hinzu, z. b.:

```
HKEY_CLASSES_ROOT
   CustomFolderType
      Shell
         MyVerb
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
```

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Diese Verben können die Standard Verben sein. in diesem Fall wird das Verb durch Doppelklicken auf den Ordner aktiviert.

 

 

 



