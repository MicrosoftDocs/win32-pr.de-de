---
description: Beispiel für Async-Filter
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Beispiel für Async-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041292"
---
# <a name="async-filter-sample"></a>Beispiel für Async-Filter

## <a name="description"></a>BESCHREIBUNG

Das Beispiel Async Filter ist ein Datei Leser Filter, der progressiven Download unterstützt. Dieser Beispiel Filter implementiert die Schnittstellen [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) und [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) . MPEG-Dateien werden unterstützt, aber keine AVI-Dateien.

## <a name="usage"></a>Verbrauch

Dieses Beispiel enthält eine kleine Befehlszeilen Anwendung, Memfile.exe, die den Filter veranschaulicht. Die Befehlszeilenargumente geben eine Mediendatei und eine Bitrate in Kilobyte pro Sekunde an. Die Anwendung liest die Datei mit der angegebenen Rate in den Arbeitsspeicher und gibt die Datei wieder. Zu diesem Zweck wird eine Instanz des Filters erstellt, dem Filter Diagramm der Filter hinzugefügt und die Ausgabe-PIN des Filters gerendert.

Geben Sie an der Befehlszeile den folgenden Befehl ein:

**Memfile-Dateiname Bitrate**  

Der ASYNC-Beispiel Filter unterstützt keine AVI-Dateien, da er keine Verbindung mit dem [avi-Splitter](avi-splitter-filter.md) Filter herstellen kann. Die Ausgabe-PIN des Async-Filters schlägt den MediaType- \_ Stream und mediasubtype \_ NULL für den Medientyp vor. Die Eingabe-PIN im AVI-Splitter Filter akzeptiert nicht mediasubtype \_ null und schlägt keine eigenen Typen vor. Daher tritt bei der Pin-Verbindung ein Fehler auf. Der Async-Filter kann erweitert werden, um bei Bedarf mediasubtype \_ AVI anzubieten. Beispielsweise könnte Sie das Dateiformat untersuchen oder die Dateierweiterung verwenden.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: \[ *SDK Root* \] \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Async.

## <a name="related-topics"></a>Zugehörige Themen



[DirectShow-Beispiele](directshow-samples.md)


 

 



