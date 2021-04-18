---
title: Verwenden der Code Beispiele für das Windows Media-Format-SDK
description: Verwenden der Code Beispiele für das Windows Media-Format-SDK
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows Media-Format-SDK, Codebeispiele
- Windows Media-Format-SDK, Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db438a8cb42bbb45768421cc34c129f19948f1c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391475"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a>Verwenden der Code Beispiele für das Windows Media-Format-SDK

Viele der erläuternden Abschnitte dieses SDK enthalten Codebeispiele. Die Beispiele sind so klar und präzise wie möglich. Wenn Sie die Beispiele lesen, sollten Sie die folgenden Konventionen beachten.

-   Bei allen Beispielen wird davon ausgegangen, dass Sie Windows. h und wmsdk. h einschließen. Alle anderen erforderlichen Header Dateien werden im erläuternden Text erwähnt.
-   Die Fehlerüberprüfung wurde auf das Abbrechen der Funktion beschränkt, wenn ein Fehler auftritt. In einer Anwendung sollten Sie nach bestimmten Fehlercodes suchen und eine Art Fehlerberichterstattung bereitstellen.

    Wenn Sie Rückgabewerte von Methoden oder Funktionen überprüfen, die einen **HRESULT** -Wert zurückgeben, sollten Sie das **failed** -Makro verwenden, um zu ermitteln, ob der Rückgabewert einen Fehler anzeigt.

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    Viele der Beispiele in dieser Dokumentation verwenden ein Makro mit dem Namen GoTo \_ Exit \_ \_ , wenn failed, das im folgenden Code definiert ist.

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    Diese Beispiel Funktionen verfügen jeweils über ein Tag mit dem Namen "Exit:", nach dem alle in der Funktion zugeordneten Schnittstellen und Arbeitsspeicher freigegeben werden und ggf. der Fehlercode zurückgegeben wird.

-   Schnittstellen und Arbeitsspeicher werden in den Codebeispielen mithilfe von Makros namens sicheres \_ Release und sicheres Löschen von Arrays freigegeben \_ \_ . Diese Makros sind im folgenden Code definiert:
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

    

-   Häufig müssen Sie die Logik eines Beispiels in einem anderen Beispiel einschließen, damit das Beispiel sinnvoll ist. In diesen Fällen ist ein TODO-Kommentar mit einem Verweis auf das entsprechende Codebeispiel enthalten.
-   Damit der Code leichter lesbar ist, überprüft keines der Beispiel Funktionen in dieser Dokumentation seine Eingabeparameter. Wenn Sie eine dieser Funktionen in Ihren Code kopieren, sollten Sie alle Eingabeparameter überprüfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einstieg**](getting-started.md)
</dt> </dl>

 

 




