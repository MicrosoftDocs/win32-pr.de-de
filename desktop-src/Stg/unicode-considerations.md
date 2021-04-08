---
title: Überlegungen zu Unicode
description: Die in der iPaper-Speichermethode verwendete Funktion "Write Teammanager tusertypestg" erfordert Unicode-Zeichen folgen Parameter.
ms.assetid: 34a1d30e-4401-474e-999e-832b963064bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7bef75ec88318f4a2af8c5c7b693f0fc7c877f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856175"
---
# <a name="unicode-considerations"></a>Überlegungen zu Unicode

Die in der [**iPaper:: Save**](ipaper--save.md) -Methode verwendete Dienstfunktion " **Beschreib tefmtusertypestg** " erfordert Unicode-Zeichen folgen Parameter. Dies ist der Fall bei com/OLE-Dienst aufrufen, die Zeichen folgen Parameter annehmen. Beim Kompilieren für ANSI-Zeichen folgen müssen die erwarteten Unicode-Parameter von ANSI in Unicode konvertiert werden. Dieser Prozess wird mithilfe einiger Makros in "apputil. h" erzielt, die Konvertierungen möglicherweise verschleiern. Informationen hierzu finden Sie beispielsweise unter " **Beschreib tefmtusertypestg**".

Der folgende-Befehl wird in der [**Save**](ipaper--save.md) -Methode angezeigt.


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



Wenn **stoservice** für ANSI (nicht für Unicode) kompiliert wird, reduziert sich dieser-Aufrufe tatsächlich auf einen-Rückruf einer internen apputil-Ersatzfunktion. Um dies zu unterstützen, wird das folgende Makro Schema in "apputil. h" verwendet, bei dem es sich um eine enthaltene Datei im gesamten Codebeispiel handelt. Cpp-Dateien.


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



Das Schema verwendet die Funktion für den Ersatzdienst Rückruf. Die ANSI-Versionen der Aufrufe beginnen mit einem \_ . Diese Stellvertreter-ANSI-Funktionen werden in "apputil. cpp" implementiert. Sie werden verwendet, wenn das Codebeispiel für ANSI-Zeichen folgen kompiliert wird (die Standardeinstellung in Makefiles). Die Dienstfunktionen, die von den Surrogates anstelle von vorhanden sind, unterstützen nur Unicode-Zeichen folgen Parameter. Dies erzwingt einige Zeichen folgen Konvertierungen von ANSI in Unicode, bevor der tatsächliche com/OLE-Dienst-Rückruf innerhalb des Ersatz Zeichens erfolgt.

Wenn z. b. Unicode während des Kompilierens nicht definiert ist, werden alle Aufrufe in den Beispielen für die Funktion " **Write-fmtusertypestg** com-Dienst" tatsächlich von den Makros in Aufrufe einer \_ in apputil implementierten Funktion "Beschreib tefmtusertypestg" geändert. CPP. Diese Funktion akzeptiert den Eingabe-ANSI-Zeichen folgen Zeiger, konvertiert sie in eine Unicode-Kopie und übergibt diese Unicode-Kopie als Zeichen folgen Parameter in einem **calltefmtusertypestg** -Vorgang.

Hier ist ein " \_ Write-fmtusertypestg" aus "apputil. cpp".

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

 

 




