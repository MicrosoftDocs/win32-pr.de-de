---
title: Steuern eines Geräts
description: Nachdem Sie Geräte ermittelt haben, können Sie diese Steuern.
ms.assetid: 6d0efb80-d6f5-4b36-a184-19f06afeb2a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ff91339c67b67de5d3e90eda0ce64ebcc68b9e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856784"
---
# <a name="controlling-a-device"></a>Steuern eines Geräts

Nachdem Sie Geräte ermittelt haben, können Sie diese Steuern.

**So zeigen Sie die Geräteeigenschaften an**

1.  Wählen Sie in der Liste **gefundene Geräte** ein Gerät aus.
2.  Klicken Sie auf **Geräteeigenschaften**. Das Fenster **Geräteeigenschaften** wird mit den angeforderten Informationen angezeigt.

> [!Note]  
> Die **View Presentation** -Funktionalität ist im C++-Beispielcode nicht verfügbar.

 

**So zeigen Sie die Präsentationsseite eines Geräts an**

1.  Wählen Sie in der Liste **gefundene Geräte** ein Gerät aus.
2.  Klicken Sie auf **Präsentation anzeigen**. Ein Internet Explorer-Fenster wird mit der angeforderten Präsentationsseite angezeigt.

> [!Note]  
> Die Funktion " **View Service DESC.** " ist im C++-Beispielcode nicht verfügbar.

 

**So zeigen Sie eine Dienst Beschreibung an**

1.  Sie können die URL für die Dienst Beschreibung im **Dienst DESC eingeben. URL** -Feld.

    ![Dienst Beschreibungs-URL](images/ucp-url.png)

2.  Klicken Sie auf **Dienst DESC anzeigen.** Das Fenster **Dienst Beschreibungs-Viewer** wird angezeigt. Anschließend können Sie die Dienst Beschreibung mithilfe der Strukturansicht durchsuchen. Diese Funktion ist im C++-Beispielcode nicht verfügbar.

    ![Dienst Beschreibungs-Viewer-Fenster](images/ucp-serv.png)

    Es gibt fünf Befehle, die Sie im Dienst Beschreibungs-Viewer-Fenster verwenden können.



| Schaltfläche                 | Ausgeführte Aktion                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Go                     | Lädt die Datei, die im **Dienst DESC angezeigt wird. URL** -Feld.                                                                                                                              |
| Aktion festlegen             | Wählen Sie in der Struktur der Dienst Beschreibung einen Aktions Namen aus, und klicken Sie auf **Aktion festlegen**. Der Aktionsname wird in das Feld **Aufruf Aktion** des **generischen Haupt-UCP** -Fensters eingegeben.       |
| Variable festlegen           | Wählen Sie einen Variablennamen in der Dienst Beschreibungs Struktur aus, und klicken Sie auf **Variable festlegen**. Der Variablenname wird in das Feld **Abfrage Variable** des **generischen Haupt-UCP** -Fensters eingegeben. |
| Variablen Liste auffüllen | Lädt alle Variablennamen aller Dienste in die **Abfrage Variablen** Liste des **generischen Haupt-UCP** -Fensters.                                                                           |
| Aktionsliste Auffüllen   | Lädt alle Aktions Namen aller Dienste in die **Aufruf Aktions** Liste des **generischen Haupt-UCP** -Fensters.                                                                              |



 

**So steuern Sie ein Gerät**

1.  Wählen Sie in der Liste **gefundene Geräte** das Gerät aus, das Sie steuern möchten.
2.  Wählen Sie in der Liste **Dienst auswählen** den Dienst aus, den Sie aufrufen möchten, oder wählen Sie die Zustands Variable aus, die Sie Abfragen möchten.

    ![Fenster "Geräte steuern"](images/ucp-contr.png)

    > [!Note]  
    > Der Inhalt der **Dienst Liste** basiert auf dem Gerät, das in der Liste **gefundene Geräte** ausgewählt ist.

     

3.  Wenn Sie den Wert einer Zustandsvariablen für den ausgewählten Dienst ermitteln möchten, geben Sie den Variablennamen in das Feld **Abfrage Variable** für Dienst ein. Klicken Sie auf **Abfragen**. Die Ergebnisse werden im Feld **Abfrage Zustandswert/Aktions Ausgabe Argumente** angezeigt.
4.  Wenn Sie eine Aktion für einen Dienst aufrufen möchten, geben Sie den Namen der Aktion im Feld **Aufruf Aktion** und alle Argumente im Feld **Aktions Argumente** ein. Klicken Sie auf **aufrufen**. Die Ergebnisse werden ggf. im Feld **Abfrage Zustandswert/Aktions Ausgabe Argumente** angezeigt.

    Der Rückgabewert ist, falls vorhanden, im ersten out-Argument enthalten.

    > [!Note]  
    > Wenn mehrere Argumente für eine Aktion vorhanden sind, trennen Sie diese durch Leerzeichen.

     

5.  Anzeigen von Ereignis Informationen im Feld " **Ereignisse** " für den ausgewählten Dienst.

 

 




