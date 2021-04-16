---
description: Fordert an, Informationen darüber zu erhalten, welche Spalten (Felder) dieser objekttabellenanforderungstyp unterstützt.
MS-HAID: vspixengine.IObjectTableRequest\_RequestSupportedColumnsAsync\_IObjectTableCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Iobjecttablerequest:: requestsupportedcolumnsasync-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0931C81A-65D5-493E-9F54-C7E98FA2FA6F
api_name:
- IObjectTableRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6773a69061e7a17d2271e1a53f89f6f2def1a6c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522747"
---
# <a name="span-idvspixengineiobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dwordspaniobjecttablerequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="f2fae-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>Iobjecttablerequest:: requestsupportedcolumnsasync-Methode</span><span class="sxs-lookup"><span data-stu-id="f2fae-103"><span id="vspixengine.iobjecttablerequest_requestsupportedcolumnsasync_iobjecttablecallback_ptr_dword"></span>IObjectTableRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="f2fae-104">Fordert an, Informationen darüber zu erhalten, welche Spalten (Felder) dieser objekttabellenanforderungstyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2fae-104">Requests to get information about what columns (fields) this object table request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2fae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2fae-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IObjectTableCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="f2fae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2fae-106">Parameters</span></span>

<span data-ttu-id="f2fae-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="f2fae-107">*requestCallback* </span></span>  
<span data-ttu-id="f2fae-108">Die Adresse des Rückrufs, der zum Benachrichtigen des Hosts der Ergebnisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2fae-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="f2fae-109">*progressintervalmsekunden* </span><span class="sxs-lookup"><span data-stu-id="f2fae-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="f2fae-110">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2fae-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2fae-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2fae-111">Return value</span></span>

<span data-ttu-id="f2fae-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f2fae-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f2fae-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f2fae-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2fae-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2fae-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f2fae-115">Header</span><span class="sxs-lookup"><span data-stu-id="f2fae-115">Header</span></span></p></td><td><span data-ttu-id="f2fae-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f2fae-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f2fae-117"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2fae-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f2fae-118">**Iobjecttablerequest**</span><span class="sxs-lookup"><span data-stu-id="f2fae-118">**IObjectTableRequest**</span></span>](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
