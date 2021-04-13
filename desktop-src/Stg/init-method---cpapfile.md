---
title: 'Init-Methode: cpapfile'
description: Im folgenden Codebeispiel wird gezeigt, wie cpapfile initialisiert wird.
ms.assetid: 8312a6b2-6f3f-4a24-8aeb-9461f3b1a905
keywords:
- 'Init-Methode: cpapfile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4fb5729ddcf20545254e3e461070c3e68f3421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390793"
---
# <a name="init-method---cpapfile"></a><span data-ttu-id="b27b1-104">Init-Methode: cpapfile</span><span class="sxs-lookup"><span data-stu-id="b27b1-104">Init Method - CPapFile</span></span>

<span data-ttu-id="b27b1-105">Im folgenden Codebeispiel wird gezeigt, wie **cpapfile** initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b27b1-105">The following code example shows how **CPapFile** is initialized.</span></span>

<span data-ttu-id="b27b1-106">Bei diesem Beispiel handelt es sich um die **cpapfile**- **Init** -Methode von papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="b27b1-106">This example is the **CPapFile** **Init** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Init(
                      TCHAR* pszAppFileName,
                      IPaper* pIPaper)
  {
    HRESULT hr = E_FAIL;

    if (NULL != pIPaper)
    {
      // Keep CPapFile copy of pIPaper. Thus AddRef it.
      // Released in Destructor.
      m_pIPaper = pIPaper;
      m_pIPaper->AddRef();

      if (NULL != pszAppFileName)
      {
        // Set the default current file name.
        StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszAppFileName);

        hr = NOERROR;
      }
    }

    return (hr);
  }
  
```



<span data-ttu-id="b27b1-107">Der *pszappfilename* -Parameter wird verwendet, um cpapfile mit einem Standard Dateinamen für alle nachfolgenden Lade-oder Speichervorgänge zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="b27b1-107">The *pszAppFileName* parameter is used to initialize CPapFile with a default file name for any subsequent load or save operations.</span></span> <span data-ttu-id="b27b1-108">Eine Kopie wird für das erste Laden im Member " **m \_ szcurrfilename** " beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b27b1-108">A copy is kept in member **m\_szCurFileName** for the first load.</span></span> <span data-ttu-id="b27b1-109">In **stoclien** wird ein solcher Ladevorgang versucht, wenn die Anwendung zum ersten Mal gestartet wird, nachdem cpapfile mit *pszappfilename* mit dem zugewiesenen "stoclien" initialisiert wurde. PAP ".</span><span class="sxs-lookup"><span data-stu-id="b27b1-109">In **StoClien**, such a load is attempted when the application first starts after CPapFile has been initialized with *pszAppFileName* assigned "STOCLIEN.PAP".</span></span> <span data-ttu-id="b27b1-110">Der Dateiname wurde in einem cguipaper-Konstruktor erstellt, indem der Name des aktuellen ausführenden Moduls erhalten wurde.</span><span class="sxs-lookup"><span data-stu-id="b27b1-110">This file name was constructed in a CGuiPaper constructor by obtaining the current executing module name.</span></span> <span data-ttu-id="b27b1-111">(Die Win32-Funktion [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) wird aufgerufen.)</span><span class="sxs-lookup"><span data-stu-id="b27b1-111">(The Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function is called).</span></span>

<span data-ttu-id="b27b1-112">Der *pipaper* -Parameter ist für cpapfile erforderlich, da er diese Schnittstelle für das copaper-Objekt verwendet, um Lade-und Speichervorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b27b1-112">The *pIPaper* parameter is required by CPapFile, because it uses this interface on the COPaper object to perform its load and save operations.</span></span> <span data-ttu-id="b27b1-113">**Adressf** wird für diese gespeicherte Kopie von *pipaper* in Übereinstimmung mit com-Regeln aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b27b1-113">**AddRef** is called on this stored copy of *pIPaper*, in accordance with COM rules.</span></span> <span data-ttu-id="b27b1-114">Das entsprechende **Release** wird im cpapfile-Dekonstruktor aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b27b1-114">The matching **Release** is called in the CPapFile destructor.</span></span>

 

 