---
description: Gibt den Offset eines angegebenen Protokolls im Frame zurück.
ms.assetid: bfe5f477-c9de-4bb9-99e5-b8db895b0ae6
title: Getprotocolstarttffset-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ff760c4a61cb39ba897351d706c39d240389bf49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353018"
---
# <a name="getprotocolstartoffset-function"></a><span data-ttu-id="1b935-103">Getprotocolstartffset-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b935-103">GetProtocolStartOffset function</span></span>

<span data-ttu-id="1b935-104">Die **getprotocolstartoffset** -Funktion gibt den Offset eines angegebenen Protokolls im Frame zurück.</span><span class="sxs-lookup"><span data-stu-id="1b935-104">The **GetProtocolStartOffset** function returns the offset of a specified protocol in the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b935-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b935-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffset(
   HFRAME hFrame,
   LPSTR  ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="1b935-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b935-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b935-107">*hframe*</span><span class="sxs-lookup"><span data-stu-id="1b935-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="1b935-108">Ein Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="1b935-108">A handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="1b935-109">*ProtocolName*</span><span class="sxs-lookup"><span data-stu-id="1b935-109">*ProtocolName*</span></span> 
</dt> <dd>

<span data-ttu-id="1b935-110">Der Protokoll Name, z. b. TCP.</span><span class="sxs-lookup"><span data-stu-id="1b935-110">The Protocol name, such as TCP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b935-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b935-111">Return value</span></span>

<span data-ttu-id="1b935-112">Wenn die Funktion erfolgreich ist, handelt es sich bei dem Rückgabewert um einen **DWORD** -Offset bis zum Anfang des gesuchten Protokolls für einen Rückgabewert von NULL gibt an, dass das Protokoll das erste Protokoll im Frame ist.</span><span class="sxs-lookup"><span data-stu-id="1b935-112">If the function is successful, the return value is a **DWORD** offset to the beginning of the protocol being searched for   a return value of zero indicates the protocol is the first protocol in the frame.</span></span>

<span data-ttu-id="1b935-113">Wenn die Funktion nicht erfolgreich ist, befindet sich das Protokoll nicht im Frame, der Rückgabewert ist-1.</span><span class="sxs-lookup"><span data-stu-id="1b935-113">If the function is unsuccessful, the protocol is not in the frame, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b935-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b935-114">Remarks</span></span>

<span data-ttu-id="1b935-115">Wenn das Handle an einen Frame übergeben wird, gibt diese Funktion den Offset an ein angegebenes Protokoll im Frame zurück.</span><span class="sxs-lookup"><span data-stu-id="1b935-115">When given the handle to a frame, this function returns the offset to a specified protocol in the frame.</span></span> <span data-ttu-id="1b935-116">Um z. b. zu ermitteln, ob es sich bei dem Frame um einen DNS-Frame handelt, benötigt der DNS-Parser die Portadresse des TCP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="1b935-116">For example, to determine whether the frame is a DNS frame, the DNS parser requires the port address of the TCP protocol.</span></span> <span data-ttu-id="1b935-117">Der DNS-Parser würde diese Funktion mit TCP als *ProtocolName* -Wert bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="1b935-117">The DNS parser would call this function with TCP as the *ProtocolName* value.</span></span> <span data-ttu-id="1b935-118">Wenn der Frame vom TCP-Protokoll erkannt wird, wird der **Wort** Offset vom Anfang des Frames bis zum Anfang des TCP-Frames zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1b935-118">If the frame is recognized by the TCP protocol, the **WORD** offset from the beginning of the frame to the beginning of the TCP frame is returned.</span></span> <span data-ttu-id="1b935-119">Wenn kein TCP-Protokoll vorhanden ist, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1b935-119">If there is no TCP protocol, the return value is zero.</span></span>

<span data-ttu-id="1b935-120">Diese Funktion findet den Anfang eines Protokolls in einem Frame.</span><span class="sxs-lookup"><span data-stu-id="1b935-120">This function finds the beginning of a protocol in a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b935-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b935-121">Requirements</span></span>



| <span data-ttu-id="1b935-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b935-122">Requirement</span></span> | <span data-ttu-id="1b935-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1b935-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1b935-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b935-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1b935-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b935-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1b935-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b935-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1b935-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b935-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1b935-128">Header</span><span class="sxs-lookup"><span data-stu-id="1b935-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b935-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b935-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1b935-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b935-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b935-131"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b935-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1b935-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1b935-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b935-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b935-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




