---
title: Übersicht über StoClien
description: Das StoClien-Beispiel veranschaulicht, wie der Client strukturierten Speicher verwendet und wie er eine Serverkomponente zur Verwendung dieses Speichers leitet.
ms.assetid: 1f540e0f-2189-4f45-aad3-9b4b56732907
keywords:
- Übersicht über StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a28c8d0f4740b5a1d5f93934fb055d16e2ed9d843bcb11b210e6cde9589d53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661850"
---
# <a name="stoclien-overview"></a>Übersicht über StoClien

## <a name="purpose"></a>Zweck

Der Hauptfokus des [StoClien-Beispiels](structured-storage-client-sample--stoclien-.md) liegt darauf, wie der Client strukturierten Speicher verwendet und wie er eine Serverkomponente anweisen soll, diesen Speicher zu verwenden. Das StoClien-Beispiel veranschaulicht ein Programmiermodell strukturierter Speicherdienste.

## <a name="functionality"></a>Funktionalität

Die [StoClien-Funktionalität](structured-storage-client-sample--stoclien-.md) ähnelt den "scribble"-Beispielen in einigen Versionen Microsoft Visual C++. Der Unterschied zwischen dem StoClien-Beispiel und dem [StoServe-Beispiel](structured-storage-server-sample--stoserve-.md) ist eine interne Architektur, die auf COM-Technologie basiert. Zwischen COM-Client und COM-Server wird eine klare architektonische Unterscheidung beibehalten.

[StoClien lädt](structured-storage-client-sample--stoclien-.md) und speichert seine Zeichnungen im strukturierten Speicher von COM-Verbunddateien.

Im [StoClien-Beispiel](structured-storage-client-sample--stoclien-.md) wird das verbindungsfähige COM-Objekt COPaper erstellt und verwendet, das als CLSID-DllPaper-Komponente auf dem \_ [StoServe-Server bereitgestellt](structured-storage-server-sample--stoserve-.md) wird. Der StoClien-Client erstellt ein COPaper-Objekt und steuert es über die IPaper-Schnittstelle, die das Objekt verfügbar macht. StoClien erhält Zeichnungsdaten vom Benutzer und stellt sie grafisch in einem von ihm verwalteten Fenster dar. StoClien verwendet die COPaper-IPaper-Schnittstelle, um die Zeichnungsdaten in COPaper zu speichern und Dateispeichervorgänge auf diese Daten zu richten.

Ein COPaper COM-Objekt kapselt nur den serverbasierten Speicher der Zeichnungsdokumentdaten: Auf der Serverseite wird kein Grafisches Benutzeroberflächenverhalten bereitgestellt. Das verhalten der grafischen Benutzeroberfläche ist im Client isoliert. Die Datenverwaltungs- und Speicherfunktionen von COPaper-Objekten sind nur über die benutzerdefinierte COM-Schnittstelle IPaper verfügbar.

[StoClien arbeitet](structured-storage-client-sample--stoclien-.md) mit dem COPaper zusammen, um die COPaper-Zeichnungsdaten zu laden und zu speichern. StoClien erhält eine [**IStorage-Schnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istorage) für das Speicherobjekt in einer Verbunddatei. Beim Laden und Speichern übergibt StoClien einen Zeiger auf die **IStorage-Schnittstelle** an COPaper auf dem Server. COPaper verwendet das bereitgestellte **IStorage,** um Streams im Speicher zu erstellen. COPaper kann dann die [**IStream-Standardschnittstelle**](/windows/desktop/api/Objidl/nn-objidl-istream) zum Lesen und Schreiben der verwalteten Zeichnungsdaten verwenden.

COPaper verwaltet nur die Zeichnungsdaten. Es werden keine GUI-Aktionen durchgeführt. [StoClien stellt](structured-storage-client-sample--stoclien-.md) die grafische Benutzeroberfläche für die Zeichnungsanwendung zur Anwendung. Sie kapselt diese in einem zentralen CGuiPaper-C++-Objekt.

[StoClien implementiert](structured-storage-client-sample--stoclien-.md) auch die benutzerdefinierte IPaperSink-Schnittstelle in einem COPaperSink-COM-Objekt und verbindet diese Schnittstelle mit einem entsprechenden Verbindungspunkt im COPaper-Serverobjekt. COPaper verwendet die verbundene IPaperSink-Schnittstelle, um Benachrichtigungen zurück an StoClien zu senden. Die normale GUI-Neuzeichnung der COPaper-Zeichnungsdaten erfolgt in StoClien mithilfe der COPaper-Technologie für verbindende Objekte.

[StoClien](structured-storage-client-sample--stoclien-.md) ist eine Anwendung, die Sie direkt auf normale Weise oder über das Eingabeaufforderungsfenster ausführen können. StoClien akzeptiert einen optionalen Dateinamenparameter in der Befehlszeile.

Im folgenden Beispiel ist Drawing.pap eine Verbunddatei, die dllPaper-kompatible strukturierte Speicherung von Zeichnungsdaten enthält. Wenn kein Parameter für den Namen der Befehlszeilendatei angegeben ist, verwendet [StoClien](structured-storage-client-sample--stoclien-.md) den Standarddateinamen Stoclien.pap und versucht, ihn im gleichen Verzeichnis wie die ausführende Datei Stoclien.exe.

**StoClien c: \\ drawings \\ drawing.pap**

## <a name="support-information"></a>Supportinformationen

Weitere Informationen, Funktionsbeschreibungen und ein Codetutorial für [StoClien](structured-storage-client-sample--stoclien-.md)finden Sie im Abschnitt Code Tour in Stoclien.htm. Weitere Informationen zum Externen Benutzerbetrieb von StoClien finden Sie in den Abschnitten Verwendung und Betrieb in Stoclien.htm. Führen Sie Stoclient.htm Im Hauptverzeichnis des Tutorials aus, und klicken Sie in der Tabelle der Lektionen auf die Lektion StoClien Tutorial.exe, um die Stoclient.htm zu lesen. Klicken Sie alternativ auf Stoclien.htm, nachdem Sie im Explorer das Hauptverzeichnis des Tutorials Windows haben. Weitere Informationen zur Funktionsweise [**von StoServe**](structured-storage-server-sample--stoserve-.md) und zum Verfügbar machen seiner Dienste für StoClien finden Sie unter Stoserve.htm im Hauptverzeichnis des Tutorials. Beachten Sie, dass Sie die Stoserve.dll erstellen müssen, bevor Sie StoClien erstellen. Das Makefile für [**StoServe**](structured-storage-server-sample--stoserve-.md) registriert diesen Server in der Systemregistrierung. Daher müssen Sie [**StoServe**](structured-storage-server-sample--stoserve-.md) erstellen, bevor Sie versuchen, StoClien ausführen zu können.

Weitere Informationen zum Einrichten eines Systems zum Erstellen und Testen der Codebeispiele in dieser COM-Tutorialreihe finden Sie unter [Erstellen von Beispielen.](how-to-build-samples.md) Das angegebene Makefile (MAKEFILE) ist mit Microsoft NMAKE kompatibel. Um einen Debugbuild zu erstellen, geben Sie den NMAKE-Befehl im Eingabeaufforderungsfenster aus.

Der Einfachheit halber wird für jedes Beispiel eine Projektdatei für die Verwendung in Microsoft Visual Studio. Um das Projekt für das [StoClien-Beispiel](structured-storage-client-sample--stoclien-.md) zu laden, führen Visual Studio an der Eingabeaufforderung im Beispielverzeichnis wie folgt aus:

MSDEV STOCLIEN. Dsp

Sie können auch auf die Datei Stoclient.dsp im Windows Explorer doppelklicken, um ein Beispielprojekt in Visual Studio. In Visual Studio können Sie die C++-Klassen der Beispielquelle durchsuchen und im Allgemeinen die anderen Edit-Compile-Debug-Vorgänge ausführen. Beachten Sie, dass die Kompilierung dieser Beispiele aus Visual Studio im Rahmen des Server SDK die ordnungsgemäße Einstellung von Verzeichnispfaden in Visual Studio. Weitere Informationen finden Sie unter [Erstellen von Beispielen.](how-to-build-samples.md)

## <a name="remarks"></a>Hinweise

Das Clientbeispiel und andere zugehörige Beispiele müssen kompiliert werden, bevor Sie den Client ausführen können. Weitere Informationen zum Erstellen der Beispiele finden Sie unter [Erstellen von Beispielen.](how-to-build-samples.md) Wenn Sie die entsprechenden Beispiele erstellt haben, Stoclien.exe die ausführbare Clientdatei, die für dieses Beispiel ausgeführt werden soll.

Die Stoclien.exe-Anwendung stellt die Benutzeroberfläche für dieses Tutorial bereit. Sie führt die zugeordneten, aber unabhängigen Stoserve.dll, um die Client- und Servernutzung des strukturierten COM-Speichers in Verbunddateien zu veranschaulichen.

 

 




