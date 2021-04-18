---
description: Die Funktion "erkenzeframe Export" gibt an, ob ein Datenelement als das vom Parser erkannte Protokoll erkannt wird. Die Funktion "erkenzeframe Export" muss für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Erkenzeframe-Rückruffunktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351585"
---
# <a name="recognizeframe-callback-function"></a><span data-ttu-id="f6c8d-104">Erkenzeframe-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="f6c8d-104">RecognizeFrame callback function</span></span>

<span data-ttu-id="f6c8d-105">Die Funktion " **erkenzeframe** Export" gibt an, ob ein Datenelement als das vom Parser erkannte Protokoll erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-105">The **RecognizeFrame** export function indicates whether a piece of data is recognized as the protocol that the parser detects.</span></span> <span data-ttu-id="f6c8d-106">Die Funktion " **erkenzeframe** Export" muss für jeden Parser implementiert werden, der von der Parser-DLL unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-106">The **RecognizeFrame** export function must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c8d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6c8d-107">Syntax</span></span>


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="f6c8d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6c8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6c8d-109">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-110">Handle für den Frame, der die Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-110">Handle to the frame that contains the data.</span></span>

</dd> <dt>

<span data-ttu-id="f6c8d-111">*lpframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-112">Zeiger auf das erste Byte eines Frames.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-112">Pointer to the first byte of a frame.</span></span> <span data-ttu-id="f6c8d-113">Der-Zeiger bietet eine Möglichkeit, Daten anzuzeigen, die von anderen-Parser erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-113">The pointer provides a way to view data that other parsers recognize.</span></span>

</dd> <dt>

<span data-ttu-id="f6c8d-114">*lpprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-114">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-115">Zeiger auf den Anfang der nicht beanspruchten Daten.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-115">Pointer to the start of the unclaimed data.</span></span> <span data-ttu-id="f6c8d-116">In der Regel befinden sich die nicht beanspruchten Daten in der Mitte eines Frames, da ein vorheriger Parser Daten vor diesem Parser beansprucht hat.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-116">Typically, the unclaimed data is located in the middle of a frame because a previous parser has claimed data before this parser.</span></span> <span data-ttu-id="f6c8d-117">Der Parser muss zuerst die nicht beanspruchten Daten testen.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-117">The parser must test the unclaimed data first.</span></span>

</dd> <dt>

<span data-ttu-id="f6c8d-118">*MacType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-118">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-119">Der Mac-Wert des ersten Protokolls in einem Frame.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-119">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="f6c8d-120">In der Regel wird der *MacType* -Wert verwendet, wenn der Parser das erste Protokoll in einem Frame identifizieren muss.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-120">Typically, the *MacType* value is used when the parser must identify the first protocol in a frame.</span></span> <span data-ttu-id="f6c8d-121">Der *MacType* -Wert kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="f6c8d-121">The *MacType* value can be one of the following:</span></span>



| <span data-ttu-id="f6c8d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f6c8d-122">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="f6c8d-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f6c8d-123">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="f6c8d-124"><dt>**Mac- \_ Typ \_ Ethernet**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c8d-124"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="f6c8d-125">802.3</span><span class="sxs-lookup"><span data-stu-id="f6c8d-125">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="f6c8d-126"><dt>**Mac- \_ Typ \_ TokenRing**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c8d-126"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="f6c8d-127">802.5</span><span class="sxs-lookup"><span data-stu-id="f6c8d-127">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="f6c8d-128"><dt>**Mac- \_ Typ " \_ f"**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c8d-128"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="f6c8d-129">ANSI x3t 9,5</span><span class="sxs-lookup"><span data-stu-id="f6c8d-129">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="f6c8d-130">*Bytesleft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-130">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-131">Die verbleibende Anzahl von Bytes von einer Position in einem Frame bis zum Ende des Frames.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-131">The remaining number of bytes from a location in a frame to the end of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="f6c8d-132">*hpreviousproycol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-132">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-133">Handle des vorherigen Protokolls.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-133">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="f6c8d-134">*npreviousprotocoloffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-134">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-135">Offset des vorherigen Protokolls beginnend mit dem Frame.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-135">Offset of the previous protocol   beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="f6c8d-136">*Protocolstatus Code* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-136">*ProtocolStatusCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-137">Protokoll Status Indikator.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-137">Protocol status indicator.</span></span> <span data-ttu-id="f6c8d-138">Die Parser-DLL muss einen der folgenden Statuscodes festlegen.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-138">The parser DLL must set one of the following status codes.</span></span>



| <span data-ttu-id="f6c8d-139">Wert</span><span class="sxs-lookup"><span data-stu-id="f6c8d-139">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="f6c8d-140">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f6c8d-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <span data-ttu-id="f6c8d-141"><dt>**Protokoll \_ Status \_ erkannt**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c8d-141"><dt>**PROTOCOL\_STATUS\_RECOGNIZED**</dt></span></span> </dl>              | <span data-ttu-id="f6c8d-142">Der Parser erkennt die Daten, weiß aber nicht, welches Protokoll befolgt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-142">The parser recognizes the data but does not know which protocol follows.</span></span> <span data-ttu-id="f6c8d-143">Nachdem Sie den Code festgelegt haben, geben Sie einen Zeiger auf die verbleibenden nicht beanspruchten Daten zurück, die dem erkannten Protokoll folgen.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-143">After setting the code, return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="f6c8d-144">Netzwerkmonitor verwendet den [*folgenden Protokoll Satz*](f.md) , um die Verarbeitung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-144">Network Monitor uses the [*follow set*](f.md) of the protocol to continue parsing.</span></span> <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <span data-ttu-id="f6c8d-145"><dt>**der Protokoll \_ Status wurde \_ nicht \_ erkannt.**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c8d-145"><dt>**PROTOCOL\_STATUS\_NOT\_RECOGNIZED**</dt></span></span> </dl> | <span data-ttu-id="f6c8d-146">Der Parser erkennt die Daten nicht.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-146">The parser does not recognize the data.</span></span> <span data-ttu-id="f6c8d-147">Nachdem Sie diesen Code festgelegt haben, geben Sie den Zeiger auf den Anfang der Daten zurück, indem Sie den Zeiger verwenden, den der *lpprotocol* -Parameter an die Parser-DLL übergibt.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-147">After setting this code, return the pointer to the beginning of the data   using the pointer that the *lpProtocol* parameter passes to the parser DLL.</span></span> <span data-ttu-id="f6c8d-148">Netzwerkmonitor verwendet den *folgenden Satz* des vorherigen Protokolls, um die Verarbeitung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-148">Network Monitor uses the *follow set* of the previous protocol to continue parsing.</span></span> <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <span data-ttu-id="f6c8d-149"><dt>**Protokoll \_ Status \_ beansprucht**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c8d-149"><dt>**PROTOCOL\_STATUS\_CLAIMED**</dt></span></span> </dl>                       | <span data-ttu-id="f6c8d-150">Der Parser erkennt die Daten und beansprucht die verbleibenden Daten.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-150">The parser recognizes the data and claims the remaining data.</span></span> <span data-ttu-id="f6c8d-151">Nachdem Sie den Code festgelegt haben, geben Sie **null** zurück, damit Netzwerkmonitor die Verarbeitung eines Frames beenden kann.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-151">After setting the code, return **NULL** for Network Monitor to terminate parsing a frame.</span></span> <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <span data-ttu-id="f6c8d-152"><dt>**Protokoll \_ Status \_ nächstes \_ Protokoll**</dt></span><span class="sxs-lookup"><span data-stu-id="f6c8d-152"><dt>**PROTOCOL\_STATUS\_NEXT\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="f6c8d-153">Der Parser erkennt die Daten und weiß, welches Protokoll befolgt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-153">The parser recognizes the data and knows which protocol follows.</span></span> <span data-ttu-id="f6c8d-154">Nachdem Sie den Code festgelegt haben, legen Sie den Parameter *phnextprotocol* fest, und geben Sie einen Zeiger auf die verbleibenden nicht beanspruchten Daten zurück, die dem erkannten Protokoll folgen.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-154">After setting the code, set the *phNextProtocol* parameter, and return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="f6c8d-155">Netzwerkmonitor die Verarbeitung des Frames fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-155">Network Monitor continues parsing the frame.</span></span> <br/>                               |



 

</dd> <dt>

<span data-ttu-id="f6c8d-156">*phnextprotocol* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-156">*phNextProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-157">Zeiger auf das Handle des nächsten Protokolls.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-157">Pointer to the handle of the next protocol.</span></span> <span data-ttu-id="f6c8d-158">Dieser Parameter wird festgelegt, wenn ein Protokoll das Protokoll identifiziert, das einem Protokoll folgt.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-158">This parameter is set when a protocol identifies the protocol that follows a protocol.</span></span> <span data-ttu-id="f6c8d-159">Um das Handle des nächsten Protokolls zu erhalten, rufen Sie die [getprotocolfromtable](getprotocolfromtable.md) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-159">To obtain the handle of the next protocol, call the [GetProtocolFromTable](getprotocolfromtable.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f6c8d-160">*lpinstdata* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-160">*lpInstData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6c8d-161">Bei Eingabe ein Zeiger auf die Instanzdaten aus dem vorherigen Protokoll.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-161">On input, a pointer to the instance data from the previous protocol.</span></span>

<span data-ttu-id="f6c8d-162">Bei der Ausgabe ein Zeiger auf die Instanzdaten für das aktuelle Protokoll.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-162">On output, a pointer to the instance data for the current protocol.</span></span> <span data-ttu-id="f6c8d-163">Instanzdaten dürfen nicht länger sein als eine Länge von DWORD \_ ptr.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-163">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6c8d-164">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6c8d-164">Return value</span></span>

<span data-ttu-id="f6c8d-165">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf das erste Byte nach den erkannten Parserdaten.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-165">If the function is successful, the return value is a pointer to the first byte after the recognized parser data.</span></span> <span data-ttu-id="f6c8d-166">Wenn der Parser alle verbleibenden Daten beansprucht, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-166">If the parser claims all the remaining data, the return value is **NULL**.</span></span>

<span data-ttu-id="f6c8d-167">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein anfänglicher Zeiger, den der *lpprotocol* -Parameter übergibt.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-167">If the function is unsuccessful, the return value is an initial pointer that the *lpProtocol* parameter passes-in.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6c8d-168">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6c8d-168">Remarks</span></span>

<span data-ttu-id="f6c8d-169">Die Funktion " **erkenzeframe** " bestimmt, ob der Parser die Rohdaten erkennt, beginnend beim *lpprotocol* -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-169">The **RecognizeFrame** function determines whether the parser recognizes the raw data   starting at the *lpProtocol* pointer.</span></span>

-   <span data-ttu-id="f6c8d-170">Wenn das Protokoll die Daten erkennt, gibt die Funktion " **erkenzeframe** " einen Zeiger auf die restlichen Daten zurück oder gibt **null** zurück, wenn das aktuelle Protokoll das letzte Protokoll in einem Frame ist.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-170">If the protocol recognizes the data, the **RecognizeFrame** function returns a pointer to the remaining data, or returns **NULL** if the current protocol is the last protocol in a frame.</span></span>
-   <span data-ttu-id="f6c8d-171">Wenn das Protokoll die Daten nicht erkennt, gibt die Funktion " **erkennzeframe** " den Zeiger zurück, der an die Parser-DLL im *lpprotocol* -Parameter übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-171">If the protocol does not recognize the data, the **RecognizeFrame** function returns the pointer passed to the parser DLL in the *lpProtocol* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="f6c8d-172">" *Erkenzeframe* " kann aufgerufen werden, bevor die [*Register*](register-parser.md) -Funktion aufgerufen wird, um die Protokoll Eigenschaften zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-172">*RecognizeFrame* can be called before the [*Register*](register-parser.md) function is called to register the protocol properties.</span></span> <span data-ttu-id="f6c8d-173">Aus diesem Grund ist die Implementierung der Funktion " *erkennzeframe* " nicht auf Eigenschaften oder Strukturen angewiesen, die während der Implementierung der Protokoll **Registrierungs** Funktion erstellt oder initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-173">For that reason, the implementation of the *RecognizeFrame* function does not rely on any properties or structures that are created or initialized during the implementation of the protocol **Register** function.</span></span>

 

<span data-ttu-id="f6c8d-174">**Handoff festgelegtes und Resultset**</span><span class="sxs-lookup"><span data-stu-id="f6c8d-174">**Handoff Set and Follow Set**</span></span>

<span data-ttu-id="f6c8d-175">Ein Parser kann einen Handzettel Satz oder einen nachfolgenden Satz verwenden, um zu ermitteln, ob das Protokoll auf erkannte Daten folgt Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-175">A parser can use a handoff set or follow set to identify for Network Monitor the protocol that follows recognized data.</span></span>

-   <span data-ttu-id="f6c8d-176">Wenn Informationen in erkannten Daten verfügbar sind, verwendet der Parser seine handsemenge, um ein Handle für das nächste Protokoll abzurufen, und übergibt dieses Handle dann an Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-176">If information is available in recognized data, the parser uses its handoff set to obtain a handle to the next protocol, and then passes that handle to Network Monitor.</span></span>
-   <span data-ttu-id="f6c8d-177">Wenn keine Informationen verfügbar sind, übergibt der Parser kein Handle, und Netzwerkmonitor verwendet die parserfolgenmenge, um zu bestimmen, welches Protokoll befolgt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-177">If information is not available, the parser does not pass a handle, and Network Monitor uses the parser follow set to determine which protocol follows.</span></span>

<span data-ttu-id="f6c8d-178">**Übergeben von Informationen zwischen Protokollen**</span><span class="sxs-lookup"><span data-stu-id="f6c8d-178">**Passing information between protocols**</span></span>

<span data-ttu-id="f6c8d-179">Verwenden Sie den *lpinstdata* -Parameter, um Informationen zwischen Protokollen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-179">Use the *lpInstData* parameter to pass information between protocols.</span></span> <span data-ttu-id="f6c8d-180">Bei der Eingabe können Sie die Informationen aus dem vorherigen Protokoll abrufen.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-180">On input, you can retrieve the information from the previous protocol.</span></span> <span data-ttu-id="f6c8d-181">Bei der Ausgabe können Sie Informationen an das nächste Protokoll übergeben.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-181">On output, you can pass information to the next protocol.</span></span>

<span data-ttu-id="f6c8d-182">Instanzdaten können beliebige Daten sein, die kleiner oder gleich einem DWORD- \_ ptr sind, oder ein Zeiger auf Daten, wie z. b. unformatierte Frame-Daten, die nicht vom Parser zugeordnet oder freigegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-182">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>



| <span data-ttu-id="f6c8d-183">Informationen zu</span><span class="sxs-lookup"><span data-stu-id="f6c8d-183">For Information on</span></span>                                        | <span data-ttu-id="f6c8d-184">Siehe</span><span class="sxs-lookup"><span data-stu-id="f6c8d-184">See</span></span>                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c8d-185">Welche Parser sind und wie Sie mit Netzwerkmonitor funktionieren.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-185">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="f6c8d-186">Parser</span><span class="sxs-lookup"><span data-stu-id="f6c8d-186">Parsers</span></span>](parsers.md)                                                                                                    |
| <span data-ttu-id="f6c8d-187">Welche Einstiegspunkte in der Parser-DLL enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-187">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="f6c8d-188">Architektur der Parser-DLL</span><span class="sxs-lookup"><span data-stu-id="f6c8d-188">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                                                                    |
| <span data-ttu-id="f6c8d-189">Zum Implementieren von " **erkenzeframe**  " gehört ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-189">How to implement **RecognizeFrame**  includes an example.</span></span> | [<span data-ttu-id="f6c8d-190">Implementieren von "erkenzeframe"</span><span class="sxs-lookup"><span data-stu-id="f6c8d-190">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)                                                            |
| <span data-ttu-id="f6c8d-191">Gibt an, wie ein Übergabe festgelegt und der Satz befolgt wird.</span><span class="sxs-lookup"><span data-stu-id="f6c8d-191">How to specify a handoff set and follow set.</span></span>              | <span data-ttu-id="f6c8d-192">[Angeben eines handsesets](specifying-a-handoff-set.md)mit[Angabe eines folgenden](specifying-a-follow-set.md) Satzes</span><span class="sxs-lookup"><span data-stu-id="f6c8d-192">[Specifying a Handoff Set](specifying-a-handoff-set.md)[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f6c8d-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6c8d-193">Requirements</span></span>



| <span data-ttu-id="f6c8d-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6c8d-194">Requirement</span></span> | <span data-ttu-id="f6c8d-195">Wert</span><span class="sxs-lookup"><span data-stu-id="f6c8d-195">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c8d-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6c8d-196">Minimum supported client</span></span><br/> | <span data-ttu-id="f6c8d-197">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f6c8d-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6c8d-198">Minimum supported server</span></span><br/> | <span data-ttu-id="f6c8d-199">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6c8d-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f6c8d-200">Header</span><span class="sxs-lookup"><span data-stu-id="f6c8d-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6c8d-201"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6c8d-201"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6c8d-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6c8d-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6c8d-203">Getprotocolfromtable</span><span class="sxs-lookup"><span data-stu-id="f6c8d-203">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> </dl>

 

 




