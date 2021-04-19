---
description: Die TAPI-Telefon \_ Antwortnachricht wird an eine Anwendung gesendet, um die Ergebnisse des Funktionsaufrufs zu melden, die asynchron abgeschlossen wurden.
ms.assetid: 434f37d6-f385-4cc9-9658-2b683cab532c
title: PHONE_REPLY Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091920c631bf56d58959d60288a1af039495d2d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367516"
---
# <a name="phone_reply-message"></a><span data-ttu-id="1c645-103">Telefon \_ Antwortnachricht</span><span class="sxs-lookup"><span data-stu-id="1c645-103">PHONE\_REPLY message</span></span>

<span data-ttu-id="1c645-104">Die TAPI- **Telefon \_ Antwort** Nachricht wird an eine Anwendung gesendet, um die Ergebnisse des Funktionsaufrufs zu melden, die asynchron abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="1c645-104">The TAPI **PHONE\_REPLY** message is sent to an application to report the results of function call that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="1c645-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c645-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c645-106">*hphone*</span><span class="sxs-lookup"><span data-stu-id="1c645-106">*hPhone*</span></span> 
</dt> <dd>

<span data-ttu-id="1c645-107">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c645-107">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="1c645-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="1c645-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="1c645-109">Gibt die Rückruf Instanz der Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="1c645-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="1c645-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="1c645-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="1c645-111">Der Anforderungs Bezeichner, für den dies die Antwort ist.</span><span class="sxs-lookup"><span data-stu-id="1c645-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="1c645-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="1c645-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="1c645-113">Die Erfolgs-oder Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="1c645-113">The success or error indication.</span></span> <span data-ttu-id="1c645-114">Die Anwendung sollte diesen Parameter in einen Long-Typ umwandeln.</span><span class="sxs-lookup"><span data-stu-id="1c645-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="1c645-115">NULL gibt den Erfolg an; eine negative Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="1c645-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="1c645-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="1c645-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="1c645-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c645-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c645-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c645-118">Return value</span></span>

<span data-ttu-id="1c645-119">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="1c645-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c645-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c645-120">Remarks</span></span>

<span data-ttu-id="1c645-121">Funktionen, die asynchron agieren, geben einen positiven Anforderungs-ID-Wert an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="1c645-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="1c645-122">Dieser Anforderungs Bezeichner wird mit der Antwortnachricht zurückgegeben, um die abgeschlossene Anforderung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1c645-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="1c645-123">Der andere Parameter für die **Telefon \_ Antwort** Nachricht enthält die Erfolgs-oder Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="1c645-123">The other parameter for the **PHONE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="1c645-124">Mögliche Fehler sind identisch mit denen, die von der entsprechenden Funktion definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1c645-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="1c645-125">Diese Meldung kann nicht deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="1c645-125">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c645-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c645-126">Requirements</span></span>



| <span data-ttu-id="1c645-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c645-127">Requirement</span></span> | <span data-ttu-id="1c645-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1c645-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1c645-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="1c645-129">TAPI version</span></span><br/> | <span data-ttu-id="1c645-130">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="1c645-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1c645-131">Header</span><span class="sxs-lookup"><span data-stu-id="1c645-131">Header</span></span><br/>       | <dl> <span data-ttu-id="1c645-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c645-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




