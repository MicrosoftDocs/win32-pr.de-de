---
description: Die "attachproperties"-Exportfunktion ordnet die Eigenschaften einem Speicherort innerhalb einer erkannten Daten zu. Attachproperties müssen für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Attachproperties-Rückruffunktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359020"
---
# <a name="attachproperties-callback-function"></a><span data-ttu-id="a510c-104">Attachproperties-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="a510c-104">AttachProperties callback function</span></span>

<span data-ttu-id="a510c-105">Die " **attachproperties** "-Exportfunktion ordnet die Eigenschaften einem Speicherort innerhalb einer erkannten Daten zu.</span><span class="sxs-lookup"><span data-stu-id="a510c-105">The **AttachProperties** export function maps the properties to a location within a piece of recognized data.</span></span> <span data-ttu-id="a510c-106">**Attachproperties** müssen für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a510c-106">**AttachProperties** must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="a510c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a510c-107">Syntax</span></span>


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="a510c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a510c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a510c-109">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a510c-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a510c-110">Handle des Frames, der analysiert wird.</span><span class="sxs-lookup"><span data-stu-id="a510c-110">Handle of the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="a510c-111">*lpframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a510c-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a510c-112">Zeiger auf das erste Byte in einem Frame.</span><span class="sxs-lookup"><span data-stu-id="a510c-112">Pointer to the first byte in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="a510c-113">*lpprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a510c-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a510c-114">Zeiger auf den Anfang der erkannten Daten.</span><span class="sxs-lookup"><span data-stu-id="a510c-114">Pointer to the start of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="a510c-115">*MacType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a510c-115">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a510c-116">Der Mac-Wert des ersten Protokolls in einem Frame.</span><span class="sxs-lookup"><span data-stu-id="a510c-116">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="a510c-117">*MacType* kann einen der folgenden Typen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="a510c-117">The *MacType* can be one of the following:</span></span>



| <span data-ttu-id="a510c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a510c-118">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="a510c-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a510c-119">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="a510c-120"><dt>**Mac- \_ Typ \_ Ethernet**</dt></span><span class="sxs-lookup"><span data-stu-id="a510c-120"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="a510c-121">802.3</span><span class="sxs-lookup"><span data-stu-id="a510c-121">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="a510c-122"><dt>**Mac- \_ Typ \_ TokenRing**</dt></span><span class="sxs-lookup"><span data-stu-id="a510c-122"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="a510c-123">802.5</span><span class="sxs-lookup"><span data-stu-id="a510c-123">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="a510c-124"><dt>**Mac- \_ Typ " \_ f"**</dt></span><span class="sxs-lookup"><span data-stu-id="a510c-124"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="a510c-125">ANSI x3t 9,5</span><span class="sxs-lookup"><span data-stu-id="a510c-125">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="a510c-126">*Bytesleft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a510c-126">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a510c-127">Die verbleibende Anzahl von Bytes in einem Frame, beginnend am Anfang der erkannten Daten.</span><span class="sxs-lookup"><span data-stu-id="a510c-127">The remaining number of bytes in a frame   starting at the beginning of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="a510c-128">*hpreviousproycol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a510c-128">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a510c-129">Handle des vorherigen Protokolls.</span><span class="sxs-lookup"><span data-stu-id="a510c-129">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="a510c-130">*npreviousprotocoloffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a510c-130">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a510c-131">Der Offset des vorherigen Protokolls ab dem Anfang des Frames.</span><span class="sxs-lookup"><span data-stu-id="a510c-131">Offset of the previous protocol   starting at the beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="a510c-132">*lpinstdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a510c-132">*lpInstData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a510c-133">Zeiger auf die Instanzdaten, die das vorherige Protokoll bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a510c-133">Pointer to the instance data that the previous protocol provides.</span></span> <span data-ttu-id="a510c-134">Instanzdaten dürfen nicht länger sein als eine Länge von DWORD \_ ptr.</span><span class="sxs-lookup"><span data-stu-id="a510c-134">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a510c-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a510c-135">Return value</span></span>

<span data-ttu-id="a510c-136">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf das erste Byte nach den erkannten Daten in einem Frame oder **null** , wenn es sich bei den erkannten Daten um das letzte Datenelement in einem Frame handelt.</span><span class="sxs-lookup"><span data-stu-id="a510c-136">If the function is successful, the return value is a pointer to the first byte after the recognized data in a frame or **NULL** if the recognized data is the last piece of data in a frame.</span></span>

<span data-ttu-id="a510c-137">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein Zeiger auf die erkannten Daten.</span><span class="sxs-lookup"><span data-stu-id="a510c-137">If the function is unsuccessful, the return value is a pointer to the recognized data.</span></span> <span data-ttu-id="a510c-138">Der *lpprotocol* -Parameter übergibt den Zeiger an die Parser-DLL.</span><span class="sxs-lookup"><span data-stu-id="a510c-138">The *lpProtocol* parameter passes the pointer to the parser DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a510c-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a510c-139">Remarks</span></span>

<span data-ttu-id="a510c-140">Netzwerkmonitor Ruft die **attachproperties** -Funktion für jeden Parser auf, der ein Datenelement in einem Frame erkennt.</span><span class="sxs-lookup"><span data-stu-id="a510c-140">Network Monitor calls the **AttachProperties** function for each parser that recognizes a piece of data in a frame.</span></span> <span data-ttu-id="a510c-141">Beachten Sie, dass der Parser bestimmt, welche Eigenschaften in den erkannten Daten vorhanden sind und wo sich die einzelnen Eigenschaften befinden.</span><span class="sxs-lookup"><span data-stu-id="a510c-141">Note that the parser determines which properties exist in the recognized data, and where each property is located.</span></span>

<span data-ttu-id="a510c-142">Bei der Implementierung von **attachproperties** wird [attachpropertyinstance](attachpropertyinstance.md) aufgerufen, um die Daten zu verwenden, wie Sie in der Erfassung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a510c-142">During the implementation of **AttachProperties**, call [AttachPropertyInstance](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="a510c-143">Sie können auch die [attachpropertyinstanceex](attachpropertyinstanceex.md) -Funktion aufrufen, um die Eigenschaften Daten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a510c-143">You can also call [AttachPropertyInstanceEx](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="a510c-144">Es wird jedoch empfohlen, dass Sie die Daten verwenden, wie Sie in der Erfassung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a510c-144">However, it is advised that you use the data as it exists in the capture.</span></span>

<span data-ttu-id="a510c-145">Die Funktionen " **attachpropertyinstanceex** " und " **attachpropertyinstance** " werden nur für die Eigenschaften aufgerufen, die in den erkannten Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a510c-145">The **AttachPropertyInstanceEx** and **AttachPropertyInstance** functions are called only for the properties that exist in the recognized data.</span></span> <span data-ttu-id="a510c-146">Beachten Sie, dass Netzwerkmonitor über eine Eigenschaften [*Datenbank*](p.md) für den Parser verfügt, der eine Beschreibung aller Eigenschaften enthält, die der Parser unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a510c-146">Note that Network Monitor has a [*property database*](p.md) for the parser that contains a description of all the properties that the parser supports.</span></span>

<span data-ttu-id="a510c-147">**Instanzdaten**</span><span class="sxs-lookup"><span data-stu-id="a510c-147">**Instance data**</span></span>

<span data-ttu-id="a510c-148">Instanzdaten sind Informationen, die von einem Parser an einen anderen übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a510c-148">Instance data is information that is passed from one parser to another.</span></span> <span data-ttu-id="a510c-149">Instanzdaten können beliebige Daten sein, die kleiner oder gleich einem DWORD- \_ ptr sind, oder ein Zeiger auf Daten, wie z. b. unformatierte Frame-Daten, die nicht vom Parser zugeordnet oder freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a510c-149">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span> <span data-ttu-id="a510c-150">Im *lpinstdata* -Parameter der **Eigenschaften attachproperties** und [erkennzeframe](recognizeframe.md) stellt Netzwerkmonitor einen Zeiger auf die Instanzdaten des vorherigen Protokolls bereit.</span><span class="sxs-lookup"><span data-stu-id="a510c-150">In the *lpInstData* parameter of the **AttachProperties** and [RecognizeFrame](recognizeframe.md) functions, Network Monitor provides a pointer to the instance data of the previous protocol.</span></span> <span data-ttu-id="a510c-151">Sie können die Instanzdaten für den Parser während der Implementierung von " **erkenzeframe**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="a510c-151">You can set the instance data for your parser during your implementation of **RecognizeFrame**.</span></span>



| <span data-ttu-id="a510c-152">Für Informationen zu</span><span class="sxs-lookup"><span data-stu-id="a510c-152">For information on</span></span>                                          | <span data-ttu-id="a510c-153">Siehe</span><span class="sxs-lookup"><span data-stu-id="a510c-153">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a510c-154">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="a510c-154">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="a510c-155">Parser</span><span class="sxs-lookup"><span data-stu-id="a510c-155">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="a510c-156">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a510c-156">What entry points are included in the parser DLL.</span></span>           | [<span data-ttu-id="a510c-157">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="a510c-157">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="a510c-158">Erkennen von Daten.</span><span class="sxs-lookup"><span data-stu-id="a510c-158">How to recognize data.</span></span>                                      | [<span data-ttu-id="a510c-159">Implementieren von "erkenzeframe"</span><span class="sxs-lookup"><span data-stu-id="a510c-159">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)     |
| <span data-ttu-id="a510c-160">So erstellen Sie eine Eigenschaften Datenbank</span><span class="sxs-lookup"><span data-stu-id="a510c-160">How to create a property database.</span></span>                          | [<span data-ttu-id="a510c-161">Implementieren von Register</span><span class="sxs-lookup"><span data-stu-id="a510c-161">Implementing Register</span></span>](implementing-register.md)                 |
| <span data-ttu-id="a510c-162">Zum Implementieren von **attachproperties**  gehört ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="a510c-162">How to implement **AttachProperties**  includes an example.</span></span> | [<span data-ttu-id="a510c-163">Implementieren von attachproperties</span><span class="sxs-lookup"><span data-stu-id="a510c-163">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="a510c-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a510c-164">Requirements</span></span>



| <span data-ttu-id="a510c-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a510c-165">Requirement</span></span> | <span data-ttu-id="a510c-166">Wert</span><span class="sxs-lookup"><span data-stu-id="a510c-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a510c-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a510c-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a510c-168">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a510c-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a510c-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a510c-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a510c-170">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a510c-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a510c-171">Header</span><span class="sxs-lookup"><span data-stu-id="a510c-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="a510c-172"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a510c-172"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a510c-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a510c-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a510c-174">Attachpropertyinstance</span><span class="sxs-lookup"><span data-stu-id="a510c-174">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="a510c-175">Attachpropertyinstanceex</span><span class="sxs-lookup"><span data-stu-id="a510c-175">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="a510c-176">Erkenzeframe</span><span class="sxs-lookup"><span data-stu-id="a510c-176">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




