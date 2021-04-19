---
description: Installiert eine Katalog Datei.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: psetupinstallcatalog-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352027"
---
# <a name="psetupinstallcatalog-function"></a><span data-ttu-id="2d652-103">psetupinstallcatalog-Funktion</span><span class="sxs-lookup"><span data-stu-id="2d652-103">pSetupInstallCatalog function</span></span>

<span data-ttu-id="2d652-104">\[Diese Funktion wird von Microsoft nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d652-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="2d652-105">Entwickler sollten **cryptchart adminaddcatalog** verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="2d652-105">Developers should use **CryptCATAdminAddCatalog**.\]</span></span>

<span data-ttu-id="2d652-106">Installiert eine Katalog Datei.</span><span class="sxs-lookup"><span data-stu-id="2d652-106">Installs a catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d652-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d652-107">Syntax</span></span>


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="2d652-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d652-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d652-109">*Catalogfullpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d652-109">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d652-110">Der voll qualifizierte Pfad des Katalogs, der auf dem System installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d652-110">The fully qualified path of the catalog to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="2d652-111">*Newbasename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d652-111">*NewBaseName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d652-112">Der neue Basis Name, der verwendet werden soll, wenn die Katalog Datei in den Katalog Speicher kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="2d652-112">The new base name to use when the catalog file is copied into the catalog store.</span></span>

</dd> <dt>

<span data-ttu-id="2d652-113">*Newcatalogfullpath* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="2d652-113">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d652-114">Empfängt optional den voll qualifizierten Pfad der Katalog Datei im Katalog Speicher.</span><span class="sxs-lookup"><span data-stu-id="2d652-114">Optionally receives the fully qualified path of the catalog file within the catalog store.</span></span> <span data-ttu-id="2d652-115">Dieser Puffer muss mindestens eine maximale Anzahl von **\_ Pfad** bytes (ANSI-Version) oder "Zeichen" (Unicode-Version) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2d652-115">This buffer should be at least **MAX\_PATH** bytes (ANSI version) or chars (Unicode version).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d652-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d652-116">Return value</span></span>

<span data-ttu-id="2d652-117">Wenn die Funktion erfolgreich ausgeführt wird, wird **kein \_ Fehler** zurückgegeben; andernfalls wird ein Win32-Fehlercode zurückgegeben, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="2d652-117">If the function succeeds, it returns **NO\_ERROR**; otherwise, it returns a Win32 error code that indicates the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d652-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d652-118">Remarks</span></span>

<span data-ttu-id="2d652-119">Die Datei wird vom System in ein spezielles Verzeichnis kopiert und optional umbenannt.</span><span class="sxs-lookup"><span data-stu-id="2d652-119">The file is copied by the system into a special directory and is optionally renamed.</span></span>

<span data-ttu-id="2d652-120">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2d652-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d652-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d652-121">Requirements</span></span>



| <span data-ttu-id="2d652-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d652-122">Requirement</span></span> | <span data-ttu-id="2d652-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2d652-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d652-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2d652-124">DLL</span></span><br/> | <dl> <span data-ttu-id="2d652-125"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d652-125"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d652-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d652-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d652-127">**Cryptder adminaddcatalog**</span><span class="sxs-lookup"><span data-stu-id="2d652-127">**CryptCATAdminAddCatalog**</span></span>](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
