---
description: Aufbauen von DirectShow-Filtern
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Aufbauen von DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5553c4358f97809214ebbdea23c129aa7c214e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747072"
---
# <a name="building-directshow-filters"></a>Aufbauen von DirectShow-Filtern

Die DirectShow-Basisklassen werden zum Implementieren von DirectShow-Filtern empfohlen. Um mit den Basisklassen zu erstellen, führen Sie zusätzlich zu den unter [Einrichten der Buildumgebung](setting-up-the-build-environment.md)aufgeführten Schritten die folgenden Schritte aus:

-   Erstellen Sie die Basisklassen Bibliothek, die sich in den Verzeichnis Beispielen \\ Multimedia \\ DirectShow \\ baseclasses unter dem SDK-Stammverzeichnis befindet. Es gibt zwei Versionen der Bibliothek: eine Verkaufsversion ("-Version. lib") und eine Debugversion ("straumbasd. lib").
-   Schließen Sie die Header Datei Streams. h ein.
-   Verwenden Sie die \_ \_ StdCall-Aufruf Konvention.
-   Verwenden Sie die Multithread-C-Lauf Zeit Bibliothek (Debug oder Retail).
-   Schließen Sie eine Definitionsdatei (. def) ein, mit der die DLL-Funktionen exportiert werden. Im folgenden finden Sie ein Beispiel für eine Definitionsdatei. Dabei wird davon ausgegangen, dass die Ausgabedatei MyFilter.dll benannt ist.
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   Verknüpfen Sie die folgenden lib-Dateien.

    |              |                                      |
    |--------------|--------------------------------------|
    | Build Debuggen  | "Straumbasd. lib", "msvcrtd. lib", "winmm. lib" |
    | Retail-Build | "Ermbase. lib", "Msvcrt. lib", "winmm. lib"  |

    

     

-   Wählen Sie die Option "Standardbibliotheken ignorieren" in den Linker-Einstellungen aus.
-   Deklarieren Sie den DLL-Einstiegspunkt wie folgt im Quellcode:
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Frühere Versionen

Für Versionen der Basisklassen Bibliothek vor DirectShow 9,0 müssen Sie auch die folgenden Schritte ausführen:

-   Definieren Sie für Debugbuilds das präprozessorflag Debuggen.

Dieser Schritt ist für die Version der Basisklassen Bibliothek, die in DirectShow 9,0 und höher verfügbar ist, nicht erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



