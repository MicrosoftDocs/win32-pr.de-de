---
title: Verwenden der Windows Sdk-Codebeispiele für das Medienformat
description: Verwenden der Windows Sdk-Codebeispiele für das Medienformat
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Medienformat-SDK, Codebeispiele
- Windows Medienformat-SDK, Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a5b6718bf7665d04fedb5d5a0bad473a632cbeeabdfd756a52877ccdc84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963939"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a>Verwenden der Windows Sdk-Codebeispiele für das Medienformat

Viele der erläuternden Abschnitte dieses SDK enthalten Codebeispiele. Die Beispiele werden so klar und präzise wie möglich geschrieben. Beim Lesen der Beispiele sollten Sie die folgenden Konventionen beachten.

-   Es wird davon ausgegangen, dass alle Beispiele windows.h und wmsdk.h enthalten. Alle anderen erforderlichen Headerdateien werden im erläuternden Text erwähnt.
-   Die Fehlerüberprüfung wurde auf das Ausbrechen der Funktion beschränkt, wenn ein Fehler auftritt. In einer Anwendung sollten Sie nach bestimmten Fehlercodes überprüfen und eine Art Fehlerberichterstattung bereitstellen.

    Wenn Sie Rückgabewerte von Methoden oder Funktionen überprüfen, die einen **HRESULT-Wert** zurückgeben, sollten Sie das **FAILED-Makro** verwenden, um zu bestimmen, ob der Rückgabewert auf einen Fehler hinweist.

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    In vielen Beispielen in dieser Dokumentation wird ein Makro mit dem Namen GOTO EXIT IF FAILED verwendet, das \_ im folgenden Code definiert \_ \_ ist.

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    Diese Beispielfunktionen verfügen jeweils über ein Tag mit dem Namen "Exit:", nach dem alle Schnittstellen und der in der Funktion zugeordnete Arbeitsspeicher freigegeben werden und der Fehlercode zurückgegeben wird, falls dies der Fall ist.

-   Schnittstellen und Arbeitsspeicher werden in den Codebeispielen mit Makros namens SAFE \_ RELEASE und SAFE ARRAY DELETE \_ \_ freigegeben. Diese Makros werden im folgenden Code definiert:
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   Häufig müssen Sie die Logik eines Beispiels in ein anderes Beispiel einindnen, damit das Beispiel aussagekräftig ist. In diesen Fällen ist ein TODO-Kommentar mit einem Verweis auf das entsprechende Codebeispiel enthalten.
-   Damit der Code leichter lesbar ist, überprüft keine der Beispielfunktionen in dieser Dokumentation ihre Eingabeparameter. Wenn Sie eine dieser Funktionen in Ihren Code kopieren, sollten Sie alle Eingabeparameter überprüfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erste Schritte**](getting-started.md)
</dt> </dl>

 

 




