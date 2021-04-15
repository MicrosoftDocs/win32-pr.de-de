---
description: Sucht den nächsten Frame im aktuellen Erfassungs Kontext, der mit dem Filter übereinstimmt.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Findnextframe-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525151"
---
# <a name="findnextframe-function"></a><span data-ttu-id="0e91b-103">Findnextframe-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e91b-103">FindNextFrame function</span></span>

<span data-ttu-id="0e91b-104">Die **findnextframe** -Funktion findet den nächsten Frame im aktuellen Aufzeichnungs Kontext, der mit dem Filter übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0e91b-104">The **FindNextFrame** function finds the next frame in the current capture context that matches the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e91b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e91b-105">Syntax</span></span>


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a><span data-ttu-id="0e91b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e91b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e91b-107">*hcurrentframe*</span><span class="sxs-lookup"><span data-stu-id="0e91b-107">*hCurrentFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="0e91b-108">Ein Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="0e91b-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="0e91b-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="0e91b-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="0e91b-110">Der Protokoll Name, z. b. TCP.</span><span class="sxs-lookup"><span data-stu-id="0e91b-110">The protocol name, such as TCP.</span></span>

</dd> <dt>

<span data-ttu-id="0e91b-111">*DestinationAddress*</span><span class="sxs-lookup"><span data-stu-id="0e91b-111">*DestinationAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="0e91b-112">Die Zieladresse.</span><span class="sxs-lookup"><span data-stu-id="0e91b-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="0e91b-113">*SourceAddress*</span><span class="sxs-lookup"><span data-stu-id="0e91b-113">*SourceAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="0e91b-114">Die Quelladresse.</span><span class="sxs-lookup"><span data-stu-id="0e91b-114">The source address.</span></span>

</dd> <dt>

<span data-ttu-id="0e91b-115">*Protocoloffset*</span><span class="sxs-lookup"><span data-stu-id="0e91b-115">*ProtocolOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="0e91b-116">Ein Zeiger auf ein **Wort** , das den Protokoll Offset empfängt.</span><span class="sxs-lookup"><span data-stu-id="0e91b-116">A pointer to a **WORD** that will receive the protocol offset.</span></span>

</dd> <dt>

<span data-ttu-id="0e91b-117">*Originalframenum*</span><span class="sxs-lookup"><span data-stu-id="0e91b-117">*OriginalFrameNumber*</span></span> 
</dt> <dd>

<span data-ttu-id="0e91b-118">Der Ausgangspunkt der Suche.</span><span class="sxs-lookup"><span data-stu-id="0e91b-118">The starting point of the search.</span></span> <span data-ttu-id="0e91b-119">Diese Funktion durchsucht standardmäßig 1.000 Frames vom Ausgangspunkt *originalframenum* .</span><span class="sxs-lookup"><span data-stu-id="0e91b-119">By default, this function searches forward 1,000 frames from the *OriginalFrameNumber* starting point.</span></span> <span data-ttu-id="0e91b-120">Fügen Sie die folgende Zeile zur Nmapi.ini Datei hinzu, die sich im Netzwerkmonitor Verzeichnis befindet, um die Suche nach vorn zu ändern \\ .</span><span class="sxs-lookup"><span data-stu-id="0e91b-120">To change the search-forward distance, add this line to the Nmapi.ini file, located in the \\Network Monitor directory.</span></span>

<span data-ttu-id="0e91b-121">Maxlookback =<new lookforward distance></span><span class="sxs-lookup"><span data-stu-id="0e91b-121">MAXLOOKBACK=<new lookforward distance></span></span>

</dd> <dt>

<span data-ttu-id="0e91b-122">*Highestframe*</span><span class="sxs-lookup"><span data-stu-id="0e91b-122">*HighestFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="0e91b-123">Die höchste Frame Nummer in der Erfassung, die durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="0e91b-123">The highest frame number in the capture that is searched.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e91b-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e91b-124">Return value</span></span>

<span data-ttu-id="0e91b-125">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Handle für den nächsten Frame.</span><span class="sxs-lookup"><span data-stu-id="0e91b-125">If the function is successful, the return value is a handle to the next frame.</span></span>

<span data-ttu-id="0e91b-126">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="0e91b-126">If the function is not successful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e91b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e91b-127">Remarks</span></span>

<span data-ttu-id="0e91b-128">Der Erfassungs Filter wird primär durch den *ProtocolName* -Parameter definiert, der die einzige erforderliche Filter Eingabe ist. Sie können *DestinationAddress* -und *SourceAddress* -Daten hinzufügen, um die Erfassungs Geschwindigkeit zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="0e91b-128">The capture filter is defined primarily by the *ProtocolName* parameter, which is the only required filter input; you can add *DestinationAddress* and *SourceAddress* data to increase the capture speed.</span></span>

<span data-ttu-id="0e91b-129">Der *protocoloffset* -Zeiger wird an den aufrufenden Parser zurückgegeben, der das **Wort** dem Zeiger hinzufügt, der durch Sperren des Frames (mit [parsertemporarylockframe](parsertemporarylockframe.md)) zurückgegeben wird, um das **LPBYTE** des gesuchten Protokolls abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0e91b-129">The *ProtocolOffset* pointer is returned to the calling parser, which adds the **WORD** to the pointer returned by locking the frame (with [ParserTemporaryLockFrame](parsertemporarylockframe.md)) to get the **LPBYTE** of the protocol searched for.</span></span> <span data-ttu-id="0e91b-130">Bei der Rückgabe wird dem Parser der hframe, der den Filter übergeben hat, übergeben.</span><span class="sxs-lookup"><span data-stu-id="0e91b-130">On return, the HFRAME that passed the filter is given to the parser.</span></span> <span data-ttu-id="0e91b-131">Wenn der Parser feststellt, dass es sich bei diesem Frame nicht um den gesuchten Frame handelt, kann der Parser den hframe zurück an die **findnextframe** -Funktion übergeben, um den nächsten Frame zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0e91b-131">If the parser finds that this frame is not the one sought, the parser can hand the HFRAME back to the **FindNextFrame** function to get the next frame.</span></span> <span data-ttu-id="0e91b-132">Die Quell-und Zieladressen sind nicht erforderlich und können als **null**-Werte übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="0e91b-132">The source and destination addresses are not required and can be passed as **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e91b-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e91b-133">Requirements</span></span>



| <span data-ttu-id="0e91b-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e91b-134">Requirement</span></span> | <span data-ttu-id="0e91b-135">Wert</span><span class="sxs-lookup"><span data-stu-id="0e91b-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0e91b-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e91b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0e91b-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e91b-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0e91b-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e91b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0e91b-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e91b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0e91b-140">Header</span><span class="sxs-lookup"><span data-stu-id="0e91b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e91b-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e91b-141"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0e91b-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e91b-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="0e91b-143"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e91b-143"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0e91b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0e91b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e91b-145"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e91b-145"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




