---
title: WINBIO_OPERATION_TYPE Konstanten (winbio \_ types. h)
description: Geben Sie den Typ des asynchronen Vorgangs an, der ausgeführt wird.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106496"
---
# <a name="winbio_operation_type-constants"></a><span data-ttu-id="1bc3c-103">Winbio \_ - \_ Vorgangstyp Konstanten</span><span class="sxs-lookup"><span data-stu-id="1bc3c-103">WINBIO\_OPERATION\_TYPE Constants</span></span>

<span data-ttu-id="1bc3c-104">Die folgenden Konstanten können von der Windows-Biometrieframework in einem asynchronen [**winbio- \_ \_ Ergebnis**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) zurückgegeben werden, um den Typ des asynchronen Vorgangs anzugeben, der ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-104">The following constants can be returned by the Windows Biometric Framework in a [**WINBIO\_ASYNC\_RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) to specify the type of asynchronous operation being performed.</span></span>

<dl> <dt>

<span data-ttu-id="1bc3c-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**winbio- \_ Vorgang " \_ None"**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**WINBIO\_OPERATION\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-106">0</span><span class="sxs-lookup"><span data-stu-id="1bc3c-106">0</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-107">Es wurde kein Vorgang identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-107">No operation has been identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**winbio- \_ Vorgang \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO\_OPERATION\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-109">1</span><span class="sxs-lookup"><span data-stu-id="1bc3c-109">1</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-110">Eine biometrische Sitzung wurde geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-110">A biometric session was opened.</span></span> <span data-ttu-id="1bc3c-111">Weitere Informationen finden Sie unter [**winbioasyncopensession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-111">For more information see [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**winbio- \_ Vorgang \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO\_OPERATION\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-113">2</span><span class="sxs-lookup"><span data-stu-id="1bc3c-113">2</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-114">Eine biometrische Sitzung wurde geschlossen.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-114">A biometric session was closed.</span></span> <span data-ttu-id="1bc3c-115">Weitere Informationen finden Sie unter [**winbioclosesession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-115">For more information, see [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**Überprüfung des winbio- \_ Vorgangs \_**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO\_OPERATION\_VERIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-117">3</span><span class="sxs-lookup"><span data-stu-id="1bc3c-117">3</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-118">Ein biometrisches Beispiel wurde anhand einer Benutzeridentität überprüft.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-118">A biometric sample was verified against a user identity.</span></span> <span data-ttu-id="1bc3c-119">Weitere Informationen finden Sie unter [**winbioverify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-119">For more information, see [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**winbio- \_ Vorgang \_ identifizieren**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO\_OPERATION\_IDENTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-121">4</span><span class="sxs-lookup"><span data-stu-id="1bc3c-121">4</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-122">Ein biometrisches Beispiel wurde aufgezeichnet und mit einer vorhandenen Vorlage verglichen.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-122">A biometric sample was captured and compared to an existing template.</span></span> <span data-ttu-id="1bc3c-123">Weitere Informationen finden Sie unter [**winbioidentifi.**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)</span><span class="sxs-lookup"><span data-stu-id="1bc3c-123">For more information, see [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**winbio- \_ Vorgang zum \_ Suchen des \_ Sensors**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO\_OPERATION\_LOCATE\_SENSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-125">5</span><span class="sxs-lookup"><span data-stu-id="1bc3c-125">5</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-126">Die ID-Nummer einer biometrischen Einheit wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-126">The ID number of a biometric unit was retrieved.</span></span> <span data-ttu-id="1bc3c-127">Weitere Informationen finden Sie unter [**winbiolosinesensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-127">For more information, see [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**Beginn der winbio- \_ Operation beim \_ registrieren \_**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO\_OPERATION\_ENROLL\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-129">6</span><span class="sxs-lookup"><span data-stu-id="1bc3c-129">6</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-130">Eine biometrische Registrierungs Sequenz wurde initiiert.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-130">A biometric enrollment sequence was initiated.</span></span> <span data-ttu-id="1bc3c-131">Weitere Informationen finden Sie unter [**winbioeinschreibung**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-131">For more information, see [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**Erfassung von winbio- \_ Operation \_ registrieren \_**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO\_OPERATION\_ENROLL\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-133">7</span><span class="sxs-lookup"><span data-stu-id="1bc3c-133">7</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-134">Ein biometrisches Beispiel wurde aufgezeichnet und der Vorlage hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-134">A biometric sample was captured and added to the template.</span></span> <span data-ttu-id="1bc3c-135">Weitere Informationen finden Sie unter [**winbioregistricapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-135">For more information, see [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**winbio- \_ Vorgangs Registrierungs \_ \_ Commit**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO\_OPERATION\_ENROLL\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-137">8</span><span class="sxs-lookup"><span data-stu-id="1bc3c-137">8</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-138">Eine ausstehende biometrische Vorlage wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-138">A pending biometric template was finalized.</span></span> <span data-ttu-id="1bc3c-139">Weitere Informationen finden Sie unter [**winbioregistricommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-139">For more information, see [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**die Registrierung des winbio- \_ Vorgangs wird \_ \_ verworfen.**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**WINBIO\_OPERATION\_ENROLL\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-141">9</span><span class="sxs-lookup"><span data-stu-id="1bc3c-141">9</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-142">Eine ausstehende biometrische Vorlage wurde verworfen.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-142">A pending biometric template was discarded.</span></span> <span data-ttu-id="1bc3c-143">Weitere Informationen finden Sie unter [**winbioregistrierungs verwerfen**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-143">For more information, see [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**winbio-Operation-Aufzählungs \_ \_ \_ Registrierungen**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**WINBIO\_OPERATION\_ENUM\_ENROLLMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-145">10</span><span class="sxs-lookup"><span data-stu-id="1bc3c-145">10</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-146">Die unter Faktoren für eine bestimmte Vorlage wurden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-146">The sub-factors for a given template were enumerated.</span></span> <span data-ttu-id="1bc3c-147">Weitere Informationen finden Sie unter [**winbioenumregistrierungen**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-147">For more information, see [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**Vorlage zum Löschen des winbio- \_ Vorgangs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO\_OPERATION\_DELETE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-149">11</span><span class="sxs-lookup"><span data-stu-id="1bc3c-149">11</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-150">Eine biometrische Vorlage wurde aus dem Speicher gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-150">A biometric template was deleted from the store.</span></span> <span data-ttu-id="1bc3c-151">Weitere Informationen finden Sie unter [**winbiodeletetemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-151">For more information, see [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**Beispiel für winbio- \_ Vorgangs \_ Erfassung \_**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**WINBIO\_OPERATION\_CAPTURE\_SAMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-153">12</span><span class="sxs-lookup"><span data-stu-id="1bc3c-153">12</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-154">Ein biometrisches Beispiel wurde aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-154">A biometric sample was captured.</span></span> <span data-ttu-id="1bc3c-155">Weitere Informationen finden Sie unter [**winbiocapturesample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-155">For more information, see [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**winbio- \_ Operation \_ get- \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO\_OPERATION\_GET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-157">13</span><span class="sxs-lookup"><span data-stu-id="1bc3c-157">13</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-158">Eine biometrische Sitzung, eine Einheit oder eine Vorlagen Eigenschaft wurde abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-158">A biometric session, unit, or template property was retrieved.</span></span> <span data-ttu-id="1bc3c-159">Weitere Informationen finden Sie unter [**winbiogetproperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-159">For more information, see [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**winbio \_ Operation \_ Set ( \_ Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO\_OPERATION\_SET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-161">14</span><span class="sxs-lookup"><span data-stu-id="1bc3c-161">14</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-162">Es wurde eine biometrische Sitzung, eine Einheit, eine Vorlage oder eine Konto Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-162">A biometric session, unit, template, or account property was set.</span></span> <span data-ttu-id="1bc3c-163">Weitere Informationen finden Sie unter [**winbiosetproperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-163">For more information, see [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**winbio- \_ Operation \_ get- \_ Ereignis**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO\_OPERATION\_GET\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-165">15</span><span class="sxs-lookup"><span data-stu-id="1bc3c-165">15</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-166">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-166">Not used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**winbio- \_ Vorgangs \_ Sperr \_ Einheit**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO\_OPERATION\_LOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-168">16</span><span class="sxs-lookup"><span data-stu-id="1bc3c-168">16</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-169">Eine biometrische Einheit wurde für eine ausschließliche Verwendung durch eine Sitzung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-169">A biometric unit was locked for exclusive use by a session.</span></span> <span data-ttu-id="1bc3c-170">Weitere Informationen finden Sie unter [**winbiolockunit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-170">For more information, see [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**winbio- \_ Vorgang zum \_ Entsperren der \_ Einheit**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO\_OPERATION\_UNLOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-172">17</span><span class="sxs-lookup"><span data-stu-id="1bc3c-172">17</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-173">Die Sitzungs Sperre für eine biometrische Einheit wurde freigegeben.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-173">The session lock on a biometric unit was released.</span></span> <span data-ttu-id="1bc3c-174">Weitere Informationen finden Sie unter [**winbiounlockunit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-174">For more information, see [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**winbio- \_ Vorgangs \_ Steuerungs \_ Einheit**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-176">18</span><span class="sxs-lookup"><span data-stu-id="1bc3c-176">18</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-177">Hersteller definierte Vorgänge wurden für eine Steuereinheit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-177">Vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="1bc3c-178">Weitere Informationen finden Sie unter [**winbiocontrolunit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-178">For more information, see [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**privilegierter winbio- \_ Vorgangs \_ Steuerungs \_ Einheit \_**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-180">19</span><span class="sxs-lookup"><span data-stu-id="1bc3c-180">19</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-181">Privilegierte Hersteller definierte Vorgänge wurden für eine Steuerungseinheit durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-181">Privileged vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="1bc3c-182">Weitere Informationen finden Sie unter [**winbiocontrolunitprivilegiert**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-182">For more information, see [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**winbio \_ Operation \_ Open \_ Framework**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO\_OPERATION\_OPEN\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-184">20</span><span class="sxs-lookup"><span data-stu-id="1bc3c-184">20</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-185">Ein Handle für das biometrische Framework wurde geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-185">A handle to the biometric framework was opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**winbio- \_ Vorgang \_ Schließen- \_ Framework**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO\_OPERATION\_CLOSE\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-187">21</span><span class="sxs-lookup"><span data-stu-id="1bc3c-187">21</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-188">Ein Handle für das biometrische Framework wurde geschlossen.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-188">A handle to the biometric framework was closed.</span></span> <span data-ttu-id="1bc3c-189">Weitere Informationen finden Sie unter [**winbiocloseframework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-189">For more information, see [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**winbio \_ Operation \_ Enum- \_ Dienst \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**WINBIO\_OPERATION\_ENUM\_SERVICE\_PROVIDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-191">22</span><span class="sxs-lookup"><span data-stu-id="1bc3c-191">22</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-192">Die installierten biometrischen Dienstanbieter wurden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-192">The installed biometric service providers were enumerated.</span></span> <span data-ttu-id="1bc3c-193">Weitere Informationen finden Sie unter [**winbioenumserviceproviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-193">For more information, see [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ biometrische \_ Einheiten für winbio-Operation-Aufzählung**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO\_OPERATION\_ENUM\_BIOMETRIC\_UNITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-195">23</span><span class="sxs-lookup"><span data-stu-id="1bc3c-195">23</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-196">Die angefügten biometrischen Einheiten wurden aufgezählt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-196">The attached biometric units were enumerated.</span></span> <span data-ttu-id="1bc3c-197">Weitere Informationen finden Sie unter [**winbioasyncengbiometricunits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-197">For more information, see [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**winbio-Operation-Aufzählungs \_ \_ \_ Datenbanken**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**WINBIO\_OPERATION\_ENUM\_DATABASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-199">24</span><span class="sxs-lookup"><span data-stu-id="1bc3c-199">24</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-200">Die registrierten Datenbanken wurden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-200">The registered databases were enumerated.</span></span> <span data-ttu-id="1bc3c-201">Weitere Informationen finden Sie unter [**winbioenumdatenbanken**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-201">For more information, see [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**winbio- \_ Vorgangs \_ Einheiten \_ Ankunft**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO\_OPERATION\_UNIT\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-203">25</span><span class="sxs-lookup"><span data-stu-id="1bc3c-203">25</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-204">Es wurde eine biometrische Einheit erstellt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-204">A biometric unit was created.</span></span> <span data-ttu-id="1bc3c-205">Weitere Informationen finden Sie unter [**winbioasyncmonitorframeworkchanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-205">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**Entfernen von winbio- \_ Vorgangs \_ Einheiten \_**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**WINBIO\_OPERATION\_UNIT\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-207">26</span><span class="sxs-lookup"><span data-stu-id="1bc3c-207">26</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-208">Eine biometrische Einheit wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-208">A biometric unit was deleted.</span></span> <span data-ttu-id="1bc3c-209">Weitere Informationen finden Sie unter [**winbioasyncmonitorframeworkchanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-209">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**winbio \_ -Vorgang zum \_ identifizieren \_ und \_ Freigeben des \_ Tickets**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO\_OPERATION\_IDENTIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-211">27</span><span class="sxs-lookup"><span data-stu-id="1bc3c-211">27</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-212">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-212">Reserved.</span></span> <span data-ttu-id="1bc3c-213">Dieser Wert wird ab Windows 10 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-213">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**winbio \_ -Vorgang zum \_ überprüfen \_ und \_ Freigeben des \_ Tickets**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO\_OPERATION\_VERIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-215">28</span><span class="sxs-lookup"><span data-stu-id="1bc3c-215">28</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-216">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-216">Reserved.</span></span> <span data-ttu-id="1bc3c-217">Dieser Wert wird ab Windows 10 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-217">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**Anwesenheit des winbio- \_ Vorgangs \_ Monitors \_**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**WINBIO\_OPERATION\_MONITOR\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-219">29</span><span class="sxs-lookup"><span data-stu-id="1bc3c-219">29</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-220">Der Gesichts Erkennungsmechanismus oder der Iris-Überwachungsmechanismus wurde aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-220">The facial recognition or iris monitoring mechanism was turned on.</span></span> <span data-ttu-id="1bc3c-221">Weitere Informationen finden Sie unter [**winbiomonitorpresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-221">For more information, see [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span></span> <span data-ttu-id="1bc3c-222">Dieser Wert wird ab Windows 10 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-222">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1bc3c-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**winbio- \_ Operation \_ registrieren ( \_ Select)**</span><span class="sxs-lookup"><span data-stu-id="1bc3c-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO\_OPERATION\_ENROLL\_SELECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bc3c-224">30</span><span class="sxs-lookup"><span data-stu-id="1bc3c-224">30</span></span>
</dt> <dt>



<span data-ttu-id="1bc3c-225">Eine Person aus einer Gruppe von Einzelpersonen, die durch Daten im Beispiel Puffer dargestellt wird, wurde als zu registrierende Person angegeben.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-225">An individual from a group of individuals that are represented by data in the sample buffer was specified as the individual to enroll.</span></span> <span data-ttu-id="1bc3c-226">Weitere Informationen finden Sie unter [**winbioeinschreibung Select**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span><span class="sxs-lookup"><span data-stu-id="1bc3c-226">For more information, see [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span></span> <span data-ttu-id="1bc3c-227">Dieser Wert wird ab Windows 10 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1bc3c-227">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bc3c-228">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bc3c-228">Requirements</span></span>



| <span data-ttu-id="1bc3c-229">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bc3c-229">Requirement</span></span> | <span data-ttu-id="1bc3c-230">Wert</span><span class="sxs-lookup"><span data-stu-id="1bc3c-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc3c-231">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1bc3c-231">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc3c-232">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bc3c-232">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="1bc3c-233">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1bc3c-233">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc3c-234">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1bc3c-234">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="1bc3c-235">Header</span><span class="sxs-lookup"><span data-stu-id="1bc3c-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bc3c-236"><dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc3c-236"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bc3c-237">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bc3c-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc3c-238">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="1bc3c-238">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





