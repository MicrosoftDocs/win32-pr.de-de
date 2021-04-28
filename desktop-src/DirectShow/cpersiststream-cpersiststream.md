---
description: 'CPersistStream.CPersistStream-Konstruktor : Konstruktormethode.'
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: CPersistStream.CPersistStream-Konstruktor (Pstream.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e3be9233d76929ebfcb79121c60ef6c1af35b56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085608"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="406dc-103">CPersistStream.CPersistStream-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="406dc-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="406dc-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="406dc-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="406dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="406dc-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="406dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="406dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="406dc-107">*Punk*</span><span class="sxs-lookup"><span data-stu-id="406dc-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="406dc-108">Zeiger auf die **IUnknown-Schnittstelle** des delegierenden Objekts.</span><span class="sxs-lookup"><span data-stu-id="406dc-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="406dc-109">*Phr*</span><span class="sxs-lookup"><span data-stu-id="406dc-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="406dc-110">Zeiger auf den allgemeinen COM-Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="406dc-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="406dc-111">Dieser Wert wird nur geändert, wenn diese Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="406dc-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="406dc-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="406dc-112">Requirements</span></span>



| <span data-ttu-id="406dc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="406dc-113">Requirement</span></span> | <span data-ttu-id="406dc-114">Wert</span><span class="sxs-lookup"><span data-stu-id="406dc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="406dc-115">Header</span><span class="sxs-lookup"><span data-stu-id="406dc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="406dc-116"><dt>Pstream.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="406dc-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="406dc-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="406dc-117">Library</span></span><br/> | <dl> <span data-ttu-id="406dc-118"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="406dc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="406dc-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="406dc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="406dc-120">**CPersistStream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="406dc-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




