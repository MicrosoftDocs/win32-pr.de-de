---
description: Eine Dynamic-Link Library (DLL) kann globale oder lokale Daten enthalten.
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Dynamic-Link-Bibliotheksdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8902eb6388624d958c7176a14b8893f8e2245ddd9370f6ba2ac71605b2379cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048440"
---
# <a name="dynamic-link-library-data"></a>Dynamic-Link-Bibliotheksdaten

Eine Dynamic-Link Library (DLL) kann globale oder lokale Daten enthalten.

## <a name="variable-scope"></a>Variablenbereich

Variablen, die in einer DLL-Quellcodedatei als global deklariert sind, werden vom Compiler und Linker als globale Variablen behandelt, aber jeder Prozess, der eine bestimmte DLL lädt, erhält eine eigene Kopie der globalen Variablen dieser DLL. Der Bereich statischer Variablen ist auf den Block beschränkt, in dem die statischen Variablen deklariert werden. Daher verfügt jeder Prozess standardmäßig über eine eigene Instanz der globalen und statischen DLL-Variablen.

> [!Note]  
> Mit Ihren Entwicklungstools können Sie möglicherweise das Standardverhalten außer Kraft setzen. Beispielsweise unterstützt der Visual C++ Compiler **\# den Pragmaabschnitt** und der Linker die Option /SECTION. Weitere Informationen finden Sie in der Dokumentation, die in Ihren Entwicklungstools enthalten ist.

 

## <a name="dynamic-memory-allocation"></a>Dynamischer Arbeitsspeicher Zuordnung

Wenn eine DLL Speicher mithilfe einer der Speicherbelegungsfunktionen [**(GlobalAlloc,**](/windows/desktop/api/winbase/nf-winbase-globalalloc) [**LocalAlloc,**](/windows/desktop/api/winbase/nf-winbase-localalloc) [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)und [**VirtualAlloc)**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)zuordnet, wird der Arbeitsspeicher im virtuellen Adressraum des aufrufenden Prozesses zugeordnet und ist nur für die Threads dieses Prozesses zugänglich.

Eine DLL kann die Dateizuordnung verwenden, um Arbeitsspeicher zuzuweisen, der von Prozessen gemeinsam genutzt werden kann. Eine allgemeine Erläuterung zur Verwendung der Dateizuordnung zum Erstellen von benanntem freigegebenen Speicher finden Sie unter [Dateizuordnung.](/windows/desktop/Memory/file-mapping) Ein Beispiel, in dem die [**DllMain-Funktion**](dllmain.md) verwendet wird, um freigegebenen Arbeitsspeicher mithilfe der Dateizuordnung einzurichten, finden Sie unter [Verwenden von freigegebenen Speicher in einer Dynamic-Link Bibliothek.](using-shared-memory-in-a-dynamic-link-library.md)

## <a name="thread-local-storage"></a>Threadlokaler Speicher

Die Tls-Funktionen (Thread Local Storage) ermöglichen es einer DLL, einen Index zum Speichern und Abrufen eines anderen Werts für jeden Thread eines Multithreadprozesses zuzuordnen. Beispielsweise kann eine Tabellenkalkulationsanwendung jedes Mal eine neue Instanz desselben Threads erstellen, wenn der Benutzer eine neue Kalkulationstabelle öffnet. Eine DLL, die die Funktionen für verschiedene Tabellenkalkulationsvorgänge bereitstellt, kann TLS verwenden, um Informationen zum aktuellen Zustand der einzelnen Tabellenkalkulationen (Zeile, Spalte usw.) zu speichern. Eine allgemeine Erläuterung des lokalen Threadspeichers finden Sie unter [Thread Local Storage](/windows/desktop/ProcThread/thread-local-storage). Ein Beispiel, in dem die [**DllMain-Funktion**](dllmain.md) zum Einrichten des lokalen Threadspeichers verwendet wird, finden Sie unter [Using Thread Local Storage in a Dynamic-Link Library](using-thread-local-storage-in-a-dynamic-link-library.md).

**Windows Server 2003 und Windows XP:** Der Visual C++ Compiler unterstützt eine Syntax, mit der Sie threadlokale Variablen deklarieren können: **\_ declspec(thread)**. Wenn Sie diese Syntax in einer DLL verwenden, können Sie die DLL nicht explizit mit [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) in Versionen von Windows vor Windows Vista laden. Wenn Ihre DLL explizit geladen wird, müssen Sie die lokalen Threadspeicherfunktionen anstelle von **\_ declspec(thread)** verwenden.

 

 
