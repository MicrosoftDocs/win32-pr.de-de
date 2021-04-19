---
description: Tritt auf, wenn Daten aus der Antwort verfügbar sind.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Iwinhttprequestevents:: onresponabdataavailable-Ereignis'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351759"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a><span data-ttu-id="d2a7a-103">Iwinhttprequestevents:: onresponabdataavailable-Ereignis</span><span class="sxs-lookup"><span data-stu-id="d2a7a-103">IWinHttpRequestEvents::OnResponseDataAvailable event</span></span>

<span data-ttu-id="d2a7a-104">Das **onresponondataavailable** -Ereignis tritt auf, wenn Daten aus der Antwort verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-104">The **OnResponseDataAvailable** event occurs when data is available from the response.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a7a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2a7a-105">Syntax</span></span>


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a><span data-ttu-id="d2a7a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2a7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a7a-107">*Daten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2a7a-107">*Data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a7a-108">Ein NULL basiertes Bytearray, das die von Microsoft Windows HTTP-Diensten (WinHTTP) empfangenen Antwortdaten bis zu dem Punkt empfängt, an dem dieses Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-108">A zero-based array of bytes that receives the response data received by Microsoft Windows HTTP Services (WinHTTP) up to the point that this event occurs.</span></span> <span data-ttu-id="d2a7a-109">Dies ist eine **Variante** vom Typ VT \_ array \| VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-109">This is a **VARIANT** of type VT\_ARRAY \| VT\_UI1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a7a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2a7a-110">Return value</span></span>

<span data-ttu-id="d2a7a-111">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a7a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2a7a-112">Remarks</span></span>

<span data-ttu-id="d2a7a-113">Da Daten in Bytes vorliegen, müssen Sie in breit Zeichen konvertiert werden, wenn Sie in eine Zeichenfolge mit breit Zeichen (Unicode) eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-113">Because data is in bytes, it must be converted to wide characters when placed in a wide character (Unicode) string.</span></span>

> [!Note]  
> <span data-ttu-id="d2a7a-114">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2a7a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2a7a-115">Requirements</span></span>



| <span data-ttu-id="d2a7a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2a7a-116">Requirement</span></span> | <span data-ttu-id="d2a7a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d2a7a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a7a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a7a-119">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2a7a-119">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="d2a7a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2a7a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a7a-121">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2a7a-121">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="d2a7a-122">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d2a7a-122">Redistributable</span></span><br/>          | <span data-ttu-id="d2a7a-123">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d2a7a-123">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="d2a7a-124">IDL</span><span class="sxs-lookup"><span data-stu-id="d2a7a-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2a7a-125"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2a7a-125"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a7a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2a7a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a7a-127">**Iwinhttprequestevents**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-127">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="d2a7a-128">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="d2a7a-128">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="d2a7a-129">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="d2a7a-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




