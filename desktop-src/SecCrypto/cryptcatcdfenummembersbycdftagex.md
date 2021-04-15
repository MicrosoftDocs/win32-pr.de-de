---
description: Listet die einzelnen dateimember im catalogfiles-Abschnitt einer Katalog Definitionsdatei (CDF) auf.
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: Crypttorcdfenumschlag mitgliedsbycdftagex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525733"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a><span data-ttu-id="1818e-103">Crypttorcdfenumschlag mitgliedsbycdftagex-Funktion</span><span class="sxs-lookup"><span data-stu-id="1818e-103">CryptCATCDFEnumMembersByCDFTagEx function</span></span>

<span data-ttu-id="1818e-104">\[Die Funktion " **cryptccdfenumschlag mitgliedsbycdftagex** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1818e-104">\[The **CryptCATCDFEnumMembersByCDFTagEx** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1818e-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1818e-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="1818e-106">Die Funktion **cryptingcdfenummitgliedsbycdftagex** listet die einzelnen dateimember im Abschnitt **catalogfiles** einer Katalog Definitionsdatei (CDF) auf.</span><span class="sxs-lookup"><span data-stu-id="1818e-106">The **CryptCATCDFEnumMembersByCDFTagEx** function enumerates the individual file members in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="1818e-107">**Crypt-cdfenumschlag-mitgliedsbycdftagex** wird von [MakeCat](makecat.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1818e-107">**CryptCATCDFEnumMembersByCDFTagEx** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="1818e-108">Diese Funktion verfügt über keine zugeordnete Header Datei oder Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="1818e-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="1818e-109">Um diese Funktion aufzurufen, müssen Sie eine benutzerdefinierte Header Datei erstellen und die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Mssign32.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="1818e-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1818e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="1818e-110">Syntax</span></span>


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="1818e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1818e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1818e-112">*PCDF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1818e-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1818e-113">Ein Zeiger auf eine [**cryptstreamcdf**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1818e-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1818e-114">*pwszprevcdftag* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1818e-114">*pwszPrevCDFTag* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1818e-115">Ein Zeiger auf eine **null**-terminierte Zeichenfolge, die das Katalog dateimember identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1818e-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="1818e-116">*pfnparser-Fehler* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1818e-116">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1818e-117">Ein Zeiger auf eine benutzerdefinierte Funktion zum Behandeln von Dateianalyse Fehlern.</span><span class="sxs-lookup"><span data-stu-id="1818e-117">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> <dt>

<span data-ttu-id="1818e-118">*ppmember* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1818e-118">*ppMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1818e-119">Ein Zeiger auf eine [**cryptsinmember**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) -Struktur, die die dateimember-Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="1818e-119">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the file member information.</span></span>

</dd> <dt>

<span data-ttu-id="1818e-120">Fehler bei " *f* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="1818e-120">*fContinueOnError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1818e-121">Ein-Wert, der angibt, ob im Arbeitsspeicher ein Verweis auf den letzten Enumerationsmember aufbewahrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1818e-121">A value that specifies whether to keep in memory a reference to the last enumerated member.</span></span>

</dd> <dt>

<span data-ttu-id="1818e-122">*pvReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1818e-122">*pvReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1818e-123">Dieser Parameter ist reserviert. Verwenden Sie Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="1818e-123">This parameter is reserved; do not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1818e-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1818e-124">Return value</span></span>

<span data-ttu-id="1818e-125">Bei Erfolg gibt diese Funktion einen Zeiger auf eine mit **null** endenden Zeichenfolge zurück, die ein dateimember im **catalogfiles** -Abschnitt einer CDF identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1818e-125">Upon success, this function returns a pointer to a **null**-terminated string that identifies a file member in the **CatalogFiles** section of a CDF.</span></span> <span data-ttu-id="1818e-126">Wenn ein Fehler auftritt, gibt die Funktion " **cryptstreamcdfenummitgliedsbycdftagex** " einen **null** -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="1818e-126">The **CryptCATCDFEnumMembersByCDFTagEx** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="1818e-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1818e-127">Remarks</span></span>

<span data-ttu-id="1818e-128">Diese Funktion wird in der Regel in einer Schleife aufgerufen, um alle Katalog dateimember in einer CDF aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="1818e-128">You typically call this function in a loop to enumerate all of the catalog file members in a CDF.</span></span> <span data-ttu-id="1818e-129">Legen Sie *pwszprevcdftag* vor der Eingabe der Schleife auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="1818e-129">Before entering the loop, set *pwszPrevCDFTag* to **NULL**.</span></span> <span data-ttu-id="1818e-130">Die-Funktion gibt einen Zeiger auf das erste Element zurück.</span><span class="sxs-lookup"><span data-stu-id="1818e-130">The function returns a pointer to the first member.</span></span> <span data-ttu-id="1818e-131">Legen Sie *pwszprevcdftag* auf den Rückgabewert der Funktion für nachfolgende Iterationen der Schleife fest.</span><span class="sxs-lookup"><span data-stu-id="1818e-131">Set *pwszPrevCDFTag* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="1818e-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1818e-132">Examples</span></span>

<span data-ttu-id="1818e-133">Das folgende Beispiel zeigt die korrekte Reihenfolge der Zuweisungen für den *pwszprevcdftag* -Parameter ( `pwszMemberTag` ).</span><span class="sxs-lookup"><span data-stu-id="1818e-133">The following example shows the correct sequence of assignments for the *pwszPrevCDFTag* parameter (`pwszMemberTag`).</span></span>


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="1818e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1818e-134">Requirements</span></span>



| <span data-ttu-id="1818e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1818e-135">Requirement</span></span> | <span data-ttu-id="1818e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="1818e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1818e-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1818e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1818e-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1818e-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1818e-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1818e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1818e-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1818e-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1818e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1818e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1818e-142"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1818e-142"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1818e-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1818e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1818e-144">MakeCat</span><span class="sxs-lookup"><span data-stu-id="1818e-144">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="1818e-145">**Cryptalisicdf**</span><span class="sxs-lookup"><span data-stu-id="1818e-145">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="1818e-146">**Cryptkatamember**</span><span class="sxs-lookup"><span data-stu-id="1818e-146">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="1818e-147">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="1818e-147">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="1818e-148">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="1818e-148">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
