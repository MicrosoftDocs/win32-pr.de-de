---
description: Die TAPI-Zeilen \_ Antwortnachricht wird gesendet, um die Ergebnisse von Funktionsaufrufen zu melden, die asynchron abgeschlossen wurden.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: LINE_REPLY Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371769"
---
# <a name="line_reply-message"></a><span data-ttu-id="dbe9a-103">Zeilen \_ Antwortnachricht</span><span class="sxs-lookup"><span data-stu-id="dbe9a-103">LINE\_REPLY message</span></span>

<span data-ttu-id="dbe9a-104">Die TAPI- **Zeilen \_ Antwort** Nachricht wird gesendet, um die Ergebnisse von Funktionsaufrufen zu melden, die asynchron abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-104">The TAPI **LINE\_REPLY** message is sent to report the results of function calls that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="dbe9a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbe9a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbe9a-106">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="dbe9a-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe9a-107">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="dbe9a-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="dbe9a-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe9a-109">Gibt die Rückruf Instanz der Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="dbe9a-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="dbe9a-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe9a-111">Der Anforderungs Bezeichner, für den dies die Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="dbe9a-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="dbe9a-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe9a-113">Die Erfolgs-oder Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-113">The success or error indication.</span></span> <span data-ttu-id="dbe9a-114">Die Anwendung sollte diesen Parameter in einen Long-Typ umwandeln.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="dbe9a-115">NULL gibt den Erfolg an; eine negative Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="dbe9a-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="dbe9a-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="dbe9a-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbe9a-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbe9a-118">Return value</span></span>

<span data-ttu-id="dbe9a-119">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbe9a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbe9a-120">Remarks</span></span>

<span data-ttu-id="dbe9a-121">Funktionen, die asynchron agieren, geben einen positiven Anforderungs-ID-Wert an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="dbe9a-122">Dieser Anforderungs Bezeichner wird mit der Antwortnachricht zurückgegeben, um die abgeschlossene Anforderung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="dbe9a-123">Der andere Parameter für die **Zeilen \_ Antwort** Nachricht enthält die Erfolgs-oder Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-123">The other parameter for the **LINE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="dbe9a-124">Mögliche Fehler sind identisch mit denen, die von der entsprechenden Funktion definiert werden.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="dbe9a-125">Diese Meldung kann nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-125">This message cannot be disabled.</span></span>

<span data-ttu-id="dbe9a-126">In einigen Fällen kann es vorkommen, dass eine Anwendung die **Zeilen \_ Antwort** Nachricht nicht empfängt, die einem Rückruf einer asynchronen Funktion entspricht.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-126">In some cases, an application may fail to receive the **LINE\_REPLY** message corresponding to a call to an asynchronous function.</span></span> <span data-ttu-id="dbe9a-127">Dies tritt auf, wenn die Zuordnung des entsprechenden Telefon Handles aufgehoben wird, bevor die Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-127">This occurs if the corresponding call handle is deallocated before the message has been received.</span></span>

> [!Note]  
> <span data-ttu-id="dbe9a-128">Wenn eine Anwendung einen asynchronen Vorgang aufruft, mit dem Daten in den Anwendungs Speicher geschrieben werden, muss die Anwendung diesen Arbeitsspeicher für das Schreiben verfügbar halten, bis eine **Zeilen \_ Antwort** oder eine [**Zeile \_ gatherdigits**](line-gatherdigits.md) -Nachricht empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="dbe9a-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a **LINE\_REPLY** or [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dbe9a-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbe9a-129">Requirements</span></span>



| <span data-ttu-id="dbe9a-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbe9a-130">Requirement</span></span> | <span data-ttu-id="dbe9a-131">Wert</span><span class="sxs-lookup"><span data-stu-id="dbe9a-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dbe9a-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="dbe9a-132">TAPI version</span></span><br/> | <span data-ttu-id="dbe9a-133">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="dbe9a-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="dbe9a-134">Header</span><span class="sxs-lookup"><span data-stu-id="dbe9a-134">Header</span></span><br/>       | <dl> <span data-ttu-id="dbe9a-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbe9a-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe9a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbe9a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe9a-137">**Zeilen \_ gatherziffern**</span><span class="sxs-lookup"><span data-stu-id="dbe9a-137">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> </dl>

 

 




