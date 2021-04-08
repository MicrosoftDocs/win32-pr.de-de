---
description: Überprüft die Signatur einer signierten Datei und ruft den Hashwert und den Algorithmusbezeichner für die Datei ab.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: Wthelpergetflehash-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959863"
---
# <a name="wthelpergetfilehash-function"></a><span data-ttu-id="216f3-103">Wthelpergetflehash-Funktion</span><span class="sxs-lookup"><span data-stu-id="216f3-103">WTHelperGetFileHash function</span></span>

<span data-ttu-id="216f3-104">\[Die **wthelpergetflehash** -Funktion ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="216f3-104">\[The **WTHelperGetFileHash** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="216f3-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="216f3-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="216f3-106">Die **wthelpergetflehash** -Funktion überprüft die Signatur einer signierten Datei und ruft den Hashwert und den Algorithmusbezeichner für die Datei ab.</span><span class="sxs-lookup"><span data-stu-id="216f3-106">The **WTHelperGetFileHash** function verifies the signature of a signed file and obtains the hash value and algorithm identifier for the file.</span></span>

> [!Note]  
> <span data-ttu-id="216f3-107">Diese Funktion ist nicht in einer veröffentlichten Header Datei deklariert.</span><span class="sxs-lookup"><span data-stu-id="216f3-107">This function is not declared in a published header file.</span></span> <span data-ttu-id="216f3-108">Um diese Funktion zu verwenden, deklarieren Sie Sie im exakten Format.</span><span class="sxs-lookup"><span data-stu-id="216f3-108">To use this function, declare it in the exact format shown.</span></span> <span data-ttu-id="216f3-109">Diese Funktion hat auch keine zugehörige Import Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="216f3-109">This function also has no associated import library.</span></span> <span data-ttu-id="216f3-110">Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Wintrust.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="216f3-110">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="216f3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="216f3-111">Syntax</span></span>


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a><span data-ttu-id="216f3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="216f3-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216f3-113">*pwszFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="216f3-113">*pwszFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216f3-114">Ein Zeiger auf eine NULL-terminierte Unicode-Zeichenfolge, die den Pfad und den Dateinamen der Datei enthält, für die der Hash erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="216f3-114">A pointer to a null-terminated Unicode string that contains the path and file name of the file to get the hash for.</span></span>

</dd> <dt>

<span data-ttu-id="216f3-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="216f3-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216f3-116">Dieser Parameter wird nicht verwendet und sollte NULL sein.</span><span class="sxs-lookup"><span data-stu-id="216f3-116">This parameter is not used and should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="216f3-117">*pvReserved* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="216f3-117">*pvReserved* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216f3-118">Dieser Parameter wird nicht verwendet und sollte **null** sein.</span><span class="sxs-lookup"><span data-stu-id="216f3-118">This parameter is not used and should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="216f3-119">*pbflehash* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="216f3-119">*pbFileHash* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216f3-120">Ein Zeiger auf einen Puffer, um den Hashwert für die Datei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="216f3-120">A pointer to a buffer to receive the hash value for the file.</span></span> <span data-ttu-id="216f3-121">Der *pcbflehash* -Parameter enthält die Größe dieses Puffers.</span><span class="sxs-lookup"><span data-stu-id="216f3-121">The *pcbFileHash* parameter contains the size of this buffer.</span></span>

</dd> <dt>

<span data-ttu-id="216f3-122">*pcbflehash* \[ in, out, optional\]</span><span class="sxs-lookup"><span data-stu-id="216f3-122">*pcbFileHash* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216f3-123">Ein Zeiger auf eine **DWORD** -Variable, die bei der Eingabe die Größe des *pbflehash* -Puffers in Bytes enthält und bei der Ausgabe die Größe des Hashwerts in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="216f3-123">A pointer to a **DWORD** variable that, on input, contains the size, in bytes, of the *pbFileHash* buffer and, on output, receives the size, in bytes, of the hash value.</span></span>

<span data-ttu-id="216f3-124">Um die erforderliche Größe des Hashwerts zu erhalten, übergeben Sie **null** für den *pbflehash* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="216f3-124">To obtain the required size of the hash value, pass **NULL** for the *pbFileHash* parameter.</span></span> <span data-ttu-id="216f3-125">Diese Funktion platziert die erforderliche Größe (in Bytes) des Hashwerts an diesem Speicherort.</span><span class="sxs-lookup"><span data-stu-id="216f3-125">This function will place the required size, in bytes, of the hash value in this location.</span></span>

<span data-ttu-id="216f3-126">Wenn der *pbsplehash* -Parameter nicht **null** ist und die Größe nicht groß genug ist, um den Hashwert zu erhalten, platziert diese Funktion die erforderliche Größe in Byte an diesem Speicherort und gibt **Fehler \_ Weitere \_ Daten** zurück.</span><span class="sxs-lookup"><span data-stu-id="216f3-126">If the *pbFileHash* parameter is not **NULL**, and the size is not large enough to receive the hash value, this function will place the required size, in bytes, in this location and return **ERROR\_MORE\_DATA**.</span></span>

</dd> <dt>

<span data-ttu-id="216f3-127">*phashalgid* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="216f3-127">*pHashAlgid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="216f3-128">Ein Zeiger auf eine [**ALG- \_ ID**](alg-id.md) -Variable, die den Bezeichner des Algorithmus empfängt, der zum Erstellen des Hashwerts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="216f3-128">A pointer to an [**ALG\_ID**](alg-id.md) variable to receive the identifier of the algorithm used to create the hash value.</span></span> <span data-ttu-id="216f3-129">Dieser Parameter kann **null** sein, wenn diese Informationen nicht benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="216f3-129">This parameter can be **NULL** if this information is not needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216f3-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="216f3-130">Return value</span></span>

<span data-ttu-id="216f3-131">Gibt einen Statuscode zurück, der angibt, ob die Funktion erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="216f3-131">Returns a status code that indicates the success or failure of the function.</span></span>

<span data-ttu-id="216f3-132">Mögliche Rückgabecodes sind u. a. die folgenden:</span><span class="sxs-lookup"><span data-stu-id="216f3-132">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="216f3-133">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="216f3-133">Return code</span></span>                                                                                               | <span data-ttu-id="216f3-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="216f3-134">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="216f3-135"><dt>**Fehler \_ erfolgreich**</dt></span><span class="sxs-lookup"><span data-stu-id="216f3-135"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>             | <span data-ttu-id="216f3-136">Die Datei ist signiert, und die Signatur wurde überprüft.</span><span class="sxs-lookup"><span data-stu-id="216f3-136">The file is signed, and the signature was verified.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="216f3-137"><dt>**Fehler \_ Weitere \_ Daten**</dt></span><span class="sxs-lookup"><span data-stu-id="216f3-137"><dt>**ERROR\_MORE\_DATA**</dt></span></span> </dl>          | <span data-ttu-id="216f3-138">Der *pbsplehash* -Parameter ist nicht **null**, und die vom *pcbflehash* -Parameter angegebene Größe ist nicht groß genug, um den Hash zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="216f3-138">The *pbFileHash* parameter is not **NULL**, and the size specified by the *pcbFileHash* parameter is not large enough to receive the hash.</span></span><br/> |
| <dl> <span data-ttu-id="216f3-139"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="216f3-139"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="216f3-140">Es ist ein Fehler bei der Speicher Belegung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="216f3-140">A memory allocation failure occurred.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="216f3-141"><dt>**fehlerhafter \_ \_ \_ Digest**</dt></span><span class="sxs-lookup"><span data-stu-id="216f3-141"><dt>**TRUST\_E\_BAD\_DIGEST**</dt></span></span> </dl>      | <span data-ttu-id="216f3-142">Die Signatur der Datei wurde nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="216f3-142">The signature of the file was not verified.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="216f3-143"><dt>**\_e \_ NoSignature Vertrauen**</dt></span><span class="sxs-lookup"><span data-stu-id="216f3-143"><dt>**TRUST\_E\_NOSIGNATURE**</dt></span></span> </dl>      | <span data-ttu-id="216f3-144">Die Datei wurde nicht signiert oder enthielt eine ungültige Signatur.</span><span class="sxs-lookup"><span data-stu-id="216f3-144">The file was not signed or had a signature that is not valid.</span></span><br/>                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="216f3-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="216f3-145">Requirements</span></span>



| <span data-ttu-id="216f3-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="216f3-146">Requirement</span></span> | <span data-ttu-id="216f3-147">Wert</span><span class="sxs-lookup"><span data-stu-id="216f3-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="216f3-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="216f3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="216f3-149">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="216f3-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="216f3-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="216f3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="216f3-151">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="216f3-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="216f3-152">DLL</span><span class="sxs-lookup"><span data-stu-id="216f3-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="216f3-153"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="216f3-153"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
