---
description: Ein benutzerdefiniertes Symbol muss einem Dateityp zugewiesen werden, um dem Benutzer einen visuellen Hinweis auf diesen Dateityp oder die Anwendung zu geben, der dieser Dateityp zugeordnet ist.
ms.assetid: 84F293C2-BAB1-4BF8-9F89-122B6DAB29C3
title: Zuweisen eines benutzerdefinierten Symbols zu einem Dateityp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d156322bfe0899ed48c6c27f2660b911d9e5c77791c550b6141144d95384b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092996"
---
# <a name="how-to-assign-a-custom-icon-to-a-file-type"></a>Zuweisen eines benutzerdefinierten Symbols zu einem Dateityp

Wenn einem Dateityp kein benutzerdefiniertes Standardsymbol zugewiesen ist, werden im Desktop- und Windows-Explorer alle Dateien dieses Typs mit einem generischen Standardsymbol angezeigt. Der folgende Screenshot zeigt beispielsweise dieses Standardsymbol, das mit der Datei MyDocs4.myp verwendet wird.

![Screenshot des Standardsymbols](images/icon.png)

Während alle in diesem Screenshot angezeigten Dateien einfache Textdateien sind, zeigt nur MyDocs4.myp das Windows Standardsymbol an. Dies liegt daran, .txt Erweiterung ein registrierter Dateityp ist, der über ein benutzerdefiniertes Standardsymbol verfügt.

Der folgende Screenshot zeigt ein benutzerdefiniertes Symbol, das dem Dateityp .myp zugewiesen wurde.

![Screenshot des benutzerdefinierten Symbols für MYP-Dateien](images/context4.png)

> [!Note]  
> Symbole können auch anwendungsspezifisch zugewiesen werden.

 

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Erstellen Sie einen Unterschlüssel mit **dem Namen DefaultIcon** an einem der beiden folgenden Speicherorte:

-   HKEY **\_ CLASSES \_ ROOT** \\ *.extension* für eine Dateitypzuweisung
-   Bei einer Anwendungszuweisung **HKEY \_ CLASSES \_ ROOT** \\ *ProgID*

### <a name="step-2"></a>Schritt 2:

Weisen Sie **dem Unterschlüssel DefaultIcon** einen Standardwert vom Typ **REG \_ SZ** zu, der den vollqualifizierten Pfad für die Datei angibt, die das Symbol enthält.

### <a name="step-3"></a>Schritt 3:

Rufen Sie die [**SHChangeNotify-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) auf, um die Shell zu benachrichtigen, ihren Symbolcache zu aktualisieren.

## <a name="remarks"></a>Hinweise

Das folgende Beispiel zeigt eine detaillierte Ansicht der Registrierungseinträge, die für eine Dateityp-Symbolzuweisung erforderlich sind. Die Dateierweiterung ist einer Anwendung zugeordnet, aber die Symbolzuweisung ist der Dateierweiterung selbst zugeordnet, sodass die zugeordnete Anwendung das Standardsymbol nicht vorschreiben kann.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Das folgende Beispiel zeigt eine detaillierte Ansicht der Registrierungseinträge, die für eine Anwendungssymbolzuweisung erforderlich sind. Die Dateierweiterung .myp wird zuerst der Anwendung MyProgram.1 zugeordnet. Dem Unterschlüssel MyProgram.1 ProgID wird dann das benutzerdefinierte Standardsymbol zugewiesen.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
```

Jede Datei, die ein Symbol enthält, ist akzeptabel, einschließlich ICO-, .exe- und .dll Dateien. Wenn die Datei mehrere Symbole enthält, sollte auf den Pfad ein Komma und dann der Index des Symbols folgen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateitypen](fa-file-types.md)
</dt> </dl>

 

 



