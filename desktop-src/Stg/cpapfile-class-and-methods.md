---
title: Cpapfile-Klasse und-Methoden
description: Stoclien kapselt die Verbund Datei Vorgänge in einem cpapfile C++-Objekt.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa970aecf275afbf7bc5b6d68c69de3367e48aa5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947590"
---
# <a name="cpapfile-class-and-methods"></a><span data-ttu-id="feda3-103">Cpapfile-Klasse und-Methoden</span><span class="sxs-lookup"><span data-stu-id="feda3-103">CPapFile Class and Methods</span></span>

<span data-ttu-id="feda3-104">**Stoclien** kapselt die Verbund Datei Vorgänge in einem cpapfile C++-Objekt.</span><span class="sxs-lookup"><span data-stu-id="feda3-104">**StoClien** encapsulates its compound file operations in a CPapFile C++ object.</span></span>

<span data-ttu-id="feda3-105">Im folgenden finden Sie die **cpapfile** -Klassen Deklaration von papfile. h.</span><span class="sxs-lookup"><span data-stu-id="feda3-105">The following is the **CPapFile** class declaration from Papfile.h.</span></span>


```C++
class CPapFile
  {
    public:
      CPapFile(void);
      ~CPapFile(void);
      HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
      HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
      HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);

    private:
      TCHAR          m_szCurFileName[MAX_PATH];
      IPaper*        m_pIPaper;
      IStorage*      m_pIStorage;
  };
  
```



<span data-ttu-id="feda3-106">Das cpapfile-Objekt behält einen aktuellen Dateinamen im Member " **m \_ szcurrfilename**" bei.</span><span class="sxs-lookup"><span data-stu-id="feda3-106">The CPapFile object keeps a current file name in member **m\_szCurFileName**.</span></span> <span data-ttu-id="feda3-107">Dieser Dateiname wird als Standard in den [**Load**](load-method---cpapfile.md) -und [**Save**](save-method---cpapfile.md) -Methoden verwendet, wenn er nicht explizit einen Dateinamen empfängt.</span><span class="sxs-lookup"><span data-stu-id="feda3-107">This file name is used as a default in the [**Load**](load-method---cpapfile.md) and [**Save**](save-method---cpapfile.md) methods when they do not explicitly receive a file name.</span></span>

<span data-ttu-id="feda3-108">Mitglied **m \_ pipaper** behält einen Schnittstellen Zeiger auf die copaper [**iPaper**](ipaper-methods.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="feda3-108">Member **m\_pIPaper** keeps an interface pointer to the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="feda3-109">Member **m \_ pistorage** behält einen Zeiger auf die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle für die aktuelle Verbund Datei bei, die von **stoclien** für die strukturierte Speicherung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="feda3-109">Member **m\_pIStorage** keeps a pointer to the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for the current compound file that **StoClien** is using for structured storage.</span></span>

<span data-ttu-id="feda3-110">Im folgenden finden Sie eine Zusammenfassung der cpapfile-Methoden.</span><span class="sxs-lookup"><span data-stu-id="feda3-110">The following is a summary of CPapFile's methods.</span></span>


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




