---
title: Ändern der Echodialogressource
description: Ändern der Echodialogressource
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Windows Media Player-Plug-Ins, Echo-Beispieleigenschaftenseiten
- Plug-Ins, Echo-Beispieleigenschaftenseiten
- Digitale Signalverarbeitungs-Plug-Ins, Echo-Beispieleigenschaftenseiten
- DSP-Plug-Ins, Echo-Beispieleigenschaftenseiten
- Echo-DSP-Plug-In-Beispiel, Eigenschaftenseiten
- Echo-DSP-Plug-In-Beispiel, Dialogressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37dc88fe2c1b85dfc08727a00e744f1c5c16a2f25a4c5d429b2ab13898b0fcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996140"
---
# <a name="modifying-the-echo-dialog-resource"></a>Ändern der Echodialogressource

Sie müssen die Dialogressource ändern, die die Benutzeroberfläche für das Eigenschaftenseitenobjekt ist. Sie können zuerst das vorhandene Bearbeitungsfeld und die Bezeichnung ändern, damit sie für die Verzögerungszeiteigenschaft nützlich sind, und dann ein zweites Bearbeitungsfeld und eine Bezeichnung für die Vernetzmischungseigenschaft hinzufügen.

So bearbeiten Sie die Dialogressource in Visual C++:

1.  Klicken Sie im Project Arbeitsbereich auf die Registerkarte **ResourceView.**
2.  Erweitern Sie die Ressourcenstruktur, indem Sie den Ordner der obersten Ebene öffnen.
3.  Öffnen Sie den Ordner **Dialog.**
4.  Doppelklicken Sie auf den Namen der Dialogressource IDD \_ ECHOPROPPAGE. Der Ressourcen-Editor wird im rechten Bereich angezeigt.

## <a name="changing-the-existing-resources"></a>Ändern der vorhandenen Ressourcen

So ändern Sie die vorhandenen Eigenschaftenseitenressourcen für die Verzögerungszeiteigenschaft:

1.  Ändern Sie zunächst den Text im vorhandenen statischen Textsteuerelement. Klicken Sie mit der rechten Maustaste auf das Steuerelement, und **wählen** Sie eigenschaften aus. Geben Sie im Feld **Caption (Beschriftung)** die neue Beschriftung ein:
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  Schließen Sie das Dialogfeld Texteigenschaften.
3.  Ändern Sie nun den Namen des Bearbeitungsfeld-Steuerelements. Klicken Sie hierzu mit der rechten Maustaste auf das Steuerelement, und **wählen** Sie eigenschaften aus. Geben Sie im Feld **ID** einen neuen Namen für das Steuerelement ein:
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  Schließen Sie das Dialogfeld Eigenschaften bearbeiten.
5.  Speichern Sie die Ressource.
6.  Antworten Sie **mit Ja,** wenn Sie aufgefordert werden, die Datei resource.h erneut zu laden.
7.  Klicken Sie im Project Arbeitsbereich auf die Registerkarte **FileView.** Öffnen Sie resource.h.
8.  Suchen Sie die \# Definition für die Ressource des Skalierungsfaktor-Bearbeitungsfelds (IDC \_ SCALEFACTOR), und löschen Sie sie. Sie sollte die gleiche ID-Nummer wie IDC \_ DELAYTIME aufweisen.

## <a name="adding-the-new-resources"></a>Hinzufügen der neuen Ressourcen

So fügen Sie die neuen Eigenschaftenseitenressourcen für die Vermischungseigenschaft hinzu:

1.  Klicken Sie im Project Arbeitsbereich auf die Registerkarte **ResourceView,** um sie auszuwählen.
2.  Doppelklicken Sie auf den Namen des Eigenschaftenseitendialogfelds IDD \_ ECHOPROPPAGE. Der Ressourcen-Editor wird im rechten Bereich angezeigt.
3.  Verwenden Sie die Toolbox, um der Eigenschaftenseite ein statisches Textsteuerelement und ein Bearbeitungsfeld hinzuzufügen.
4.  Klicken Sie mit der rechten Maustaste auf das statische Textsteuerelement, und wählen Sie **Eigenschaften** aus.
5.  Geben Sie im Feld **ID** einen neuen Namen für das statische Textsteuerelement ein:
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  Geben Sie eine Beschriftung für die Bezeichnung ein:
    ```C++
    Effect level (%):
    
    ```

    

7.  Schließen Sie das Dialogfeld Texteigenschaften.
8.  Klicken Sie mit der rechten Maustaste auf das Bearbeitungsfeld, und wählen Sie **Eigenschaften** aus.
9.  Geben Sie im Feld **ID** einen neuen Namen für das Bearbeitungsfeld ein:
    ```C++
    IDC_WETMIX
    
    ```

    

10. Schließen Sie das Dialogfeld Eigenschaften bearbeiten.

Wenn Sie das Projekt speichern, werden Sie möglicherweise aufgefordert, resource.h erneut zu laden. Klicken Sie in diesem Fall auf **Ja.** Der Ressourcen-Editor des Dialogfelds sollte resource.h die Ressourcennamen und ID-Nummern für die hinzugefügten Elemente hinzufügen. Wenn dies aus irgendeinem Grund nicht der Fall ist, müssen Sie resource.h öffnen und neue Einträge für das Bezeichnungs- und Bearbeitungsfeld-Steuerelement eingeben und jedem eine eindeutige ID-Nummer zuweisen.

## <a name="modifying-and-adding-the-string-resources"></a>Ändern und Hinzufügen der Zeichenfolgenressourcen

Der Beispielcode des Plug-In-Assistenten gibt eine Zeichenfolgenressource mit dem Namen IDS \_ SCALERANGEERROR an, die eine Meldung enthält, die angezeigt wird, wenn die Benutzereingabe außerhalb des Bereichs liegt. Sie können diese Ressource an Ihre Anforderungen für den Verzögerungszeitwert anpassen, indem Sie die folgenden Schritte in Visual C++ ausführen:

1.  Klicken Sie auf die Registerkarte **ResourceView.**
2.  Öffnen Sie den Ordner **Zeichenfolgentabelle.**
3.  Doppelklicken Sie auf das Symbol **Zeichenfolgentabelle,** um den Ressourcen-Editor zu öffnen.
4.  Doppelklicken Sie auf den Namen der Ressource, die Sie bearbeiten möchten, in diesem Fall IDS \_ SCALERANGEERROR. Das Dialogfeld Zeichenfolgeneigenschaften wird angezeigt.
5.  Ändern Sie den Namen im **Feld ID** in IDS \_ DELAYRANGEERROR.
6.  Ändern Sie den Text im Feld **Beschriftung:**
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  Schließen Sie das Dialogfeld Zeichenfolgeneigenschaften.

Fügen Sie als Nächstes eine neue Zeichenfolgenressource für die Fehlermeldung der Vermischungseigenschaft hinzu.

1.  Doppelklicken Sie unten im Ressourcen-Editor auf die leere Zeile.
2.  Ändern Sie den Namen im **Feld ID** in IDS \_ MIXRANGEERROR.
3.  Fügen Sie dem Feld **Caption (Beschriftung)** den folgenden Text hinzu:
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  Schließen Sie das Dialogfeld Zeichenfolgeneigenschaften.

Es gibt zwei weitere Werte, die Sie in der Zeichenfolgentabelle ändern möchten. IDS \_ FRIENDLYNAME ist der Name, der auf der Windows Media Player Benutzeroberfläche angezeigt wird, um das Plug-In zu identifizieren. MIT DER IDS-BESCHREIBUNG \_ können Sie den Benutzer über Ihr Plug-In informieren. Beide Zeichenfolgen werden als Parameter an die **Funktion IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** übergeben, die in der DllRegisterServer-Methode in Echodll.cpp aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ändern der Echo-Beispieleigenschaftenseite**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




