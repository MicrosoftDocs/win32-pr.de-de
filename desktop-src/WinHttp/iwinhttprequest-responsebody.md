---
description: Ruft den Entitäts Text der Antwort als Array nicht signierter Bytes ab.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'Iwinhttprequest:: responenbody-Eigenschaft'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351539"
---
# <a name="iwinhttprequestresponsebody-property"></a><span data-ttu-id="90451-103">Iwinhttprequest:: responenbody-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="90451-103">IWinHttpRequest::ResponseBody property</span></span>

<span data-ttu-id="90451-104">Die Response **Body** -Eigenschaft ruft den Text der Antwort Entität als Array nicht signierter Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="90451-104">The **ResponseBody** property retrieves the response entity body as an array of unsigned bytes.</span></span>

<span data-ttu-id="90451-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="90451-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="90451-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="90451-106">Syntax</span></span>


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a><span data-ttu-id="90451-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="90451-107">Property value</span></span>

<span data-ttu-id="90451-108">Ein **Variant** -Wert, der den Entitäts Text der Antwort als Array nicht signierter Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="90451-108">A **Variant** value that receives the response entity body as an array of unsigned bytes.</span></span> <span data-ttu-id="90451-109">Dieses Array enthält die Rohdaten, die direkt vom Server empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="90451-109">This array contains the raw data as received directly from the server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="90451-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="90451-110">Error codes</span></span>

<span data-ttu-id="90451-111">Der Rückgabewert ist bei Erfolg **S \_ OK** oder andernfalls ein Fehlerwert.</span><span class="sxs-lookup"><span data-stu-id="90451-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="90451-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90451-112">Remarks</span></span>

<span data-ttu-id="90451-113">Diese Eigenschaft gibt die Antwortdaten in einem Array nicht signierter Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="90451-113">This property returns the response data in an array of unsigned bytes.</span></span> <span data-ttu-id="90451-114">Wenn die Antwort keinen Antworttext enthält, wird eine leere Variante zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="90451-114">If the response does not have a response body, an empty variant is returned.</span></span> <span data-ttu-id="90451-115">Diese Eigenschaft kann nur aufgerufen werden, nachdem die [**Send**](iwinhttprequest-send.md) -Methode aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="90451-115">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="90451-116">Weitere Informationen zur Implementierung für Windows XP und Windows 2000 finden Sie unter [Lauf Zeitanforderungen](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="90451-116">For more information about implementation for Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90451-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90451-117">Requirements</span></span>



| <span data-ttu-id="90451-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90451-118">Requirement</span></span> | <span data-ttu-id="90451-119">Wert</span><span class="sxs-lookup"><span data-stu-id="90451-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="90451-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90451-120">Minimum supported client</span></span><br/> | <span data-ttu-id="90451-121">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90451-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="90451-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90451-122">Minimum supported server</span></span><br/> | <span data-ttu-id="90451-123">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90451-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="90451-124">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="90451-124">Redistributable</span></span><br/>          | <span data-ttu-id="90451-125">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="90451-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="90451-126">IDL</span><span class="sxs-lookup"><span data-stu-id="90451-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90451-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90451-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="90451-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="90451-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="90451-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90451-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="90451-130">DLL</span><span class="sxs-lookup"><span data-stu-id="90451-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90451-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90451-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="90451-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90451-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90451-133">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="90451-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="90451-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="90451-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="90451-135">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="90451-135">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="90451-136">**Response Text**</span><span class="sxs-lookup"><span data-stu-id="90451-136">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)
</dt> <dt>

[<span data-ttu-id="90451-137">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="90451-137">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




