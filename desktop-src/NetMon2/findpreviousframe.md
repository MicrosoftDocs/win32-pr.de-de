---
description: Die findpreviousframe-Funktion findet den vorherigen Frame im aktuellen Aufzeichnungs Kontext, der mit dem Filter übereinstimmt.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Findpreviousframe-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958725"
---
# <a name="findpreviousframe-function"></a><span data-ttu-id="9beef-103">Findpreviousframe-Funktion</span><span class="sxs-lookup"><span data-stu-id="9beef-103">FindPreviousFrame function</span></span>

<span data-ttu-id="9beef-104">Die **findpreviousframe** -Funktion findet den vorherigen Frame im aktuellen Aufzeichnungs Kontext, der mit dem Filter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9beef-104">The **FindPreviousFrame** function finds the previous frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9beef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9beef-105">Syntax</span></span>


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="9beef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9beef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9beef-107">*hcurrentframe*</span><span class="sxs-lookup"><span data-stu-id="9beef-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="9beef-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="9beef-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="9beef-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="9beef-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="9beef-110">Der Protokoll Name, z. b. TCP.</span><span class="sxs-lookup"><span data-stu-id="9beef-110">Protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="9beef-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="9beef-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="9beef-112">Die Zieladresse des Frame-, der gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="9beef-112">Destination address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="9beef-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="9beef-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="9beef-114">Die Quelladresse des Frame-, der gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="9beef-114">Source address of the frame that is searched for.</span></span>

</dd> <dt>

<span data-ttu-id="9beef-115">*Protocoloffset*</span><span class="sxs-lookup"><span data-stu-id="9beef-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="9beef-116">Zeiger auf ein **Wort** , das den Protokoll Offset empfängt.</span><span class="sxs-lookup"><span data-stu-id="9beef-116">Pointer to a **WORD** that receives the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="9beef-117">*Originalframenum*</span><span class="sxs-lookup"><span data-stu-id="9beef-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="9beef-118">Startpunkt der Suche.</span><span class="sxs-lookup"><span data-stu-id="9beef-118">Starting point of the search.</span></span> <span data-ttu-id="9beef-119">Standardmäßig durchsucht diese Funktion nach dem Startpunkt " *originalframenum* " rückwärts 1.000 Frames.</span><span class="sxs-lookup"><span data-stu-id="9beef-119">By default, this function searches backward 1,000 frames from *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="9beef-120">Sie können den suchbackweg ändern, indem Sie diese Zeile der Nmapi.ini-Datei hinzufügen, die sich im \\ Netzwerkmonitor Verzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="9beef-120">You can change the search-back distance by adding this line to the Nmapi.ini file, which is located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="9beef-121">Maxlookback =<new lookback distance></span><span class="sxs-lookup"><span data-stu-id="9beef-121">MAXLOOKBACK=<new lookback distance></span></span>

</dd> <dt>

<span data-ttu-id="9beef-122">*Lowestframe*</span><span class="sxs-lookup"><span data-stu-id="9beef-122">*LowestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="9beef-123">Niedrigste Frame Nummer in der Erfassung, die durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="9beef-123">Lowest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9beef-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9beef-124">Return value</span></span>

<span data-ttu-id="9beef-125">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für den vorherigen Frame.</span><span class="sxs-lookup"><span data-stu-id="9beef-125">If the function is successful, the return value is a handle to the previous frame.</span></span>

<span data-ttu-id="9beef-126">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="9beef-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9beef-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9beef-127">Remarks</span></span>

<span data-ttu-id="9beef-128">Der Erfassungs Filter wird primär durch *ProtocolName* definiert. Dies ist die einzige erforderliche Filter Eingabe. Sie können *DestinationAddress* -und *SourceAddress* -Informationen hinzufügen, um die Erfassungs Geschwindigkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="9beef-128">The capture filter is defined primarily by *ProtocolName*, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* information to increase the capture speed.</span></span>

<span data-ttu-id="9beef-129">*Protocoloffset* wird an den aufrufenden Parser zurückgegeben, der dieses **DWORD** dem Zeiger hinzufügt, der durch Sperren des Frames (mit [parsertemporarylockframe](parsertemporarylockframe.md)) zurückgegeben wird, um das LPBYTE des gesuchten Protokolls abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9beef-129">*ProtocolOffset* is returned to the calling parser, which adds this **DWORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the LPBYTE of the protocol that is being searched for.</span></span> <span data-ttu-id="9beef-130">Bei der Rückgabe wird dem Parser der hframe, der den Filter übergeben hat, übergeben.</span><span class="sxs-lookup"><span data-stu-id="9beef-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="9beef-131">Wenn der Parser feststellt, dass es sich bei dem Frame nicht um den gesuchten Frame handelt, kann der Parser diesen hframe zurück an die **findpreviousframe** -Funktion übergeben, um den nächsten Frame abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9beef-131">If the parser finds that the frame is not the one that is being sought, the parser can hand this HFRAME back to the **FindPreviousFrame** function to retrieve the next frame.</span></span> <span data-ttu-id="9beef-132">Die Quell-und Zieladressen, die nicht erforderlich sind, können als **null**-Werte angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9beef-132">The source and destination addresses, which are not required, can be passed in as **NULL**.</span></span> <span data-ttu-id="9beef-133">Wenn diese Adressen verwendet werden, können Sie den Typ Address \_ Type \_ IP usw., nicht nur Mac-Typen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9beef-133">When used, these addresses can be of type ADDRESS\_TYPE\_IP, and so on, not just MAC types.</span></span>

## <a name="requirements"></a><span data-ttu-id="9beef-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9beef-134">Requirements</span></span>



| <span data-ttu-id="9beef-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9beef-135">Requirement</span></span> | <span data-ttu-id="9beef-136">Wert</span><span class="sxs-lookup"><span data-stu-id="9beef-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9beef-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9beef-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9beef-138">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9beef-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9beef-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9beef-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9beef-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9beef-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9beef-141">Header</span><span class="sxs-lookup"><span data-stu-id="9beef-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9beef-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9beef-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9beef-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9beef-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="9beef-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9beef-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9beef-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9beef-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9beef-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9beef-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




