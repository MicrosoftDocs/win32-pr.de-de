---
description: Fordert an, dass für das angegebene Ereignis angegebene Informationen aus der Objekttabelle erhalten.
MS-HAID: vspixengine.IObjectTableRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IObjectTableCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iobjecttablerequest:: requestasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EE40F584-CDDE-465D-B4CB-A98B917DD0EE
api_name:
- IObjectTableRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c9108708475b27a7a1882051c7f0177e14470f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746728"
---
# <a name="span-idvspixengineiobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dwordspaniobjecttablerequestrequestasync-method"></a><span data-ttu-id="3cdd6-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>Iobjecttablerequest:: requestasync-Methode</span><span class="sxs-lookup"><span data-stu-id="3cdd6-103"><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>IObjectTableRequest::RequestAsync method</span></span>

<span data-ttu-id="3cdd6-104">Fordert an, dass für das angegebene Ereignis angegebene Informationen aus der Objekttabelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="3cdd6-104">Requests to get specified information from the object table for the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cdd6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cdd6-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventID,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IObjectTableCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="3cdd6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cdd6-106">Parameters</span></span>

<span data-ttu-id="3cdd6-107">*EventID* </span><span class="sxs-lookup"><span data-stu-id="3cdd6-107">*eventID* </span></span>  
<span data-ttu-id="3cdd6-108">Das angegebene Ereignis.</span><span class="sxs-lookup"><span data-stu-id="3cdd6-108">The specified event.</span></span>

<span data-ttu-id="3cdd6-109">*NumColumns* </span><span class="sxs-lookup"><span data-stu-id="3cdd6-109">*numColumns* </span></span>  
<span data-ttu-id="3cdd6-110">Die Anzahl der Spalten (Felder) der aufzurufenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="3cdd6-110">The number of columns (fields) of information to get.</span></span>

<span data-ttu-id="3cdd6-111">*count1- \_ Spalten* </span><span class="sxs-lookup"><span data-stu-id="3cdd6-111">*count1\_columns* </span></span>  
<span data-ttu-id="3cdd6-112">Die angegebenen Spalten (Felder).</span><span class="sxs-lookup"><span data-stu-id="3cdd6-112">The specified columns (fields).</span></span>

<span data-ttu-id="3cdd6-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="3cdd6-113">*requestCallback* </span></span>  
<span data-ttu-id="3cdd6-114">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3cdd6-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="3cdd6-115">*requestcookie* </span><span class="sxs-lookup"><span data-stu-id="3cdd6-115">*requestCookie* </span></span>  
<span data-ttu-id="3cdd6-116">Ein Cookie, das die Anforderung eindeutig identifiziert, und kann verwendet werden, um zu signalisieren, dass es abgebrochen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cdd6-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="3cdd6-117">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="3cdd6-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="3cdd6-118">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3cdd6-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="3cdd6-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3cdd6-119">Return value</span></span>

<span data-ttu-id="3cdd6-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="3cdd6-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3cdd6-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3cdd6-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cdd6-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3cdd6-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="3cdd6-123">Header</span><span class="sxs-lookup"><span data-stu-id="3cdd6-123">Header</span></span></p></td><td><span data-ttu-id="3cdd6-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="3cdd6-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="3cdd6-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cdd6-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="3cdd6-126">**Iobjecttablerequest**</span><span class="sxs-lookup"><span data-stu-id="3cdd6-126">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
