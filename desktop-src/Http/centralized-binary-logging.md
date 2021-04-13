---
title: Zentralisierte binäre Protokollierung
description: Die zentralisierte binäre Protokollierung ist eine Art serverseitiger Protokollierung, die für die Server Sitzung aktiviert werden kann.
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bc7bdc6f7a5fce78ff66e58b4c50eac36be3f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314961"
---
# <a name="centralized-binary-logging"></a>Zentralisierte binäre Protokollierung

Die zentralisierte binäre Protokollierung ist eine Art serverseitiger Protokollierung, die für die Server Sitzung aktiviert werden kann. Die zentralisierte binäre Protokollierung fungiert als zentrale Form der Protokollierung für alle URL-Gruppen, die unter der Server Sitzung erstellt werden, und ermöglicht allen URL-Gruppen in der Server Sitzung, binäre, unformatierte Protokolldaten an eine einzelne Protokolldatei zu senden. Diese Art der Protokollierung kann nur für die Server Sitzung aktiviert werden. Sie kann nicht für die URL-Gruppe aktiviert werden.

## <a name="when-to-use-centralized-binary-logging"></a>Verwendungszwecke der zentralisierten binären Protokollierung

Wenn die Server Sitzung über zahlreiche URL-Gruppen verfügt, kann der Prozess zum Erstellen von Hunderten von formatierten Protokolldateien für einzelne URL-Gruppen und zum Schreiben der Protokolldaten auf einen Datenträger schnell wertvolle CPU-und Speicherressourcen verbrauchen, wodurch Leistungs-und Skalierbarkeits Probleme entstehen. Die zentralisierte binäre Protokollierung minimiert die Menge an Systemressourcen, die für die Protokollierung verwendet werden, während gleichzeitig detaillierte Protokolldaten für Organisationen bereitgestellt werden, für die dies erforderlich ist.

Die zentralisierte binäre Protokollierung ist eine Server Sitzungs Eigenschaft, die bei Aktivierung die Protokollierung für alle URL-Gruppen in der Server Sitzung konfiguriert. Wenn die zentralisierte binäre Protokollierung aktiviert ist, können keine Daten für einzelne URL-Gruppen aufgezeichnet oder formatiert werden. Die zentralisierte Protokolldatei für die binäre Protokollierung verfügt über die Dateinamenerweiterung "Internet binary log" (IBL). Diese Dateinamenerweiterung stellt sicher, dass die Text Hilfsprogramme nicht versuchen, die Protokolldatei für die zentrale binäre Protokollierung zu öffnen und zu lesen.

## <a name="extracting-data-from-the-centralized-binary-log-file"></a>Extrahieren von Daten aus der zentralisierten Binärprotokoll Datei

Die folgenden Schritte werden ausgeführt, um Daten aus einer RAW-Protokolldatei zu extrahieren:

-   Erstellen Sie ein Tool, das die gewünschten Daten aus der Rohdatendatei löscht und extrahiert und die Daten in formatierten Text konvertiert. Sie können die Beschreibungen der Header Datei und des Protokolldatei Formats im IIS 6,0 Software Development Kit auf MSDN anzeigen.
-   Verwenden Sie das Protokoll Parser-Tool zum Extrahieren von Daten aus der Rohdatendatei. Das Log Parser-Tool und seine begleitende Benutzerdokumentation sind in den IIS 6,0 Resource Kit-Tools enthalten.

## <a name="centralized-binary-logging-file-format"></a>Zentralisiertes Binärprotokoll Datei Format

Die Binärprotokoll Datei der zentralisierten Binärprotokollierung besteht aus Datensätzen fester Länge oder Indexdaten Sätzen, die Zeichen folgen Bezeichner enthalten. Die Indexdaten Sätze werden angezeigt, da die Zeichen folgen Felder mit variabler Länge in dem Bemühen, so viele Informationen wie möglich aufzuzeichnen, von numerischen Bezeichnern – Indizes – ersetzt werden, die die Zeichenfolge variabler Länge dem protokollierten Bezeichner zuordnen.

Die rohdatenprotokollierung ist nicht Menschen lesbar und kann nicht mit den meisten verfügbaren Protokoll Analysen gelesen werden. Wenn Sie Daten aus einer unformatierten Protokolldatei extrahieren möchten, können Sie ein Tool erstellen, das die Daten findet und extrahiert und Sie dann in formatierten Text konvertiert.

Weitere Informationen finden Sie unter [Zentralisierte binäre Protokollierung](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) auf Microsoft TechNet.

 

 