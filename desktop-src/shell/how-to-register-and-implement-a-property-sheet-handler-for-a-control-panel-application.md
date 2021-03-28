---
description: Viele System Steuerungsanwendungen zeigen ein Eigenschaften Blatt "Eigenschaften" an, mit dem Benutzer verschiedene Geräte-und Systemeinstellungen anzeigen und ändern können.
title: Registrieren und Implementieren eines Eigenschaften Blatt Handlers für eine System Steuerungsanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864916"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a>Registrieren und Implementieren eines Eigenschaften Blatt Handlers für eine System Steuerungsanwendung

Viele System Steuerungsanwendungen zeigen ein Eigenschaften Blatt "Eigenschaften" an, mit dem Benutzer verschiedene Geräte-und Systemeinstellungen anzeigen und ändern können. Zwei dieser Anwendungen – Maus und Anzeige – ermöglichen es Eigenschaften Blatt Handlern, eine oder mehrere Ihrer Seiten durch eine benutzerdefinierte Seite zu ersetzen. Der folgende Screenshot zeigt das Eigenschaften Blatt für die **Maus Eigenschaften** .

![Eigenschaften Blatt "Maus Eigenschaften"](images/propsheethandler3.jpg)

Eigenschaften Blatt Handler für System Steuerungsanwendungen ähneln denen für Dateitypen mit zwei primären Ausnahmen:

-   Sie werden von einer System Steuerungsanwendung aufgerufen, nicht von der Shell.
-   Sie werden anders registriert.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   Shell

### <a name="prerequisites"></a>Voraussetzungen

-   Ein Verständnis der Systemsteuerung
-   Ein Verständnis der Kontextmenüs

## <a name="instructions"></a>Instructions

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a>Schritt 1: Registrieren eines Eigenschaften Blatt Handlers für eine System Steuerungsanwendung

Ein Eigenschaften Blatt Handler der System Steuerungsanwendung muss unter dem System Steuerungs Unterschlüssel registriert werden. Dieser Schlüssel kann sich an einem von zwei Speicherorten befinden, je nachdem, ob der Handler pro Benutzer oder Computer bezogen werden soll. Bei der Registrierung pro Benutzer ist der System Steuerungs Unterschlüssel **HKEY \_ Current \_ User** \\ **Control Panel**. Das \_ \_ in "regstr. h" definierte Makro "regstr Path ControlPanel" kann im Code anstelle von "Systemsteuerung" verwendet werden. Für die Registrierung pro Computer lautet der Speicherort wie folgt:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

Auf diesen Pfad kann im Code als HKEY \_ local \_ Machine \\ regstr \_ path \_ controlsfolder verwiesen werden. dabei wird das \_ \_ in regstr. h definierte regstr-Pfad controlsfolder-Makro verwendet.

Die System Steuerungsanwendungen, die Eigenschaften Blatt Handler das Ersetzen von Seiten gestatten, haben unter dem Unterschlüssel der Systemsteuerung einen Unterschlüssel, der für die Anwendung benannt ist, wie z. b. Maus und Anzeige. Der Unterschlüssel der Anwendung muss über einen **shellex** -Unterschlüssel mit einem **propertysheethandlers** -Unterschlüssel verfügen. Fügen Sie zum Registrieren eines Eigenschaften Blatt Handlers dem Unterschlüssel **propertysheethandlers** , der der System Steuerungsanwendung zugeordnet ist, die GUID hinzu. Erstellen Sie hierzu einen Unterschlüssel des unter Schlüssels **propertysheethandlers** , der für den Eigenschaften Blatt Handler benannt ist, und legen Sie dessen Standardwert auf die Zeichen folgen Form der GUID des Handlers fest.

Im folgenden Beispiel wird ein Eigenschaften Blatt Handler für die Anwendung mit der Maussteuerung auf Computer Basis registriert. Um es auf Benutzerbasis zu registrieren, ersetzen Sie **HKEY \_ local \_ Machine** \\ **regstr \_ path \_ controlsfolder** durch **HKEY \_ Current \_ User** \\ **regstr \_ path \_ ControlPanel**.

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a>Schritt 2: Implementieren eines Eigenschaften Blatt Handlers für eine System Steuerungsanwendung

Das Verfahren zum Implementieren eines Eigenschaften Blatt Handlers für die Systemsteuerung ähnelt sehr dem, das unter [registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)beschrieben wird. Der Hauptunterschied besteht darin, dass [**ishellpropsheetext:: replacepage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) jetzt anstelle von [**ishellpropsheetext:: addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)eine nicht-Token-Implementierung benötigt.

Wenn eine System Steuerungsanwendung im Begriff ist, das Eigenschaften Blatt anzuzeigen, wird die [**ishellpropsheetext:: replacepage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) -Methode des Eigenschaften Blatt Handlers einmal für jede Seite aufgerufen, die ersetzt werden kann. Der *upageid* -Parameter wird auf die ID der Seite festgelegt. Die IDs für die verfügbaren Seiten werden in "cplext. h" definiert. Die derzeit verfügbaren IDs sind in der folgenden Tabelle aufgeführt. 

| Seiten-ID                      | BESCHREIBUNG         | System Steuerungsanwendung |
|------------------------------|---------------------|---------------------------|
| cplpage- \_ Maus \_ Tasten      | Die Schaltflächen Seite    | Maus                     |
| cplpage- \_ Maus \_ ptrmotion    | Die Bewegungs Seite     | Maus                     |
| cplpage \_ - \_ Mausrad        | Die Radseite      | Maus                     |
| cplpage- \_ Tastatur \_ Geschwindigkeit     | Die Seite "Geschwindigkeit"      | Tastatur                  |
| cplpage- \_ Anzeige \_ Hintergrund | Die Hintergrundseite | Anzeige                   |



 

## <a name="remarks"></a>Bemerkungen

Die Vorgehensweise zum Erstellen und Ersetzen einer Seite ist identisch mit der Vorgehensweise zum Hinzufügen einer Seite. Weitere Informationen finden Sie unter [registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).

 

 



