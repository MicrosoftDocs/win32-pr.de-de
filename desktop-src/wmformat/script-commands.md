---
title: Skriptbefehle
description: Skriptbefehle
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows Media-Format-SDK, Skript Befehle
- Advanced Systems Format (ASF), Skript Befehle
- ASF (Advanced Systems Format), Skript Befehle
- Windows Media-Format-SDK, Skript Datenströme
- Advanced Systems Format (ASF), Skript Datenströme
- ASF (Advanced Systems Format), Skript Datenströme
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Skripts, Befehle
- Skripts, Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039812"
---
# <a name="script-commands"></a>Skriptbefehle

Die vom Windows Media SDK unterstützten Skript Befehle sind einfache Zeichen folgen Paare für Name und Wert. Ein allgemeiner Skript Befehl ist beispielsweise "URL", der von Windows Media Player und anderen Wiedergabe-Anwendungen zum Öffnen von Webseiten verwendet wird. Die andere Hälfte des Skript Paars für den Befehl "URL" enthält eine gültige URL (Uniform Resource Serverlocatorpunkt), z `https://www.adatum.com` . b.. Von den Objekten dieses SDK werden keine Unterstützung für bestimmte Befehle bereitgestellt. die Anwendung muss Logik enthalten, um beliebige Befehle zu verarbeiten, die Sie verwenden. Sie können die von Windows Media Player unterstützten Befehle verwenden, um die Kompatibilität mit den meisten Playern aufrechtzuerhalten.

Skript Befehle können auf eine von zwei Arten übermittelt werden: in einem Skript Datenstrom oder im Dateiheader.

## <a name="script-streams"></a>Skript Datenströme

Sie können Skript Befehle in einem eigenen Stream in einer ASF-Datei bereitstellen. Jede Stichprobe in einem Skript Datenstrom enthält die zwei Zeichen Folgen des Name-Wert-Paars. Der Vorteil der Verwendung eines Skript Datenstroms besteht darin, dass die Befehle zur richtigen Präsentationszeit zugestellt werden.

## <a name="script-commands-in-the-file-header"></a>Skript Befehle im Datei Header

Skript Befehle können zum Abrufen zum Zeitpunkt der Wiedergabe in den Dateiheader eingefügt werden. Die Spiel Ende Anwendung ist dafür verantwortlich, die Skript Befehle zum richtigen Zeitpunkt auszuführen. Der Vorteil der Verwendung von Skript Befehlen im Dateiheader besteht darin, dass alle Skript Befehle verfügbar sind, bevor Sie mit dem empfangen von Beispielen beginnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Verwenden von Skript Befehlen**](using-script-commands.md)
</dt> </dl>

 

 




