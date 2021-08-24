---
title: Steuern eines Geräts
description: Sobald Sie Geräte gefunden haben, können Sie sie steuern.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79d6e6993794a4af972af8538b9b1cd56902c34596197836990028b2761ffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656072"
---
# <a name="controlling-a-device"></a>Steuern eines Geräts

Sobald Sie Geräte gefunden haben, können Sie sie steuern.

**So zeigen Sie Geräteeigenschaften an**

1.  Wählen Sie in der Liste **Geräte gefunden ein Gerät** aus.
2.  Klicken Sie **auf Geräteeigenschaften**. Das **Fenster Geräteeigenschaften** wird mit den angeforderten Informationen angezeigt.

> [!Note]  
> Die **Funktion "Präsentation** anzeigen" ist im C++-Beispielcode nicht verfügbar.

 

**So zeigen Sie die Präsentationsseite eines Geräts an**

1.  Wählen Sie in der Liste **Geräte gefunden ein Gerät** aus.
2.  Klicken Sie **auf Präsentation anzeigen.** Ein Internet Explorer wird mit der angeforderten Präsentationsseite angezeigt.

> [!Note]  
> Die **Ansichtsdienst-Desc.** -Funktionalität ist im C++-Beispielcode nicht verfügbar.

 

**So zeigen Sie eine Dienstbeschreibung an**

1.  Sie können die URL zur Dienstbeschreibung in Service **Desc eingeben. URL-Feld.**

    ![Dienstbeschreibungs-URL](images/ucp-url.png)

2.  Klicken Sie **auf View Service Desc (Dienstabbild anzeigen).** Das **Fenster Service Description Viewer** wird angezeigt. Anschließend können Sie die Dienstbeschreibung mithilfe der Strukturansicht durchsuchen. Diese Funktionalität ist im C++-Beispielcode nicht verfügbar.

    ![Fenster "Service Description Viewer"](images/ucp-serv.png)

    Es gibt fünf Befehle, die Sie im Fenster Service Description Viewer verwenden können.



| Schaltfläche                 | Ausgeführte Aktion                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Go                     | Lädt die in service **desc angezeigte Datei. URL-Feld.**                                                                                                                              |
| Aktion festlegen             | Wählen Sie in der Dienstbeschreibungsstruktur einen Aktionsnamen aus, und klicken Sie **auf Aktion festlegen.** Der Aktionsname wird im Hauptfenster generischer UCP in das Feld Invoke **Action** (Aktion **aufrufen)** eingegeben.       |
| Variable festlegen           | Wählen Sie in der Dienstbeschreibungsstruktur einen Variablennamen aus, und klicken Sie **auf Variable festlegen.** Der Variablenname wird in das Feld **Abfragevariable** des Generischen **UCP-Hauptfensters** eingegeben. |
| Auffüllen der Variablenliste | Lädt alle Variablennamen des Diensts in die **Liste Abfragevariable** des Hauptfensters **Generischer UCP.**                                                                           |
| Aktionsliste auffüllen   | Lädt alle Aktionsnamen des Diensts in die **Liste Invoke Action** des Hauptfensters **Generischer UCP.**                                                                              |



 

**So steuern Sie ein Gerät**

1.  Wählen Sie **in der Liste Geräte** gefunden das Gerät aus, das Sie steuern möchten.
2.  Wählen Sie **in der Liste Dienst** auswählen den Dienst aus, den Sie aufrufen möchten, oder wählen Sie die Zustandsvariable aus, die Sie abfragen möchten.

    ![Fenster "Geräte steuern"](images/ucp-contr.png)

    > [!Note]  
    > Der Inhalt der **Dienstliste basiert** auf dem Gerät, das in der Liste Geräte gefunden **ausgewählt** wurde.

     

3.  Wenn Sie den Wert einer Zustandsvariablen für den ausgewählten Dienst herausfinden möchten, geben Sie den Variablennamen in das Feld **Abfragevariable** für den Dienst ein. Klicken Sie auf **Abfragen**. Die Ergebnisse werden im Feld **Abfragezustandswert/Aktionsergebnisargumente** angezeigt.
4.  Wenn Sie eine Aktion für einen Dienst aufrufen möchten, geben Sie den Aktionsnamen in das Feld **Aktion** aufrufen und alle Argumente in das Feld **Aktionsargumente** ein. Klicken Sie **auf Aufrufen.** Die Ergebnisse werden im Feld **Query State Value/Action Out Arguments (Abfragezustandswert/Aktionsauswerte)** angezeigt, falls dies der Fall ist.

    Der Rückgabewert ist im ersten out-Argument enthalten, sofern einer der werte ist.

    > [!Note]  
    > Wenn mehrere Argumente für eine Aktion enthalten sind, trennen Sie sie durch Leerzeichen.

     

5.  Zeigen Sie Ereignisinformationen im Feld **Ereignisse für** den ausgewählten Dienst an.

 

 




