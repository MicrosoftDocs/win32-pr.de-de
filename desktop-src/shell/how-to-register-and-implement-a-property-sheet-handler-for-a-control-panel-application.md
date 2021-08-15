---
description: Viele Systemsteuerung Anwendungen zeigen ein Eigenschaftenblatt an, mit dem Benutzer verschiedene Geräte- und Systemeinstellungen anzeigen und ändern können.
title: Registrieren und Implementieren eines Eigenschaftenblatthandlers für eine Systemsteuerung-Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6865e8e50aefdea3e3d25c29c9abd3bbbabf5c6af3b770537ed187f8b055bdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859589"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a>Registrieren und Implementieren eines Eigenschaftenblatthandlers für eine Systemsteuerung-Anwendung

Viele Systemsteuerung Anwendungen zeigen ein Eigenschaftenblatt an, mit dem Benutzer verschiedene Geräte- und Systemeinstellungen anzeigen und ändern können. Zwei dieser Anwendungen – Maus und Anzeige – ermöglichen es Eigenschaftenblatthandlern, eine oder mehrere ihrer Seiten durch eine benutzerdefinierte Seite zu ersetzen. Der folgende Screenshot zeigt das Eigenschaftenblatt **Mauseigenschaften.**

![Eigenschaftenblatt für Mauseigenschaften](images/propsheethandler3.jpg)

Eigenschaftenblatthandler für Systemsteuerung-Anwendungen ähneln denen für Dateitypen mit zwei primären Ausnahmen:

-   Sie werden von einer Systemsteuerung Anwendung aufgerufen, nicht von der Shell.
-   Sie werden unterschiedlich registriert.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   Shell

### <a name="prerequisites"></a>Voraussetzungen

-   Kenntnisse der Systemsteuerung
-   Verstehen von Kontextmenüs

## <a name="instructions"></a>Anweisungen

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a>Schritt 1: Registrieren eines Eigenschaftenblatthandlers für eine Systemsteuerung Anwendung

Ein Systemsteuerung Anwendungseigenschaftenblatthandler muss unter dem Unterschlüssel Systemsteuerung registriert werden. Dieser Schlüssel kann sich an einem von zwei Speicherorten befinden, je nachdem, ob der Handler pro Benutzer oder pro Computer erfolgen soll. Bei der Benutzerregistrierung lautet der Systemsteuerung Unterschlüssel **HKEY \_ CURRENT \_ USER** \\ **Systemsteuerung**. Das in Regstr.h definierte Makro REGSTR \_ PATH \_ CONTROLPANEL kann im Code anstelle von "Systemsteuerung" verwendet werden. Für die Computerregistrierung lautet der Speicherort:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

Dieser Pfad kann im Code als HKEY \_ LOCAL \_ MACHINE \\ REGSTR PATH \_ CONTROLSFOLDER bezeichnet \_ werden, indem das in \_ Regstr.h definierte REGSTR PATH \_ CONTROLSFOLDER-Makro verwendet wird.

Die Systemsteuerung Anwendungen, die es Eigenschaftenblatthandlern ermöglichen, Seiten zu ersetzen, verfügen über einen Unterschlüssel unter dem Unterschlüssel des Systemsteuerung, der für die Anwendung benannt ist, z. B. Maus und Anzeige. Der Unterschlüssel der Anwendung muss über einen **Shellex-Unterschlüssel** mit einem **PropertySheetHandlers-Unterschlüssel** verfügen. Um einen Eigenschaftenblatthandler zu registrieren, fügen Sie seine GUID dem **PropertySheetHandlers-Unterschlüssel** hinzu, der der Systemsteuerung Anwendung zugeordnet ist. Erstellen Sie hierzu einen Unterschlüssel des **PropertySheetHandlers-Unterschlüssels,** der für den Eigenschaftenblatthandler benannt ist, und legen Sie dessen Standardwert auf die Zeichenfolgenform der GUID des Handlers fest.

Im folgenden Beispiel wird pro Computer ein Eigenschaftenblatthandler für die Anwendung Mouse Systemsteuerung registriert. Um sie pro Benutzer zu registrieren, ersetzen Sie **HKEY \_ LOCAL \_ MACHINE** \\ **REGSTR \_ PATH \_ CONTROLSFOLDER durch** **HKEY CURRENT \_ \_ USER** \\ **REGSTR \_ PATH \_ CONTROLPANEL**.

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a>Schritt 2: Implementieren eines Eigenschaftenblatthandlers für eine Systemsteuerung Anwendung

Das Verfahren zum Implementieren eines Systemsteuerung Eigenschaftenblatthandlers ähnelt sehr dem unter [Registrieren und Implementieren eines Eigenschaftenblatthandlers für einen Dateityp](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)beschriebenen Verfahren. Der Hauptunterschied besteht darin, dass [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) jetzt eine Nichttokenimplementierungen anstelle von [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)benötigt.

Wenn eine Systemsteuerung Anwendung ihr Eigenschaftenblatt anzeigen wird, ruft sie einmal für jede Seite, die ersetzt werden kann, die [**IShellPropSheetExt::ReplacePage-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) des Eigenschaftenblatthandlers auf. Der *uPageID-Parameter* wird auf die ID der Seite festgelegt. Die IDs für die verfügbaren Seiten werden in Cplext.h definiert. Die derzeit verfügbaren IDs sind in der folgenden Tabelle aufgeführt. 

| Seiten-ID                      | BESCHREIBUNG         | Systemsteuerung Anwendung |
|------------------------------|---------------------|---------------------------|
| \_ \_ CPLPAGE-MAUSTASTEN      | Seite "Schaltflächen"    | Maus                     |
| CPLPAGE \_ MOUSE \_ PTRMOTION    | Seite "Bewegung"     | Maus                     |
| \_CPLPAGE-MAUSRAD \_        | Seite "Rad"      | Maus                     |
| \_CPLPAGE-TASTATURGESCHWINDIGKEIT \_     | Seite "Geschwindigkeit"      | Tastatur                  |
| \_CPLPAGE-ANZEIGEHINTERGRUND \_ | Seite "Hintergrund" | Anzeige                   |



 

## <a name="remarks"></a>Hinweise

Das Verfahren zum Erstellen und Ersetzen einer Seite ist identisch mit dem Verfahren zum Hinzufügen einer Seite. Weitere Informationen finden Sie unter [Registrieren und Implementieren eines Eigenschaftenblatthandlers für einen Dateityp.](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)

 

 



