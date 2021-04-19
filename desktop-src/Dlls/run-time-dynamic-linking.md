---
description: Wenn die Anwendung die Funktionen LoadLibrary oder LoadLibraryEx aufruft, versucht das System, die dll zu finden (Weitere Informationen finden Sie unter Dynamic-Link Bibliotheks Such Reihenfolge).
ms.assetid: 81e237a9-3c32-46a5-88d3-c978f43dad54
title: Dynamische Verknüpfung Run-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e215ac83ecdc0615b8030e2e215857c67fe6e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345168"
---
# <a name="run-time-dynamic-linking"></a>Dynamische Verknüpfung Run-Time

Wenn die Anwendung die Funktionen [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) aufruft, versucht das System, die dll zu finden (Weitere Informationen finden Sie unter [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md)). Wenn die Suche erfolgreich ist, ordnet das System das dll-Modul dem virtuellen Adressraum des Prozesses zu und erhöht den Verweis Zähler. Wenn der Aufruf von **LoadLibrary** oder **LoadLibraryEx** eine DLL angibt, deren Code bereits dem virtuellen Adressraum des aufrufenden Prozesses zugeordnet ist, gibt die Funktion einfach ein Handle für die DLL zurück und erhöht den dll-Verweis Zähler. Beachten Sie, dass zwei DLLs, die den gleichen Basis Dateinamen und die gleiche Erweiterung aufweisen, aber in verschiedenen Verzeichnissen gefunden werden, nicht als dieselbe dll angesehen werden.

Das System ruft die Einstiegspunkt Funktion im Kontext des Threads auf, der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)aufgerufen hat. Die Einstiegspunkt Funktion wird nicht aufgerufen, wenn die DLL bereits durch einen Aufruf von LoadLibrary oder LoadLibraryEx durch einen Aufruf von **LoadLibrary** oder **LoadLibraryEx** ohne entsprechenden Aufruf an die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion geladen wurde.

Wenn das System die dll nicht finden kann oder wenn die Einstiegspunkt Funktion false zurückgibt, gibt [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) NULL zurück. Wenn **LoadLibrary** oder **LoadLibraryEx** erfolgreich ist, wird ein Handle an das dll-Modul zurückgegeben. Der Prozess kann dieses Handle verwenden, um die dll in einem Aufrufen der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)-, [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)-oder [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread) -Funktion zu identifizieren.

Die [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) -Funktion gibt ein Handle zurück, das in " [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)", " [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)" oder " [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)" verwendet wird. Die **GetModuleHandle** -Funktion ist nur dann erfolgreich, wenn das dll-Modul bereits durch das Laden der Lade Zeit oder durch einen vorherigen Aufruf von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)dem Adressraum des Prozesses zugeordnet ist. Im Gegensatz zu **LoadLibrary** oder **LoadLibraryEx** erhöht **GetModuleHandle** nicht den Modul Verweis Zähler. Die [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) -Funktion Ruft den vollständigen Pfad des Moduls ab, das einem Handle zugeordnet ist, das von **GetModuleHandle**, **LoadLibrary** oder **LoadLibraryEx** zurückgegeben wurde.

Der Prozess kann [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um die Adresse einer exportierten Funktion in der DLL mithilfe eines von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)zurückgegebenen dll-Modul Handles zu erhalten.

Wenn das dll-Modul nicht mehr benötigt wird, kann der Prozess " [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) " oder " [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)" aufzurufen. Diese Funktionen verringern den Modul Verweis Zähler und entordnen den DLL-Code aus dem virtuellen Adressraum des Prozesses, wenn der Verweis Zähler Null ist.

Durch die dynamische Verknüpfung zur Laufzeit kann der Prozess weiterhin ausgeführt werden, auch wenn keine DLL verfügbar ist. Der Prozess kann dann eine alternative Methode verwenden, um das Ziel zu erreichen. Wenn ein Prozess z. b. eine DLL nicht finden kann, kann er versuchen, eine andere DLL zu verwenden, oder er kann den Benutzer über einen Fehler benachrichtigen. Wenn der Benutzer den vollständigen Pfad der fehlenden DLL angeben kann, kann der Prozess diese Informationen verwenden, um die dll zu laden, auch wenn Sie sich nicht im normalen Suchpfad befindet. Diese Situation steht im Gegensatz zum Lade Zeit-verknüpfen, bei dem das System einfach den Prozess beendet, wenn die dll nicht gefunden werden kann.

Die dynamische Verknüpfung zur Laufzeit kann Probleme verursachen, wenn die dll die [**DllMain**](dllmain.md) -Funktion verwendet, um für jeden Thread eines Prozesses eine Initialisierung auszuführen, da der Einstiegspunkt nicht für Threads aufgerufen wird, die vor dem Aufruf von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) vorhanden waren. Ein Beispiel für das Behandeln dieses Problems finden Sie unter Verwenden von [lokalem Thread Speicher in einer Dynamic-Link-Bibliothek](using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden dynamischer Lauf Zeit Verknüpfungen](using-run-time-dynamic-linking.md)
</dt> </dl>

 

 
