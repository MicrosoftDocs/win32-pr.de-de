---
description: Listet die Attribute der Element Dateien im catalogfiles-Abschnitt einer Katalog Definitionsdatei (CDF) auf.
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: Cryptovcdfenumschlag attributeswithcdftag-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525730"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a><span data-ttu-id="c6acd-103">Cryptovcdfenumschlag attributeswithcdftag-Funktion</span><span class="sxs-lookup"><span data-stu-id="c6acd-103">CryptCATCDFEnumAttributesWithCDFTag function</span></span>

<span data-ttu-id="c6acd-104">\[Die Funktion " **cryptccdfenumschlag attributeswithcdftag** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c6acd-104">\[The **CryptCATCDFEnumAttributesWithCDFTag** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c6acd-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c6acd-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c6acd-106">Die Funktion **crypt-cdfenumattributeswithcdftag** listet die Attribute der Element Dateien im Abschnitt **catalogfiles** einer Katalog Definitionsdatei (CDF) auf.</span><span class="sxs-lookup"><span data-stu-id="c6acd-106">The **CryptCATCDFEnumAttributesWithCDFTag** function enumerates the attributes of member files in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="c6acd-107">**Crypt-cdfenüberattributeswithcdftag** wird von [MakeCat](makecat.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c6acd-107">**CryptCATCDFEnumAttributesWithCDFTag** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="c6acd-108">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="c6acd-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="c6acd-109">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="c6acd-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c6acd-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6acd-110">Syntax</span></span>


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a><span data-ttu-id="c6acd-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6acd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6acd-112">*PCDF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6acd-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6acd-113">Ein Zeiger auf eine [**cryptstreamcdf**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c6acd-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c6acd-114">*pwszmitgliedungstag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6acd-114">*pwszMemberTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6acd-115">Ein Zeiger auf eine **null**-terminierte Zeichenfolge, die das Katalog dateimember identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c6acd-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="c6acd-116">*pmember* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6acd-116">*pMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6acd-117">Ein Zeiger auf eine [**cryptsinmember**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) -Struktur, die die Element Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="c6acd-117">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the member information.</span></span>

</dd> <dt>

<span data-ttu-id="c6acd-118">*pprevattr* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6acd-118">*pPrevAttr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6acd-119">Ein Zeiger auf eine [**cryptstreamattribute**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) -Struktur für ein dateimember-Attribut in der CDF, auf das von *PCDF* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c6acd-119">A pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure for a file member attribute in the CDF pointed to by *pCDF*.</span></span>

</dd> <dt>

<span data-ttu-id="c6acd-120">*pfnparser-Fehler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6acd-120">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6acd-121">Ein Zeiger auf eine benutzerdefinierte Funktion zum Behandeln von Dateianalyse Fehlern.</span><span class="sxs-lookup"><span data-stu-id="c6acd-121">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6acd-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6acd-122">Return value</span></span>

<span data-ttu-id="c6acd-123">Bei Erfolg gibt diese Funktion einen Zeiger auf eine [**crypttorattribute**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="c6acd-123">Upon success, this function returns a pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure.</span></span> <span data-ttu-id="c6acd-124">Die **cryptstreamcdfenumattributeswithcdftag** -Funktion gibt einen **null** -Zeiger zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="c6acd-124">The **CryptCATCDFEnumAttributesWithCDFTag** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6acd-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6acd-125">Remarks</span></span>

<span data-ttu-id="c6acd-126">Diese Funktion wird in der Regel in einer Schleife aufgerufen, um alle Attribute der Katalog Dateielemente in einer CDF aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="c6acd-126">You typically call this function in a loop to enumerate all of the catalog file member attributes in a CDF.</span></span> <span data-ttu-id="c6acd-127">Legen Sie *pprevattr* vor der Eingabe der Schleife auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="c6acd-127">Before entering the loop, set *pPrevAttr* to **NULL**.</span></span> <span data-ttu-id="c6acd-128">Die-Funktion gibt einen Zeiger auf das erste Attribut zurück.</span><span class="sxs-lookup"><span data-stu-id="c6acd-128">The function returns a pointer to the first attribute.</span></span> <span data-ttu-id="c6acd-129">Legen Sie *pprevattr* auf den Rückgabewert der Funktion für nachfolgende Iterationen der Schleife fest.</span><span class="sxs-lookup"><span data-stu-id="c6acd-129">Set *pPrevAttr* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="c6acd-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6acd-130">Examples</span></span>

<span data-ttu-id="c6acd-131">Das folgende Beispiel zeigt die korrekte Reihenfolge der Zuweisungen für den *pprevattr* -Parameter ( `pAttr` ).</span><span class="sxs-lookup"><span data-stu-id="c6acd-131">The following example shows the correct sequence of assignments for the *pPrevAttr* parameter (`pAttr`).</span></span>


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="c6acd-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6acd-132">Requirements</span></span>



| <span data-ttu-id="c6acd-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6acd-133">Requirement</span></span> | <span data-ttu-id="c6acd-134">Wert</span><span class="sxs-lookup"><span data-stu-id="c6acd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6acd-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6acd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c6acd-136">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6acd-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c6acd-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6acd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c6acd-138">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6acd-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6acd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c6acd-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6acd-140"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6acd-140"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6acd-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6acd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6acd-142">MakeCat</span><span class="sxs-lookup"><span data-stu-id="c6acd-142">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="c6acd-143">**Crypt-Attribute**</span><span class="sxs-lookup"><span data-stu-id="c6acd-143">**CRYPTCATATTRIBUTE**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[<span data-ttu-id="c6acd-144">**Cryptalisicdf**</span><span class="sxs-lookup"><span data-stu-id="c6acd-144">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="c6acd-145">**Cryptkatamember**</span><span class="sxs-lookup"><span data-stu-id="c6acd-145">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="c6acd-146">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="c6acd-146">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="c6acd-147">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="c6acd-147">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
