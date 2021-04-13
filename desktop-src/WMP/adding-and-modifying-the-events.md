---
title: Hinzufügen und Ändern der Ereignisse
description: Hinzufügen und Ändern der Ereignisse
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c8e069c20dc2c953998b9e5c2a47f509166ca3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310607"
---
# <a name="adding-and-modifying-the-events"></a>Hinzufügen und Ändern der Ereignisse

Sie müssen Ereignishandler für die en- \_ Änderungs Ereignisse angeben, die auftreten, wenn der Benutzer den Text in den Bearbeitungs Feldern der Eigenschaften Seite ändert. Diese Ereignishandler verfügen über eine einfache Implementierung, die im Dialogfeld Eigenschaften Seite nur die Option **anwenden** ermöglicht.

## <a name="modifying-the-scale-factor-event-handler"></a>Ändern des Skalierungsfaktor-Ereignis Handlers

Sie müssen den Namen des vorhandenen Ereignis Handlers ändern, den der Plug-in-Assistent für das Bearbeitungsfeld "Skalierungsfaktor" bereitgestellt hat. Sie sollten den Namen in "onchangescale" in "onchangedelay" an drei Stellen ändern:

1.  Ändern Sie in "echoproppage. h" den Namen im Abschnitt "Message Map Macro". Ersetzen Sie die Zeile, in der das Ereignis für den Skalierungsfaktor geändert wird, mit dem folgenden Code der onchangescale-Methode:
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  Ändern Sie in "echoproppage. h" den Namen in der Zeile, in der die onchangescale-Funktion Prototypen ist:
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  Ändern Sie in "echoproppage. cpp" den Namen im Funktions Header:
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a>Hinzufügen des nass Mischungs Ereignis Handlers

Sie können problemlos den Ereignishandler für das en- \_ Änderungs Ereignis hinzufügen, das an das Steuerelement für den IDC- \_ wetmix-Bearbeitungsfeld angefügt ist. Im Dialogfeld Ressourcen-Editor:

1.  Klicken Sie mit der rechten Maustaste auf das \_ Bearbeitungsfeld IDC wetmix, und wählen Sie **Ereignisse**. Das Dialogfeld neue Windows-Meldung und Ereignishandler wird angezeigt.
2.  Klicken Sie im Feld **zu behandelnde Klasse oder Objekt auf** den Namen der Bearbeitungsfeld Ressource, IDC- \_ wetmix.
3.  Klicken Sie im Feld **neue Windows-Meldungen/Ereignisse** \_ auf en ändern, um es auszuwählen.
4.  Klicken Sie auf **Handler hinzufügen**. Das Dialogfeld Element Funktion hinzufügen wird angezeigt.
5.  Geben Sie im Feld Element **Funktionsname** den Namen onchangewetmix ein.
6.  Klicken Sie auf **OK** , um das Dialogfeld Element Funktion hinzufügen zu schließen.
7.  Klicken Sie auf **OK** , um zum Dialogfeld Ressourcen-Editor zurückzukehren.

Visual C++ fügt automatisch den Code für die Meldungs Zuordnung und die Ereignishandlerfunktion in "echoproppage. h" ein. Der Code, den er einfügt, bietet einen TODO-Kommentar, in dem Sie die-Implementierung in den-Header für die Funktion einfügen können. Dies ist ein etwas anderes Format als der Windows Media Player Plug-in-Assistent, der Beispielcode verwendet, aber akzeptabel ist.

Ob Sie Ihre Implementierung in die Header Datei schreiben oder Sie in "echoproppage. cpp" verschieben möchten, ist Ihnen überlassen. In beiden Fällen benötigt die Implementierung nur eine einzige zusätzliche Codezeile, um **Apply** im Dialogfeld der Eigenschaften Seite zu aktivieren. Fügen Sie diese Codezeile vor der Zeile ein, die von der-Funktion zurückgegeben wird:


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Eigenschaften Seite Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




