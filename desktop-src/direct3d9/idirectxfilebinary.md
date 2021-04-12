---
description: Anwendungen verwenden die Methoden der idirectxfilebinary-Schnittstelle zum Lesen und Abrufen von Informationen zu Binärdaten. Veraltet.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Idirectxfilebinary-Schnittstelle (dxfile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219476"
---
# <a name="idirectxfilebinary-interface"></a><span data-ttu-id="66db7-104">Idirectxfilebinary-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="66db7-104">IDirectXFileBinary interface</span></span>

<span data-ttu-id="66db7-105">Anwendungen verwenden die Methoden der idirectxfilebinary-Schnittstelle zum Lesen und Abrufen von Informationen zu Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="66db7-105">Applications use the methods of the IDirectXFileBinary interface to read and retrieve information about binary data.</span></span> <span data-ttu-id="66db7-106">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="66db7-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="66db7-107">Member</span><span class="sxs-lookup"><span data-stu-id="66db7-107">Members</span></span>

<span data-ttu-id="66db7-108">Die **idirectxfilebinary** -Schnittstelle erbt von [**idirectxfileobject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="66db7-108">The **IDirectXFileBinary** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="66db7-109">**Idirectxfilebinary** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="66db7-109">**IDirectXFileBinary** also has these types of members:</span></span>

-   [<span data-ttu-id="66db7-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="66db7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="66db7-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="66db7-111">Methods</span></span>

<span data-ttu-id="66db7-112">Die **idirectxfilebinary** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="66db7-112">The **IDirectXFileBinary** interface has these methods.</span></span>



| <span data-ttu-id="66db7-113">Methode</span><span class="sxs-lookup"><span data-stu-id="66db7-113">Method</span></span>                                                 | <span data-ttu-id="66db7-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66db7-114">Description</span></span>                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66db7-115">**Getmimetype**</span><span class="sxs-lookup"><span data-stu-id="66db7-115">**GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md) | <span data-ttu-id="66db7-116">Ruft den Multipurpose Internet Mail Extensions (MIME)-Typ für die Binärdaten ab.</span><span class="sxs-lookup"><span data-stu-id="66db7-116">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="66db7-117">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="66db7-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="66db7-118">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="66db7-118">**GetSize**</span></span>](idirectxfilebinary--getsize.md)         | <span data-ttu-id="66db7-119">Ruft die Größe der Binärdaten ab.</span><span class="sxs-lookup"><span data-stu-id="66db7-119">Retrieves the size of the binary data.</span></span> <span data-ttu-id="66db7-120">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="66db7-120">Deprecated.</span></span><br/>                                               |
| [<span data-ttu-id="66db7-121">**Lesen**</span><span class="sxs-lookup"><span data-stu-id="66db7-121">**Read**</span></span>](idirectxfilebinary--read.md)               | <span data-ttu-id="66db7-122">Liest die Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="66db7-122">Reads the binary data.</span></span> <span data-ttu-id="66db7-123">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="66db7-123">Deprecated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="66db7-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66db7-124">Remarks</span></span>

<span data-ttu-id="66db7-125">Die GUID für die idirectxfilebinary-Schnittstelle ist IID \_ idirectxfilebinary.</span><span class="sxs-lookup"><span data-stu-id="66db7-125">The GUID for the IDirectXFileBinary interface is IID\_IDirectXFileBinary.</span></span>

<span data-ttu-id="66db7-126">Der lpdirectxfilebinary-Typ wird als Zeiger auf diese Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="66db7-126">The LPDIRECTXFileBinary type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
```



## <a name="requirements"></a><span data-ttu-id="66db7-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66db7-127">Requirements</span></span>



| <span data-ttu-id="66db7-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66db7-128">Requirement</span></span> | <span data-ttu-id="66db7-129">Wert</span><span class="sxs-lookup"><span data-stu-id="66db7-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66db7-130">Header</span><span class="sxs-lookup"><span data-stu-id="66db7-130">Header</span></span><br/>  | <dl> <span data-ttu-id="66db7-131"><dt>Dxfile. h</dt></span><span class="sxs-lookup"><span data-stu-id="66db7-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="66db7-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="66db7-132">Library</span></span><br/> | <dl> <span data-ttu-id="66db7-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66db7-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66db7-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66db7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66db7-135">**Idirectxfileobject**</span><span class="sxs-lookup"><span data-stu-id="66db7-135">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="66db7-136">X-Datei Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="66db7-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




