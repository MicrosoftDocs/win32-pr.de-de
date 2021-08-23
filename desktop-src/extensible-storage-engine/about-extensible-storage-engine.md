---
description: Weitere Informationen finden Sie unter Informationen zur erweiterbaren Storage-Engine.
title: Informationen zur erweiterbaren Storage-Engine
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 26a1d4d28f1d5957432202545ff94c4f18c37e5a521e0deadfdabfb72751adec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983870"
---
# <a name="about-extensible-storage-engine"></a>Informationen zur erweiterbaren Storage-Engine


_**Gilt für: Exchange Server** 2013 | Windows | Windows Server_

## <a name="about-extensible-storage-engine"></a>Informationen zur erweiterbaren Storage-Engine

Die erweiterbare Speicher-Engine (Extensible Storage Engine, ESE) ist eine Datenbank-Engine, die Informationen in einer logischen Sequenz speichert. Informationen können entweder sequenziell oder durch Zugriff auf definierte Indizes abgerufen werden. Aktualisierungen der Datenbank werden mit einer Transaktion implementiert, um sichere Vorgänge zu gewährleisten. ESE ermöglicht den gleichzeitigen Zugriff auf mehrere Datenbanken, einschließlich Transaktionsprotokoll-Dateidatenbanken, die für die Systemwiederherstellung verwendet werden können. ESE ist für große oder kleine Anwendungen skalierbar. Die folgenden Features sind mit der ESE-API (Application Programming Interface) verfügbar:

  - Sichern und Wiederherstellen: Eine Anwendung kann konsistente Kopien des Datenzustands erstellen, während sie online ist und den Datenzustand aktiv ändert.

  - Cursornavigation: Die Anwendung kann mit dem Cursor navigieren, um entweder sequenziell oder mithilfe von Indizes auf Daten zu zugreifen.

  - Datenbank: Eine Auflistung von Tabellen, die als einzelne Einheit sichern und wiederhergestellt werden.

  - Protokollierung und Absturzwiederherstellung: Die ESE-API stellt sicher, dass die anwendungsdefinierte Datenkonsistenz auch bei einem Systemabsturz akzeptabel ist.

  - Tabellen: Die grundlegende Struktur der ESE-Datenbank, die zum Speichern von Daten verwendet wird.

  - Transaktion: Die ESE-Datenbank-Engine stellt ACID-Transaktionen (Atomic Consistent Isolated Durable) zur Verfügung, mit denen Anwendungen Daten nur aus zuverlässigen Datenzuständen abrufen und datenkonsistent bleiben, wenn ein unerwarteter Prozess beendet oder das System heruntergefahren wird.

  - Skalierbar: Die Anwendung kann Datenbanken erstellen, die bis zu 100 GB oder nur 1 MB groß sind.

