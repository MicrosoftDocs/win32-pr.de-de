---
title: Skriptbefehle
description: Skriptbefehle
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows Medienformat-SDK, Skriptbefehle
- Advanced Systems Format (ASF), Skriptbefehle
- ASF (Advanced Systems Format), Skriptbefehle
- Windows Medienformat-SDK, Skriptstreams
- Advanced Systems Format (ASF), Skriptstreams
- ASF (Advanced Systems Format), Skriptstreams
- Windows Medienformat-SDK,Streams
- Advanced Systems Format (ASF),streams
- ASF (Advanced Systems Format), Streams
- Skripts, Befehle
- Skripts,Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6f6487958db820892f57af2b1348dcd4304031976aaaf56ddeb6233e1b8a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197528"
---
# <a name="script-commands"></a>Skriptbefehle

Die skriptbefehle, die vom Windows Media Format SDK unterstützt werden, sind einfache Name-Wert-Zeichenfolgenpaare. Ein gängiger Skriptbefehl ist z. B. "URL", der von Windows Media Player und anderen Abspielanwendungen zum Öffnen von Webseiten verwendet wird. Die andere Hälfte des Skriptpaars für den Befehl "URL" enthält eine gültige URL (Uniform Resource Locator), z. `https://www.adatum.com` B. . Die Objekte dieses SDK unterstützen keine bestimmten Befehle. Ihre Anwendung muss Logik für die Handhabung der von Ihnen verwendeten Befehle enthalten. Sie können die befehle verwenden, die von Windows Media Player, um die Kompatibilität mit den meisten Playern zu gewährleisten.

Skriptbefehle können auf zwei Arten übermittelt werden: in einem Skriptstream oder im Dateiheader.

## <a name="script-streams"></a>Skript Streams

Sie können Skriptbefehle in einem eigenen Stream in einer ASF-Datei senden. Jedes Beispiel in einem Skriptstream enthält die beiden Zeichenfolgen des Name-Wert-Paars. Der Vorteil der Verwendung eines Skriptstreams ist, dass die Befehle zur richtigen Präsentationszeit übermittelt werden.

## <a name="script-commands-in-the-file-header"></a>Skriptbefehle im Dateiheader

Skriptbefehle können zum Zeitpunkt der Wiedergabe zum Abrufen in den Dateiheader eingeschlossen werden. Die Wiedergabeanwendung ist dafür verantwortlich, die Skriptbefehle zum richtigen Zeitpunkt auszuführen. Der Vorteil der Verwendung von Skriptbefehlen im Dateiheader ist, dass alle Skriptbefehle verfügbar sind, bevor Sie mit dem Empfangen von Beispielen beginnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**Verwenden von Skriptbefehlen**](using-script-commands.md)
</dt> </dl>

 

 




