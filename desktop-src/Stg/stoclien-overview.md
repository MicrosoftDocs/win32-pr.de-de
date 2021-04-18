---
title: Übersicht über stoclien
description: Das stoclien-Beispiel veranschaulicht, wie der Client strukturierte Speicher verwendet und wie er eine Serverkomponente anweist, diesen Speicher zu verwenden.
ms.assetid: 1f540e0f-2189-4f45-aad3-9b4b56732907
keywords:
- Übersicht über stoclien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee37f6f84cf981bda637abbd96ff8e8f0314d8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338567"
---
# <a name="stoclien-overview"></a>Übersicht über stoclien

## <a name="purpose"></a>Zweck

Der Hauptschwerpunkt des [stoclien](structured-storage-client-sample--stoclien-.md) -Beispiels ist, wie der Client strukturierte Speicher verwendet und wie er eine Serverkomponente anweist, diesen Speicher zu verwenden. Das stoclien-Beispiel veranschaulicht ein Programmiermodell strukturierter Speicherdienste.

## <a name="functionality"></a>Funktionalität

Die [stoclien](structured-storage-client-sample--stoclien-.md) -Funktionalität ähnelt den "Scribble"-Beispielen in einigen Versionen von Microsoft Visual C++. Der Unterschied zwischen dem stoclien-Beispiel und dem [stoservicesbeispiel](structured-storage-server-sample--stoserve-.md) ist eine interne Architektur, die auf der com-Technologie basiert. Zwischen com-Client und com-Server wird eine deutliche Unterscheidung der Architektur beibehalten.

[Stoclien](structured-storage-client-sample--stoclien-.md) lädt und speichert seine Zeichnungen in der strukturierten Speicherung von com-Verbund Dateien.

Das [stoclien](structured-storage-client-sample--stoclien-.md) -Beispiel erstellt und verwendet das Verbindungs fähige copaper-com-Objekt, das als CLSID- \_ dllpaper-Komponente auf dem [stoservice](structured-storage-server-sample--stoserve-.md) -Server bereitgestellt wird. Der stoclien-Client erstellt ein copaper-Objekt und steuert es über die iPaper-Schnittstelle, die das Objekt verfügbar macht. Stoclien ruft Zeichnungsdaten vom Benutzer ab und stellt Sie grafisch in einem von ihm verwalteten Fenster dar. Stoclien verwendet die copaper iPaper-Schnittstelle zum Speichern der Zeichnungsdaten im copaper und zum Weiterleiten von Dateispeicher Vorgängen an diese Daten.

Ein copaper com-Objekt kapselt nur den serverbasierten Speicher der Zeichnungs Papier Daten: auf der Serverseite wird kein grafisches GUI-Verhalten (Graphical User Interface) bereitgestellt. Das gesamte GUI-Verhalten ist im Client isoliert. Die Daten Verwaltungs-und Speicherfunktionen von copaper-Objekten sind nur über eine benutzerdefinierte COM-Schnittstelle (iPaper) verfügbar.

[Stoclien](structured-storage-client-sample--stoclien-.md) arbeitet mit dem copaper zusammen, um die kopierdaten zu laden und zu speichern. Stoclien erhält eine [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle für das Speicher Objekt in einer Verbund Datei. In den Lade-und Speicher Vorgängen übergibt stoclien einen Zeiger an die **IStorage** -Schnittstelle auf dem Server. Copaper verwendet den bereitgestellten **IStorage** , um Streams im Speicher zu erstellen. Copaper kann dann die standardmäßige [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstelle verwenden, um die von ihr verwalteten Zeichnungsdaten zu lesen und zu schreiben.

Copaper verwaltet nur die Zeichnungsdaten; Es führt keine GUI-Aktionen aus. [Stoclien](structured-storage-client-sample--stoclien-.md) stellt die GUI für die Zeichnungsanwendung bereit. Dies wird in einem zentralen cguipaper C++-Objekt gekapselt.

[Stoclien](structured-storage-client-sample--stoclien-.md) implementiert auch die benutzerdefinierte ipapersink-Schnittstelle in einem copapersink-com-Objekt und verbindet diese Schnittstelle mit einem entsprechenden Verbindungspunkt im Server-copaper-Objekt. Copaper verwendet die verbundene ipapersink-Schnittstelle, um Benachrichtigungen zurück an stoclien zu senden. Das normale GUI-Neuzeichnen der copaper-Zeichnungsdaten erfolgt in stoclien mithilfe der kopierbaren Verbindungs fähigen-Objekttechnologie.

[Stoclien](structured-storage-client-sample--stoclien-.md) ist eine Anwendung, die Sie direkt oder über das Eingabe Aufforderungs Fenster ausführen können. Stoclien akzeptiert einen optionalen Dateinamen Parameter in der Befehlszeile.

Im folgenden Beispiel ist Drawing. PAP eine Verbund Datei, die eine mit dllpaper kompatible strukturierte Speicherung von Zeichnungsdaten enthält. Wenn kein Befehlszeilen-Dateiname-Parameter angegeben ist, wird von [stoclien](structured-storage-client-sample--stoclien-.md) der Standard Dateiname stoclien. PAP verwendet, und es wird versucht, das Verzeichnis im gleichen Verzeichnis wie das ausführende Stoclien.exe zu öffnen.

**Stoclien c: \\ Zeichnungen \\ Drawing. PAP**

## <a name="support-information"></a>Supportinformationen

Weitere Informationen, funktionale Beschreibungen und ein Code-Tutorial für [stoclien](structured-storage-client-sample--stoclien-.md)finden Sie im Abschnitt Code Tour in Stoclien.htm. Weitere Informationen zum externen Benutzer Vorgang von stoclien finden Sie in den Abschnitten zu Verwendung und Betrieb in Stoclien.htm. Um Stoclient.htm zu lesen, führen Sie Tutorial.exe im haupttutorial-Verzeichnis aus, und klicken Sie in der Tabelle mit Lektionen auf die stoclien-Lektion. Sie können auch auf Stoclien.htm klicken, nachdem Sie das haupttutorial Verzeichnis in Windows-Explorer gefunden haben. Weitere Informationen zur Funktionsweise von [**stoservice**](structured-storage-server-sample--stoserve-.md) und zur Bereitstellung der zugehörigen Dienste für stoclien finden Sie unter Stoserve.htm im haupttutorial Verzeichnis. Beachten Sie, dass Sie die Stoserve.dll vor dem Erstellen von stoclien erstellen müssen. Das Makefile für [**stoservice**](structured-storage-server-sample--stoserve-.md) registriert diesen Server in der Systemregistrierung. Daher müssen Sie [**stoservice**](structured-storage-server-sample--stoserve-.md) erstellen, bevor Sie versuchen, stoclien auszuführen.

Weitere Informationen zum Einrichten eines Systems zum Erstellen und Testen der Codebeispiele in dieser com-tutorialreihe finden Sie unter [Erstellen von Beispielen](how-to-build-samples.md). Das angegebene Makefile-Element (Makefile) ist Microsoft NMAKE-kompatibel. Wenn Sie einen Debugbuild erstellen möchten, geben Sie im Eingabe Aufforderungs Fenster den Befehl NMAKE aus.

Zur einfacheren Verwendung wird für jedes Beispiel eine Projektdatei bereitgestellt, die in Microsoft Visual Studio verwendet werden kann. Um das Projekt für das [stoclien](structured-storage-client-sample--stoclien-.md) -Beispiel zu laden, führen Sie Visual Studio wie folgt an der Eingabeaufforderung im Beispiel Verzeichnis aus:

Msdev-stoclien. DSP

Sie können auch auf die Datei stoclient. DSP in Windows-Explorer doppelklicken, um ein Beispiel Projekt in Visual Studio zu laden. In Visual Studio können Sie die C++-Klassen der Beispiel Quelle durchsuchen und im Allgemeinen die anderen edit-compile-Debug-Vorgänge durchführen. Beachten Sie, dass die Kompilierung dieser Beispiele in Visual Studio als Teil des Server-SDK die ordnungsgemäße Einstellung von Verzeichnis Pfaden in Visual Studio erfordert. Weitere Informationen finden Sie unter [Erstellen von Beispielen](how-to-build-samples.md).

## <a name="remarks"></a>Bemerkungen

Das Client Beispiel und andere verwandte Beispiele müssen kompiliert werden, bevor Sie den Client ausführen können. Weitere Informationen zum Erstellen der Beispiele finden Sie unter [Erstellen von Beispielen](how-to-build-samples.md). Wenn Sie die entsprechenden Beispiele erstellt haben, ist Stoclien.exe die ausführbare Client Datei für dieses Beispiel.

Die Stoclien.exe-Anwendung stellt die Benutzeroberfläche für dieses Tutorial bereit. Er führt die zugeordneten, aber unabhängigen Stoserve.dll aus, um die Client-und Server Verwendung von com-strukturiertem Speicher in Verbund Dateien zu veranschaulichen.

 

 




