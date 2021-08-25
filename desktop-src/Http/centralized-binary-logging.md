---
title: Zentralisierte binäre Protokollierung
description: Die zentralisierte binäre Protokollierung ist eine Art der serverseitigen Protokollierung, die in der Serversitzung aktiviert werden kann.
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2006270a6bdb2b06748214bff6170b369de791456577caeb62a9abc4b625bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047570"
---
# <a name="centralized-binary-logging"></a>Zentralisierte binäre Protokollierung

Die zentralisierte binäre Protokollierung ist eine Art der serverseitigen Protokollierung, die in der Serversitzung aktiviert werden kann. Die zentralisierte binäre Protokollierung fungiert als zentralisierte Form der Protokollierung für alle URL-Gruppen, die unter der Serversitzung erstellt wurden, und ermöglicht es allen URL-Gruppen unter der Serversitzung, binäre, unformatierte Protokolldaten an eine einzelne Protokolldatei zu senden. Diese Art der Protokollierung kann nur für die Serversitzung aktiviert werden. sie kann nicht für die URL-Gruppe aktiviert werden.

## <a name="when-to-use-centralized-binary-logging"></a>Verwendung der zentralisierten binären Protokollierung

Wenn die Serversitzung über zahlreiche URL-Gruppen verfügt, kann der Prozess der Erstellung von Hunderten formatierter Protokolldateien für einzelne URL-Gruppen und das Schreiben der Protokolldaten auf einen Datenträger schnell wertvolle CPU- und Arbeitsspeicherressourcen verbrauchen, wodurch Leistungs- und Skalierbarkeitsprobleme entstehen. Die zentralisierte binäre Protokollierung minimiert die Menge der Systemressourcen, die für die Protokollierung verwendet werden, während gleichzeitig detaillierte Protokolldaten für Organisationen zur Verfügung stehen, die sie benötigen.

Die zentralisierte binäre Protokollierung ist eine Serversitzungseigenschaft, die bei Aktivierung die Protokollierung für alle URL-Gruppen in der Serversitzung konfiguriert. Wenn die zentralisierte binäre Protokollierung aktiviert ist, können Daten nicht für einzelne URL-Gruppen aufgezeichnet oder formatiert werden. Die protokolldatei für die zentralisierte binäre Protokollierung verfügt über die Dateinamenerweiterung Internet binary log (.ibl). Diese Dateinamenerweiterung stellt sicher, dass Text-Hilfsprogramme nicht versuchen, die zentrale binäre Protokollierungsprotokolldatei zu öffnen und zu lesen.

## <a name="extracting-data-from-the-centralized-binary-log-file"></a>Extrahieren von Daten aus der zentralisierten binären Protokolldatei

Die folgenden Schritte werden ausgeführt, um Daten aus einer unformatierten Protokolldatei zu extrahieren:

-   Erstellen Sie ein Tool, das die gewünschten Daten aus der Rohdatendatei sucht und extrahiert und die Daten in formatierten Text konvertiert. Sie können eine Beschreibung des Header- und Protokolldateiformats im IIS 6.0 Software Development Kit auf MSDN anzeigen.
-   Verwenden Sie das Protokollparsertool, um Daten aus der Rohdatendatei zu extrahieren. Das Protokollparsertool und die zugehörige Benutzerdokumentation sind in den IIS 6.0 Resource Kit Tools enthalten.

## <a name="centralized-binary-logging-file-format"></a>Zentralisiertes binäres Protokollierungsdateiformat

Die unformatierte protokolldatei für die zentralisierte binäre Protokollierung besteht aus Datensätzen fester Länge oder Indexdatensätzen, die Zeichenfolgenbezeichner enthalten. Die Indexdatensätze werden angezeigt, da bei dem Versuch, so viele Informationen wie möglich aufzuzeichnen, Zeichenfolgenfelder variabler Länge durch numerische Bezeichner (Indizes) ersetzt werden, die die Zeichenfolge variabler Länge dem protokollierten Bezeichner zuordnen.

Die unformatierte Protokolldatei ist nicht lesbar und kann nicht mit den meisten verfügbaren Protokollanalysetools gelesen werden. Um Daten aus einer unformatierten Protokolldatei zu extrahieren, können Sie ein Tool erstellen, das die Daten sucht und extrahiert und dann in formatierten Text konvertiert.

Weitere Informationen finden Sie unter [Zentralisierte binäre Protokollierung](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) auf Microsoft TechNet.

 

 