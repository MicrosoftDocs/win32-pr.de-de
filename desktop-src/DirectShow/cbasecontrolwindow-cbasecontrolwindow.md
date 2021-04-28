---
description: CBaseControlWindow.CBaseControlWindow-Konstruktor – Konstruktormethode.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: CBaseControlWindow.CBaseControlWindow-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47c8277a76dbf0fbb9e05262eea5b419466044cc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096338"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="0f05a-103">CBaseControlWindow.CBaseControlWindow-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="0f05a-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="0f05a-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="0f05a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f05a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f05a-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="0f05a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f05a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f05a-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="0f05a-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="0f05a-108">Zeiger auf das besitzende Medienfilterobjekt.</span><span class="sxs-lookup"><span data-stu-id="0f05a-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="0f05a-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="0f05a-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="0f05a-110">Zeiger auf den kritischen Abschnitt, der zum Sperren verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f05a-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="0f05a-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="0f05a-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0f05a-112">Zeiger auf die Objektbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="0f05a-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="0f05a-113">*Punk*</span><span class="sxs-lookup"><span data-stu-id="0f05a-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0f05a-114">Zeiger auf die steuernde **IUnknown-Schnittstelle,** wenn das Objekt Teil eines Aggregats ist; Andernfalls muss **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="0f05a-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0f05a-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="0f05a-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0f05a-116">Zeiger auf eine Variable, die einen HRESULT-Wert empfängt, der den Erfolg oder Fehler der Konstruktormethode angibt.</span><span class="sxs-lookup"><span data-stu-id="0f05a-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f05a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f05a-117">Requirements</span></span>



| <span data-ttu-id="0f05a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f05a-118">Requirement</span></span> | <span data-ttu-id="0f05a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0f05a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f05a-120">Header</span><span class="sxs-lookup"><span data-stu-id="0f05a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0f05a-121"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f05a-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f05a-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0f05a-122">Library</span></span><br/> | <dl> <span data-ttu-id="0f05a-123"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0f05a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f05a-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0f05a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f05a-125">**CBaseControlWindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0f05a-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




