---
title: Hinzufügen und Ändern der Ereignisse
description: Hinzufügen und Ändern der Ereignisse
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Windows Media Player-Plug-Ins,Echo-Beispieleigenschaftsseiten
- Plug-Ins, Echo-Beispieleigenschaftsseiten
- Plug-Ins für die digitale Signalverarbeitung, Echo-Beispiel-Eigenschaftenseiten
- DSP-Plug-Ins, Echo-Beispiel-Eigenschaftenseiten
- Echo DSP-Plug-In-Beispiel, Eigenschaftenseiten
- Echo DSP-Plug-In-Beispiel,Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 464d20b600a5535e3cf2c02be01fa19c10a590e143c7a96375580719b70c274c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865340"
---
# <a name="adding-and-modifying-the-events"></a>Hinzufügen und Ändern der Ereignisse

Sie müssen Ereignishandler für die EN CHANGE-Ereignisse enthalten, die auftreten, wenn der Benutzer den Text in den Bearbeitungsfeldern \_ der Eigenschaftenseite ändert. Diese Ereignishandler verfügen über eine einfache  Implementierung, die im Eigenschaftenseitendialogfeld nur Anwenden aktiviert.

## <a name="modifying-the-scale-factor-event-handler"></a>Ändern des Scale Factor-Ereignishandlers

Sie müssen den Namen des vorhandenen Ereignishandlers ändern, den der Plug-In-Assistent für das Bearbeitungsfeld für Skalierungsfaktor bereitgestellt hat. Sie sollten den Namen an drei Stellen von OnChangeScale in OnChangeDelay ändern:

1.  Ändern Sie in EchoPropPage.h den Namen im Abschnitt mit dem Nachrichtenzuordnungsmakro. Ersetzen Sie die Zeile, die das Skalierungsfaktoränderungsereignis der OnChangeScale-Methode zu ordnet, durch den folgenden Code:
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  Ändern Sie in EchoPropPage.h den Namen in der Zeile, die den Prototyp der OnChangeScale-Funktion erstellt:
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  Ändern Sie in EchoPropPage.cpp den Namen im Funktionsheader:
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a>Hinzufügen des Vermischungsmischungsereignishandlers

Sie können problemlos den Ereignishandler für das EN CHANGE-Ereignis hinzufügen, das an \_ das Bearbeitungsfeld-Steuerelement IDC \_ VERDRMIX angefügt ist. Im Ressourcen-Editor des Dialogfelds:

1.  Klicken Sie mit der rechten Maustaste auf das Bearbeitungsfeld IDC \_ VERDRMIX, und wählen Sie **Ereignisse aus.** Das Dialogfeld Neue Windows und Ereignishandler wird angezeigt.
2.  Klicken Sie **im Feld Klasse oder Zu behandelnde** Objekt auf den Namen der Bearbeitungsfeldressource IDC \_ VERDRMIX.
3.  Klicken Sie **im Windows Nachrichten/Ereignisse** auf ÄNDERN, \_ um es auszuwählen.
4.  Klicken Sie **auf Handler hinzufügen.** Das Dialogfeld Memberfunktion hinzufügen wird angezeigt.
5.  Geben Sie **im Feld Member function name** (Name der Memberfunktion) den Namen OnChangeWetmix ein.
6.  Klicken Sie **auf OK,** um das Dialogfeld Memberfunktion hinzufügen zu schließen.
7.  Klicken Sie **auf OK,** um zum Ressourcen-Editor des Dialogfelds zurückzukehren.

Visual C++ fügt echoPropPage.h automatisch den Code für die Meldungszuordnung und für die Ereignishandlerfunktion hinzu. Der eingefügte Code stellt einen TODO-Kommentar zur Verfügung, in dem Sie die Implementierung im Header für die Funktion hinzufügen können. Dies ist ein etwas anderer Stil als der Windows Media Player Code des Plug-In-Assistenten verwendet, ist aber akzeptabel.

Ob Sie Ihre Implementierung in die Headerdatei schreiben oder in EchoPropPage.cpp verschieben möchten, liegt bei Ihnen. In beiden Fällen benötigt die Implementierung nur eine einzige zusätzliche Codezeile, um **Anwenden** im Dialogfeld der Eigenschaftenseite zu aktivieren. Fügen Sie diese Codezeile vor der Zeile ein, die von der Funktion zurückgegeben wird:


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Eigenschaftenseite des Echobeispiels**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




