---
title: Ändern der Echo Dialog-Ressource
description: Ändern der Echo Dialog-Ressource
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Windows Media Player-Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-ins, Echo Sample-Eigenschaften Seiten
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample-Eigenschaften Seiten
- DSP-Plug-ins, Echo Sample-Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Eigenschaften Seiten
- Echo DSP-Plug-in-Beispiel, Dialog Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310644"
---
# <a name="modifying-the-echo-dialog-resource"></a>Ändern der Echo Dialog-Ressource

Sie müssen die Dialogfeld Ressource ändern, bei der es sich um die Benutzeroberfläche des Eigenschaften Seiten Objekts handelt. Sie können zuerst das vorhandene Bearbeitungsfeld und die Bezeichnung so ändern, dass Sie für die Eigenschaft Verzögerungszeit nützlich sind, und dann ein zweites Bearbeitungsfeld und eine Bezeichnung für die Eigenschaft "nass Mischung" hinzufügen.

So bearbeiten Sie die Dialog Ressource in Visual C++:

1.  Klicken Sie im Projekt Arbeitsbereich auf die Registerkarte **resourceview** .
2.  Erweitern Sie die strukturressourcen, indem Sie den Ordner auf oberster Ebene öffnen.
3.  Öffnen Sie den **Dialog** Ordner.
4.  Doppelklicken Sie auf den Ressourcennamen des Dialog Felds, IDD \_ echoproppage. Der Ressourcen-Editor wird im rechten Bereich angezeigt.

## <a name="changing-the-existing-resources"></a>Ändern der vorhandenen Ressourcen

So ändern Sie die vorhandenen Eigenschaften Seiten Ressourcen für die Eigenschaft Verzögerungszeit:

1.  Ändern Sie zunächst den Text im vorhandenen statischen Text Steuerelement. Klicken Sie mit der rechten Maustaste auf das Steuerelement und dann auf **Eigenschaften**. Geben Sie im Feld **Beschriftung** die neue Beschriftung ein:
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  Schließen Sie das Dialogfeld Text Eigenschaften.
3.  Ändern Sie nun den Namen des Steuer Elements "Bearbeitungsfeld". Klicken Sie hierzu mit der rechten Maustaste auf das Steuerelement, und wählen Sie dann **Eigenschaften** aus. Geben Sie im Feld **ID** einen neuen Namen für das Steuerelement ein:
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  Schließen Sie das Dialogfeld Eigenschaften bearbeiten.
5.  Speichern Sie die Ressource.
6.  **Ja** , wenn Sie aufgefordert werden, die Datei "Resource. h" erneut zu laden
7.  Klicken Sie im Projekt Arbeitsbereich auf die Registerkarte **fileview** . Ressource öffnen. h
8.  Suchen \# Sie die Ressource für das Bearbeitungsfeld für den Skalierungsfaktor (IDC \_ scalefactor), und löschen Sie Sie. Er muss dieselbe ID-Nummer wie IDC \_ Delta Time aufweisen.

## <a name="adding-the-new-resources"></a>Hinzufügen der neuen Ressourcen

Zum Hinzufügen der neuen Eigenschaften Seiten Ressourcen für die Eigenschaft "nass Mischung":

1.  Klicken Sie im Projekt Arbeitsbereich auf die Registerkarte **resourceview** , um Sie auszuwählen.
2.  Doppelklicken Sie auf den Namen des Dialog Felds Eigenschaften Seite, IDD \_ echoproppage. Der Ressourcen-Editor wird im rechten Bereich angezeigt.
3.  Verwenden Sie die Toolbox, um der Eigenschaften Seite ein statisches Text Steuerelement und ein Bearbeitungsfeld hinzuzufügen.
4.  Klicken Sie mit der rechten Maustaste auf das statische Text Steuerelement, **und wählen Sie**
5.  Geben Sie im Feld **ID** einen neuen Namen für das statische Text Steuerelement ein:
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  Geben Sie eine Beschriftung für die Bezeichnung ein:
    ```C++
    Effect level (%):
    
    ```

    

7.  Schließen Sie das Dialogfeld Text Eigenschaften.
8.  Klicken Sie mit der rechten Maustaste, und wählen Sie **Eigenschaften** aus.
9.  Geben Sie im Feld **ID** einen neuen Namen für das Bearbeitungsfeld ein:
    ```C++
    IDC_WETMIX
    
    ```

    

10. Schließen Sie das Dialogfeld Eigenschaften bearbeiten.

Wenn Sie das Projekt speichern, werden Sie möglicherweise aufgefordert, "Resource. h" neu zu laden. Klicken Sie in diesem Fall auf **Ja** . Der Ressourcen-Editor des Dialog Felds sollte "Resource. h" die Ressourcennamen und ID-Nummern für die hinzugefügten Elemente hinzufügen. Wenn dies nicht der Fall ist, müssen Sie "Resource. h" öffnen und neue Einträge für das Steuerelement "Bezeichnung" und "Bearbeitungsfeld" eingeben und jedem eine eindeutige ID-Nummer zuweisen.

## <a name="modifying-and-adding-the-string-resources"></a>Ändern und Hinzufügen der Zeichen folgen Ressourcen

Der Beispielcode des Plug-in-Assistenten gibt eine Zeichen folgen Ressource mit dem Namen IDs \_ scalerangeerror an, die eine Meldung enthält, die angezeigt wird, wenn die Benutzereingabe außerhalb des gültigen Bereichs liegt. Sie können diese Ressource so ändern, dass Sie Ihren Anforderungen für den Wert für Verzögerungszeit entspricht, indem Sie die folgenden Schritte in Visual C++ ausführen:

1.  Klicken Sie auf die Registerkarte **resourceview** .
2.  Öffnen Sie den Zeichen folgen- **Tabellen** Ordner.
3.  Doppelklicken Sie auf das Symbol **Zeichen folgen Tabelle** , um den Ressourcen-Editor zu öffnen.
4.  Doppelklicken Sie auf den Namen der Ressource, die Sie bearbeiten möchten, in diesem Fall IDs \_ scalerangeerror. Das Dialogfeld Zeichen folgen Eigenschaften wird angezeigt.
5.  Ändern Sie den Namen im Feld ID in IDs Delta- **ID** - \_ Fehler.
6.  Ändern Sie den Text im **Beschriftungs** Feld:
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  Schließen Sie das Dialogfeld Zeichen folgen Eigenschaften.

Fügen Sie als nächstes eine neue Zeichen folgen Ressource für die Fehlermeldung der nass Mischungs Eigenschaft hinzu.

1.  Doppelklicken Sie auf die leere Zeile am unteren Rand des Ressourcen-Editors.
2.  Ändern Sie den Namen im Feld **ID** in IDs \_ mixrangeerror.
3.  Fügen Sie dem **Beschriftungs** Feld den folgenden Text hinzu:
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  Schließen Sie das Dialogfeld Zeichen folgen Eigenschaften.

Es gibt zwei weitere Werte, die Sie in der Zeichen folgen Tabelle ändern möchten. IDs \_ FriendlyName ist der Name, der in der Windows Media Player-Benutzeroberfläche angezeigt wird, um das Plug-in zu identifizieren. \_Mit der ID-Beschreibung können Sie den Benutzer über Ihr Plug-in informieren. Beide Zeichen folgen werden als Parameter an die **iwmpmediapluginregistrar:: wmpregisterplayerplugin** -Funktion übergeben, die in der DllRegisterServer-Methode in Echo dll. cpp aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Eigenschaften Seite Echo Sample**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




