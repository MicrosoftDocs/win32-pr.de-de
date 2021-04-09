---
description: Durch dynamisches Verknüpfen kann ein Modul nur die Informationen einschließen, die zum Auffinden einer exportierten DLL-Funktion zur Ladezeit oder zur Laufzeit erforderlich sind.
ms.assetid: df2a8e4c-7ad0-46ea-9643-1528a9ea1503
title: Informationen zu Dynamic-Link-Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdb24048e17e9164aaf39d0ab337aea33576c95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863375"
---
# <a name="about-dynamic-link-libraries"></a>Informationen zu Dynamic-Link-Bibliotheken

Durch dynamisches Verknüpfen kann ein Modul nur die Informationen einschließen, die zum Auffinden einer exportierten DLL-Funktion zur Ladezeit oder zur Laufzeit erforderlich sind. Dynamische Verknüpfungen unterscheiden sich von der vertrauten statischen Verknüpfung, bei der der Linker den Code einer Bibliotheksfunktion in jedes Modul kopiert, das Sie aufruft.

## <a name="types-of-dynamic-linking"></a>Dynamische Verknüpfungs Typen

Es gibt zwei Methoden zum Aufrufen einer Funktion in einer DLL:

-   Beim *dynamischen Verknüpfen der Ladezeit* führt ein Modul explizite Aufrufe an exportierte DLL-Funktionen aus, als wären es lokale Funktionen. Dies erfordert, dass Sie das Modul mit der Import Bibliothek für die DLL verknüpfen, die die Funktionen enthält. Eine Import Bibliothek stellt dem System die Informationen zur Verfügung, die zum Laden der dll und zum Auffinden der exportierten DLL-Funktionen erforderlich sind, wenn die Anwendung geladen wird.
-   Bei der *dynamischen Verknüpfung zur Laufzeit* verwendet ein Modul die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion oder die [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion, um die dll zur Laufzeit zu laden. Nachdem die dll geladen wurde, ruft das Modul die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion auf, um die Adressen der exportierten DLL-Funktionen zu erhalten. Das Modul ruft die exportierten DLL-Funktionen mithilfe der von **GetProcAddress** zurückgegebenen Funktionszeiger auf. Dadurch entfällt die Notwendigkeit einer Import Bibliothek.

## <a name="dlls-and-memory-management"></a>DLLs und Speicherverwaltung

Jeder Prozess, der die dll lädt, ordnet Sie dem virtuellen Adressraum zu. Nachdem der Prozess die dll in seine virtuelle Adresse geladen hat, kann Sie die exportierten DLL-Funktionen aufzurufen.

Das System verwaltet einen pro-Prozess-Verweis Zähler für jede DLL. Wenn ein Thread die dll lädt, wird der Verweis Zähler um eins erhöht. Wenn der Prozess beendet wird oder wenn der Verweis Zähler Null wird (nur Lauf Zeit dynamische Verknüpfung), wird die dll aus dem virtuellen Adressraum des Prozesses entladen.

Wie jede andere Funktion wird eine exportierte DLL-Funktion im Kontext des Threads ausgeführt, von dem Sie aufgerufen wird. Daher gelten die folgenden Bedingungen:

-   Die Threads des Prozesses, der die dll aufgerufen hat, können Handles verwenden, die von einer DLL-Funktion geöffnet wurden. Ebenso können Handles, die von einem beliebigen Thread des aufrufenden Prozesses geöffnet werden, in der DLL-Funktion verwendet werden.
-   Die dll verwendet den Stapel des aufrufenden Threads und den virtuellen Adressraum des aufrufenden Prozesses.
-   Die dll weist Speicher aus dem virtuellen Adressraum des aufrufenden Prozesses zu.

Weitere Informationen zu DLLs finden Sie in den folgenden Themen:

-   [Vorteile dynamischer Verknüpfungen](advantages-of-dynamic-linking.md)
-   [Erstellung von Dynamic Link Library](dynamic-link-library-creation.md)
-   [Dynamic-Link Library Entry-Point-Funktion](dynamic-link-library-entry-point-function.md)
-   [Dynamische Verknüpfung der Ladezeit](load-time-dynamic-linking.md)
-   [Dynamische Verknüpfung zur Laufzeit](run-time-dynamic-linking.md)
-   [Dynamic Link Library-Suchreihenfolge](dynamic-link-library-search-order.md)
-   [Dynamic Link Library-Daten](dynamic-link-library-data.md)
-   [Umleitung von Dynamic Link Library](dynamic-link-library-redirection.md)
-   [Dynamic Link Library-Aktualisierungen](dynamic-link-library-updates.md)
-   [Dynamic Link Library-Sicherheit](dynamic-link-library-security.md)
-   [AppInit-DLLs und sicherer Start](secure-boot-and-appinit-dlls.md)

 

 
