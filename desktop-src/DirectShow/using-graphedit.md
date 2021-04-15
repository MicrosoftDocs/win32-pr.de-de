---
description: Verwenden von GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Verwenden von GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529522"
---
# <a name="using-graphedit"></a>Verwenden von GraphEdit

GraphEdit ist im Microsoft Windows Software Development Kit (SDK) () verfügbar <https://go.microsoft.com/fwlink/p/?linkid=62332> .

Der Name der GraphEdit-Anwendung ist "graphedt.exe". Nachdem Sie das SDK installiert haben, befindet sich "graphedt.exe" im folgenden Verzeichnis: \[ Programmdateien \] \\ Microsoft SDKs \\ Windows- \\ \[ Version \] \\ bin \\ .

Verwenden Sie vor dem Ausführen von GraphEdit das regsvr32-Hilfsprogramm, um die folgenden DLLs zu registrieren, die sich im selben Verzeichnis befinden:

-   proppage.dll
-   evrprop.dll

Diese DLLs ermöglichen GraphEdit das Anzeigen von Eigenschaften Seiten für einige der integrierten DirectShow-Filter.

## <a name="build-a-file-playback-graph"></a>Erstellen eines Dateiwiedergabe Diagramms

GraphEdit kann ein Filter Diagramm für die Wiedergabe von Dateien erstellen. Diese Funktion entspricht dem Aufrufen der [**igraphbuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) -Methode in einer Anwendung. Klicken Sie im Menü **Datei** auf **Mediendatei Rendering**. GraphEdit zeigt das Dialogfeld **Datei öffnen** an. Wählen Sie eine Multimedia-Datei aus, **und klicken Sie** auf GraphEdit erstellt ein Filter Diagramm, um die Datei wiederzugeben, die Sie ausgewählt haben.

Sie können auch eine Mediendatei an einer URL Rendering. Klicken Sie im Menü **Datei** auf **URL** Wiedergabe. GraphEdit zeigt ein Dialogfeld an, in das Sie die URL eingeben können.

## <a name="build-a-filter-graph"></a>Erstellen eines Filter Diagramms

GraphEdit kann mithilfe eines beliebigen Filters, der auf Ihrem System registriert ist, ein benutzerdefiniertes Filter Diagramm erstellen. Klicken Sie im Menü **Diagramm** auf **Filter einfügen**. Es wird ein Dialogfeld mit einer Liste der Filter in Ihrem System angezeigt, geordnet Nachfilter Kategorie. GraphEdit erstellt diese Liste aus den Informationen in der Registrierung. Die folgende Abbildung zeigt das Dialogfeld.

![welche Filter möchten Sie einfügen?](images/gedit12.png)

Wenn Sie dem Diagramm einen Filter hinzufügen möchten, wählen Sie den Namen des Filters aus, und klicken Sie auf die Schaltfläche **Filter einfügen** , oder Doppelklicken Sie auf den Filternamen. Nachdem Sie die Filter hinzugefügt haben, können Sie zwei Filter verbinden, indem Sie die Maus von der Ausgabe-PIN eines Filters zur Eingabe-PIN eines anderen Filters ziehen. Wenn die Pins die Verbindung akzeptieren, zeichnet GraphEdit einen Pfeil, der Sie verbindet.

![Verbinden von zwei Filtern](images/gedit-connect.png)

## <a name="run-the-graph"></a>Ausführen des Diagramms

Nachdem Sie ein Filter Diagramm in der Graph-Bearbeitung erstellt haben, können Sie das Diagramm ausführen, um zu sehen, ob es erwartungsgemäß funktioniert. Das Menü **Diagramm** enthält die Menübefehle **abspielen**,  **Anhalten und anhalten**. Diese Befehle rufen [**auf, um**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)die [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) -Methoden [**auszuführen**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**anzuhalten**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)und zu stoppen. Die GraphEdit-Symbolleiste verfügt auch über Schaltflächen für diese Befehle:

![anhalten, wiedergeben und stoppen der Schaltflächen](images/gedit-toolbar.png)

> [!Note]  
> Der GraphEdit-Befehl zum **Anhalten hält** zuerst das Diagramm an und versucht, die Zeit NULL (vorausgesetzt, das Diagramm ist suchbar). Bei der Wiedergabe von Dateien setzt diese Aktion das Videofenster auf den ersten Frame zurück. Dann ruft GraphEdit [**IMediaControl:: Station**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)auf.

 

Wenn das Diagramm suchbar ist, können Sie es durchziehen des Schiebereglers, der unterhalb der Symbolleiste angezeigt wird, durchsuchen. Durchziehen des Schiebereglers wird die [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode aufgerufen.

## <a name="view-property-pages"></a>Anzeigen von Eigenschaften Seiten

Einige Filter unterstützen benutzerdefinierte Eigenschaften Seiten, die eine Benutzeroberfläche für das Festlegen von Eigenschaften für den Filter bereitstellen. Um die Eigenschaften Seite eines Filters in GraphEdit anzuzeigen, klicken Sie mit der rechten Maustaste auf den Filter, und wählen Sie im Popup Fenster **Eigenschaften** aus. GraphEdit zeigt eine Eigenschaften Seite an, die die durch den Filter definierten Eigenschaften Blätter enthält (sofern vorhanden). Außerdem enthält GraphEdit ein Eigenschaften Blatt für jede PIN im Filter. Die PIN-Eigenschaften Blätter werden durch GraphEdit, nicht durch den Filter definiert. Wenn die PIN verbunden ist, zeigt das PIN-Eigenschaften Blatt den Medientyp für die Verbindung an. Andernfalls werden die bevorzugten Medientypen der PIN aufgelistet.

> [!Note]  
> Wenn Sie die integrierten Eigenschaften Seiten von GraphEdit verwenden möchten, müssen Sie proppage.dll registrieren. Diese dll ist in der Windows SDK verfügbar. Die dll enthält auch zusätzliche Eigenschaften Seiten für einige DirectShow-Filter. Diese Eigenschaften Seiten werden nur zu Debugzwecken bereitgestellt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Simulieren der Diagramm Erstellung mit GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



