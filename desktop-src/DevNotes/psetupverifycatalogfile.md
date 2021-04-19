---
description: Überprüft eine einzelne Katalog Datei mithilfe der Standard Code Signatur Richtlinie des Betriebssystems, z. b. Treiber Signatur.
ms.assetid: 1e2a18a5-506e-46a8-9309-666bec92182d
title: psetupverifycatalogfile-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupVerifyCatalogFile
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 3de792ae6738277d2ab7cb21d8be7f4c5ecfb573
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366898"
---
# <a name="psetupverifycatalogfile-function"></a><span data-ttu-id="a18b4-103">psetupverifycatalogfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="a18b4-103">pSetupVerifyCatalogFile function</span></span>

<span data-ttu-id="a18b4-104">\[Diese Funktion wird von Microsoft nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a18b4-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="a18b4-105">Für eine INF-Datei (Geräteinstallation) sollten Entwickler **setupverifyinffile** verwenden.</span><span class="sxs-lookup"><span data-stu-id="a18b4-105">For an INF file (device install), developers should use **SetupVerifyInfFile**.</span></span> <span data-ttu-id="a18b4-106">Verwenden Sie zum Überprüfen eines nicht-INF-basierten Katalogs **WinVerifyTrust**.\]</span><span class="sxs-lookup"><span data-stu-id="a18b4-106">To validate a non-INF based catalog, use **WinVerifyTrust**.\]</span></span>

<span data-ttu-id="a18b4-107">Überprüft eine einzelne Katalog Datei mithilfe der Standard Code Signatur Richtlinie des Betriebssystems, z. b. Treiber Signatur.</span><span class="sxs-lookup"><span data-stu-id="a18b4-107">Verifies a single catalog file using standard operating system code signing policy, such as driver signing.</span></span>

## <a name="syntax"></a><span data-ttu-id="a18b4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a18b4-108">Syntax</span></span>


```C++
DWORD pSetupVerifyCatalogFile(
  _In_ LPCTSTR CatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="a18b4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a18b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a18b4-110">*Catalogfullpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a18b4-110">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a18b4-111">Der voll qualifizierte Pfad der Katalog Datei, die überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="a18b4-111">The fully qualified path of the catalog file to be verified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a18b4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a18b4-112">Return value</span></span>

<span data-ttu-id="a18b4-113">Wenn die Funktion erfolgreich ausgeführt wird, wird ein **Fehler \_ Erfolg** zurückgegeben; andernfalls wird der Fehler von [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a18b4-113">If the function succeeds, it returns **ERROR\_SUCCESS**; otherwise, it returns the error from [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust).</span></span>

## <a name="remarks"></a><span data-ttu-id="a18b4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a18b4-114">Remarks</span></span>

<span data-ttu-id="a18b4-115">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a18b4-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a18b4-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a18b4-116">Requirements</span></span>



| <span data-ttu-id="a18b4-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a18b4-117">Requirement</span></span> | <span data-ttu-id="a18b4-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a18b4-118">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a18b4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a18b4-119">DLL</span></span><br/> | <dl> <span data-ttu-id="a18b4-120"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a18b4-120"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a18b4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a18b4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a18b4-122">**Setupverifyinffile**</span><span class="sxs-lookup"><span data-stu-id="a18b4-122">**SetupVerifyInfFile**</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupverifyinffilea)
</dt> <dt>

[<span data-ttu-id="a18b4-123">**WinVerifyTrust**</span><span class="sxs-lookup"><span data-stu-id="a18b4-123">**WinVerifyTrust**</span></span>](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)
</dt> </dl>

 

 
