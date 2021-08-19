---
description: Durch dynamisches Verknüpfen kann ein Modul nur die Informationen enthalten, die zum Suchen einer exportierten DLL-Funktion zur Ladezeit oder Zur Laufzeit erforderlich sind.
ms.assetid: df2a8e4c-7ad0-46ea-9643-1528a9ea1503
title: Informationen zu Dynamic-Link-Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62e6a6a23315e915bd4a5a7fe6e2dcb54a9a2ebfbd66bf5d4ba7a2519a04576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815909"
---
# <a name="about-dynamic-link-libraries"></a>Informationen zu Dynamic-Link-Bibliotheken

Durch dynamisches Verknüpfen kann ein Modul nur die Informationen enthalten, die zum Suchen einer exportierten DLL-Funktion zur Ladezeit oder Zur Laufzeit erforderlich sind. Dynamisches Verknüpfen unterscheidet sich von der vertrauteren statischen Verknüpfung, bei der der Linker den Code einer Bibliotheksfunktion in jedes Modul kopiert, das sie aufruft.

## <a name="types-of-dynamic-linking"></a>Typen der dynamischen Verknüpfung

Es gibt zwei Methoden zum Aufrufen einer Funktion in einer DLL:

-   Beim dynamischen Verknüpfen zur Ladezeit ruft ein Modul explizit exportierte *DLL-Funktionen* auf, als wären sie lokale Funktionen. Dazu müssen Sie das Modul mit der Importbibliothek für die DLL verknüpfen, die die Funktionen enthält. Eine Importbibliothek stellt dem System die Informationen bereit, die zum Laden der DLL und zum Suchen der exportierten DLL-Funktionen beim Laden der Anwendung erforderlich sind.
-   Beim dynamischen Verknüpfen zur Laufzeit verwendet ein Modul die [**LoadLibrary-**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx-Funktion,**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) um die DLL zur Laufzeit zu laden.  Nachdem die DLL geladen wurde, ruft das Modul die [**GetProcAddress-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) auf, um die Adressen der exportierten DLL-Funktionen abzurufen. Das Modul ruft die exportierten DLL-Funktionen mithilfe der funktionszeiger auf, die von **GetProcAddress** zurückgegeben werden. Dadurch entfällt die Notwendigkeit einer Importbibliothek.

## <a name="dlls-and-memory-management"></a>DLLs und Speicherverwaltung

Jeder Prozess, der die DLL lädt, ordnet sie ihrem virtuellen Adressraum zu. Nachdem der Prozess die DLL in die virtuelle Adresse geladen hat, kann sie die exportierten DLL-Funktionen aufrufen.

Das System verwaltet einen prozessbezogenen Verweiszähler für jede DLL. Wenn ein Thread die DLL lädt, wird der Verweiszähler um eins erhöht. Wenn der Prozess beendet wird oder der Verweiszähler 0 (nur dynamisches Verknüpfen zur Laufzeit) wird, wird die DLL aus dem virtuellen Adressraum des Prozesses entladen.

Wie jede andere Funktion wird eine exportierte DLL-Funktion im Kontext des Threads ausgeführt, der sie aufruft. Daher gelten die folgenden Bedingungen:

-   Die Threads des Prozesses, der die DLL aufgerufen hat, können Handles verwenden, die von einer DLL-Funktion geöffnet werden. Auf ähnliche Weise können Handles, die von jedem Thread des aufrufenden Prozesses geöffnet werden, in der DLL-Funktion verwendet werden.
-   Die DLL verwendet den Stapel des aufrufenden Threads und den virtuellen Adressraum des aufrufenden Prozesses.
-   Die DLL belegt Arbeitsspeicher aus dem virtuellen Adressraum des aufrufenden Prozesses.

Weitere Informationen zu DLLs finden Sie in den folgenden Themen:

-   [Vorteile der dynamischen Verknüpfung](advantages-of-dynamic-linking.md)
-   [Dynamic Link Library Creation (Erstellen einer Dynamic Link Library)](dynamic-link-library-creation.md)
-   [Dynamic Link Library Entry-Point-Funktion](dynamic-link-library-entry-point-function.md)
-   [Dynamische Verknüpfung zur Ladezeit](load-time-dynamic-linking.md)
-   [Dynamische Laufzeitverknüpfung](run-time-dynamic-linking.md)
-   [Dynamic Link Library-Suchreihenfolge](dynamic-link-library-search-order.md)
-   [Dynamic Link Library-Daten](dynamic-link-library-data.md)
-   [Dynamic Link Library Redirection (Umleitung der Dynamic Link-Bibliothek)](dynamic-link-library-redirection.md)
-   [Dynamic Link Library-Updates](dynamic-link-library-updates.md)
-   [Sicherheit der Dynamic Link Library](dynamic-link-library-security.md)
-   [AppInit-DLLs und sicherer Start](secure-boot-and-appinit-dlls.md)

 

 
