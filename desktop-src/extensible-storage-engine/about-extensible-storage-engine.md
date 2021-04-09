---
description: 'Weitere Informationen finden Sie hier: Informationen zum Extensible Storage Engine'
title: Informationen zur Extensible Storage-Engine
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958666"
---
# <a name="about-extensible-storage-engine"></a>Informationen zur Extensible Storage-Engine


_**Gilt für:** Exchange Server 2013 | Windows | Windows Server_

## <a name="about-extensible-storage-engine"></a>Informationen zur Extensible Storage-Engine

Bei der Extensible Storage Engine (ESE) handelt es sich um eine Datenbank-Engine, die Informationen in einer logischen Sequenz speichert. Informationen können entweder sequenziell oder durch Zugriff auf definierte Indizes abgerufen werden. Aktualisierungen der Datenbank werden mit einer Transaktion implementiert, um sichere Vorgänge sicherzustellen. ESE ermöglicht den gleichzeitigen Zugriff auf mehrere Datenbanken, einschließlich der Datenbanken für Transaktionsprotokoll Dateien, die für die Systemwiederherstellung verwendet werden können. ESE ist für große oder kleine Anwendungen skalierbar. Die folgenden Features sind für die ESE-Anwendungsprogrammierschnittstelle (Application Programming Interface, API) verfügbar:

  - Sicherung und Wiederherstellung: eine Anwendung kann konsistente Kopien des Daten Zustands erstellen, während Sie online ist, und den Daten Zustand Aktiv ändern.

  - Cursor Navigation: die Anwendung kann mit dem Cursor navigieren, um entweder sequenziell oder mithilfe von Indizes auf Daten zuzugreifen.

  - Database: eine Sammlung von Tabellen, die als einzelne Einheit gesichert und wieder hergestellt werden.

  - Protokollierung und Wiederherstellung von Abstürzen: die ESE-API stellt sicher, dass die Anwendungs definierte Datenkonsistenz auch bei einem Systemabsturz berücksichtigt wird.

  - Tables: die grundlegende Struktur der ESE-Datenbank, die zum Speichern von Daten verwendet wird.

  - Transaktion: das ESE-Datenbankmodul stellt atomarische, isolierte, dauerhafte (ACID) Transaktionen bereit, die es Anwendungen ermöglichen, Daten nur aus zuverlässigen Daten Zuständen abzurufen, und behält die Datenkonsistenz bei einer unerwarteten Beendigung des Prozesses oder beim Herunterfahren des Systems bei.

  - Skalierbar: die Anwendung kann Datenbanken mit einer Größe von 100 GB oder bis zu 1 MB erstellen.

