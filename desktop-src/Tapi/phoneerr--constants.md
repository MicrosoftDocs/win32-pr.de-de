---
description: Dies ist die Liste der Fehlercodes, die die Implementierung zurückgeben kann, wenn Vorgänge auf Telefongeräten aufgerufen werden. Überprüfen Sie anhand der einzelnen Funktionsbeschreibungen, welche dieser Fehlercodes von den einzelnen Funktionen zurückgegeben werden können.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: PHONEERR_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b41ba5d14f4aa12318dd4bc9f2b20e4e9e2e6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370871"
---
# <a name="phoneerr_-constants"></a><span data-ttu-id="0c3ef-104">Phoneerr- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="0c3ef-104">PHONEERR\_ Constants</span></span>

<span data-ttu-id="0c3ef-105">Dies ist die Liste der Fehlercodes, die die Implementierung zurückgeben kann, wenn Vorgänge auf Telefongeräten aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-105">This is the list of error codes that the implementation can return when invoking operations on phone devices.</span></span> <span data-ttu-id="0c3ef-106">Überprüfen Sie anhand der einzelnen Funktionsbeschreibungen, welche dieser Fehlercodes von den einzelnen Funktionen zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-106">Consult the individual function descriptions to determine which of these error codes each function can return.</span></span>

<dl> <dt>

<span data-ttu-id="0c3ef-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**zugewiesene phoneerr \_**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-108">Die angegebene Ressource ist bereits zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-108">The specified resource is already allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**phoneerr \_ badde viceid**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-110">Der angegebene Geräte Bezeichner ist ungültig oder liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-110">The specified device identifier is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**phoneerr \_ getrennt**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-112">Der-Rückruf wurde getrennt.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-112">The call was disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**phoneerr \_ incompatibleapiversion**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-114">Von der Anwendung wurde eine API-Version oder ein Versions Bereich angefordert, die von der telefonieimplementierung oder dem entsprechenden Dienstanbieter nicht unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-114">The application requested an API version or version range that cannot be supported by the Telephony API implementation or the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**phoneerr \_ incompatibleextversion**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-116">Die Anwendung hat eine Erweiterungs Version oder einen Versions Bereich angefordert, der vom Dienstanbieter nicht unterstützt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-116">The application requested an extension version or version range that cannot be supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**phoneerr \_ inifilebeschädigt**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-118">Aufgrund interner Inkonsistenzen oder Formatierungs Probleme in der Telephon.ini-Datei kann Sie von TAPI nicht gelesen und verstanden werden.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-118">Because of internal inconsistencies or formatting problems in the Telephon.ini file, it cannot be read and understood properly by TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**phoneerr- \_ InUse**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-120">Das Gerät wird zurzeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-120">The device is currently in use.</span></span> <span data-ttu-id="0c3ef-121">Das Gerät kann nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-121">The device cannot be configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**phoneerr \_ invalapphandle**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-123">Das angegebene Verwendungs handle oder Registrierungs Handle der Anwendung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-123">The application's specified usage handle or registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**phoneerr \_ invalappname**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-125">Der angegebene Anwendungsname ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-125">The specified application name is invalid.</span></span> <span data-ttu-id="0c3ef-126">Wenn ein Anwendungsname von der Anwendung angegeben wird, wird davon ausgegangen, dass die Zeichenfolge keine nicht anzeigbaren Zeichen enthält und **null**-terminierte Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-126">If an application name is specified by the application, it is assumed that the string does not contain any nondisplayable characters and is **NULL**-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**phoneerr \_ invalbuttonlampid**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR\_INVALBUTTONLAMPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-128">Der angegebene Schaltflächen-/Lamp-Bezeichner liegt außerhalb des gültigen Bereichs oder ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-128">The specified button/lamp identifier is out of range or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**phoneerr- \_ invalbuttonmode**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR\_INVALBUTTONMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-130">Der Parameter für den Schaltflächen Modus ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-130">The button mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**phoneerr \_ invalbuttonstate**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR\_INVALBUTTONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-132">Der Optionsparameter für die Schaltfläche ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-132">The button states parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**phoneerr \_ invaldataid**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR\_INVALDATAID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-134">Der angegebene Daten Bezeichner ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-134">The specified data identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**phoneerr \_ invalentviceclass**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-136">Das angegebene Telefon unterstützt die angegebene Geräteklasse nicht.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-136">The specified phone does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**phoneerr \_ invalextversion**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-138">Die Versionsnummer der Dienstanbieter Erweiterung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-138">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**phoneerr \_ invalhuokswitchdev**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR\_INVALHOOKSWITCHDEV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-140">Der Geräteparameter "huokswitch" ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-140">The hookswitch device parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**phoneerr \_ invalchokswitchmode**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR\_INVALHOOKSWITCHMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-142">Der Parameter "sokswitch Mode" ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-142">The hookswitch mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**phoneerr- \_ invallampmode**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR\_INVALLAMPMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-144">Der angegebene Lamp-Modusparameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-144">The specified lamp mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**phoneerr \_ invalparam**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-146">Ein Parameter, z. b. ein Zeilen-oder Spaltenwert oder ein Fenster Handle, ist ungültig oder liegt außerhalb des gültigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-146">A parameter, such as a row or column value or a window handle, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**phoneerr \_ invalphonehandle**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR\_INVALPHONEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-148">Das angegebene Geräte Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-148">The specified device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**phoneerr \_ invalphonestate**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR\_INVALPHONESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-150">Das Telefongerät befindet sich nicht in einem gültigen Zustand für den angeforderten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-150">The phone device is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**phoneerr- \_ invalpointer**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-152">Mindestens einer der angegebenen Zeiger Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-152">One or more of the specified pointer parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**phoneerr \_ invalprivilege**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR\_INVALPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-154">Der *dwprivilege* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-154">The *dwPrivilege* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**phoneerr- \_ invalringmode**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR\_INVALRINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-156">Der ringmodusparameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-156">The ring mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**phoneerr- \_ nodevice**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-158">Der angegebene Geräte Bezeichner, der zuvor gültig war, wird nicht mehr akzeptiert, weil das zugehörige Gerät seit der letzten Initialisierung von TAPI aus dem System entfernt wurde oder auf eine Weise beschädigt ist, die bei der Initialisierung nicht erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-158">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized or is corrupt in a way that was not detected at initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**phoneerr- \_ nodriver**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-160">Der Telefon Dienstanbieter für das angegebene Gerät hat festgestellt, dass eine der Komponenten fehlt oder beschädigt ist, weil Sie beim Initialisierungs Zeitpunkt nicht erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-160">The telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="0c3ef-161">Der Benutzer sollte aufgefordert werden, das Problem mithilfe der Telefonie-Systemsteuerung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-161">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**phoneerr \_ NOMEM**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-163">Nicht genügend Arbeitsspeicher, um den angeforderten Vorgang abzuschließen, oder es kann kein Arbeitsspeicher belegt oder gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-163">Insufficient memory to complete the requested operation, or unable to allocate or lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**phoneerr- \_ notowner**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-165">Die Anwendung verfügt nicht über die Berechtigung "Besitzer" für das angegebene Telefongerät.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-165">The application does not have owner privilege to the specified phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**phoneerr- \_ operationfailed**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-167">Der Vorgang ist aus einem nicht angegebenen Grund fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-167">The operation failed for an unspecified reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**phoneerr \_ operationunnütz**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-169">Der Vorgang ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-169">The operation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**phoneerr \_ Reit**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-171">Wenn die TAPI-Neuinitialisierung angefordert wurde, z. b. aufgrund des Hinzufügens oder Entfernens eines Telefoniedienstanbieters, anschließend werden [**phoneinitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)-, [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) -oder [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) -Anforderungen mit diesem Fehler zurückgewiesen, bis die letzte Anwendung die Verwendung der API herunterfährt (mithilfe von " [**phoneshutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)"). zu diesem Zeitpunkt wird die neue Konfiguration wirksam, und Anwendungen sind erneut berechtigt, **phoneinitialize** oder **phoneinitializeex** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-171">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) or [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **phoneInitialize** or **phoneInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**phoneerr \_ requestüberlauf**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-173">Die maximal zulässige Anzahl von ausstehenden Telefon Anforderungen wurde überschritten.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-173">The maximum number of outstanding phone requests has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**phoneerr \_ resourceunnütz**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-175">Der Vorgang kann nicht abgeschlossen werden, da eine übermäßige Ressourcen Überschreitung besteht.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-175">The operation cannot be completed because of resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**phoneerr \_ structureum**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-177">Die angegebene Telefon Caps-Struktur ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-177">The specified phone caps structure is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c3ef-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**phoneerr \_ nicht initialisiert**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c3ef-179">Der Vorgang wurde vor einer Anwendung namens [**phoneinitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-179">The operation was invoked before any application called [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c3ef-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c3ef-180">Remarks</span></span>

<span data-ttu-id="0c3ef-181">Die Werte 0xC0000000 bis 0xffffffff sind für gerätespezifische Erweiterungen verfügbar. die Werte 0x80000000 bis 0xBFFFFFFF sind reserviert. und 0x00000000 bis 0x7FFFFFFF werden als Anforderungs Bezeichner verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-181">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions; the values 0x80000000 through 0xBFFFFFFF are reserved; and 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="0c3ef-182">Wenn eine Anwendung eine Fehlermeldung erhält, die Sie nicht speziell behandelt (z. b. einen Fehler, der durch eine gerätespezifische Erweiterung definiert wurde), sollte Sie den Fehler als phoneerr \_ operationfailed (aus einem nicht angegebenen Grund) behandeln.</span><span class="sxs-lookup"><span data-stu-id="0c3ef-182">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a PHONEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c3ef-183">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c3ef-183">Requirements</span></span>



| <span data-ttu-id="0c3ef-184">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c3ef-184">Requirement</span></span> | <span data-ttu-id="0c3ef-185">Wert</span><span class="sxs-lookup"><span data-stu-id="0c3ef-185">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0c3ef-186">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="0c3ef-186">TAPI version</span></span><br/> | <span data-ttu-id="0c3ef-187">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0c3ef-187">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0c3ef-188">Header</span><span class="sxs-lookup"><span data-stu-id="0c3ef-188">Header</span></span><br/>       | <dl> <span data-ttu-id="0c3ef-189"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c3ef-189"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c3ef-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c3ef-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c3ef-191">**phoneinitialize**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-191">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="0c3ef-192">**phoneinitializeex**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-192">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="0c3ef-193">**phoneopen**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-193">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="0c3ef-194">**phoneshutdown**</span><span class="sxs-lookup"><span data-stu-id="0c3ef-194">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




