---
description: Verwenden von GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Verwenden von GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f12dd613339680ac22352f4538b7029d8c9cea213c55f66e1986a8d32d0a68ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072156"
---
# <a name="using-graphedit"></a>Verwenden von GraphEdit

GraphEdit ist im Microsoft Windows Software Development Kit (SDK) verfügbar ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).

Der Name der GraphEdit-Anwendung ist "graphedt.exe". Nach der Installation des SDK befindet sich "graphedt.exe" im folgenden Verzeichnis: \[ Programme \] \\ Microsoft SDKs \\ Windows Version Bin \\ \[ \] \\ \\ .

Verwenden Sie vor dem Ausführen von GraphEdit das Hilfsprogramm regsvr32, um die folgenden DLLs zu registrieren, die sich im selben Verzeichnis befinden:

-   proppage.dll
-   evrprop.dll

Diese DLLs ermöglichen GraphEdit das Anzeigen von Eigenschaftenseiten für einige der integrierten DirectShow-Filter.

## <a name="build-a-file-playback-graph"></a>Erstellen eines Dateiwiedergabe-Graph

GraphEdit kann ein Filterdiagramm für die Dateiwiedergabe erstellen. Diese Funktion entspricht dem Aufrufen der [**IGraphBuilder::RenderFile-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) in einer Anwendung. Klicken Sie **im Menü** Datei auf **Mediendatei rendern.** GraphEdit zeigt ein Dialogfeld **Datei** öffnen an. Wählen Sie eine Multimediadatei aus, und klicken Sie **auf Öffnen.** GraphEdit erstellt ein Filterdiagramm zur Wiedergabe der ausgewählten Datei.

Sie können auch eine Mediendatei rendern, die sich unter einer URL befindet. Klicken Sie **im Menü** Datei auf **URL rendern.** GraphEdit zeigt ein Dialogfeld an, in das die URL eingegeben werden soll.

## <a name="build-a-filter-graph"></a>Erstellen eines Graph

GraphEdit kann ein benutzerdefiniertes Filterdiagramm erstellen, indem einer der auf Ihrem System registrierten Filter verwendet wird. Klicken Sie **Graph** Menü auf **Filter einfügen.** Ein Dialogfeld wird mit einer Liste der Filter auf Ihrem System angezeigt, die nach Filterkategorie organisiert sind. GraphEdit erstellt diese Liste aus Informationen in der Registrierung. Die folgende Abbildung zeigt das Dialogfeld.

![Welche Filter möchten Sie einfügen?](images/gedit12.png)

Um dem Diagramm einen Filter hinzuzufügen, wählen Sie  den Namen des Filters aus, und klicken Sie auf die Schaltfläche Filter einfügen, oder doppelklicken Sie auf den Filternamen. Nachdem Sie die Filter hinzugefügt haben, können Sie zwei Filter verbinden, indem Sie die Maus vom Ausgabepin eines Filters an den Eingabepin eines anderen Filters ziehen. Wenn die Stecknadeln die Verbindung akzeptieren, zeichnet GraphEdit einen Pfeil, der sie verbindet.

![Verbinden von zwei Filtern](images/gedit-connect.png)

## <a name="run-the-graph"></a>Führen Sie die Graph

Nachdem Sie ein Filterdiagramm in Graph Bearbeiten erstellt haben, können Sie das Diagramm ausführen, um zu sehen, ob es wie erwartet funktioniert. Das **Graph** enthält die Menübefehle **Play**, **Pause** und **Stop**. Diese Befehle rufen auf die [**IMediaControl-Methoden**](/windows/desktop/api/Control/nn-control-imediacontrol) [**Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)bzw. [**Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)auf. Die GraphEdit-Symbolleiste enthält auch Schaltflächen für diese Befehle:

![Pausen-, Wiedergabe- und Stoppschaltflächen](images/gedit-toolbar.png)

> [!Note]  
> Der Befehl GraphEdit **Stop** hält zuerst das Diagramm an und versucht, die Zeit 0 (null) zu erhalten (vorausgesetzt, das Diagramm ist suchbar). Bei der Dateiwiedergabe setzt diese Aktion das Videofenster auf den ersten Frame zurück. GraphEdit ruft dann [**IMediaControl::Stop auf.**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)

 

Wenn das Diagramm durchsetzbar ist, können Sie es suchen, indem Sie den Schieberegler ziehen, der unter der Symbolleiste angezeigt wird. Durch Ziehen des Schiebereglers wird die [**IMediaSeeking::SetPositions-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) aufgerufen.

## <a name="view-property-pages"></a>Anzeigen von Eigenschaftenseiten

Einige Filter unterstützen benutzerdefinierte Eigenschaftenseiten, die eine Benutzeroberfläche zum Festlegen von Eigenschaften für den Filter bereitstellen. Um die Eigenschaftenseite eines Filters in GraphEdit anzuzeigen,  klicken Sie mit der rechten Maustaste auf den Filter, und wählen Sie im Popupfenster Eigenschaften aus. GraphEdit zeigt eine Eigenschaftenseite an, die die vom Filter definierten Eigenschaftenblätter enthält (sofern verfügbar). Darüber hinaus enthält GraphEdit ein Eigenschaftenblatt für jeden Pin im Filter. Die Pin-Eigenschaftenblätter werden durch GraphEdit und nicht durch den Filter definiert. Wenn die Stecknadel verbunden ist, zeigt das Pin-Eigenschaftenblatt den Medientyp für die Verbindung an. Andernfalls werden die bevorzugten Medientypen des Pins aufgeführt.

> [!Note]  
> Um die integrierten Eigenschaftenseiten von GraphEdit verwenden zu können, müssen Sie proppage.dll. Diese DLL ist im Windows SDK verfügbar. Die DLL enthält auch zusätzliche Eigenschaftenseiten für einige DirectShow-Filter. Diese Eigenschaftenseiten werden nur zu Debugzwecken bereitgestellt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Simulieren von Graph Building mit GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



