---
title: 'Load-Methode: cpapfile'
description: Wenn diese Vorgänge erfolgreich ausgeführt wurden, wird die erhaltene IStorage-Schnittstelle freigegeben. Dadurch wird die Datei geschlossen, und es wird angegeben, dass die Datei bei anderen Client Vorgängen nicht offen gehalten ist. Sie wird bei Bedarf erneut geöffnet.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- 'Load-Methode: cpapfile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857004"
---
# <a name="load-method---cpapfile"></a><span data-ttu-id="d2d5f-106">Load-Methode: cpapfile</span><span class="sxs-lookup"><span data-stu-id="d2d5f-106">Load Method - CPapFile</span></span>

<span data-ttu-id="d2d5f-107">Wenn diese Vorgänge erfolgreich ausgeführt wurden, wird die erhaltene [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle freigegeben.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-107">When these operations are successful, the obtained [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface is released.</span></span> <span data-ttu-id="d2d5f-108">Dadurch wird die Datei geschlossen, und es wird angegeben, dass die Datei bei anderen Client Vorgängen nicht offen gehalten ist.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-108">This closes the file and indicates that the file is not held open during other client operations.</span></span> <span data-ttu-id="d2d5f-109">Sie wird bei Bedarf erneut geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-109">It will be reopened when required.</span></span>

<span data-ttu-id="d2d5f-110">Bei diesem Beispiel handelt es sich um die **cpapfile**-Methode zum  **Laden** von papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-110">This example is the **CPapFile** **Load** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a><span data-ttu-id="d2d5f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2d5f-111">Remarks</span></span>

<span data-ttu-id="d2d5f-112">Wie bei der [**Save**](save-method---cpapfile.md) -Methode wird beim Übergeben von **null** für den *pszFileName* -Parameter der gespeicherte Inhalt des Members **m \_ szcurrfilename** als Dateiname verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-112">As with the [**Save**](save-method---cpapfile.md) method, if **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="d2d5f-113">Da eine vorhandene Datei geöffnet werden kann, wird zuerst die apputil **FileExist** -Funktion verwendet, um zu überprüfen, ob die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-113">Because an existing file may be opened, the APPUTIL **FileExist** function is first used to verify that the file exists.</span></span> <span data-ttu-id="d2d5f-114">Wenn dies der Fall ist, wird die Standard Dienstfunktion " [**stgisstoragefile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) " aufgerufen, um das Format der Datei zu überprüfen, um festzustellen, ob es sich um eine gültige Verbund Datei handelt.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-114">If it exists, the standard [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) service function is called to verify the format of the file to determine if it is a valid compound file.</span></span>

<span data-ttu-id="d2d5f-115">Wenn die Datei gültig ist, wird die Standard Dienstfunktion " [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) " aufgerufen, um die Datei zu öffnen und einen Zeiger auf eine [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle für Sie zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-115">If the file is valid, the standard [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) service function is called to open the file and return a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for it.</span></span>

<span data-ttu-id="d2d5f-116">Der erste Parameter ist der Name der zu öffnenden Verbund Datei.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-116">The first parameter is the name of the compound file to open.</span></span> <span data-ttu-id="d2d5f-117">Wie beim " [**stganatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) "-Befehl wird diese Zeichenfolge in der Unicode-Form erwartet. während der ANSI-Kompilierung wird ein apputil-Makro verwendet, um sicherzustellen, dass der ANSI-Parameter in den erwarteten Unicode-Parameter konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-117">As with the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) call, this string is expected in the Unicode form, and during ANSI compilation an APPUTIL macro is used to ensure the ANSI parameter is converted to the expected Unicode.</span></span>

<span data-ttu-id="d2d5f-118">Der Speicher Parameter für die zweite Priorität ist **null**, was darauf hinweist, dass er in diesem Beispiel nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-118">The second priority storage parameter is **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="d2d5f-119">Die zugriffsmodusflags werden als dritter Parameter übergeben, um anzugeben, welche Zugriffs Modi für die geöffnete Datei zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-119">The access mode flags are passed as the third parameter to specify what access modes are permitted on the opened file.</span></span> <span data-ttu-id="d2d5f-120">[**STGM \_ Lesen**](stgm-constants.md) öffnet die Datei mit der Berechtigung schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-120">[**STGM\_READ**](stgm-constants.md) opens the file with read-only permission.</span></span> <span data-ttu-id="d2d5f-121">[**STGM \_ Direkt**](stgm-constants.md) öffnet die Datei für den direkten Zugriff im Gegensatz zum transaktiven Zugriff.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-121">[**STGM\_DIRECT**](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="d2d5f-122">[**STGM \_ Freigabe \_ exklusiv**](stgm-constants.md) öffnet die Datei für den exklusiven, nicht freigegebenen Gebrauch durch den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-122">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="d2d5f-123">Der vierte Element Ausschluss Parameter in **null**, der angibt, dass er in diesem Beispiel nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-123">The fourth element exclusion parameter in **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="d2d5f-124">Der fünfte Parameter ist für die zukünftige Verwendung reserviert und muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-124">The fifth parameter is reserved for future use and must be zero.</span></span>

<span data-ttu-id="d2d5f-125">Die Adresse der Zeiger Variablen **m \_ pistorage** wird als der sechste Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-125">The address of pointer variable **m\_pIStorage** is passed as the sixth parameter.</span></span> <span data-ttu-id="d2d5f-126">Wenn der-Rückruf erfolgreich zurückgegeben wurde, enthält **m \_ pistorage** einen Zeiger auf eine [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-126">When the call successfully returns, **m\_pIStorage** contains a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="d2d5f-127">Dies ist die Schnittstelle, die für nachfolgende Vorgänge in der geöffneten Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-127">This is the interface that is used for any subsequent operations on the opened file.</span></span>

<span data-ttu-id="d2d5f-128">Der wichtige Vorgang in diesem Fall besteht darin, dass das copaper-Objekt seine Zeichnungsdaten aus der Datei lädt.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-128">The important operation in this case is to have the COPaper object load its drawing data from the file.</span></span> <span data-ttu-id="d2d5f-129">Dies erfolgt oben mithilfe der **Load** -Methode der [**iPaper**](ipaper-methods.md) -Schnittstelle von copaper.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-129">This is done above using the **Load** method of COPaper's [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="d2d5f-130">Wenn copaper das Laden der Daten mit dem bereitgestellten [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) erfolgreich durchläuft, wird der Name der Verbund Datei als neuer aktueller Dateiname in **m \_ szcurrfilename** kopiert.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-130">If COPaper succeeds in loading its data using the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

<span data-ttu-id="d2d5f-131">Wenn diese Vorgänge erfolgreich abgeschlossen wurden, wird die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle freigegeben, die abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-131">When these operations are successfully completed, the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface that was obtained is released.</span></span> <span data-ttu-id="d2d5f-132">Dadurch wird die Datei geschlossen und bedeutet, dass die Datei bei anderen Client Vorgängen nicht offen gehalten wird.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-132">This closes the file and means that the file is not held open during other client operations.</span></span> <span data-ttu-id="d2d5f-133">Sie wird bei Bedarf erneut geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d2d5f-133">It will be reopened when required.</span></span>

 

 




