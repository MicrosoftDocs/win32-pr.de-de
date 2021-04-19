---
description: PNRP verwendet die wsanspioctl-Funktion, um Benachrichtigungen zu Änderungen an folgenden Informationen zu erhalten.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP und wsanspioctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349863"
---
# <a name="pnrp-and-wsanspioctl"></a><span data-ttu-id="0ab82-103">PNRP und wsanspioctl</span><span class="sxs-lookup"><span data-stu-id="0ab82-103">PNRP and WSANSPIoctl</span></span>

<span data-ttu-id="0ab82-104">PNRP verwendet die [**wsanspioctl**](winsock-nsp-reference-links.md) -Funktion, um Benachrichtigungen zu Änderungen an folgenden Informationen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="0ab82-104">PNRP uses the [**WSANSPIoctl**](winsock-nsp-reference-links.md) function to receive notifications about changes to the following:</span></span>

-   <span data-ttu-id="0ab82-105">Eine netzwerkcloudliste</span><span class="sxs-lookup"><span data-stu-id="0ab82-105">A network cloud list</span></span>
-   <span data-ttu-id="0ab82-106">Verfügbarkeit der Ergebnisse einer namens Auflösungs Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ab82-106">Availability of results of a name resolution request</span></span>

<span data-ttu-id="0ab82-107">Der erste [**wsalookupservicebegin**](winsock-nsp-reference-links.md) -Befehl definiert den Typ der Informationen, über die ein Client benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="0ab82-107">The first call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) defines the type of information that a client is notified about.</span></span> <span data-ttu-id="0ab82-108">Ein Client kann mit einer Windows-Meldung, einer Abschluss Routine, einem Handle für ein wsaevent-Objekt oder einem Port benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="0ab82-108">A client can be notified with a Windows message, a completion routine, a handle to a WSAEVENT object, or a port.</span></span> <span data-ttu-id="0ab82-109">Weitere Informationen zu Optionen und zum Festlegen des *lpcompletion* -Parameters finden Sie unter **wsanspioctl**.</span><span class="sxs-lookup"><span data-stu-id="0ab82-109">For more information about options and setting the *lpCompletion* parameter, see **WSANSPIoctl**.</span></span>

<span data-ttu-id="0ab82-110">Um nach einem [**WSALookupServiceNext**](winsock-nsp-reference-links.md)-Aufrufvorgang weiterhin Benachrichtigungen zu empfangen, muss eine Anwendung **wsanspioctl** erneut abrufen.</span><span class="sxs-lookup"><span data-stu-id="0ab82-110">To continue receiving notifications after a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md), an application must call **WSANSPIoctl** again.</span></span>

<span data-ttu-id="0ab82-111">Die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion wird blockiert, auch wenn **wsanspioctl** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0ab82-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="0ab82-112">Vor dem Aufrufen von **WSALookupServiceNext** muss eine Anwendung warten, bis Sie eine Benachrichtigung erhält – Wenn die Blockierung ein Problem ist.</span><span class="sxs-lookup"><span data-stu-id="0ab82-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

<span data-ttu-id="0ab82-113">Wenn diese Funktion aufgerufen wird, müssen die Parameter die folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="0ab82-113">When calling this function, the parameters must have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="0ab82-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*HLOOKUP*</span><span class="sxs-lookup"><span data-stu-id="0ab82-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span></span>
</dt> <dd>

<span data-ttu-id="0ab82-115">Gibt das Handle an, das [**wsalookupservicebegin**](winsock-nsp-reference-links.md) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0ab82-115">Specifies the handle that [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) returns.</span></span>

</dd> <dt>

<span data-ttu-id="0ab82-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwcontrolcode*</span><span class="sxs-lookup"><span data-stu-id="0ab82-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span></span>
</dt> <dd>

<span data-ttu-id="0ab82-117">Muss eine **\_ MSP- \_ Benachrichtigungs \_ Änderung** sein.</span><span class="sxs-lookup"><span data-stu-id="0ab82-117">Must be **SIO\_NSP\_NOTIFY\_CHANGE**.</span></span>

</dd> <dt>

<span data-ttu-id="0ab82-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvinbuffer*</span><span class="sxs-lookup"><span data-stu-id="0ab82-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="0ab82-119">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0ab82-119">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ab82-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbinbuffer*</span><span class="sxs-lookup"><span data-stu-id="0ab82-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="0ab82-121">Muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="0ab82-121">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="0ab82-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvoutbuffer*</span><span class="sxs-lookup"><span data-stu-id="0ab82-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="0ab82-123">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0ab82-123">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ab82-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cboutbuffer*</span><span class="sxs-lookup"><span data-stu-id="0ab82-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="0ab82-125">Muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="0ab82-125">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="0ab82-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbbyteszurück gegeben*</span><span class="sxs-lookup"><span data-stu-id="0ab82-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span></span>
</dt> <dd>

<span data-ttu-id="0ab82-127">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0ab82-127">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ab82-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpcompletion*</span><span class="sxs-lookup"><span data-stu-id="0ab82-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span></span>
</dt> <dd>

<span data-ttu-id="0ab82-129">Gibt entweder **null** oder einen Zeiger auf eine [**wsacompletion**](winsock-nsp-reference-links.md) -Struktur an.</span><span class="sxs-lookup"><span data-stu-id="0ab82-129">Specifies either **NULL** or a pointer to a [**WSACOMPLETION**](winsock-nsp-reference-links.md) structure.</span></span>

</dd> </dl>

<span data-ttu-id="0ab82-130">Nachdem eine Benachrichtigung empfangen wurde, rufen Sie [**WSALookupServiceNext**](winsock-nsp-reference-links.md) einmal auf, um die Ergebnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ab82-130">After a notification is received, call [**WSALookupServiceNext**](winsock-nsp-reference-links.md) one time to obtain the results.</span></span>

<span data-ttu-id="0ab82-131">Um eine Suche zu beenden, nennen Sie [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span><span class="sxs-lookup"><span data-stu-id="0ab82-131">To end a search, call [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span></span>

## <a name="resolution-notifications"></a><span data-ttu-id="0ab82-132">Auflösungs Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="0ab82-132">Resolution Notifications</span></span>

<span data-ttu-id="0ab82-133">Ein Client kann jederzeit benachrichtigt werden, wenn ein namens Auflösungs Eintrag hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0ab82-133">A client can be notified any time that a name resolution entry is added.</span></span> <span data-ttu-id="0ab82-134">Der Client ruft dann [**WSALookupServiceNext**](winsock-nsp-reference-links.md) auf, um die Auflösungs Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0ab82-134">The client then calls [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to obtain the resolution data.</span></span>

<span data-ttu-id="0ab82-135">Wenn der Client dieses Verfahren nicht verwendet, kann ein [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Aufrufe blockiert werden, bis das angegebene Timeout eintritt.</span><span class="sxs-lookup"><span data-stu-id="0ab82-135">If the client does not use this technique, a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) can be blocked until the specified timeout occurs.</span></span>

## <a name="cloud-list-notifications"></a><span data-ttu-id="0ab82-136">Benachrichtigungen in der cloudliste</span><span class="sxs-lookup"><span data-stu-id="0ab82-136">Cloud List Notifications</span></span>

<span data-ttu-id="0ab82-137">Ein Client kann jederzeit benachrichtigt werden, wenn eine Gruppe von Clouds geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0ab82-137">A client can be notified any time there is a change to a set of clouds.</span></span>

<span data-ttu-id="0ab82-138">Die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion gibt **WSA \_ E \_ nicht \_ mehr** als festgelegter Trennzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="0ab82-138">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns **WSA\_E\_NO\_MORE** as a set delimiter.</span></span> <span data-ttu-id="0ab82-139">Die Client Anwendung muss vorhandene Clouds aufzählen, bis diese Nachricht zurückgegeben wird, und dann ein Benachrichtigungs Schema verwenden, um nachfolgende Änderungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0ab82-139">The client application must enumerate existing clouds until this message is returned, and then use a notification scheme to retrieve subsequent changes as they occur.</span></span> <span data-ttu-id="0ab82-140">Eine Client Anwendung kann auch **WSALookupServiceNext** anrufen, aber der-Befehl wird blockiert, bis eine Änderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="0ab82-140">A client application can also call **WSALookupServiceNext**, but the call is blocked until a change occurs.</span></span>

<span data-ttu-id="0ab82-141">Die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion gibt eine Cloud in einer **wsaqueryset** -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="0ab82-141">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns a cloud in a **WSAQUERYSET** structure.</span></span> <span data-ttu-id="0ab82-142">Eines der folgenden Flags wird im **dwoutputflags** -Member zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0ab82-142">One of the following flags is returned in the **dwOutputFlags** member.</span></span>



| <span data-ttu-id="0ab82-143">Wert</span><span class="sxs-lookup"><span data-stu-id="0ab82-143">Value</span></span>               | <span data-ttu-id="0ab82-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0ab82-144">Description</span></span>                                             |
|---------------------|---------------------------------------------------------|
| <span data-ttu-id="0ab82-145">Ergebnis \_ wird \_ hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="0ab82-145">RESULT\_IS\_ADDED</span></span>   | <span data-ttu-id="0ab82-146">Die zurückgegebene Cloud wird hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0ab82-146">The cloud that is returned is added.</span></span>                    |
| <span data-ttu-id="0ab82-147">Ergebnis \_ wurde \_ geändert</span><span class="sxs-lookup"><span data-stu-id="0ab82-147">RESULT\_IS\_CHANGED</span></span> | <span data-ttu-id="0ab82-148">Die zurückgegebene Cloud wird geändert.</span><span class="sxs-lookup"><span data-stu-id="0ab82-148">The cloud that is returned is changed.</span></span>                  |
| <span data-ttu-id="0ab82-149">Das Ergebnis \_ ist \_ gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0ab82-149">RESULT\_IS\_DELETED</span></span> | <span data-ttu-id="0ab82-150">Die zurückgegebene Cloud wird gelöscht und ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0ab82-150">The cloud that is returned is deleted and is not valid.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0ab82-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0ab82-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ab82-152">PNRP und wsalookupservicebegin</span><span class="sxs-lookup"><span data-stu-id="0ab82-152">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="0ab82-153">PNRP und WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="0ab82-153">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="0ab82-154">PNRP und wsaqueryset</span><span class="sxs-lookup"><span data-stu-id="0ab82-154">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="0ab82-155">PNRP-NSP-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="0ab82-155">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="0ab82-156">**Wsanspioctl**</span><span class="sxs-lookup"><span data-stu-id="0ab82-156">**WSANSPIoctl**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="0ab82-157">**Wsalookupservicebegin**</span><span class="sxs-lookup"><span data-stu-id="0ab82-157">**WSALookupServiceBegin**</span></span>
</dt> <dt>

<span data-ttu-id="0ab82-158">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="0ab82-158">**WSALookupServiceEnd**</span></span>
</dt> <dt>

<span data-ttu-id="0ab82-159">**Wsaqueryset**</span><span class="sxs-lookup"><span data-stu-id="0ab82-159">**WSAQUERYSET**</span></span>
</dt> </dl>

 

 



