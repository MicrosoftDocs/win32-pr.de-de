---
description: 'Die GetInfo-Methode ruft Informationen über die aktuellen streamsteuerungseinstellungen ab, einschließlich der Start-und Endzeiten. Diese Methode implementiert die iamstreamcontrol:: GetInfo-Methode.'
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Cbasestreamcontrol. GetInfo-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369214"
---
# <a name="cbasestreamcontrolgetinfo-method"></a><span data-ttu-id="ae884-104">Cbasestreamcontrol. GetInfo-Methode</span><span class="sxs-lookup"><span data-stu-id="ae884-104">CBaseStreamControl.GetInfo method</span></span>

<span data-ttu-id="ae884-105">Die- `GetInfo` Methode ruft Informationen zu den aktuellen streamsteuerungseinstellungen ab, einschließlich der Start-und Endzeiten.</span><span class="sxs-lookup"><span data-stu-id="ae884-105">The `GetInfo` method retrieves information about the current stream-control settings, including the start and stop times.</span></span> <span data-ttu-id="ae884-106">Diese Methode implementiert die [**iamstreamcontrol:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ae884-106">This method implements the [**IAMStreamControl::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae884-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae884-107">Syntax</span></span>


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ae884-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae884-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae884-109">*pinfo*</span><span class="sxs-lookup"><span data-stu-id="ae884-109">*pInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ae884-110">Ein Zeiger auf eine [**am- \_ Stream- \_ Informations**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) Struktur, die vom Aufrufer zugeordnet wird und die die aktuellen streamsteuerungseinstellungen empfängt.</span><span class="sxs-lookup"><span data-stu-id="ae884-110">Pointer to an [**AM\_STREAM\_INFO**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) structure, allocated by the caller, that receives the current stream-control settings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae884-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae884-111">Return value</span></span>

<span data-ttu-id="ae884-112">Gibt den S \_ OK-oder E- \_ Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="ae884-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae884-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae884-113">Requirements</span></span>



| <span data-ttu-id="ae884-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae884-114">Requirement</span></span> | <span data-ttu-id="ae884-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ae884-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae884-116">Header</span><span class="sxs-lookup"><span data-stu-id="ae884-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ae884-117"><dt>"Strauch. h" (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae884-117"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ae884-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae884-118">Library</span></span><br/> | <dl> <span data-ttu-id="ae884-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ae884-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae884-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae884-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae884-121">**Cbasestreamcontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ae884-121">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




