---
title: Matrix4x3F-Klasse (D2d1 \_ Helper. h)
description: Die Matrix4x3F-Klasse stellt eine 4 x 3-Matrix dar und bietet Hilfsmethoden zum Erstellen von Matrizen.
ms.assetid: 633B1828-0CB5-4CD3-9826-C65083C6C0A9
keywords:
- Matrix4x3F-Klasse Direct2D
- Matrix4x3F-Klasse Direct2D, beschrieben
topic_type:
- apiref
api_name:
- Matrix4x3F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81467b51eb22586d537c7ea8032e13a30da19c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859315"
---
# <a name="matrix4x3f-class"></a><span data-ttu-id="7d3f9-105">Matrix4x3F-Klasse</span><span class="sxs-lookup"><span data-stu-id="7d3f9-105">Matrix4x3F class</span></span>

<span data-ttu-id="7d3f9-106">Die **Matrix4x3F** -Klasse stellt eine 4 x 3-Matrix dar und bietet Hilfsmethoden zum Erstellen von Matrizen.</span><span class="sxs-lookup"><span data-stu-id="7d3f9-106">The **Matrix4x3F** class represents a 4-by-3 matrix and provides convenience methods for creating matrices.</span></span>

## <a name="members"></a><span data-ttu-id="7d3f9-107">Member</span><span class="sxs-lookup"><span data-stu-id="7d3f9-107">Members</span></span>

<span data-ttu-id="7d3f9-108">Die **Matrix4x3F** -Klasse erbt von [**D2D1 \_ Matrix \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f).</span><span class="sxs-lookup"><span data-stu-id="7d3f9-108">The **Matrix4x3F** class inherits from [**D2D1\_MATRIX\_4X3\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f).</span></span> <span data-ttu-id="7d3f9-109">**Matrix4x3F** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="7d3f9-109">**Matrix4x3F** also has these types of members:</span></span>

-   [<span data-ttu-id="7d3f9-110">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="7d3f9-110">Constructors</span></span>](#constructors)

### <a name="constructors"></a><span data-ttu-id="7d3f9-111">Konstruktoren</span><span class="sxs-lookup"><span data-stu-id="7d3f9-111">Constructors</span></span>

<span data-ttu-id="7d3f9-112">Die **Matrix4x3F** -Klasse verfügt über diese Konstruktoren.</span><span class="sxs-lookup"><span data-stu-id="7d3f9-112">The **Matrix4x3F** class has these constructors.</span></span>



| <span data-ttu-id="7d3f9-113">Konstruktor</span><span class="sxs-lookup"><span data-stu-id="7d3f9-113">Constructor</span></span>                                                                                                                                                                                           | <span data-ttu-id="7d3f9-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d3f9-114">Description</span></span>                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d3f9-115">**Matrix4x3F()**</span><span class="sxs-lookup"><span data-stu-id="7d3f9-115">**Matrix4x3F()**</span></span>](matrix4x3f-matrix4x3f--.md)                                                                                                                                                       | <span data-ttu-id="7d3f9-116">Instanziiert eine neue Instanz einer nicht initialisierten **Matrix4x3F** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="7d3f9-116">Instantiates a new instance of an uninitialized **Matrix4x3F** class.</span></span><br/>                                                   |
| [<span data-ttu-id="7d3f9-117">**Matrix4x3F (float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-, float-**</span><span class="sxs-lookup"><span data-stu-id="7d3f9-117">**Matrix4x3F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)**</span></span>](matrix4x3f-matrix4x3f-floats-.md) | <span data-ttu-id="7d3f9-118">Instanziiert eine neue Instanz einer **Matrix4x3F** -Klasse, die mit allen Gleit Komma-Matrix Werten initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7d3f9-118">Instantiates a new instance of a **Matrix4x3F** class that is initialized with all of the floating point matrix values.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7d3f9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7d3f9-119">Requirements</span></span>



| <span data-ttu-id="7d3f9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7d3f9-120">Requirement</span></span> | <span data-ttu-id="7d3f9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7d3f9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3f9-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7d3f9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7d3f9-123">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7d3f9-123">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="7d3f9-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7d3f9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7d3f9-125">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7d3f9-125">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="7d3f9-126">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="7d3f9-126">Minimum supported phone</span></span><br/>  | <span data-ttu-id="7d3f9-127">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="7d3f9-127">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="7d3f9-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d3f9-128">Namespace</span></span><br/>                | <span data-ttu-id="7d3f9-129">D2D1</span><span class="sxs-lookup"><span data-stu-id="7d3f9-129">D2D1</span></span><br/>                                                                                                                          |
| <span data-ttu-id="7d3f9-130">Header</span><span class="sxs-lookup"><span data-stu-id="7d3f9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d3f9-131"><dt>D2d1 \_ Helper. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d3f9-131"><dt>D2d1\_helper.h</dt></span></span> </dl>                                                |
| <span data-ttu-id="7d3f9-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7d3f9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="7d3f9-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d3f9-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="7d3f9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7d3f9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d3f9-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d3f9-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



## <a name="see-also"></a><span data-ttu-id="7d3f9-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d3f9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d3f9-137">**D2D1 \_ Matrix \_ 4X3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="7d3f9-137">**D2D1\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)
</dt> </dl>

 

 





