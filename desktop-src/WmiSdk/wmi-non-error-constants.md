---
description: WMI-Rückgabecodes, die den Status anzeigen und keinen Fehler angeben.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: WMI-nicht-Fehler Konstanten (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215445"
---
# <a name="wmi-non-error-constants"></a><span data-ttu-id="59c9c-103">WMI-nicht-Fehler-Konstanten</span><span class="sxs-lookup"><span data-stu-id="59c9c-103">WMI Non-Error Constants</span></span>

<span data-ttu-id="59c9c-104">WMI-Rückgabecodes, die den Status anzeigen und keinen Fehler angeben.</span><span class="sxs-lookup"><span data-stu-id="59c9c-104">WMI return codes that indicate status and do not indicate an error.</span></span>

<span data-ttu-id="59c9c-105">Wenn ein Vorgang nicht zu einem Fehler führt, gibt WMI einen der folgenden Codes als **HRESULT** zurück, der den Status des Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="59c9c-105">If an operation does not result in an error, WMI returns one of the following codes as an **HRESULT** that indicates the status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="59c9c-106">Einige Methoden in WMI-Klassen können System-und Netzwerkfehler Codes zurückgeben (z. b. 64).</span><span class="sxs-lookup"><span data-stu-id="59c9c-106">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="59c9c-107">Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den Befehl **net helpmsg** im Eingabe Aufforderungs Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="59c9c-107">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="59c9c-108">Der Befehl **net helpmsg 64** gibt beispielsweise die folgende Meldung zurück: der angegebene Netzwerkname ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59c9c-108">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="59c9c-109">In C++ können Sie [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) und **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** als Nachrichten Modul angeben.</span><span class="sxs-lookup"><span data-stu-id="59c9c-109">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="59c9c-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ S \_ - \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="59c9c-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM\_S\_NO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-111">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="59c9c-111">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-112">Der Vorgang wurde durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="59c9c-112">The operation was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ false**</span><span class="sxs-lookup"><span data-stu-id="59c9c-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM\_S\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-114">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="59c9c-114">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-115">Es sind keine weiteren Objekte verfügbar, die Anzahl der zurückgegebenen Objekte ist kleiner als die angeforderte Anzahl, oder es handelt sich um das Ende einer Enumeration.</span><span class="sxs-lookup"><span data-stu-id="59c9c-115">No more objects are available, the number of objects returned is less than the number requested, or this is the end of an enumeration.</span></span> <span data-ttu-id="59c9c-116">Dieser Wert wird auch zurückgegeben, wenn diese Methode mit dem Wert 0 für den *uCount* -Parameter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="59c9c-116">This value is also returned when this method is called with a value of 0 for the *uCount* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="59c9c-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM\_S\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-118">262145 (0x40001)</span><span class="sxs-lookup"><span data-stu-id="59c9c-118">262145 (0x40001)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-119">Es wurde versucht, ein Objekt oder eine Klasse zu erstellen, die bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="59c9c-119">An attempt was made to create an object or class that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM \_ S \_ \_ auf \_ Standard zurücksetzen**</span><span class="sxs-lookup"><span data-stu-id="59c9c-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM\_S\_RESET\_TO\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-121">262146 (0x40002)</span><span class="sxs-lookup"><span data-stu-id="59c9c-121">262146 (0x40002)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-122">Es wurde eine überschriebene Eigenschaft gelöscht.</span><span class="sxs-lookup"><span data-stu-id="59c9c-122">An overridden property was deleted.</span></span> <span data-ttu-id="59c9c-123">Dieser Wert wird zurückgegeben, um zu signalisieren, dass der ursprüngliche, nicht überschriebene Wert als Ergebnis der Löschung wieder hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="59c9c-123">This value is returned to signal that the original non-overridden value has been restored as a result of the deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ anders**</span><span class="sxs-lookup"><span data-stu-id="59c9c-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM\_S\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-125">262147 (0x40003)</span><span class="sxs-lookup"><span data-stu-id="59c9c-125">262147 (0x40003)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-126">Die Elemente (Objekte, Klassen usw.), die verglichen werden, sind nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="59c9c-126">The items (objects, classes, and so on) that are being compared are not identical.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM \_ S- \_ TimedOut**</span><span class="sxs-lookup"><span data-stu-id="59c9c-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM\_S\_TIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-128">262148 (0x40004)</span><span class="sxs-lookup"><span data-stu-id="59c9c-128">262148 (0x40004)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-129">Timeout bei einem-Timeout. Dies ist keine Fehlerbedingung.</span><span class="sxs-lookup"><span data-stu-id="59c9c-129">A call timed out. This is not an error condition.</span></span> <span data-ttu-id="59c9c-130">Aus diesem Grund wurden möglicherweise auch einige Ergebnisse zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="59c9c-130">Therefore, some results may have also been returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S \_ keine \_ \_ Daten mehr**</span><span class="sxs-lookup"><span data-stu-id="59c9c-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM\_S\_NO\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-132">262149 (0x40005)</span><span class="sxs-lookup"><span data-stu-id="59c9c-132">262149 (0x40005)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-133">Aus der-Enumeration sind keine weiteren Daten verfügbar, und der Benutzer muss die-Enumeration beenden.</span><span class="sxs-lookup"><span data-stu-id="59c9c-133">No more data is available from the enumeration, and the user must terminate the enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM \_ S- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="59c9c-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM\_S\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-135">262150 (0x40006)</span><span class="sxs-lookup"><span data-stu-id="59c9c-135">262150 (0x40006)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-136">Der Vorgang wurde absichtlich oder versehentlich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="59c9c-136">The operation was intentionally or unintentionally canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ Ausstehend**</span><span class="sxs-lookup"><span data-stu-id="59c9c-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM\_S\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-138">262151 (0x40007)</span><span class="sxs-lookup"><span data-stu-id="59c9c-138">262151 (0x40007)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-139">Eine Anforderung wird noch ausgeführt, und die Ergebnisse sind noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="59c9c-139">A request is still in progress, and the results are not yet available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**doppelte WBEM- \_ \_ \_ Objekte**</span><span class="sxs-lookup"><span data-stu-id="59c9c-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM\_S\_DUPLICATE\_OBJECTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-141">262152 (0x40008)</span><span class="sxs-lookup"><span data-stu-id="59c9c-141">262152 (0x40008)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-142">Im Resultset einer Enumeration wurde mehr als eine Kopie desselben Objekts gefunden.</span><span class="sxs-lookup"><span data-stu-id="59c9c-142">More than one copy of the same object was detected in the result set of an enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM \_ S- \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="59c9c-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM\_S\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-144">262153 (0x40009 betragen)</span><span class="sxs-lookup"><span data-stu-id="59c9c-144">262153 (0x40009)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-145">Dem Benutzer wurde der Zugriff auf einige, jedoch nicht auf alle Ressourcen verweigert.</span><span class="sxs-lookup"><span data-stu-id="59c9c-145">The user was denied access to some but not all resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ Teilergebnisse von WBEM S \_**</span><span class="sxs-lookup"><span data-stu-id="59c9c-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**WBEM\_S\_PARTIAL\_RESULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-147">262160 (0x40010)</span><span class="sxs-lookup"><span data-stu-id="59c9c-147">262160 (0x40010)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-148">Der Benutzer hat nicht alle Objekte empfangen, die aufgrund von nicht zugänglichen Ressourcen (außer Sicherheitsverletzungen) angefordert wurden.</span><span class="sxs-lookup"><span data-stu-id="59c9c-148">The user did not receive all of the objects requested due to inaccessible resources (other than security violations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**eingeschränkter WBEM- \_ \_ \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="59c9c-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM\_S\_LIMITED\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-150">274433 (0x43001)</span><span class="sxs-lookup"><span data-stu-id="59c9c-150">274433 (0x43001)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-151">Der Anbieter ist in der Lage, den Dienst zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="59c9c-151">The provider is capable of limited service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="59c9c-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ S \_ indirekt \_ aktualisiert**</span><span class="sxs-lookup"><span data-stu-id="59c9c-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM\_S\_INDIRECTLY\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="59c9c-153">274434 (0x43002)</span><span class="sxs-lookup"><span data-stu-id="59c9c-153">274434 (0x43002)</span></span>
</dt> <dt>



<span data-ttu-id="59c9c-154">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="59c9c-154">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59c9c-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59c9c-155">Requirements</span></span>



| <span data-ttu-id="59c9c-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59c9c-156">Requirement</span></span> | <span data-ttu-id="59c9c-157">Wert</span><span class="sxs-lookup"><span data-stu-id="59c9c-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59c9c-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59c9c-158">Minimum supported client</span></span><br/> | <span data-ttu-id="59c9c-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59c9c-159">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="59c9c-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59c9c-160">Minimum supported server</span></span><br/> | <span data-ttu-id="59c9c-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59c9c-161">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="59c9c-162">Header</span><span class="sxs-lookup"><span data-stu-id="59c9c-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c9c-163"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="59c9c-163"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="59c9c-164">IDL</span><span class="sxs-lookup"><span data-stu-id="59c9c-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59c9c-165"><dt>Wbemcli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="59c9c-165"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59c9c-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59c9c-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c9c-167">WMI-Rückgabe Codes</span><span class="sxs-lookup"><span data-stu-id="59c9c-167">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

