---
description: 'CBaseControlVideo.CBaseControlVideo-Konstruktor : Konstruktormethode.'
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: CBaseControlVideo.CBaseControlVideo-Konstruktor (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096348"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="8035a-103">CBaseControlVideo.CBaseControlVideo-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="8035a-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="8035a-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="8035a-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8035a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8035a-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="8035a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8035a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8035a-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="8035a-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="8035a-108">Zeiger auf das besitzende Medienfilterobjekt.</span><span class="sxs-lookup"><span data-stu-id="8035a-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="8035a-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="8035a-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="8035a-110">Zeiger auf den kritischen Abschnitt, der zum Sperren verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8035a-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="8035a-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="8035a-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="8035a-112">Zeiger auf die Objektbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="8035a-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="8035a-113">*Punk*</span><span class="sxs-lookup"><span data-stu-id="8035a-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8035a-114">Zeiger auf die steuernde **IUnknown-Schnittstelle,** wenn das Objekt Teil eines Aggregats ist; andernfalls muss NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="8035a-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8035a-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="8035a-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8035a-116">Zeiger auf eine Variable, die einen HRESULT-Wert empfängt, der den Erfolg oder Fehler der Konstruktormethode angibt.</span><span class="sxs-lookup"><span data-stu-id="8035a-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8035a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8035a-117">Remarks</span></span>

<span data-ttu-id="8035a-118">Das -Objekt implementiert die [**IBasicVideo-Steuerelementschnittstelle.**](/windows/desktop/api/Control/nn-control-ibasicvideo)</span><span class="sxs-lookup"><span data-stu-id="8035a-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="8035a-119">Alle Schnittstellenmethoden von [**IBasicVideo,**](/windows/desktop/api/Control/nn-control-ibasicvideo) die diese Klasse implementiert, erfordern, dass der Filter ordnungsgemäß verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8035a-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="8035a-120">Aus diesem Grund wird der Klasse ein Pin übergeben, mit dem sie synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8035a-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="8035a-121">Jedes Mal, wenn eine Schnittstellenmethode aufgerufen wird, bestimmt das -Objekt, dass die Stecknadel weiterhin verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8035a-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="8035a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8035a-122">Requirements</span></span>



| <span data-ttu-id="8035a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8035a-123">Requirement</span></span> | <span data-ttu-id="8035a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="8035a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8035a-125">Header</span><span class="sxs-lookup"><span data-stu-id="8035a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8035a-126"><dt>Ctlutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8035a-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8035a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8035a-127">Library</span></span><br/> | <dl> <span data-ttu-id="8035a-128"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8035a-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8035a-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8035a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8035a-130">**CBaseControlVideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8035a-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




