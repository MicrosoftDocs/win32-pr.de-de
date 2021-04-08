---
title: 'Save-Methode: cpapfile'
description: Wenn cpapfile initialisiert ist, kann es verwendet werden, um die aktuellen Zeichnungsdaten im copaper-Objekt zu speichern.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- 'Save-Methode: cpapfile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948094"
---
# <a name="save-method---cpapfile"></a><span data-ttu-id="ea8bb-104">Save-Methode: cpapfile</span><span class="sxs-lookup"><span data-stu-id="ea8bb-104">Save Method - CPapFile</span></span>

<span data-ttu-id="ea8bb-105">Wenn **cpapfile** initialisiert ist, kann es verwendet werden, um die aktuellen Zeichnungsdaten im copaper-Objekt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-105">When **CPapFile** is initialized, it can be used to save the current drawing data held in the COPaper object.</span></span>

## <a name="save-method-papfilecpp"></a><span data-ttu-id="ea8bb-106">Save-Methode (papfile. CPP</span><span class="sxs-lookup"><span data-stu-id="ea8bb-106">Save Method (PAPFILE.CPP)</span></span>

<span data-ttu-id="ea8bb-107">Bei diesem Beispiel handelt es sich um die **cpapfile**-Methode zum  [**Speichern**](ipaper--save.md) von papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-107">This example is the **CPapFile** [**Save**](ipaper--save.md) method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



<span data-ttu-id="ea8bb-108">Wenn **null** für den *pszFileName* -Parameter übergeben wird, wird der gespeicherte Inhalt des Members **m \_ szcurrfilename** als Dateiname verwendet.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-108">If **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="ea8bb-109">Der *nlockkey* ist der Client Sperr Schlüssel, der in einem vorherigen-Befehl der copaper [**Lock**](ipaper-methods.md) -Methode in der **iPaper** -Schnittstelle abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-109">The *nLockKey* is the client lock key obtained in a previous call to the COPaper [**Lock**](ipaper-methods.md) method in the **IPaper** interface.</span></span>

<span data-ttu-id="ea8bb-110">Die Dienstfunktion "com-Standard [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) " wird aufgerufen, um die Verbund Datei zu erstellen, in der die Zeichnungsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-110">The COM standard [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) service function is called to create the compound file in which the drawing data will be saved.</span></span>

<span data-ttu-id="ea8bb-111">Der Name der zu erstellenden Verbund Datei wird als erster Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-111">The name of the compound file to create is passed as the first parameter.</span></span> <span data-ttu-id="ea8bb-112">Dies wird von [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) als Unicode-Zeichenfolge erwartet.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-112">This is expected by [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as a Unicode string.</span></span> <span data-ttu-id="ea8bb-113">Wenn **stoclien** für ANSI-Zeichen folgen kompiliert werden (Unicode ist nicht definiert, was der Standardwert in Makefile ist), reduziert sich dieser Aufrufe tatsächlich auf einen Aufrufen einer internen apputil-Funktion, **einer \_ stgfiatedocfile**.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-113">When **StoClien** is compiled for ANSI strings (UNICODE is not defined, which is the default in the makefile), this call actually reduces to a call to an internal APPUTIL function, **A\_StgCreateDocfile**.</span></span> <span data-ttu-id="ea8bb-114">Diese Funktion führt die ordnungsgemäße Konvertierung des ANSI pszFile-Parameters in eine Unicode-Version vor, bevor **StgCreateDocfile** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-114">This function performs the proper conversion of the ANSI pszFile parameter to a Unicode version before calling **StgCreateDocfile**.</span></span> <span data-ttu-id="ea8bb-115">Weitere Informationen finden Sie unter apputil. h und Stoserve.htm.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-115">For more information, see Apputil.h and Stoserve.htm.</span></span>

<span data-ttu-id="ea8bb-116">Die zugriffsmodusflags werden als zweiter Parameter übergeben und legen fest, welche Zugriffs Modi für die neue Datei zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-116">The access mode flags are passed as the second parameter and determine which access modes are permitted on the new file.</span></span> <span data-ttu-id="ea8bb-117">Mit dem STGM-Flag zum [ \_ Erstellen](stgm-constants.md) eines Zugriffsmodus wird eine neue Verbund Datei erstellt oder ein vorhandener mit dem gleichen Namen überschrieben.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-117">The [STGM\_CREATE](stgm-constants.md) access mode flag creates a new compound file or overwrites an existing one of the same name.</span></span> <span data-ttu-id="ea8bb-118">[STGM \_ Der Lesevorgang öffnet die](stgm-constants.md) Datei mit Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-118">[STGM\_READWRITE](stgm-constants.md) opens the file with read-write permission.</span></span> <span data-ttu-id="ea8bb-119">[STGM \_ Direkt](stgm-constants.md) öffnet die Datei für den direkten Zugriff im Gegensatz zum transaktiven Zugriff.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-119">[STGM\_DIRECT](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="ea8bb-120">[STGM \_ Freigabe \_ exklusiv](stgm-constants.md) öffnet die Datei für den exklusiven, nicht freigegebenen Gebrauch durch den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-120">[STGM\_SHARE\_EXCLUSIVE](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="ea8bb-121">Der dritte Parameter ist reserviert und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-121">The third parameter is reserved and must be zero.</span></span>

<span data-ttu-id="ea8bb-122">Die Adresse der Zeiger Variablen **m \_ pistorage** wird als vierter Parameter an [**stgkreatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) übergeben.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-122">The address of pointer variable **m\_pIStorage** is passed to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as the fourth parameter.</span></span> <span data-ttu-id="ea8bb-123">Wenn der-Rückruf erfolgreich zurückgegeben wurde, enthält **m \_ pistorage** einen Schnittstellen Zeiger auf eine [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-123">When the call successfully returns, **m\_pIStorage** contains an interface pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="ea8bb-124">Dies ist die Schnittstelle, die für nachfolgende Vorgänge in der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-124">This is the interface that is used for any subsequent operations on the file.</span></span>

<span data-ttu-id="ea8bb-125">Der wichtige Vorgang in diesem Fall besteht darin, dass das copaper-Objekt seine Zeichnungsdaten in der Datei speichert.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-125">The important operation in this case is to have the COPaper object store its drawing data in the file.</span></span> <span data-ttu-id="ea8bb-126">Dies erfolgt oben mithilfe der [**Save**](ipaper--save.md) -Methode der copaper [**iPaper**](ipaper-methods.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-126">This is done above using the [**Save**](ipaper--save.md) method of the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="ea8bb-127">Wenn copaper das Speichern der Daten im angegebenen Speicher Objekt erfolgreich abgeschlossen hat, wird der Name der Verbund Datei als neuer aktueller Dateiname in **m \_ szcurrfilename** kopiert.</span><span class="sxs-lookup"><span data-stu-id="ea8bb-127">If COPaper succeeds in saving its data in the storage object provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

 

 




