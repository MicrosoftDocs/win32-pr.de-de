---
description: Erstellen von DirectShow-Filtern
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Erstellen von DirectShow-Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7090eed702b1abe8ee863d5fa3ac9c1fd413690e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908618"
---
# <a name="building-directshow-filters"></a>Erstellen von DirectShow-Filtern

Die DirectShow-Basisklassen werden für die Implementierung von DirectShow-Filtern empfohlen. Führen Sie zum Erstellen mit den Basisklassen zusätzlich zu den unter Einrichten der [Buildumgebung](setting-up-the-build-environment.md)aufgeführten Schritten die folgenden Schritte aus:

-   Erstellen Sie die Basisklassenbibliothek im Verzeichnis Samples \\ Multimedia \\ DirectShow \\ BaseClasses unter dem SDK-Stammverzeichnis. Es gibt zwei Versionen der Bibliothek: eine Verkaufsversion (Strmbase.lib) und eine Debugversion (Strmbasd.lib).
-   Schließen Sie die Headerdatei Streams.h ein.
-   Verwenden Sie die \_ \_ Stdcall-Aufrufkonvention.
-   Verwenden Sie die Multithread-C-Laufzeitbibliothek (debuggen oder retail, je nach Bedarf).
-   Schließen Sie eine Definitionsdatei (DEF-Datei) ein, die die DLL-Funktionen exportiert. Im Folgenden wird ein Beispiel für eine Definitionsdatei beschrieben. Es wird davon ausgegangen, dass die Ausgabedatei MyFilter.dll heißt.
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   Link zu den folgenden Bibliothekendateien.

| Bezeichnung | Wert |
    |--------------|--------------------------------------|
    | Debugbuild  | Strmbasd.lib, Msvcrtd.lib, Winmm.lib |
    | Retail Build | Strmbase.lib, Msvcrt.lib, Winmm.lib  |

    

     

-   Wählen Sie in den Linkereinstellungen die Option "Standardbibliotheken ignorieren" aus.
-   Deklarieren Sie den DLL-Einstiegspunkt im Quellcode wie folgt:
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Frühere Versionen

Für Versionen der Basisklassenbibliothek vor DirectShow 9.0 müssen Sie auch folgende Schritte unternehmen:

-   Definieren Sie für Debugbuilds das Präprozessorflag DEBUG.

Dieser Schritt ist für die Version der Basisklassenbibliothek, die in DirectShow 9.0 und höher verfügbar ist, nicht erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> <dt>

[Schreiben von DirectShow-Filtern](writing-directshow-filters.md)
</dt> </dl>

 

 



