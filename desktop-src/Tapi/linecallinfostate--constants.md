---
description: Die bitflagkonstanten von linecallinfostate \_ beschreiben verschiedene Aufruf Informationselemente, über die eine Anwendung in der Zeile CallInfo-Nachricht benachrichtigt werden kann \_ .
ms.assetid: c216d9b7-8e2f-4604-ba93-1d9e1a5d23fc
title: LINECALLINFOSTATE_ Konstanten (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f560cfd6ba65929a9f6cf5c9aa6cd8bc2f48b24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364441"
---
# <a name="linecallinfostate_-constants"></a><span data-ttu-id="99c2d-103">Linecallinfostate- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="99c2d-103">LINECALLINFOSTATE\_ Constants</span></span>

<span data-ttu-id="99c2d-104">Die bitflagkonstanten von **linecallinfostate \_** beschreiben verschiedene Aufruf Informationselemente, über die eine Anwendung in der [**Zeile \_ CallInfo**](line-callinfo.md) -Nachricht benachrichtigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="99c2d-104">The **LINECALLINFOSTATE\_** bit-flag constants describe various call information items about which an application can be notified in the [**LINE\_CALLINFO**](line-callinfo.md) message.</span></span>

<dl> <dt>

<span data-ttu-id="99c2d-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**linecallinfostate \_ AppSpecific**</span><span class="sxs-lookup"><span data-stu-id="99c2d-105"><span id="LINECALLINFOSTATE_APPSPECIFIC"></span><span id="linecallinfostate_appspecific"></span>**LINECALLINFOSTATE\_APPSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-106">Das anwendungsspezifische Feld des aufrufsinformationen-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="99c2d-106">The application-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**linecallinfostate \_ bearermode**</span><span class="sxs-lookup"><span data-stu-id="99c2d-107"><span id="LINECALLINFOSTATE_BEARERMODE"></span><span id="linecallinfostate_bearermode"></span>**LINECALLINFOSTATE\_BEARERMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-108">Das bearermodusfeld des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-108">The bearer mode field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**linecallinfostate \_ calldata**</span><span class="sxs-lookup"><span data-stu-id="99c2d-109"><span id="LINECALLINFOSTATE_CALLDATA"></span><span id="linecallinfostate_calldata"></span>**LINECALLINFOSTATE\_CALLDATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-110">Der **calldata** -Member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="99c2d-110">The **CallData** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**linecallinfostate \_ calledid**</span><span class="sxs-lookup"><span data-stu-id="99c2d-111"><span id="LINECALLINFOSTATE_CALLEDID"></span><span id="linecallinfostate_calledid"></span>**LINECALLINFOSTATE\_CALLEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-112">Eines der calledid-bezogenen Felder des aufrufsinformationen-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="99c2d-112">One of the calledID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**linecallinfostate \_ CallerID**</span><span class="sxs-lookup"><span data-stu-id="99c2d-113"><span id="LINECALLINFOSTATE_CALLERID"></span><span id="linecallinfostate_callerid"></span>**LINECALLINFOSTATE\_CALLERID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-114">Eines der CallerID-bezogenen Felder des Aufruf Informationsdaten Satzes.</span><span class="sxs-lookup"><span data-stu-id="99c2d-114">One of the callerID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**linecallinfostate- \_ kallid**</span><span class="sxs-lookup"><span data-stu-id="99c2d-115"><span id="LINECALLINFOSTATE_CALLID"></span><span id="linecallinfostate_callid"></span>**LINECALLINFOSTATE\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-116">Das Feld für die aufrufskennung des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-116">The call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**linecallinfostate \_ charginginfo**</span><span class="sxs-lookup"><span data-stu-id="99c2d-117"><span id="LINECALLINFOSTATE_CHARGINGINFO"></span><span id="linecallinfostate_charginginfo"></span>**LINECALLINFOSTATE\_CHARGINGINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-118">Die Abrechnungsinformationen des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-118">The charging information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**completionid für linecallinfostate \_**</span><span class="sxs-lookup"><span data-stu-id="99c2d-119"><span id="LINECALLINFOSTATE_COMPLETIONID"></span><span id="linecallinfostate_completionid"></span>**LINECALLINFOSTATE\_COMPLETIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-120">Das Feld für den Abschluss Bezeichner des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-120">The completion identifier field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**linecallinfostate \_ connectedid**</span><span class="sxs-lookup"><span data-stu-id="99c2d-121"><span id="LINECALLINFOSTATE_CONNECTEDID"></span><span id="linecallinfostate_connectedid"></span>**LINECALLINFOSTATE\_CONNECTEDID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-122">Eines der connectordid-bezogenen Felder des aufrufsinformationen-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="99c2d-122">One of the connectedID-related fields of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**linecallinfostate \_ DevSpecific**</span><span class="sxs-lookup"><span data-stu-id="99c2d-123"><span id="LINECALLINFOSTATE_DEVSPECIFIC"></span><span id="linecallinfostate_devspecific"></span>**LINECALLINFOSTATE\_DEVSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-124">Das gerätespezifische Feld des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-124">The device-specific field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**linecallinfostate- \_ dialparser**</span><span class="sxs-lookup"><span data-stu-id="99c2d-125"><span id="LINECALLINFOSTATE_DIALPARAMS"></span><span id="linecallinfostate_dialparams"></span>**LINECALLINFOSTATE\_DIALPARAMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-126">Die Wählparameter des aufrufsinformationen-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="99c2d-126">The dial parameters of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**linecallinfostate- \_ Anzeige**</span><span class="sxs-lookup"><span data-stu-id="99c2d-127"><span id="LINECALLINFOSTATE_DISPLAY"></span><span id="linecallinfostate_display"></span>**LINECALLINFOSTATE\_DISPLAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-128">Das Anzeige Feld des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-128">The display field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**linecallinfostate \_ highlevelcomp**</span><span class="sxs-lookup"><span data-stu-id="99c2d-129"><span id="LINECALLINFOSTATE_HIGHLEVELCOMP"></span><span id="linecallinfostate_highlevelcomp"></span>**LINECALLINFOSTATE\_HIGHLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-130">Das allgemeine Kompatibilitäts Feld des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-130">The high level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**linecallinfostate \_ lowlevelcomp**</span><span class="sxs-lookup"><span data-stu-id="99c2d-131"><span id="LINECALLINFOSTATE_LOWLEVELCOMP"></span><span id="linecallinfostate_lowlevelcomp"></span>**LINECALLINFOSTATE\_LOWLEVELCOMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-132">Das Kompatibilitäts Feld auf niedriger Ebene des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-132">The low level compatibility field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**linecallinfostate \_ mediamode**</span><span class="sxs-lookup"><span data-stu-id="99c2d-133"><span id="LINECALLINFOSTATE_MEDIAMODE"></span><span id="linecallinfostate_mediamode"></span>**LINECALLINFOSTATE\_MEDIAMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-134">Das Feld Medientyp des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-134">The media type field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**linecallinfostate- \_ Monitormodi**</span><span class="sxs-lookup"><span data-stu-id="99c2d-135"><span id="LINECALLINFOSTATE_MONITORMODES"></span><span id="linecallinfostate_monitormodes"></span>**LINECALLINFOSTATE\_MONITORMODES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-136">Mindestens eines der Ziffern-, Ton-oder Medien Überwachungs Felder im aufrufsinformationen-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="99c2d-136">One or more of the digit, tone, or media monitoring fields in the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**linecallinfostate- \_ nummonitors**</span><span class="sxs-lookup"><span data-stu-id="99c2d-137"><span id="LINECALLINFOSTATE_NUMMONITORS"></span><span id="linecallinfostate_nummonitors"></span>**LINECALLINFOSTATE\_NUMMONITORS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-138">Das Feld Anzahl von Monitoren im Datensatz "Callcenter" hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="99c2d-138">The number of monitors field in the call-information record has changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**linecallinfostate \_ numuwnerdecr**</span><span class="sxs-lookup"><span data-stu-id="99c2d-139"><span id="LINECALLINFOSTATE_NUMOWNERDECR"></span><span id="linecallinfostate_numownerdecr"></span>**LINECALLINFOSTATE\_NUMOWNERDECR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-140">Die Anzahl der Besitzer Felder im Datensatz "Callcenter" wurde gesenkt.</span><span class="sxs-lookup"><span data-stu-id="99c2d-140">The number of owner field in the call-information record was decreased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**linecallinfostate \_ numuwnerincr**</span><span class="sxs-lookup"><span data-stu-id="99c2d-141"><span id="LINECALLINFOSTATE_NUMOWNERINCR"></span><span id="linecallinfostate_numownerincr"></span>**LINECALLINFOSTATE\_NUMOWNERINCR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-142">Die Anzahl der Besitzer Felder im Datensatz "Callcenter" wurde angehoben.</span><span class="sxs-lookup"><span data-stu-id="99c2d-142">The number of owner field in the call-information record was increased.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**linecallinfostate- \_ Ursprung**</span><span class="sxs-lookup"><span data-stu-id="99c2d-143"><span id="LINECALLINFOSTATE_ORIGIN"></span><span id="linecallinfostate_origin"></span>**LINECALLINFOSTATE\_ORIGIN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-144">Das Ursprungs Feld des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-144">The origin field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**anderer linecallinfostate \_**</span><span class="sxs-lookup"><span data-stu-id="99c2d-145"><span id="LINECALLINFOSTATE_OTHER"></span><span id="linecallinfostate_other"></span>**LINECALLINFOSTATE\_OTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-146">Andere als die unten aufgeführten aufrufungsinformationselemente haben sich geändert.</span><span class="sxs-lookup"><span data-stu-id="99c2d-146">Call information items other than those listed below have changed.</span></span> <span data-ttu-id="99c2d-147">Die Anwendung sollte die aktuellen aufrufsinformationen überprüfen, um zu bestimmen, welche Elemente geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="99c2d-147">The application should check the current call information to determine which items have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**linecallinfostate \_ QoS**</span><span class="sxs-lookup"><span data-stu-id="99c2d-148"><span id="LINECALLINFOSTATE_QOS"></span><span id="linecallinfostate_qos"></span>**LINECALLINFOSTATE\_QOS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-149">Mindestens eines der **QoS** -Member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="99c2d-149">One or more of the **QOS** members in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**linecallinfostate- \_ Rate**</span><span class="sxs-lookup"><span data-stu-id="99c2d-150"><span id="LINECALLINFOSTATE_RATE"></span><span id="linecallinfostate_rate"></span>**LINECALLINFOSTATE\_RATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-151">Das Raten Feld des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-151">The rate field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**linecallinfostate- \_ Grund**</span><span class="sxs-lookup"><span data-stu-id="99c2d-152"><span id="LINECALLINFOSTATE_REASON"></span><span id="linecallinfostate_reason"></span>**LINECALLINFOSTATE\_REASON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-153">Das Feld "Grund" des Datensatzes "Callcenter".</span><span class="sxs-lookup"><span data-stu-id="99c2d-153">The reason field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**linecallinfostate \_ redirectingid**</span><span class="sxs-lookup"><span data-stu-id="99c2d-154"><span id="LINECALLINFOSTATE_REDIRECTINGID"></span><span id="linecallinfostate_redirectingid"></span>**LINECALLINFOSTATE\_REDIRECTINGID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-155">Der Adress Bezeichner des Speicher Orts, der einen-Befehl umgeleitet hat.</span><span class="sxs-lookup"><span data-stu-id="99c2d-155">The address identifier of the location that redirected a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**linecallinfostate \_ redirectionid**</span><span class="sxs-lookup"><span data-stu-id="99c2d-156"><span id="LINECALLINFOSTATE_REDIRECTIONID"></span><span id="linecallinfostate_redirectionid"></span>**LINECALLINFOSTATE\_REDIRECTIONID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-157">Der Adress Bezeichner des Speicher Orts, an den ein-Rückruf umgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="99c2d-157">The address identifier of the location to which a call has been redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**linecallinfostate \_ relatedcallid**</span><span class="sxs-lookup"><span data-stu-id="99c2d-158"><span id="LINECALLINFOSTATE_RELATEDCALLID"></span><span id="linecallinfostate_relatedcallid"></span>**LINECALLINFOSTATE\_RELATEDCALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-159">Das zugehörige aufrufungsbezeichnerfeld des aufrufsinformationen-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="99c2d-159">The related call ID field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**linecallinfostate- \_ Terminal**</span><span class="sxs-lookup"><span data-stu-id="99c2d-160"><span id="LINECALLINFOSTATE_TERMINAL"></span><span id="linecallinfostate_terminal"></span>**LINECALLINFOSTATE\_TERMINAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-161">Die terminalmodusinformationen des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-161">The terminal mode information of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**linecallinfostate- \_ Behandlung**</span><span class="sxs-lookup"><span data-stu-id="99c2d-162"><span id="LINECALLINFOSTATE_TREATMENT"></span><span id="linecallinfostate_treatment"></span>**LINECALLINFOSTATE\_TREATMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-163">Der **calltreatment** -Member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) wurde aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="99c2d-163">The **CallTreatment** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) has been updated.</span></span> <span data-ttu-id="99c2d-164">Dies kann als Reaktion auf eine [**linesetcalltreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) -Funktion, eine Aufruf Zustandsänderung, einen Aufruf "Vector" oder ein anderes Skript, das den Aufruf steuert, oder nach Abschluss der Wiedergabe einer aufgezeichneten Nachricht auftreten (normalerweise eine Änderung an "Stille" oder "Musik").</span><span class="sxs-lookup"><span data-stu-id="99c2d-164">This can occur in response to a [**lineSetCallTreatment**](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment) function, a call state change, a call "vector" or other script controlling the call, or upon completion of playback of a recorded message (ordinarily, indicating a change to "silence" or "music").</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**linecallinfostate- \_ trunk**</span><span class="sxs-lookup"><span data-stu-id="99c2d-165"><span id="LINECALLINFOSTATE_TRUNK"></span><span id="linecallinfostate_trunk"></span>**LINECALLINFOSTATE\_TRUNK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-166">Das trunk Feld des aufrufsinformationen-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="99c2d-166">The trunk field of the call-information record.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="99c2d-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**linecallinfostate \_ useruserinfo**</span><span class="sxs-lookup"><span data-stu-id="99c2d-167"><span id="LINECALLINFOSTATE_USERUSERINFO"></span><span id="linecallinfostate_useruserinfo"></span>**LINECALLINFOSTATE\_USERUSERINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="99c2d-168">Die Benutzer Benutzerinformationen des Datensatzes zum Abrufen von Informationen.</span><span class="sxs-lookup"><span data-stu-id="99c2d-168">The user-user information of the call-information record.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99c2d-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99c2d-169">Remarks</span></span>

<span data-ttu-id="99c2d-170">Keine Erweiterbarkeit.</span><span class="sxs-lookup"><span data-stu-id="99c2d-170">No extensibility.</span></span> <span data-ttu-id="99c2d-171">Alle 32 Bits sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="99c2d-171">All 32 bits are reserved.</span></span>

<span data-ttu-id="99c2d-172">Wenn in dieser Datenstruktur Änderungen auftreten, wird eine [**Zeile \_ CallInfo**](line-callinfo.md) -Meldung an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="99c2d-172">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="99c2d-173">Die Parameter für diese Nachricht sind ein Handle für den-Befehl und ein Hinweis auf das geänderte Informationselement.</span><span class="sxs-lookup"><span data-stu-id="99c2d-173">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="99c2d-174">Die Datenstruktur [**lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) gibt auch an, welche dieser Aufruf Informationselemente für jeden Aufruf der Adresse gültig sind.</span><span class="sxs-lookup"><span data-stu-id="99c2d-174">The [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) data structure also indicates which of these call information elements are valid for every call on the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="99c2d-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99c2d-175">Requirements</span></span>



| <span data-ttu-id="99c2d-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99c2d-176">Requirement</span></span> | <span data-ttu-id="99c2d-177">Wert</span><span class="sxs-lookup"><span data-stu-id="99c2d-177">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="99c2d-178">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="99c2d-178">TAPI version</span></span><br/> | <span data-ttu-id="99c2d-179">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="99c2d-179">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="99c2d-180">Header</span><span class="sxs-lookup"><span data-stu-id="99c2d-180">Header</span></span><br/>       | <dl> <span data-ttu-id="99c2d-181"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="99c2d-181"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99c2d-182">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99c2d-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c2d-183">**\_liniencallinfo**</span><span class="sxs-lookup"><span data-stu-id="99c2d-183">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="99c2d-184">**Lineaddresscaps**</span><span class="sxs-lookup"><span data-stu-id="99c2d-184">**LINEADDRESSCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[<span data-ttu-id="99c2d-185">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="99c2d-185">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="99c2d-186">**linesetcalltreatment**</span><span class="sxs-lookup"><span data-stu-id="99c2d-186">**lineSetCallTreatment**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetcalltreatment)
</dt> </dl>

 

 




