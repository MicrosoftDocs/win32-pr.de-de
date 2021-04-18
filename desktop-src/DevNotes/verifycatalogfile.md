---
description: Überprüft eine einzelne Katalog Datei.
ms.assetid: 4b2de733-ef95-4b0a-8f53-7bc73ffaa2c2
title: Verifycatalogfile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 52083b23041f7f21aa51e326bc00d4cabc76eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365178"
---
# <a name="verifycatalogfile-function"></a><span data-ttu-id="fcddd-103">Verifycatalogfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="fcddd-103">VerifyCatalogFile function</span></span>

<span data-ttu-id="fcddd-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="fcddd-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="fcddd-105">Überprüft eine einzelne Katalog Datei.</span><span class="sxs-lookup"><span data-stu-id="fcddd-105">Verifies a single catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcddd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcddd-106">Syntax</span></span>


```C++
DWORD VerifyCatalogFile(
   LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="fcddd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcddd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcddd-108">*Catalogfullpath*</span><span class="sxs-lookup"><span data-stu-id="fcddd-108">*CatalogFullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="fcddd-109">Der voll qualifizierte Pfad der Katalog Datei, die überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="fcddd-109">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcddd-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fcddd-110">Return value</span></span>

<span data-ttu-id="fcddd-111">Wenn die Funktion erfolgreich ausgeführt wird, wird ein **Fehler \_ Erfolg** zurückgegeben; andernfalls wird der Fehler von [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fcddd-111">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

<span data-ttu-id="fcddd-112">Wenn es sich bei dem Katalog um einen mit Authenticode signierten Katalog handelt, gibt diese Funktion **Fehler \_ Authenticode \_ vertrauenswürdiger \_ Verleger** zurück, wenn Sie erfolgreich ist. andernfalls wird der **Fehler \_ Authenticode- \_ Vertrauensstellung \_ nicht \_ festgelegt**.</span><span class="sxs-lookup"><span data-stu-id="fcddd-112">If the catalog is an Authenticode-signed catalog, this function returns **ERROR\_AUTHENTICODE\_TRUSTED\_PUBLISHER** if it succeeds; otherwise, it returns **ERROR\_AUTHENTICODE\_TRUST\_NOT\_ESTABLISHED**.</span></span>

<span data-ttu-id="fcddd-113">Wenn die Funktion nicht ermitteln kann, ob der Verleger vertrauenswürdig ist, kann der Fehler **nicht \_ \_ identifiziert werden.**</span><span class="sxs-lookup"><span data-stu-id="fcddd-113">If the function is unable to determine whether the publisher is trusted, it may also return **ERROR\_UNIDENTIFIED\_ERROR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcddd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcddd-114">Remarks</span></span>

<span data-ttu-id="fcddd-115">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fcddd-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcddd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcddd-116">Requirements</span></span>



| <span data-ttu-id="fcddd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fcddd-117">Requirement</span></span> | <span data-ttu-id="fcddd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="fcddd-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcddd-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fcddd-119">DLL</span></span><br/> | <dl> <span data-ttu-id="fcddd-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcddd-120"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
