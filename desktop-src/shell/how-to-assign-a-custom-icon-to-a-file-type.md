---
description: Ein benutzerdefiniertes Symbol muss einem Dateityp zugewiesen werden, um dem Benutzer dieses Dateityps oder der Anwendung, der der Dateityp zugeordnet ist, einen visuellen Hinweis zu geben.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Zuweisen eines benutzerdefinierten Symbols zu einem Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf625eb6177471702096f462846b8035772177ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979617"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a>Zuweisen eines benutzerdefinierten Symbols zu einem Dateityp

Wenn einem Dateityp kein benutzerdefiniertes Standard Symbol zugewiesen ist, zeigen der Desktop und Windows-Explorer alle Dateien dieses Typs mit einem generischen Standard Symbol an. Der folgende Screenshot zeigt z. b. das Standard Symbol, das mit der Datei MyDocs4. MYP verwendet wird.

![Screenshot des Standard Symbols](images/icon.png)

Obwohl es sich bei allen in diesem Screenshot angezeigten Dateien um einfache Textdateien handelt, zeigt nur MyDocs4. MYP das Windows-Standard Symbol an. Dies liegt daran, dass die Erweiterung ". txt" ein registrierter Dateityp mit einem benutzerdefinierten Standard Symbol ist.

Der folgende Screenshot zeigt ein benutzerdefiniertes Symbol, das dem Dateityp MYP zugewiesen wurde.

![Screenshot des benutzerdefinierten Symbols für MYP-Dateien](images/context4.png)

> [!Note]  
> Symbole können auch anwendungsspezifisch zugewiesen werden.

 

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Erstellen Sie einen Unterschlüssel mit dem Namen **DefaultIcon** an einem der beiden folgenden Speicherorte:

-   Für eine Dateityp Zuweisung, **HKEY- \_ Klassen \_ root** \\ *. Extension*
-   Für eine Anwendungs Zuweisung, **HKEY \_ - \_ Klassen** \\ *Stamm-ProgID*

### <a name="step-2"></a>Schritt 2:

Weisen Sie den Unterschlüssel **DefaultIcon** einem Standardwert des Typs **reg \_ SZ** zu, der den voll qualifizierten Pfad für die Datei angibt, in der das Symbol enthalten ist.

### <a name="step-3"></a>Schritt 3:

Rufen Sie die [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) -Funktion auf, um die Shell zu benachrichtigen, ihren Symbol Cache zu aktualisieren.

## <a name="remarks"></a>Bemerkungen

Das folgende Beispiel zeigt eine detaillierte Ansicht der Registrierungseinträge, die für eine Dateityp-Symbol Zuweisung benötigt werden. Die Dateinamenerweiterung ist einer Anwendung zugeordnet, aber die Symbol Zuweisung erfolgt in der Dateinamenerweiterung selbst, sodass die zugehörige Anwendung das Standard Symbol nicht vorschreibt.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Das folgende Beispiel zeigt eine detaillierte Ansicht der Registrierungseinträge, die für eine Anwendungssymbol Zuweisung benötigt werden. Die Dateinamenerweiterung MYP ist zuerst der Anwendung MyProgram. 1 zugeordnet. Dem Unterschlüssel MyProgram. 1 ProgID wird dann das benutzerdefinierte Standard Symbol zugewiesen.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Jede Datei, die ein Symbol enthält, ist akzeptabel, einschließlich ICO-, exe-und dll-Dateien. Wenn in der Datei mehr als ein Symbol vorhanden ist, muss auf den Pfad ein Komma und dann auf den Index des Symbols folgen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateitypen](fa-file-types.md)
</dt> </dl>

 

 



