---
description: Installiert einen Katalog in einem Verzeichnis.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: Installcatalog-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356020"
---
# <a name="installcatalog-function"></a><span data-ttu-id="eb9cf-103">Installcatalog-Funktion</span><span class="sxs-lookup"><span data-stu-id="eb9cf-103">InstallCatalog function</span></span>

<span data-ttu-id="eb9cf-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="eb9cf-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="eb9cf-105">Installiert einen Katalog in einem Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-105">Installs a catalog in a directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb9cf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb9cf-106">Syntax</span></span>


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="eb9cf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb9cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb9cf-108">*Catalogfullpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb9cf-108">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9cf-109">Ein Zeiger auf eine Zeichenfolge, die den vollständigen Pfad des Katalogs vor der Installation darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-109">A pointer to a string that represents the full path of the catalog before installation.</span></span>

</dd> <dt>

<span data-ttu-id="eb9cf-110">*Newbasename* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="eb9cf-110">*NewBaseName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9cf-111">Ein Zeiger auf den neuen Basisnamen.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-111">A pointer to the new base name.</span></span>

</dd> <dt>

<span data-ttu-id="eb9cf-112">*Newcatalogfullpath* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="eb9cf-112">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb9cf-113">Ein Zeiger auf eine Zeichenfolge, die den vollständigen Pfad des Katalogs nach der Installation darstellt.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-113">A pointer to a string that represent the full path of the catalog after installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb9cf-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eb9cf-114">Return value</span></span>

<span data-ttu-id="eb9cf-115">Diese Funktion ist zurzeit nicht implementiert, sodass Sie keinen tatsächlichen Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-115">This function is not currently implemented, so it does not return an actual value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb9cf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb9cf-116">Remarks</span></span>

<span data-ttu-id="eb9cf-117">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eb9cf-117">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb9cf-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb9cf-118">Requirements</span></span>



| <span data-ttu-id="eb9cf-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb9cf-119">Requirement</span></span> | <span data-ttu-id="eb9cf-120">Wert</span><span class="sxs-lookup"><span data-stu-id="eb9cf-120">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb9cf-121">DLL</span><span class="sxs-lookup"><span data-stu-id="eb9cf-121">DLL</span></span><br/> | <dl> <span data-ttu-id="eb9cf-122"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb9cf-122"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
