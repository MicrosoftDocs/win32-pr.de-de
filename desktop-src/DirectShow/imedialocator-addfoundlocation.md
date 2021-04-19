---
description: Die addfoundlocation-Methode fügt dem Verzeichnis Cache ein Verzeichnis hinzu.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: 'Imedialocator:: addfoundlocation-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 76d878e5b013b8c6a061d777d4ec837bca85f8e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354048"
---
# <a name="imedialocatoraddfoundlocation-method"></a><span data-ttu-id="4e181-103">Imedialocator:: addfoundlocation-Methode</span><span class="sxs-lookup"><span data-stu-id="4e181-103">IMediaLocator::AddFoundLocation method</span></span>

> [!Note]  
> <span data-ttu-id="4e181-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="4e181-104">\[Deprecated.</span></span> <span data-ttu-id="4e181-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="4e181-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4e181-106">Die- `AddFoundLocation` Methode fügt dem Verzeichnis Cache ein Verzeichnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="4e181-106">The `AddFoundLocation` method adds a directory to the directory cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e181-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e181-107">Syntax</span></span>


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a><span data-ttu-id="4e181-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e181-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e181-109">*Verzeichnisname*</span><span class="sxs-lookup"><span data-stu-id="4e181-109">*DirectoryName*</span></span> 
</dt> <dd>

<span data-ttu-id="4e181-110">Verzeichnispfad, der dem Cache hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4e181-110">Directory path to add to the cache.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e181-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e181-111">Return value</span></span>

<span data-ttu-id="4e181-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e181-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e181-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4e181-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e181-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e181-114">Remarks</span></span>

<span data-ttu-id="4e181-115">Der medienlocator speichert einen Cache von Verzeichnis Pfaden, in denen Dateien in früheren Such Vorgängen erfolgreich gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="4e181-115">The media locator keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="4e181-116">Wenn eine Datei erfolgreich lokalisiert wurde, wird das Verzeichnis dem Cache hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4e181-116">When it successfully locates a file, it adds the directory to the cache.</span></span>

> [!Note]  
> <span data-ttu-id="4e181-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="4e181-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4e181-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="4e181-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4e181-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4e181-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4e181-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e181-120">Requirements</span></span>



| <span data-ttu-id="4e181-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e181-121">Requirement</span></span> | <span data-ttu-id="4e181-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4e181-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e181-123">Header</span><span class="sxs-lookup"><span data-stu-id="4e181-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4e181-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4e181-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4e181-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e181-125">Library</span></span><br/> | <dl> <span data-ttu-id="4e181-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="4e181-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e181-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e181-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e181-128">**Imedialocator-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4e181-128">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="4e181-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="4e181-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




