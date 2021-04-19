---
description: Eine Dynamic-Link Bibliothek (dll) kann globale Daten oder lokale Daten enthalten.
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Bibliotheksdaten Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83280d3bfc449061c44f9e8bfd9b47833e7eca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355370"
---
# <a name="dynamic-link-library-data"></a>Bibliotheksdaten Dynamic-Link

Eine Dynamic-Link Bibliothek (dll) kann globale Daten oder lokale Daten enthalten.

## <a name="variable-scope"></a>Variablenbereich

Variablen, die in einer DLL-Quell Code Datei als global deklariert werden, werden vom Compiler und Linker als globale Variablen behandelt, aber jeder Prozess, der eine bestimmte dll lädt, erhält seine eigene Kopie der globalen Variablen dieser DLL. Der Bereich statischer Variablen ist auf den Block beschränkt, in dem die statischen Variablen deklariert werden. Daher verfügt jeder ProzessStandard mäßig über eine eigene Instanz der globalen und statischen DLL-Variablen.

> [!Note]  
> Die Entwicklungs Tools ermöglichen Ihnen möglicherweise das Überschreiben des Standard Verhaltens. Der Visual C++-Compiler unterstützt z. b. **\# pragma Section** , und der Linker unterstützt die/Section-Option. Weitere Informationen finden Sie in der Dokumentation, die in ihren Entwicklungs Tools enthalten ist.

 

## <a name="dynamic-memory-allocation"></a>Dynamischer Arbeitsspeicher Zuordnung

Wenn eine DLL mithilfe einer der Speicher Belegungs Funktionen ([**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)und [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)) Arbeitsspeicher zuordnet, wird der Arbeitsspeicher im virtuellen Adressraum des aufrufenden Prozesses zugeordnet und ist nur für die Threads dieses Prozesses zugänglich.

Eine DLL kann die Datei Zuordnung verwenden, um Speicher zuzuweisen, der von Prozessen gemeinsam genutzt werden kann. Eine allgemeine Erörterung der Verwendung der Datei Zuordnung zum Erstellen von benanntem frei gegebenem Speicher finden Sie unter [Datei Zuordnung](/windows/desktop/Memory/file-mapping). Ein Beispiel für die Verwendung der [**DllMain**](dllmain.md) -Funktion zum Einrichten von frei gegebenem Speicher mithilfe der Datei Zuordnung finden Sie unter Verwenden von frei gegebenem Arbeits [Speicher in einer Dynamic-Link-Bibliothek](using-shared-memory-in-a-dynamic-link-library.md).

## <a name="thread-local-storage"></a>Threadlokaler Speicher

Mit den TLS-Funktionen (Thread Local Storage) kann eine DLL einen Index zum Speichern und Abrufen eines anderen Werts für jeden Thread eines multithreadprozesses zuordnen. Eine Tabellenkalkulationsanwendung kann z. b. jedes Mal, wenn der Benutzer eine neue Tabelle öffnet, eine neue Instanz desselben Threads erstellen. Eine DLL, die die Funktionen für verschiedene Tabellen Vorgänge bereitstellt, kann TLS zum Speichern von Informationen über den aktuellen Status der einzelnen Arbeitsblätter (Zeile, Spalte usw.) verwenden. Eine allgemeine Erörterung des lokalen Thread Speichers finden Sie unter [Thread lokaler Speicher](/windows/desktop/ProcThread/thread-local-storage). Ein Beispiel, in dem die [**DllMain**](dllmain.md) -Funktion zum Einrichten des lokalen Thread Speichers verwendet wird, finden [Sie unter Verwenden von lokalem Thread Speicher in einer Dynamic-Link-Bibliothek](using-thread-local-storage-in-a-dynamic-link-library.md).

**Windows Server 2003 und Windows XP:** Der Visual C++-Compiler unterstützt eine Syntax, die es Ihnen ermöglicht, Thread lokale Variablen zu deklarieren: **\_ declspec (Thread)**. Wenn Sie diese Syntax in einer DLL verwenden, können Sie die dll nicht explizit mithilfe von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) auf Windows-Versionen vor Windows Vista laden. Wenn die dll explizit geladen wird, müssen Sie anstelle von **\_ declspec (Thread)** die lokalen Thread Speicherfunktionen verwenden.

 

 
