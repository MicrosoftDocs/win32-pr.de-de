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
# <a name="unicode-considerations"></a><span data-ttu-id="a3bb7-103">Überlegungen zu Unicode</span><span class="sxs-lookup"><span data-stu-id="a3bb7-103">Unicode Considerations</span></span>

<span data-ttu-id="a3bb7-104">Die in der [**iPaper:: Save**](ipaper--save.md) -Methode verwendete Dienstfunktion " **Beschreib tefmtusertypestg** " erfordert Unicode-Zeichen folgen Parameter.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-104">The **WriteFmtUserTypeStg** service function, used in the [**IPaper::Save**](ipaper--save.md) method, requires Unicode string parameters.</span></span> <span data-ttu-id="a3bb7-105">Dies ist der Fall bei com/OLE-Dienst aufrufen, die Zeichen folgen Parameter annehmen.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-105">This is the case with COM/OLE service calls that take string parameters.</span></span> <span data-ttu-id="a3bb7-106">Beim Kompilieren für ANSI-Zeichen folgen müssen die erwarteten Unicode-Parameter von ANSI in Unicode konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-106">When compiling for ANSI strings, the expected Unicode parameters need conversion from ANSI to Unicode.</span></span> <span data-ttu-id="a3bb7-107">Dieser Prozess wird mithilfe einiger Makros in "apputil. h" erzielt, die Konvertierungen möglicherweise verschleiern.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-107">This process is achieved using some macros in APPUTIL.h that may obscure conversions.</span></span> <span data-ttu-id="a3bb7-108">Informationen hierzu finden Sie beispielsweise unter " **Beschreib tefmtusertypestg**".</span><span class="sxs-lookup"><span data-stu-id="a3bb7-108">For example, see **WriteFmtUserTypeStg**.</span></span>

<span data-ttu-id="a3bb7-109">Der folgende-Befehl wird in der [**Save**](ipaper--save.md) -Methode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-109">The following call appears in the [**Save**](ipaper--save.md) method.</span></span>


```C++
WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, TEXT(CLIPBDFMT_STR));
```



<span data-ttu-id="a3bb7-110">Wenn **stoservice** für ANSI (nicht für Unicode) kompiliert wird, reduziert sich dieser-Aufrufe tatsächlich auf einen-Rückruf einer internen apputil-Ersatzfunktion.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-110">When **StoServe** is compiled for ANSI (not for Unicode), this call actually reduces to a call to an internal APPUTIL surrogate function.</span></span> <span data-ttu-id="a3bb7-111">Um dies zu unterstützen, wird das folgende Makro Schema in "apputil. h" verwendet, bei dem es sich um eine enthaltene Datei im gesamten Codebeispiel handelt. Cpp-Dateien.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-111">To support this, the following macro scheme is used in Apputil.h, which is an included file in all code sample .CPP files.</span></span>


```C++
#if !defined(UNICODE)

  STDAPI A_WriteFmtUserTypeStg(IStorage*, CLIPFORMAT, LPSTR);

  #if !defined(_NOANSIMACROS_)

  #undef WriteFmtUserTypeStg
  #define WriteFmtUserTypeStg(a, b, c) A_WriteFmtUserTypeStg(a, b, c)

  #endif

  #endif
```



<span data-ttu-id="a3bb7-112">Das Schema verwendet die Funktion für den Ersatzdienst Rückruf.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-112">The scheme uses surrogate service call functions.</span></span> <span data-ttu-id="a3bb7-113">Die ANSI-Versionen der Aufrufe beginnen mit einem \_ .</span><span class="sxs-lookup"><span data-stu-id="a3bb7-113">The ANSI versions of the calls begin with A\_.</span></span> <span data-ttu-id="a3bb7-114">Diese Stellvertreter-ANSI-Funktionen werden in "apputil. cpp" implementiert.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-114">These surrogate ANSI functions are implemented in Apputil.cpp.</span></span> <span data-ttu-id="a3bb7-115">Sie werden verwendet, wenn das Codebeispiel für ANSI-Zeichen folgen kompiliert wird (die Standardeinstellung in Makefiles).</span><span class="sxs-lookup"><span data-stu-id="a3bb7-115">They are used when the code sample is being compiled for ANSI strings (the default in the makefiles).</span></span> <span data-ttu-id="a3bb7-116">Die Dienstfunktionen, die von den Surrogates anstelle von vorhanden sind, unterstützen nur Unicode-Zeichen folgen Parameter.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-116">The service functions that the surrogates stand in place of support only Unicode string parameters.</span></span> <span data-ttu-id="a3bb7-117">Dies erzwingt einige Zeichen folgen Konvertierungen von ANSI in Unicode, bevor der tatsächliche com/OLE-Dienst-Rückruf innerhalb des Ersatz Zeichens erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-117">This forces some string conversions from ANSI to Unicode before the real COM/OLE service call is made inside the surrogate.</span></span>

<span data-ttu-id="a3bb7-118">Wenn z. b. Unicode während des Kompilierens nicht definiert ist, werden alle Aufrufe in den Beispielen für die Funktion " **Write-fmtusertypestg** com-Dienst" tatsächlich von den Makros in Aufrufe einer \_ in apputil implementierten Funktion "Beschreib tefmtusertypestg" geändert. CPP.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-118">For example, if UNICODE is not defined during compiling, any calls in the samples to the **WriteFmtUserTypeStg** COM service function are actually changed by the macros into calls to an A\_WriteFmtUserTypeStg function that is implemented in APPUTIL.CPP.</span></span> <span data-ttu-id="a3bb7-119">Diese Funktion akzeptiert den Eingabe-ANSI-Zeichen folgen Zeiger, konvertiert sie in eine Unicode-Kopie und übergibt diese Unicode-Kopie als Zeichen folgen Parameter in einem **calltefmtusertypestg** -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a3bb7-119">This function accepts the input ANSI string pointer, converts it to a Unicode copy, and passes that Unicode copy as the string parameter in a call to the actual **WriteFmtUserTypeStg** function.</span></span>

<span data-ttu-id="a3bb7-120">Hier ist ein " \_ Write-fmtusertypestg" aus "apputil. cpp".</span><span class="sxs-lookup"><span data-stu-id="a3bb7-120">Here is A\_WriteFmtUserTypeStg from Apputil.cpp.</span></span>

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

 

 




