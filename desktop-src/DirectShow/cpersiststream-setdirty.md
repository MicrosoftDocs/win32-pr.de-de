---
description: Ändert das Änderungsflag für den aktuellen Stream.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Cpersiststream. SetDirty-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361532"
---
# <a name="cpersiststreamsetdirty-method"></a><span data-ttu-id="8a4fc-103">Cpersiststream. SetDirty-Methode</span><span class="sxs-lookup"><span data-stu-id="8a4fc-103">CPersistStream.SetDirty method</span></span>

<span data-ttu-id="8a4fc-104">Ändert das Änderungsflag für den aktuellen Stream.</span><span class="sxs-lookup"><span data-stu-id="8a4fc-104">Changes the dirty flag for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a4fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a4fc-105">Syntax</span></span>


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a><span data-ttu-id="8a4fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a4fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a4fc-107">*nicht geändert*</span><span class="sxs-lookup"><span data-stu-id="8a4fc-107">*fDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="8a4fc-108">Neues Änderungsflag für diesen Stream.</span><span class="sxs-lookup"><span data-stu-id="8a4fc-108">New dirty flag for this stream.</span></span> <span data-ttu-id="8a4fc-109">" **True** " bedeutet, dass die Daten nicht gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="8a4fc-109">**TRUE** means that the data has not been saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a4fc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a4fc-110">Return value</span></span>

<span data-ttu-id="8a4fc-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8a4fc-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a4fc-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a4fc-112">Requirements</span></span>



| <span data-ttu-id="8a4fc-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a4fc-113">Requirement</span></span> | <span data-ttu-id="8a4fc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8a4fc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a4fc-115">Header</span><span class="sxs-lookup"><span data-stu-id="8a4fc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8a4fc-116"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a4fc-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8a4fc-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8a4fc-117">Library</span></span><br/> | <dl> <span data-ttu-id="8a4fc-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8a4fc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a4fc-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a4fc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a4fc-120">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8a4fc-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




