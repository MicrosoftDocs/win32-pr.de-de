---
title: Unicode-Überlegungen
description: Die Dienstfunktion WriteFmtUserTypeStg, die in der IPaper Save-Methode verwendet wird, erfordert Unicode-Zeichenfolgenparameter.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06f8fa9592d3f29ccf82d42f38a48b2dc57d36bccf79b22b8fe159bad337cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886738"
---
# <a name="unicode-considerations"></a>Unicode-Überlegungen

Die **WriteFmtUserTypeStg-Dienstfunktion,** die in der [**IPaper::Save-Methode**](ipaper--save.md) verwendet wird, erfordert Unicode-Zeichenfolgenparameter. Dies ist bei COM/OLE-Dienstaufrufen der Fall, die Zeichenfolgenparameter annehmen. Beim Kompilieren für ANSI-Zeichenfolgen müssen die erwarteten Unicode-Parameter von ANSI in Unicode konvertiert werden. Dieser Prozess wird mithilfe einiger Makros in APPUTIL.h erreicht, die Konvertierungen möglicherweise verbergen. Beispiel: **WriteFmtUserTypeStg.**

Der folgende Aufruf wird in der [**Save-Methode**](ipaper--save.md) angezeigt.


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



Wenn **StoServe** für ANSI kompiliert wird (nicht für Unicode), wird dieser Aufruf tatsächlich auf einen Aufruf einer internen APPUTIL-Ersatzfunktion reduziert. Um dies zu unterstützen, wird das folgende Makroschema in Apputil.h verwendet, bei dem es sich um eine eingeschlossene Datei in allen Codebeispielen handelt. CPP-Dateien.


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



Das Schema verwendet Ersatzdienstaufruffunktionen. Die ANSI-Versionen der Aufrufe beginnen mit A \_ . Diese Ersatz-ANSI-Funktionen werden in Apputil.cpp implementiert. Sie werden verwendet, wenn das Codebeispiel für ANSI-Zeichenfolgen kompiliert wird (der Standardwert in den Makefiles). Die Dienstfunktionen, die die Ersatzzeichen anstelle von unterstützen, unterstützen nur Unicode-Zeichenfolgenparameter. Dies erzwingt einige Zeichenfolgenkonvertierungen von ANSI in Unicode, bevor der tatsächliche COM/OLE-Dienstaufruf innerhalb des Ersatzzeichens erfolgt.

Wenn unicode beispielsweise während der Kompilierung nicht definiert wird, werden alle Aufrufe in den Beispielen der COM-Dienstfunktion **WriteFmtUserTypeStg** tatsächlich von den Makros in Aufrufe einer \_ In APPUTIL implementierten WriteFmtUserTypeStg-Funktion geändert. Cpp. Diese Funktion akzeptiert den EINGABE-ANSI-Zeichenfolgenzeiger, konvertiert ihn in eine Unicode-Kopie und übergibt diese Unicode-Kopie als Zeichenfolgenparameter in einem Aufruf an die eigentliche **WriteFmtUserTypeStg-Funktion.**

Hier ist ein \_ WriteFmtUserTypeStg aus Apputil.cpp.

``` syntax
STDAPI A_WriteFmtUserTypeStg(
           IStorage* pIStorage,
           CLIPFORMAT ClipFmt,
           LPSTR pszUserType)
  {
    HRESULT hr = E_INVALIDARG;
    WCHAR wszUc[MAX_PATH];

    if (NULL != pszUserType)
    {
      // Convert from ANSI in pszUserType to Unicode in wszUc.
      AnsiToUc(pszUserType, wszUc, MAX_PATH);

      // Use the Unicode string in the actual service call.
      hr = WriteFmtUserTypeStg(pIStorage, ClipFmt, wszUc);
    }

    return hr;
  }
```

 

 




