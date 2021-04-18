---
description: Wenn ein Fehler auftritt, gibt WMI einen Fehlercode als HRESULT-Wert zurück. Diese Codes können von Skripts, C++-Anwendungen oder WMIC zurückgegeben werden.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: WMI-Fehler Konstanten (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368211"
---
# <a name="wmi-error-constants"></a><span data-ttu-id="9be87-104">WMI-Fehler Konstanten</span><span class="sxs-lookup"><span data-stu-id="9be87-104">WMI Error Constants</span></span>

<span data-ttu-id="9be87-105">Wenn ein Fehler auftritt, gibt WMI einen Fehlercode als **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9be87-105">If an error occurs, WMI returns an error code as an **HRESULT** value.</span></span> <span data-ttu-id="9be87-106">Diese Codes können von Skripts, C++-Anwendungen oder [**WMIC**](wmic.md)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md).</span></span>

> [!Note]
>
> <span data-ttu-id="9be87-107">Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren.</span><span class="sxs-lookup"><span data-stu-id="9be87-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="9be87-108">Wenn Sie ein Endbenutzer sind, bei dem eine Fehlermeldung zu WMI aufgetreten ist, sollten Sie [Microsoft-Support](https://support.microsoft.com/) aufrufen und nach dem Fehlercode suchen, der in der Fehlermeldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9be87-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="9be87-109">Weitere Informationen zur Behebung von Problemen mit WMI-Skripts und dem WMI-Dienst finden Sie unter [WMI funktioniert nicht!](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="9be87-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10)).</span></span>
>
> <span data-ttu-id="9be87-110">Wenn WMI Fehlermeldungen zurückgibt, beachten Sie, dass Sie möglicherweise nicht auf Probleme im WMI-Dienst oder in WMI-Anbietern hinweisen.</span><span class="sxs-lookup"><span data-stu-id="9be87-110">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="9be87-111">Fehler können aus anderen Teilen des Betriebssystems stammen und als Fehler über WMI auftreten.</span><span class="sxs-lookup"><span data-stu-id="9be87-111">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="9be87-112">Löschen Sie das WMI-Repository unter Umständen nicht als erste Aktion, da das Löschen des Repository zu Beschädigungen des Systems oder der installierten Anwendungen führen kann.</span><span class="sxs-lookup"><span data-stu-id="9be87-112">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="9be87-113">Um weitere Informationen zur Ursache des Problems zu erhalten, können Sie das Befehlszeilen Tool [WMI-Diagnosehilfsprogramm](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnose herunterladen und ausführen.</span><span class="sxs-lookup"><span data-stu-id="9be87-113">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="9be87-114">Mit diesem Tool wird ein Bericht erstellt, der in der Regel die Ursache des Problems isolieren und Anweisungen zur Behebung des Problems bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="9be87-114">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="9be87-115">Der Bericht hilft Ihnen auch bei der Unterstützung durch den Microsoft-Support.</span><span class="sxs-lookup"><span data-stu-id="9be87-115">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="9be87-116">Sie können die WMI-Diagnosehilfsprogramm [hier](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="9be87-116">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

<span data-ttu-id="9be87-117">Einige Methoden in WMI-Klassen können System-und Netzwerkfehler Codes zurückgeben (z. b. 64).</span><span class="sxs-lookup"><span data-stu-id="9be87-117">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="9be87-118">Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den Befehl **net helpmsg** im Eingabe Aufforderungs Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="9be87-118">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="9be87-119">Der Befehl **net helpmsg 64** gibt beispielsweise die folgende Meldung zurück: der angegebene Netzwerkname ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9be87-119">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

<span data-ttu-id="9be87-120">In der folgenden Liste sind einige allgemeine Fehler Bereiche aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9be87-120">The following list lists some common ranges of errors.</span></span>

<dl> <dt>

<span data-ttu-id="9be87-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068-0x80041099</span><span class="sxs-lookup"><span data-stu-id="9be87-121"><span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099</span></span>
</dt> <dd>

<span data-ttu-id="9be87-122">Fehler, die von WMI selbst stammen.</span><span class="sxs-lookup"><span data-stu-id="9be87-122">Errors that originate in WMI itself.</span></span>

<span data-ttu-id="9be87-123">Fehler bei einem bestimmten WMI-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9be87-123">A specific WMI operation failed because of</span></span>

-   <span data-ttu-id="9be87-124">Ein Fehler in der Anforderung, z. b. eine WQL-Abfrage, oder das Konto verfügt nicht über die richtigen Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="9be87-124">An error in the request, for example, a WQL query fails or the account does not have the correct permissions.</span></span>
-   <span data-ttu-id="9be87-125">Ein WMI-Infrastrukturproblem, z. b. eine falsche CIM-oder DCOM-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="9be87-125">A WMI infrastructure problem, such as incorrect CIM or DCOM registration.</span></span>

</dd> <dt>

<span data-ttu-id="9be87-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span><span class="sxs-lookup"><span data-stu-id="9be87-126"><span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx</span></span>
</dt> <dd>

<span data-ttu-id="9be87-127">Fehler, die im Kernbetriebssystem auftreten.</span><span class="sxs-lookup"><span data-stu-id="9be87-127">Errors originating in the core operating system.</span></span> <span data-ttu-id="9be87-128">Diese Art von Fehler kann von WMI aufgrund eines externen Fehlers (z. b. DCOM-Sicherheitsfehler) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-128">WMI may return this type of error because of an external failure, for example, DCOM security failure.</span></span>

</dd> <dt>

<span data-ttu-id="9be87-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span><span class="sxs-lookup"><span data-stu-id="9be87-129"><span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx</span></span>
</dt> <dd>

<span data-ttu-id="9be87-130">Fehler, die in DCOM ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-130">Errors originating in DCOM.</span></span> <span data-ttu-id="9be87-131">Beispielsweise ist die DCOM-Konfiguration für Vorgänge auf einem Remote Computer möglicherweise falsch.</span><span class="sxs-lookup"><span data-stu-id="9be87-131">For example, the DCOM configuration for operations to a remote computer may be incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="9be87-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span><span class="sxs-lookup"><span data-stu-id="9be87-132"><span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx</span></span>
</dt> <dd>

<span data-ttu-id="9be87-133">Fehler aus ADSI (Active Directory-Dienst Schnittstellen) oder LDAP (Lightweight Directory Access Protocol), z. b. ein Active Directory Zugriffsfehler, wenn die WMI-Active Directory Anbieter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-133">Error originating from ADSI (Active Directory Service Interfaces) or LDAP (Lightweight Directory Access Protocol), for example, an Active Directory access failure when using the WMI Active Directory providers.</span></span>

</dd> </dl>

<span data-ttu-id="9be87-134">Einige Methoden in WMI-Klassen können System-und Netzwerkfehler Codes zurückgeben (z. b. 64).</span><span class="sxs-lookup"><span data-stu-id="9be87-134">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="9be87-135">Sie können die Definition dieser Arten von Fehlercodes überprüfen, indem Sie den Befehl **net helpmsg** im Eingabe Aufforderungs Fenster verwenden.</span><span class="sxs-lookup"><span data-stu-id="9be87-135">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="9be87-136">Der Befehl **net helpmsg 64** gibt beispielsweise die folgende Meldung zurück: der angegebene Netzwerkname ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9be87-136">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span> <span data-ttu-id="9be87-137">In C++ können Sie [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) und **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** als Nachrichten Modul angeben.</span><span class="sxs-lookup"><span data-stu-id="9be87-137">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="9be87-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="9be87-138"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-139">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9be87-139">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-140">Fehler beim Abrufen.</span><span class="sxs-lookup"><span data-stu-id="9be87-140">Call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="9be87-141"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-142">2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="9be87-142">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-143">Das Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="9be87-143">Object cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM \_ E- \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="9be87-144"><span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-145">2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="9be87-145">2147749891 (0x80041003)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-146">Der aktuelle Benutzer verfügt nicht über die Berechtigung zum Ausführen der Aktion.</span><span class="sxs-lookup"><span data-stu-id="9be87-146">Current user does not have permission to perform the action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**Fehler beim WBEM \_ E- \_ Anbieter. \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-147"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-148">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="9be87-148">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-149">Der Anbieter ist zu einem anderen Zeitpunkt als während der Initialisierung fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="9be87-149">Provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM \_ E- \_ Typen Konflikt \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-150"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-151">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="9be87-151">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-152">Es ist ein Typen Konflikt aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9be87-152">Type mismatch occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**nicht genügend \_ Arbeits \_ \_ Speicher für \_ WBEM E**</span><span class="sxs-lookup"><span data-stu-id="9be87-153"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-154">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="9be87-154">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-155">Nicht genügend Arbeitsspeicher für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9be87-155">Not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM \_ E ( \_ ungültiger \_ Kontext)**</span><span class="sxs-lookup"><span data-stu-id="9be87-156"><span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**WBEM\_E\_INVALID\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-157">2147749895 (0x80041007)</span><span class="sxs-lookup"><span data-stu-id="9be87-157">2147749895 (0x80041007)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-158">Das [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Objekt ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-158">The [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_Ungültiger WBEM E- \_ \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="9be87-159"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-160">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="9be87-160">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-161">Einer der Parameter für den Aufruf ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="9be87-161">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="9be87-162"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-163">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="9be87-163">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-164">Die Ressource (in der Regel ein Remote Server) ist zurzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9be87-164">Resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**kritischer WBEM \_ E- \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="9be87-165"><span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**WBEM\_E\_CRITICAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-166">2147749898 (0x8004100a)</span><span class="sxs-lookup"><span data-stu-id="9be87-166">2147749898 (0x8004100A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-167">Interner, kritischer und unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="9be87-167">Internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="9be87-168">Melden Sie den Fehler an den technischen Support von Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9be87-168">Report the error to Microsoft Technical Support.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM \_ E \_ ungültiger \_ Stream**</span><span class="sxs-lookup"><span data-stu-id="9be87-169"><span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**WBEM\_E\_INVALID\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-170">2147749899 (0x8004100b)</span><span class="sxs-lookup"><span data-stu-id="9be87-170">2147749899 (0x8004100B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-171">Während einer Remotesitzung wurde mindestens ein Netzwerkpaket beschädigt.</span><span class="sxs-lookup"><span data-stu-id="9be87-171">One or more network packets were corrupted during a remote session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="9be87-172"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-173">2147749900 (0x8004100c)</span><span class="sxs-lookup"><span data-stu-id="9be87-173">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-174">Die Funktion oder der Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-174">Feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM \_ E \_ ungültige \_ Superclass.**</span><span class="sxs-lookup"><span data-stu-id="9be87-175"><span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**WBEM\_E\_INVALID\_SUPERCLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-176">2147749901 (0x8004100d)</span><span class="sxs-lookup"><span data-stu-id="9be87-176">2147749901 (0x8004100D)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-177">Die angegebene übergeordnete Klasse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-177">Parent class specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E ( \_ ungültiger \_ Namespace)**</span><span class="sxs-lookup"><span data-stu-id="9be87-178"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-179">2147749902 (0x8004100e)</span><span class="sxs-lookup"><span data-stu-id="9be87-179">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-180">Der angegebene Namespace wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="9be87-180">Namespace specified cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**ungültiges WBEM- \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="9be87-181"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-182">2147749903 (0x8004100f)</span><span class="sxs-lookup"><span data-stu-id="9be87-182">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-183">Die angegebene Instanz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-183">Specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**\_ungültige WBEM E- \_ \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="9be87-184"><span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM\_E\_INVALID\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-185">2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="9be87-185">2147749904 (0x80041010)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-186">Die angegebene Klasse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-186">Specified class is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**der WBEM \_ E- \_ Anbieter wurde \_ nicht \_ gefunden.**</span><span class="sxs-lookup"><span data-stu-id="9be87-187"><span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**WBEM\_E\_PROVIDER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-188">2147749905 (0x80041011)</span><span class="sxs-lookup"><span data-stu-id="9be87-188">2147749905 (0x80041011)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-189">Der Anbieter, auf den im Schema verwiesen wird, verfügt über keine entsprechende Registrierung.</span><span class="sxs-lookup"><span data-stu-id="9be87-189">Provider referenced in the schema does not have a corresponding registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**\_ \_ ungültige \_ Anbieter \_ Registrierung für WBEM E**</span><span class="sxs-lookup"><span data-stu-id="9be87-190"><span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**WBEM\_E\_INVALID\_PROVIDER\_REGISTRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-191">2147749906</span><span class="sxs-lookup"><span data-stu-id="9be87-191">2147749906</span></span>
</dt> <dt>



<span data-ttu-id="9be87-192">Der im Schema referenzierte Anbieter weist eine falsche oder unvollständige Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="9be87-192">Provider referenced in the schema has an incorrect or incomplete registration.</span></span>

<span data-ttu-id="9be87-193">Dieser Fehler kann durch eine Vielzahl von Bedingungen verursacht werden, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="9be87-193">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="9be87-194">Ein fehlender [ \# pragma-Namespace](pragma-namespace.md) Befehl in der Managed Object Format (MOF)-Datei, die zum Registrieren des Anbieters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9be87-194">A missing [\#pragma namespace](pragma-namespace.md) command in the Managed Object Format (MOF) file used to register the provider.</span></span> <span data-ttu-id="9be87-195">Der Anbieter kann im falschen WMI-Namespace registriert werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-195">The provider may be registered in the wrong WMI namespace.</span></span>
-   <span data-ttu-id="9be87-196">Fehler beim Abrufen der com-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="9be87-196">Failure to retrieve the COM registration.</span></span>
-   <span data-ttu-id="9be87-197">Das Hostingmodell ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-197">Hosting model is not valid.</span></span> <span data-ttu-id="9be87-198">Weitere Informationen finden Sie unter [Anbieter Hosting und-Sicherheit](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="9be87-198">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>
-   <span data-ttu-id="9be87-199">Eine in der Registrierung angegebene Klasse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-199">An class specified in the registration is not valid.</span></span>
-   <span data-ttu-id="9be87-200">Fehler beim Erstellen einer Instanz von oder Erben von der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, um die Anbieter Registrierung in der MOF-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9be87-200">Failure to create an instance of or inherit from the [**\_\_Win32Provider**](--win32provider.md) class to create the provider registration in the MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**Fehler beim Laden des WBEM \_ E- \_ Anbieters \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-201"><span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**WBEM\_E\_PROVIDER\_LOAD\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-202">2147749907 (0x80041013)</span><span class="sxs-lookup"><span data-stu-id="9be87-202">2147749907 (0x80041013)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-203">COM kann keinen Provider finden, auf den im Schema verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="9be87-203">COM cannot locate a provider referenced in the schema.</span></span>

<span data-ttu-id="9be87-204">Dieser Fehler kann durch eine Vielzahl von Bedingungen verursacht werden, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="9be87-204">This error may be caused by many conditions, including the following:</span></span>

-   <span data-ttu-id="9be87-205">Der Anbieter verwendet eine WMI-dll, die nicht mit der LIB-Datei identisch ist, die beim Erstellen des Anbieters verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9be87-205">Provider is using a WMI DLL that does not match the .lib file used when the provider was built.</span></span>
-   <span data-ttu-id="9be87-206">Die Anbieter-DLL oder eine der DLLs, von denen Sie abhängt, ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="9be87-206">Provider's DLL, or any of the DLLs on which it depends, is corrupt.</span></span>
-   <span data-ttu-id="9be87-207">Der Anbieter konnte [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)nicht exportieren.</span><span class="sxs-lookup"><span data-stu-id="9be87-207">Provider failed to export [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span>
-   <span data-ttu-id="9be87-208">Der in-Process-Anbieter wurde nicht mit dem **regsvr32** -Befehl registriert.</span><span class="sxs-lookup"><span data-stu-id="9be87-208">In-process provider was not registered using the **regsvr32** command.</span></span>
-   <span data-ttu-id="9be87-209">Der Out-of-Process-Anbieter wurde nicht mit dem Schalter **/RegServer** registriert.</span><span class="sxs-lookup"><span data-stu-id="9be87-209">Out-of-process provider was not registered using the **/regserver** switch.</span></span> <span data-ttu-id="9be87-210">Beispielsweise **myprog.exe/RegServer**.</span><span class="sxs-lookup"><span data-stu-id="9be87-210">For example, **myprog.exe /regserver**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM \_ E- \_ Initialisierungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="9be87-211"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-212">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="9be87-212">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-213">Die Komponente, z. b. ein Anbieter, konnte aus internen Gründen nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-213">Component, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM \_ E- \_ Transport \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="9be87-214"><span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**WBEM\_E\_TRANSPORT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-215">2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="9be87-215">2147749909 (0x80041015)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-216">Netzwerkfehler, der den normalen Betrieb verhindert.</span><span class="sxs-lookup"><span data-stu-id="9be87-216">Networking error that prevents normal operation has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_Ungültiger WBEM E- \_ \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="9be87-217"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-218">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="9be87-218">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-219">Der angeforderte Vorgang ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-219">Requested operation is not valid.</span></span> <span data-ttu-id="9be87-220">Dieser Fehler betrifft i. A. ungültige Versuche, Klassen oder Eigenschaften zu löschen.</span><span class="sxs-lookup"><span data-stu-id="9be87-220">This error usually applies to invalid attempts to delete classes or properties.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ungültige WBEM E- \_ \_ Abfrage**</span><span class="sxs-lookup"><span data-stu-id="9be87-221"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-222">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="9be87-222">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-223">Die Abfrage war nicht syntaktisch gültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-223">Query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_Ungültiger WBEM E- \_ \_ Abfragetyp \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-224"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-225">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="9be87-225">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-226">Die angeforderte Abfragesprache wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-226">Requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="9be87-227"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-228">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="9be87-228">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-229">In einem Put-Vorgang wurde das Flag " **wbemchangeflagkreateonly** " angegeben, aber die Instanz ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9be87-229">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**außer Kraft Setzung von WBEM \_ E \_ \_ nicht \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="9be87-230"><span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**WBEM\_E\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-231">2147749914 (0x8004101a)</span><span class="sxs-lookup"><span data-stu-id="9be87-231">2147749914 (0x8004101A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-232">Der Add-Vorgang kann für diesen Qualifizierer nicht durchgeführt werden, da das besitzende Objekt keine über schreibungen zulässt.</span><span class="sxs-lookup"><span data-stu-id="9be87-232">Not possible to perform the add operation on this qualifier because the owning object does not permit overrides.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM \_ E \_ - \_ Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="9be87-233"><span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**WBEM\_E\_PROPAGATED\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-234">2147749915 (0x8004101b)</span><span class="sxs-lookup"><span data-stu-id="9be87-234">2147749915 (0x8004101B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-235">Der Benutzer hat versucht, einen Qualifizierer zu löschen, der nicht im Besitz</span><span class="sxs-lookup"><span data-stu-id="9be87-235">User attempted to delete a qualifier that was not owned.</span></span> <span data-ttu-id="9be87-236">Der Qualifizierer wurde von einer übergeordneten Klasse vererbt.</span><span class="sxs-lookup"><span data-stu-id="9be87-236">The qualifier was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**\_propagierte WBEM E- \_ \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="9be87-237"><span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**WBEM\_E\_PROPAGATED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-238">2147749916 (0x8004101c)</span><span class="sxs-lookup"><span data-stu-id="9be87-238">2147749916 (0x8004101C)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-239">Der Benutzer hat versucht, eine Eigenschaft zu löschen, deren Besitzer er nicht war.</span><span class="sxs-lookup"><span data-stu-id="9be87-239">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="9be87-240">Die Eigenschaft wurde von einer übergeordneten Klasse vererbt.</span><span class="sxs-lookup"><span data-stu-id="9be87-240">The property was inherited from a parent class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ unerwartet**</span><span class="sxs-lookup"><span data-stu-id="9be87-241"><span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM\_E\_UNEXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-242">2147749917 (0x8004101d)</span><span class="sxs-lookup"><span data-stu-id="9be87-242">2147749917 (0x8004101D)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-243">Der Client hat eine unerwartete und unzulässige Sequenz von Aufrufen vorgenommen, z. b. das Aufrufen von [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) vor dem Aufrufen von [**beginenumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span><span class="sxs-lookup"><span data-stu-id="9be87-243">Client made an unexpected and illegal sequence of calls, such as calling [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) before calling [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**Ungültiger WBEM- \_ \_ \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="9be87-244"><span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**WBEM\_E\_ILLEGAL\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-245">2147749918 (0x8004101e)</span><span class="sxs-lookup"><span data-stu-id="9be87-245">2147749918 (0x8004101E)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-246">Der Benutzer hat einen ungültigen Vorgang angefordert, z. b. das Abrufen einer Klasse aus einer Instanz.</span><span class="sxs-lookup"><span data-stu-id="9be87-246">User requested an illegal operation, such as spawning a class from an instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ darf \_ nicht \_ Schlüssel sein.**</span><span class="sxs-lookup"><span data-stu-id="9be87-247"><span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM\_E\_CANNOT\_BE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-248">2147749919 (0x8004101f)</span><span class="sxs-lookup"><span data-stu-id="9be87-248">2147749919 (0x8004101F)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-249">Unzulässiger Versuch, einen Schlüssel Qualifizierer für eine Eigenschaft anzugeben, die kein Schlüssel sein kann.</span><span class="sxs-lookup"><span data-stu-id="9be87-249">Illegal attempt to specify a key qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="9be87-250">Die Schlüssel sind in der Klassendefinition für ein Objekt angegeben und können nicht für jede Instanz einzeln geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-250">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**unvollständige WBEM \_ E- \_ \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="9be87-251"><span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**WBEM\_E\_INCOMPLETE\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-252">2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="9be87-252">2147749920 (0x80041020)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-253">Das aktuelle Objekt ist keine gültige Klassendefinition.</span><span class="sxs-lookup"><span data-stu-id="9be87-253">Current object is not a valid class definition.</span></span> <span data-ttu-id="9be87-254">Entweder ist sie unvollständig, oder Sie wurde nicht bei WMI mithilfe von " [**errbemubject. \_ Put**](swbemobject-put-.md)" registriert.</span><span class="sxs-lookup"><span data-stu-id="9be87-254">Either it is incomplete or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ungültige WBEM E- \_ \_ Syntax**</span><span class="sxs-lookup"><span data-stu-id="9be87-255"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-256">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="9be87-256">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-257">Die Abfrage ist syntaktisch ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-257">Query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**nicht ergänzten WBEM- \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="9be87-258"><span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**WBEM\_E\_NONDECORATED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-259">2147749922 (0x80041022)</span><span class="sxs-lookup"><span data-stu-id="9be87-259">2147749922 (0x80041022)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-260">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9be87-260">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E schreibgeschützt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-261"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-262">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="9be87-262">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-263">Es wurde versucht, eine schreibgeschützte Eigenschaft zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9be87-263">An attempt was made to modify a read-only property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E \_ - \_ Anbieter \_ ist nicht fähig**</span><span class="sxs-lookup"><span data-stu-id="9be87-264"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-265">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="9be87-265">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-266">Der Anbieter kann den angeforderten Vorgang nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="9be87-266">Provider cannot perform the requested operation.</span></span> <span data-ttu-id="9be87-267">Dies kann eine Abfrage enthalten, die zu komplex ist, eine Instanz abruft, eine Klasse erstellt oder aktualisiert, eine Klasse löscht oder eine Klasse auflistet.</span><span class="sxs-lookup"><span data-stu-id="9be87-267">This can include a query that is too complex, retrieving an instance, creating or updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM \_ E- \_ Klasse \_ hat \_ untergeordnete Elemente**</span><span class="sxs-lookup"><span data-stu-id="9be87-268"><span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**WBEM\_E\_CLASS\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-269">2147749925 (0x80041025)</span><span class="sxs-lookup"><span data-stu-id="9be87-269">2147749925 (0x80041025)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-270">Es wurde versucht, eine Änderung vorzunehmen, durch die eine Unterklasse ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="9be87-270">Attempt was made to make a change that invalidates a subclass.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM \_ E- \_ Klasse \_ verfügt über \_ Instanzen**</span><span class="sxs-lookup"><span data-stu-id="9be87-271"><span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**WBEM\_E\_CLASS\_HAS\_INSTANCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-272">2147749926 (0x80041026)</span><span class="sxs-lookup"><span data-stu-id="9be87-272">2147749926 (0x80041026)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-273">Es wurde versucht, eine Klasse zu löschen oder zu ändern, die Instanzen enthält.</span><span class="sxs-lookup"><span data-stu-id="9be87-273">Attempt was made to delete or modify a class that has instances.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM \_ E- \_ Abfrage \_ nicht \_ implementiert**</span><span class="sxs-lookup"><span data-stu-id="9be87-274"><span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**WBEM\_E\_QUERY\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-275">2147749927 (0x80041027)</span><span class="sxs-lookup"><span data-stu-id="9be87-275">2147749927 (0x80041027)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-276">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9be87-276">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ unzulässig \_ null**</span><span class="sxs-lookup"><span data-stu-id="9be87-277"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-278">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="9be87-278">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-279">Der Wert Nothing/**null** wurde für eine Eigenschaft angegeben, die über einen Wert verfügen muss, z. b. einen, der durch einen [**Schlüssel**](key-qualifier.md), einen [**indizierten**](optional-qualifiers.md)oder einen **nicht- \_ null** -Qualifizierer gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="9be87-279">Value of Nothing/**NULL** was specified for a property that must have a value, such as one that is marked by a [**Key**](key-qualifier.md), [**Indexed**](optional-qualifiers.md), or **Not\_Null** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**\_Ungültiger WBEM E- \_ \_ Qualifizierertyp \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-280"><span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**WBEM\_E\_INVALID\_QUALIFIER\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-281">2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="9be87-281">2147749929 (0x80041029)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-282">Der Variant-Wert für einen Qualifizierer wurde bereitgestellt, der kein gültiger qualifizierungstyp ist.</span><span class="sxs-lookup"><span data-stu-id="9be87-282">Variant value for a qualifier was provided that is not a legal qualifier type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**\_Ungültiger WBEM E- \_ \_ \_ Eigenschaftentyp**</span><span class="sxs-lookup"><span data-stu-id="9be87-283"><span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**WBEM\_E\_INVALID\_PROPERTY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-284">2147749930 (0x8004102a)</span><span class="sxs-lookup"><span data-stu-id="9be87-284">2147749930 (0x8004102A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-285">Der für eine Eigenschaft angegebene CIM-Typ ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-285">CIM type specified for a property is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_der Wert von WBEM E liegt \_ \_ außerhalb \_ des zulässigen \_ Bereichs.**</span><span class="sxs-lookup"><span data-stu-id="9be87-286"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-287">2147749931 (0x8004102b)</span><span class="sxs-lookup"><span data-stu-id="9be87-287">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-288">Die Anforderung wurde mit einem Wert außerhalb des gültigen Bereichs erstellt, oder Sie ist mit dem Typ nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9be87-288">Request was made with an out-of-range value or it is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ darf \_ kein \_ Singleton sein.**</span><span class="sxs-lookup"><span data-stu-id="9be87-289"><span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM\_E\_CANNOT\_BE\_SINGLETON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-290">2147749932 (0x8004102c)</span><span class="sxs-lookup"><span data-stu-id="9be87-290">2147749932 (0x8004102C)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-291">Es wurde ein unzulässiger Versuch unternommen, eine Singleton-Klasse zu erstellen, z. b. wenn die Klasse von einer nicht-Singleton-Klasse abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="9be87-291">Illegal attempt was made to make a class singleton, such as when the class is derived from a non-singleton class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E, \_ ungültiger \_ CIM- \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="9be87-292"><span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM\_E\_INVALID\_CIM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-293">2147749933 (0x8004102d)</span><span class="sxs-lookup"><span data-stu-id="9be87-293">2147749933 (0x8004102D)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-294">Der angegebene CIM-Typ ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-294">CIM type specified is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ungültige WBEM E- \_ \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="9be87-295"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-296">2147749934 (0x8004102e)</span><span class="sxs-lookup"><span data-stu-id="9be87-296">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-297">Die angeforderte Methode ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9be87-297">Requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_ \_ ungültige \_ Methoden \_ Parameter für WBEM E**</span><span class="sxs-lookup"><span data-stu-id="9be87-298"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-299">2147749935 (0x8004102f)</span><span class="sxs-lookup"><span data-stu-id="9be87-299">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-300">Die für die Methode angegebenen Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-300">Parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM \_ E- \_ System \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="9be87-301"><span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**WBEM\_E\_SYSTEM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-302">2147749936 (0x80041030)</span><span class="sxs-lookup"><span data-stu-id="9be87-302">2147749936 (0x80041030)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-303">Es wurde versucht, Qualifizierer für eine Systemeigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9be87-303">There was an attempt to get qualifiers on a system property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**\_ungültige WBEM E- \_ \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="9be87-304"><span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**WBEM\_E\_INVALID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-305">2147749937 (0x80041031)</span><span class="sxs-lookup"><span data-stu-id="9be87-305">2147749937 (0x80041031)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-306">Der Eigenschaftentyp wird nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="9be87-306">Property type is not recognized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM \_ E- \_ Rückruf \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="9be87-307"><span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**WBEM\_E\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-308">2147749938 (0x80041032)</span><span class="sxs-lookup"><span data-stu-id="9be87-308">2147749938 (0x80041032)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-309">Der asynchrone Prozess wurde intern oder vom Benutzer abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9be87-309">Asynchronous process has been canceled internally or by the user.</span></span> <span data-ttu-id="9be87-310">Beachten Sie, dass der Vorgang aufgrund der zeitlichen Steuerung und der Art des asynchronen Vorgangs möglicherweise nicht wirklich abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="9be87-310">Note that due to the timing and nature of the asynchronous operation, the operation may not have been truly canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM \_ E \_ wird \_ heruntergefahren**</span><span class="sxs-lookup"><span data-stu-id="9be87-311"><span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**WBEM\_E\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-312">2147749939 (0x80041033)</span><span class="sxs-lookup"><span data-stu-id="9be87-312">2147749939 (0x80041033)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-313">Der Benutzer hat einen Vorgang angefordert, während WMI gerade heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="9be87-313">User has requested an operation while WMI is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_propagierte WBEM E- \_ \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="9be87-314"><span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**WBEM\_E\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-315">2147749940 (0x80041034)</span><span class="sxs-lookup"><span data-stu-id="9be87-315">2147749940 (0x80041034)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-316">Es wurde versucht, einen vorhandenen Methodennamen aus einer übergeordneten Klasse wiederzuverwenden, und die Signaturen stimmen nicht ab.</span><span class="sxs-lookup"><span data-stu-id="9be87-316">Attempt was made to reuse an existing method name from a parent class and the signatures do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**\_nicht unterstützter WBEM E- \_ \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="9be87-317"><span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**WBEM\_E\_UNSUPPORTED\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-318">2147749941 (0x80041035)</span><span class="sxs-lookup"><span data-stu-id="9be87-318">2147749941 (0x80041035)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-319">Mindestens ein Parameterwert (z. B. ein Abfragetext) ist zu komplex oder wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-319">One or more parameter values, such as a query text, is too complex or unsupported.</span></span> <span data-ttu-id="9be87-320">Daher wird WMI aufgefordert, den Vorgang mit einfacheren Parametern erneut auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9be87-320">WMI is therefore requested to retry the operation with simpler parameters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**\_ \_ fehlende \_ Parameter- \_ ID für WBEM E**</span><span class="sxs-lookup"><span data-stu-id="9be87-321"><span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**WBEM\_E\_MISSING\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-322">2147749942 (0x80041036)</span><span class="sxs-lookup"><span data-stu-id="9be87-322">2147749942 (0x80041036)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-323">Im Methoden aufruffehlte ein Parameter.</span><span class="sxs-lookup"><span data-stu-id="9be87-323">Parameter was missing from the method call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**\_ \_ ungültige Parameter- \_ \_ ID für WBEM E**</span><span class="sxs-lookup"><span data-stu-id="9be87-324"><span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**WBEM\_E\_INVALID\_PARAMETER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-325">2147749943 (0x80041037)</span><span class="sxs-lookup"><span data-stu-id="9be87-325">2147749943 (0x80041037)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-326">Der Methoden Parameter weist einen ungültigen [**ID**](standard-wmi-qualifiers.md) -Qualifizierer auf.</span><span class="sxs-lookup"><span data-stu-id="9be87-326">Method parameter has an [**ID**](standard-wmi-qualifiers.md) qualifier that is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_ \_ nicht aufeinander folgende Parameter- \_ \_ IDs in WBEM E**</span><span class="sxs-lookup"><span data-stu-id="9be87-327"><span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**WBEM\_E\_NONCONSECUTIVE\_PARAMETER\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-328">2147749944 (0x80041038)</span><span class="sxs-lookup"><span data-stu-id="9be87-328">2147749944 (0x80041038)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-329">Mindestens ein Methoden Parameter hat [**ID**](standard-wmi-qualifiers.md) -Qualifizierer, die nicht in der Reihenfolge sind.</span><span class="sxs-lookup"><span data-stu-id="9be87-329">One or more of the method parameters have [**ID**](standard-wmi-qualifiers.md) qualifiers that are out of sequence.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM \_ E- \_ Parameter- \_ ID \_ in \_ retval**</span><span class="sxs-lookup"><span data-stu-id="9be87-330"><span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**WBEM\_E\_PARAMETER\_ID\_ON\_RETVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-331">2147749945 (0x80041039)</span><span class="sxs-lookup"><span data-stu-id="9be87-331">2147749945 (0x80041039)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-332">Der Rückgabewert einer Methode hat einen [**ID**](standard-wmi-qualifiers.md) -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="9be87-332">Return value for a method has an [**ID**](standard-wmi-qualifiers.md) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E ( \_ ungültiger \_ Objekt \_ Pfad)**</span><span class="sxs-lookup"><span data-stu-id="9be87-333"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-334">2147749946 (0x8004103a)</span><span class="sxs-lookup"><span data-stu-id="9be87-334">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-335">Der angegebene Objekt Pfad war ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-335">Specified object path was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM \_ E \_ nicht mehr genügend \_ \_ Speicher \_ Platz**</span><span class="sxs-lookup"><span data-stu-id="9be87-336"><span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**WBEM\_E\_OUT\_OF\_DISK\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-337">2147749947 (0x8004103b)</span><span class="sxs-lookup"><span data-stu-id="9be87-337">2147749947 (0x8004103B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-338">Nicht genügend Speicherplatz auf dem Datenträger, oder das Limit von 4 GB auf dem WMI-Repository (CIM-Repository) wurde erreicht.</span><span class="sxs-lookup"><span data-stu-id="9be87-338">Disk is out of space or the 4 GB limit on WMI repository (CIM repository) size is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM \_ E- \_ Puffer \_ zu \_ klein**</span><span class="sxs-lookup"><span data-stu-id="9be87-339"><span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**WBEM\_E\_BUFFER\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-340">2147749948 (0x8004103c)</span><span class="sxs-lookup"><span data-stu-id="9be87-340">2147749948 (0x8004103C)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-341">Der angegebene Puffer war zu klein, um alle Objekte im Enumerator aufzunehmen oder eine Zeichen folgen Eigenschaft zu lesen.</span><span class="sxs-lookup"><span data-stu-id="9be87-341">Supplied buffer was too small to hold all of the objects in the enumerator or to read a string property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**\_ \_ nicht unterstützte put- \_ \_ Erweiterung für WBEM E**</span><span class="sxs-lookup"><span data-stu-id="9be87-342"><span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**WBEM\_E\_UNSUPPORTED\_PUT\_EXTENSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-343">2147749949 (0x8004103d)</span><span class="sxs-lookup"><span data-stu-id="9be87-343">2147749949 (0x8004103D)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-344">Der angeforderte Put-Vorgang wird vom Anbieter nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-344">Provider does not support the requested put operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**\_ \_ unbekannter \_ Objekttyp WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-345"><span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**WBEM\_E\_UNKNOWN\_OBJECT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-346">2147749950 (0x8004103e)</span><span class="sxs-lookup"><span data-stu-id="9be87-346">2147749950 (0x8004103E)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-347">Beim Mars Hallen wurde ein Objekt mit einem falschen Typ oder einer falschen Version gefunden.</span><span class="sxs-lookup"><span data-stu-id="9be87-347">Object with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_ \_ unbekannter \_ \_ Pakettyp WBEM E.**</span><span class="sxs-lookup"><span data-stu-id="9be87-348"><span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**WBEM\_E\_UNKNOWN\_PACKET\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-349">2147749951 (0x8004103f)</span><span class="sxs-lookup"><span data-stu-id="9be87-349">2147749951 (0x8004103F)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-350">Beim Mars Hallen wurde ein Paket mit einem falschen Typ oder einer falschen Version gefunden.</span><span class="sxs-lookup"><span data-stu-id="9be87-350">Packet with an incorrect type or version was encountered during marshaling.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**nicht übereinstimmende WBEM \_ E \_ Marshal- \_ Version \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-351"><span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**WBEM\_E\_MARSHAL\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-352">2147749952 (0x80041040)</span><span class="sxs-lookup"><span data-stu-id="9be87-352">2147749952 (0x80041040)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-353">Das Paket weist eine nicht unterstützte Version auf.</span><span class="sxs-lookup"><span data-stu-id="9be87-353">Packet has an unsupported version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM \_ E \_ Mars Hall \_ ungültige \_ Signatur**</span><span class="sxs-lookup"><span data-stu-id="9be87-354"><span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**WBEM\_E\_MARSHAL\_INVALID\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-355">2147749953 (0x80041041)</span><span class="sxs-lookup"><span data-stu-id="9be87-355">2147749953 (0x80041041)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-356">Das Paket ist anscheinend beschädigt.</span><span class="sxs-lookup"><span data-stu-id="9be87-356">Packet appears to be corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**Ungültiger WBEM- \_ \_ \_ Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="9be87-357"><span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**WBEM\_E\_INVALID\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-358">2147749954 (0x80041042)</span><span class="sxs-lookup"><span data-stu-id="9be87-358">2147749954 (0x80041042)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-359">Es wurde versucht, Qualifizierer zu stimmen, wie z. b. das Einfügen \[ \] von Schlüsseln für ein Objekt anstelle einer Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9be87-359">Attempt was made to mismatch qualifiers, such as putting \[key\] on an object instead of a property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM \_ E mit \_ ungültigem \_ doppelten \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="9be87-360"><span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**WBEM\_E\_INVALID\_DUPLICATE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-361">2147749955 (0x80041043)</span><span class="sxs-lookup"><span data-stu-id="9be87-361">2147749955 (0x80041043)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-362">Ein doppelter Parameter wurde in einer CIM-Methode deklariert.</span><span class="sxs-lookup"><span data-stu-id="9be87-362">Duplicate parameter was declared in a CIM method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ zu \_ viele \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="9be87-363"><span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM\_E\_TOO\_MUCH\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-364">2147749956 (0x80041044)</span><span class="sxs-lookup"><span data-stu-id="9be87-364">2147749956 (0x80041044)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-365">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9be87-365">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM \_ E- \_ Server ist \_ \_ ausgelastet.**</span><span class="sxs-lookup"><span data-stu-id="9be87-366"><span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**WBEM\_E\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-367">2147749957 (0x80041045)</span><span class="sxs-lookup"><span data-stu-id="9be87-367">2147749957 (0x80041045)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-368">Beim Aufrufen von [**iwbemubjectsink:: Hinweis**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="9be87-368">Call to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) has failed.</span></span> <span data-ttu-id="9be87-369">Der Anbieter kann das Ereignis erneut auslösen.</span><span class="sxs-lookup"><span data-stu-id="9be87-369">The provider can refire the event.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM \_ E ist \_ ungültig. \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-370"><span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**WBEM\_E\_INVALID\_FLAVOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-371">2147749958 (0x80041046)</span><span class="sxs-lookup"><span data-stu-id="9be87-371">2147749958 (0x80041046)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-372">Die angegebene qualifiziererkonfiguration war ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-372">Specified qualifier flavor was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM \_ E \_ Zirkel \_ Verweis**</span><span class="sxs-lookup"><span data-stu-id="9be87-373"><span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**WBEM\_E\_CIRCULAR\_REFERENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-374">2147749959 (0x80041047)</span><span class="sxs-lookup"><span data-stu-id="9be87-374">2147749959 (0x80041047)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-375">Es wurde versucht, einen Zirkel Verweis (z. b. eine Klasse von sich selbst abzuleiten) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9be87-375">Attempt was made to create a reference that is circular (for example, deriving a class from itself).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM \_ E \_ nicht unterstütztes \_ Klassen \_ Update**</span><span class="sxs-lookup"><span data-stu-id="9be87-376"><span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**WBEM\_E\_UNSUPPORTED\_CLASS\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-377">2147749960 (0x80041048)</span><span class="sxs-lookup"><span data-stu-id="9be87-377">2147749960 (0x80041048)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-378">Die angegebene Klasse wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-378">Specified class is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ kann \_ die \_ Schlüssel \_ Vererbung nicht ändern**</span><span class="sxs-lookup"><span data-stu-id="9be87-379"><span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_KEY\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-380">2147749961 (0x80041049)</span><span class="sxs-lookup"><span data-stu-id="9be87-380">2147749961 (0x80041049)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-381">Es wurde versucht, einen Schlüssel zu ändern, wenn der Schlüssel bereits von Instanzen oder Unterklassen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9be87-381">Attempt was made to change a key when instances or subclasses are already using the key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ kann \_ die \_ Index \_ Vererbung nicht ändern**</span><span class="sxs-lookup"><span data-stu-id="9be87-382"><span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM\_E\_CANNOT\_CHANGE\_INDEX\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-383">2147749968 (0x80041050)</span><span class="sxs-lookup"><span data-stu-id="9be87-383">2147749968 (0x80041050)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-384">Es wurde versucht, einen Index zu ändern, wenn bereits Instanzen oder Unterklassen den Index verwenden.</span><span class="sxs-lookup"><span data-stu-id="9be87-384">An attempt was made to change an index when instances or subclasses are already using the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ zu \_ viele \_ Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="9be87-385"><span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM\_E\_TOO\_MANY\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-386">2147749969 (0x80041051)</span><span class="sxs-lookup"><span data-stu-id="9be87-386">2147749969 (0x80041051)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-387">Es wurde versucht, mehr Eigenschaften zu erstellen, als von der aktuellen Version der Klasse unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-387">Attempt was made to create more properties than the current version of the class supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM \_ E \_ - \_ Updatetyp \_ stimmen nicht überein.**</span><span class="sxs-lookup"><span data-stu-id="9be87-388"><span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**WBEM\_E\_UPDATE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-389">2147749970 (0x80041052)</span><span class="sxs-lookup"><span data-stu-id="9be87-389">2147749970 (0x80041052)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-390">Die Eigenschaft wurde mit einem in Konflikt stehenden Typ in einer abgeleiteten Klasse neu definiert.</span><span class="sxs-lookup"><span data-stu-id="9be87-390">Property was redefined with a conflicting type in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**außer Kraft Setzung von WBEM \_ E- \_ Updates \_ \_ nicht \_ zulässig**</span><span class="sxs-lookup"><span data-stu-id="9be87-391"><span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**WBEM\_E\_UPDATE\_OVERRIDE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-392">2147749971 (0x80041053)</span><span class="sxs-lookup"><span data-stu-id="9be87-392">2147749971 (0x80041053)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-393">Es wurde versucht, in einer abgeleiteten Klasse einen Qualifizierer zu überschreiben, der nicht überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="9be87-393">Attempt was made in a derived class to override a qualifier that cannot be overridden.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_propagierte WBEM E- \_ Update \_ \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="9be87-394"><span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**WBEM\_E\_UPDATE\_PROPAGATED\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-395">2147749972 (0x80041054)</span><span class="sxs-lookup"><span data-stu-id="9be87-395">2147749972 (0x80041054)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-396">Die Methode wurde mit einer in Konflikt stehenden Signatur in einer abgeleiteten Klasse neu deklariert.</span><span class="sxs-lookup"><span data-stu-id="9be87-396">Method was re-declared with a conflicting signature in a derived class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM \_ E- \_ Methode \_ nicht \_ implementiert**</span><span class="sxs-lookup"><span data-stu-id="9be87-397"><span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**WBEM\_E\_METHOD\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-398">2147749973 (0x80041055)</span><span class="sxs-lookup"><span data-stu-id="9be87-398">2147749973 (0x80041055)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-399">Es wurde versucht, eine Methode auszuführen, die nicht \[ mit \] in einer relevanten Klasse implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9be87-399">Attempt was made to execute a method not marked with \[implemented\] in any relevant class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM \_ E- \_ Methode \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="9be87-400"><span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd> <dl> <span data-ttu-id="9be87-401"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="9be87-401"><dt>


</dt> <dt></span></span>



<span data-ttu-id="9be87-402">Es wurde versucht, eine mit "deaktiviert" markierte Methode auszuführen \[ \] .</span><span class="sxs-lookup"><span data-stu-id="9be87-402">Attempt was made to execute a method marked with \[disabled\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM \_ E- \_ Auffrischung \_ ausgelastet**</span><span class="sxs-lookup"><span data-stu-id="9be87-403"><span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**WBEM\_E\_REFRESHER\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-404">2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="9be87-404">2147749975 (0x80041057)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-405">Das Aktualisierungs Programm ist mit einem anderen Vorgang ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="9be87-405">Refresher is busy with another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**nicht-alisier Bare WBEM- \_ \_ \_ Abfrage**</span><span class="sxs-lookup"><span data-stu-id="9be87-406"><span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**WBEM\_E\_UNPARSABLE\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-407">2147749976 (0x80041058)</span><span class="sxs-lookup"><span data-stu-id="9be87-407">2147749976 (0x80041058)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-408">Die Filter Abfrage ist syntaktisch ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-408">Filtering query is syntactically not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ Not ( \_ Ereignis \_ Klasse)**</span><span class="sxs-lookup"><span data-stu-id="9be87-409"><span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM\_E\_NOT\_EVENT\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-410">2147749977 (0x80041059)</span><span class="sxs-lookup"><span data-stu-id="9be87-410">2147749977 (0x80041059)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-411">Die from-Klausel einer Filter Abfrage verweist auf eine Klasse, die keine Ereignisklasse ist (nicht vom [**\_ \_ Ereignis**](--event.md)abgeleitet).</span><span class="sxs-lookup"><span data-stu-id="9be87-411">The FROM clause of a filtering query references a class that is not an event class (not derived from [**\_\_Event**](--event.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM \_ E \_ fehlt \_ Gruppe \_ in**</span><span class="sxs-lookup"><span data-stu-id="9be87-412"><span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**WBEM\_E\_MISSING\_GROUP\_WITHIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-413">2147749978 (0x8004105a)</span><span class="sxs-lookup"><span data-stu-id="9be87-413">2147749978 (0x8004105A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-414">Eine GROUP BY-Klausel wurde ohne die entsprechende GROUP WITHIN-Klausel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9be87-414">A GROUP BY clause was used without the corresponding GROUP WITHIN clause.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM \_ E \_ fehlende \_ Aggregations \_ Liste**</span><span class="sxs-lookup"><span data-stu-id="9be87-415"><span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**WBEM\_E\_MISSING\_AGGREGATION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-416">2147749979 (0x8004105b)</span><span class="sxs-lookup"><span data-stu-id="9be87-416">2147749979 (0x8004105B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-417">Es wurde eine GROUP BY-Klausel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9be87-417">A GROUP BY clause was used.</span></span> <span data-ttu-id="9be87-418">Die Aggregation für alle Eigenschaften wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-418">Aggregation on all properties is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM \_ E \_ - \_ Eigenschaft \_ kein \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="9be87-419"><span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**WBEM\_E\_PROPERTY\_NOT\_AN\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-420">2147749980 (0x8004105c)</span><span class="sxs-lookup"><span data-stu-id="9be87-420">2147749980 (0x8004105C)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-421">Für eine Eigenschaft, die kein eingebettetes Objekt ist, wurde Punktnotation verwendet.</span><span class="sxs-lookup"><span data-stu-id="9be87-421">Dot notation was used on a property that is not an embedded object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM \_ E \_ Aggregations \_ nach \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="9be87-422"><span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**WBEM\_E\_AGGREGATING\_BY\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-423">2147749981 (0x8004105d)</span><span class="sxs-lookup"><span data-stu-id="9be87-423">2147749981 (0x8004105D)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-424">Eine GROUP BY-Klausel verweist auf eine Eigenschaft, bei der es sich um ein eingebettetes Objekt ohne Verwendung der Punktnotation handelt.</span><span class="sxs-lookup"><span data-stu-id="9be87-424">A GROUP BY clause references a property that is an embedded object without using dot notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**Abfrage des \_ \_ nicht interpretierbaren WBEM E- \_ Anbieters \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-425"><span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**WBEM\_E\_UNINTERPRETABLE\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-426">2147749983 (0x8004105f)</span><span class="sxs-lookup"><span data-stu-id="9be87-426">2147749983 (0x8004105F)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-427">Die Ereignis Anbieter-Registrierungs Abfrage ([**\_ \_ eventproviderregistration**](--eventproviderregistration.md)) hat nicht die Klassen angegeben, für die Ereignisse bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9be87-427">Event provider registration query ([**\_\_EventProviderRegistration**](--eventproviderregistration.md)) did not specify the classes for which events were provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM \_ E \_ Backup \_ Restore \_ WinMgmt wird \_ ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="9be87-428"><span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**WBEM\_E\_BACKUP\_RESTORE\_WINMGMT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-429">2147749984 (0x80041060)</span><span class="sxs-lookup"><span data-stu-id="9be87-429">2147749984 (0x80041060)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-430">Es wurde angefordert, das Repository zu sichern oder wiederherzustellen, während es von WinMgmt.exe oder vom Svchost-Prozess verwendet wurde, der den WMI-Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="9be87-430">Request was made to back up or restore the repository while it was in use by WinMgmt.exe, or by the SVCHOST process that contains the WMI service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**Überlauf der WBEM \_ E- \_ Warteschlange \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-431"><span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**WBEM\_E\_QUEUE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-432">2147749985 (0x80041061)</span><span class="sxs-lookup"><span data-stu-id="9be87-432">2147749985 (0x80041061)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-433">Überlauf der asynchronen Übermittlungs Warteschlange von dem Ereignisconsumer zu langsam.</span><span class="sxs-lookup"><span data-stu-id="9be87-433">Asynchronous delivery queue overflowed from the event consumer being too slow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM \_ E- \_ Berechtigung \_ nicht \_ aufrechterhalten**</span><span class="sxs-lookup"><span data-stu-id="9be87-434"><span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**WBEM\_E\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-435">2147749986 (0x80041062)</span><span class="sxs-lookup"><span data-stu-id="9be87-435">2147749986 (0x80041062)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-436">Der Vorgang konnte nicht ausgeführt werden, da der Client nicht über die erforderlichen Sicherheits Berechtigungen verfügte.</span><span class="sxs-lookup"><span data-stu-id="9be87-436">Operation failed because the client did not have the necessary security privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**\_Ungültiger WBEM E- \_ \_ Operator**</span><span class="sxs-lookup"><span data-stu-id="9be87-437"><span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM\_E\_INVALID\_OPERATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-438">2147749987 (0x80041063)</span><span class="sxs-lookup"><span data-stu-id="9be87-438">2147749987 (0x80041063)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-439">Der Operator ist für diesen Eigenschaftentyp ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-439">Operator is not valid for this property type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**lokale WBEM \_ E- \_ \_ Anmelde Informationen**</span><span class="sxs-lookup"><span data-stu-id="9be87-440"><span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**WBEM\_E\_LOCAL\_CREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-441">2147749988 (0x80041064)</span><span class="sxs-lookup"><span data-stu-id="9be87-441">2147749988 (0x80041064)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-442">Der Benutzer hat einen Benutzernamen/ein Kennwort/eine Autorität für eine lokale Verbindung angegeben.</span><span class="sxs-lookup"><span data-stu-id="9be87-442">User specified a username/password/authority on a local connection.</span></span> <span data-ttu-id="9be87-443">Der Benutzer muss einen leeren Benutzernamen/ein leeres Kennwort verwenden und auf die Standard Sicherheit zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="9be87-443">The user must use a blank username/password and rely on default security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ darf \_ nicht \_ abstrakt sein.**</span><span class="sxs-lookup"><span data-stu-id="9be87-444"><span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM\_E\_CANNOT\_BE\_ABSTRACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-445">2147749989 (0x80041065)</span><span class="sxs-lookup"><span data-stu-id="9be87-445">2147749989 (0x80041065)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-446">Die Klasse wurde als abstrakt erstellt, wenn die übergeordnete Klasse nicht abstrakt ist.</span><span class="sxs-lookup"><span data-stu-id="9be87-446">Class was made abstract when its parent class is not abstract.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E- \_ geändertes \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="9be87-447"><span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM\_E\_AMENDED\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-448">2147749990 (0x80041066)</span><span class="sxs-lookup"><span data-stu-id="9be87-448">2147749990 (0x80041066)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-449">Das geänderte Objekt wurde geschrieben, ohne dass das **WBEM- \_ Flag ein \_ \_ geändertes \_ qualifizierungsflag verwendet** .</span><span class="sxs-lookup"><span data-stu-id="9be87-449">Amended object was written without the **WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS** flag being specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM \_ E- \_ Client \_ zu \_ langsam**</span><span class="sxs-lookup"><span data-stu-id="9be87-450"><span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**WBEM\_E\_CLIENT\_TOO\_SLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-451">2147749991 (0x80041067)</span><span class="sxs-lookup"><span data-stu-id="9be87-451">2147749991 (0x80041067)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-452">Der Client hat Objekte nicht schnell genug aus einer Enumeration abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9be87-452">Client did not retrieve objects quickly enough from an enumeration.</span></span> <span data-ttu-id="9be87-453">Diese Konstante wird zurückgegeben, wenn ein Client ein Enumerationsobjekt erstellt, aber nicht rechtzeitig Objekte aus dem Enumerator abruft, was dazu führt, dass die Objekt Caches des Enumerators gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-453">This constant is returned when a client creates an enumeration object, but does not retrieve objects from the enumerator in a timely fashion, causing the enumerator's object caches to back up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM \_ E \_ NULL- \_ Sicherheits \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9be87-454"><span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**WBEM\_E\_NULL\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-455">2147749992 (0x80041068)</span><span class="sxs-lookup"><span data-stu-id="9be87-455">2147749992 (0x80041068)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-456">NULL-Sicherheits Beschreibung wurde verwendet.</span><span class="sxs-lookup"><span data-stu-id="9be87-456">Null security descriptor was used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**Timeout bei WBEM \_ E. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-457"><span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**WBEM\_E\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-458">2147749993 (0x80041069)</span><span class="sxs-lookup"><span data-stu-id="9be87-458">2147749993 (0x80041069)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-459">Timeout beim Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9be87-459">Operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM \_ E \_ ungültige Zuordnung \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-460"><span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**WBEM\_E\_INVALID\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-461">2147749994</span><span class="sxs-lookup"><span data-stu-id="9be87-461">2147749994</span></span>
</dt> <dt>



<span data-ttu-id="9be87-462">Die Zuordnung ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-462">Association is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**mehrdeutiger WBEM- \_ \_ \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="9be87-463"><span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**WBEM\_E\_AMBIGUOUS\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-464">2147749995 (0x8004106b)</span><span class="sxs-lookup"><span data-stu-id="9be87-464">2147749995 (0x8004106B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-465">Der Vorgang war mehrdeutig.</span><span class="sxs-lookup"><span data-stu-id="9be87-465">Operation was ambiguous.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_ \_ Kontingent Verletzung für WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-466"><span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**WBEM\_E\_QUOTA\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-467">2147749996 (0x8004106c)</span><span class="sxs-lookup"><span data-stu-id="9be87-467">2147749996 (0x8004106C)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-468">WMI nimmt zu viel Arbeitsspeicher in Anspruch.</span><span class="sxs-lookup"><span data-stu-id="9be87-468">WMI is taking up too much memory.</span></span> <span data-ttu-id="9be87-469">Dies kann auf eine geringe Speicherverfügbarkeit oder eine übermäßige Arbeitsspeicher Auslastung durch WMI zurückzuführen sein.</span><span class="sxs-lookup"><span data-stu-id="9be87-469">This can be caused by low memory availability or excessive memory consumption by WMI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM \_ E- \_ Transaktions \_ Konflikt**</span><span class="sxs-lookup"><span data-stu-id="9be87-470"><span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**WBEM\_E\_TRANSACTION\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-471">2147749997 (0x8004106d)</span><span class="sxs-lookup"><span data-stu-id="9be87-471">2147749997 (0x8004106D)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-472">Der Vorgang führte zu einem Transaktions Konflikt.</span><span class="sxs-lookup"><span data-stu-id="9be87-472">Operation resulted in a transaction conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**\_ \_ erzwungenes Rollback für WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-473"><span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**WBEM\_E\_FORCED\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-474">2147749998 (0x8004106e)</span><span class="sxs-lookup"><span data-stu-id="9be87-474">2147749998 (0x8004106E)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-475">Die Transaktion hat ein Rollback erzwungen.</span><span class="sxs-lookup"><span data-stu-id="9be87-475">Transaction forced a rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**von WBEM \_ E \_ nicht unterstütztes Gebiets Schema \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-476"><span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**WBEM\_E\_UNSUPPORTED\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-477">2147749999 (0x8004106f)</span><span class="sxs-lookup"><span data-stu-id="9be87-477">2147749999 (0x8004106F)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-478">Das im-Befehl verwendete Gebiets Schema wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-478">Locale used in the call is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM \_ E- \_ handle ist \_ \_ \_ veraltet.**</span><span class="sxs-lookup"><span data-stu-id="9be87-479"><span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**WBEM\_E\_HANDLE\_OUT\_OF\_DATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-480">2147750000 (0x80041070)</span><span class="sxs-lookup"><span data-stu-id="9be87-480">2147750000 (0x80041070)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-481">Objekt Handle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="9be87-481">Object handle is out-of-date.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM \_ E- \_ Verbindung \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="9be87-482"><span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**WBEM\_E\_CONNECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-483">2147750001 (0x80041071)</span><span class="sxs-lookup"><span data-stu-id="9be87-483">2147750001 (0x80041071)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-484">Fehler beim Herstellen einer Verbindung mit der SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9be87-484">Connection to the SQL database failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM \_ E \_ ungültige \_ handle- \_ Anforderung**</span><span class="sxs-lookup"><span data-stu-id="9be87-485"><span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**WBEM\_E\_INVALID\_HANDLE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-486">2147750002 (0x80041072)</span><span class="sxs-lookup"><span data-stu-id="9be87-486">2147750002 (0x80041072)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-487">Die Handle-Anforderung war ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-487">Handle request was not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**der \_ Eigenschafts Name für WBEM E ist \_ \_ \_ zu \_ breit.**</span><span class="sxs-lookup"><span data-stu-id="9be87-488"><span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**WBEM\_E\_PROPERTY\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-489">2147750003 (0x80041073)</span><span class="sxs-lookup"><span data-stu-id="9be87-489">2147750003 (0x80041073)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-490">Der Eigenschaftsname enthält mehr als 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9be87-490">Property name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM \_ E- \_ Klassen \_ Name \_ zu \_ breit**</span><span class="sxs-lookup"><span data-stu-id="9be87-491"><span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**WBEM\_E\_CLASS\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-492">2147750004 (0x80041074)</span><span class="sxs-lookup"><span data-stu-id="9be87-492">2147750004 (0x80041074)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-493">Der Klassenname enthält mehr als 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9be87-493">Class name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**der WBEM \_ E- \_ Methoden \_ Name ist \_ zu \_ breit.**</span><span class="sxs-lookup"><span data-stu-id="9be87-494"><span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**WBEM\_E\_METHOD\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-495">2147750005 (0x80041075)</span><span class="sxs-lookup"><span data-stu-id="9be87-495">2147750005 (0x80041075)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-496">Der Methodenname enthält mehr als 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9be87-496">Method name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM \_ E \_ - \_ qualifizierername \_ zu \_ breit**</span><span class="sxs-lookup"><span data-stu-id="9be87-497"><span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**WBEM\_E\_QUALIFIER\_NAME\_TOO\_WIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-498">2147750006 (0x80041076)</span><span class="sxs-lookup"><span data-stu-id="9be87-498">2147750006 (0x80041076)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-499">Der qualifizierername enthält mehr als 255 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9be87-499">Qualifier name contains more than 255 characters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**Befehl "WBEM \_ E \_ erneut ausführen" \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-500"><span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**WBEM\_E\_RERUN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-501">2147750007 (0x80041077)</span><span class="sxs-lookup"><span data-stu-id="9be87-501">2147750007 (0x80041077)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-502">Der SQL-Befehl muss erneut ausgeführt werden, da in SQL ein Deadlock auftritt.</span><span class="sxs-lookup"><span data-stu-id="9be87-502">The SQL command must be rerun because there is a deadlock in SQL.</span></span> <span data-ttu-id="9be87-503">Dies kann nur zurückgegeben werden, wenn Daten in einer SQL-Datenbank gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-503">This can be returned only when data is being stored in an SQL database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM \_ E- \_ Daten Bank Konflikt nicht \_ \_ übereinstimmen**</span><span class="sxs-lookup"><span data-stu-id="9be87-504"><span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**WBEM\_E\_DATABASE\_VER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-505">2147750008 (0x80041078)</span><span class="sxs-lookup"><span data-stu-id="9be87-505">2147750008 (0x80041078)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-506">Die Datenbankversion entspricht nicht der Version, die der Repository-Treiber verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9be87-506">The database version does not match the version that the repository driver processes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E- \_ Veto \_ Löschen**</span><span class="sxs-lookup"><span data-stu-id="9be87-507"><span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM\_E\_VETO\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-508">2147750009 (0x80041079)</span><span class="sxs-lookup"><span data-stu-id="9be87-508">2147750009 (0x80041079)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-509">Der Löschvorgang kann von WMI nicht ausgeführt werden, da der Anbieter den Löschvorgang nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="9be87-509">WMI cannot execute the delete operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E- \_ Veto \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-510"><span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM\_E\_VETO\_PUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-511">2147750010 (0x8004107a)</span><span class="sxs-lookup"><span data-stu-id="9be87-511">2147750010 (0x8004107A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-512">Der Put-Vorgang kann von WMI nicht ausgeführt werden, da der Anbieter ihn nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="9be87-512">WMI cannot execute the put operation because the provider does not allow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM \_ E, \_ Ungültiges Gebiets Schema \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-513"><span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**WBEM\_E\_INVALID\_LOCALE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-514">2147750016 (0x80041080)</span><span class="sxs-lookup"><span data-stu-id="9be87-514">2147750016 (0x80041080)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-515">Der angegebene Gebiets Schema Bezeichner für den Vorgang ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-515">Specified locale identifier was not valid for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM \_ E- \_ Anbieter angeh \_ alten**</span><span class="sxs-lookup"><span data-stu-id="9be87-516"><span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**WBEM\_E\_PROVIDER\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-517">2147750017 (0x80041081)</span><span class="sxs-lookup"><span data-stu-id="9be87-517">2147750017 (0x80041081)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-518">Der Anbieter wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="9be87-518">Provider is suspended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM \_ E- \_ Synchronisierung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9be87-519"><span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**WBEM\_E\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-520">2147750018 (0x80041082)</span><span class="sxs-lookup"><span data-stu-id="9be87-520">2147750018 (0x80041082)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-521">Das Objekt muss in das WMI-Repository geschrieben und erneut abgerufen werden, bevor der angeforderte Vorgang erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9be87-521">Object must be written to the WMI repository and retrieved again before the requested operation can succeed.</span></span> <span data-ttu-id="9be87-522">Diese Konstante wird zurückgegeben, wenn ein Objekt committet und abgerufen werden muss, um den Eigenschafts Wert anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9be87-522">This constant is returned when an object must be committed and retrieved to see the property value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM \_ E \_ kein \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="9be87-523"><span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**WBEM\_E\_NO\_SCHEMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-524">2147750019 (0x80041083)</span><span class="sxs-lookup"><span data-stu-id="9be87-524">2147750019 (0x80041083)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-525">Der Vorgang kann nicht abgeschlossen werden. Es ist kein Schema verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9be87-525">Operation cannot be completed; no schema is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**der WBEM \_ E- \_ Anbieter wurde \_ bereits \_ registriert.**</span><span class="sxs-lookup"><span data-stu-id="9be87-526"><span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**WBEM\_E\_PROVIDER\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-527">02147750020 (0x119f D010)</span><span class="sxs-lookup"><span data-stu-id="9be87-527">02147750020 (0x119FD010)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-528">Der Anbieter kann nicht registriert werden, da er bereits registriert ist.</span><span class="sxs-lookup"><span data-stu-id="9be87-528">Provider cannot be registered because it is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM \_ E- \_ Anbieter \_ nicht \_ registriert**</span><span class="sxs-lookup"><span data-stu-id="9be87-529"><span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**WBEM\_E\_PROVIDER\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-530">2147750021 (0x80041085)</span><span class="sxs-lookup"><span data-stu-id="9be87-530">2147750021 (0x80041085)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-531">Der Anbieter wurde nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="9be87-531">Provider was not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM E schwerwiegender \_ \_ \_ Transport \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="9be87-532"><span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**WBEM\_E\_FATAL\_TRANSPORT\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-533">2147750022 (0x80041086)</span><span class="sxs-lookup"><span data-stu-id="9be87-533">2147750022 (0x80041086)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-534">Schwerwiegender Transport Fehler.</span><span class="sxs-lookup"><span data-stu-id="9be87-534">A fatal transport error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM \_ E- \_ verschlüsselte \_ Verbindung \_ erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9be87-535"><span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-536">2147750023 (0x80041087)</span><span class="sxs-lookup"><span data-stu-id="9be87-536">2147750023 (0x80041087)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-537">Der Benutzer hat versucht, einen Computernamen oder eine Domäne ohne verschlüsselte Verbindung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9be87-537">User attempted to set a computer name or domain without an encrypted connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**Timeout des WBEM \_ E- \_ Anbieters \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-538"><span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**WBEM\_E\_PROVIDER\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-539">2147750024 (0x80041088)</span><span class="sxs-lookup"><span data-stu-id="9be87-539">2147750024 (0x80041088)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-540">Ein Anbieter konnte die Ergebnisse innerhalb des angegebenen Timeouts nicht melden.</span><span class="sxs-lookup"><span data-stu-id="9be87-540">A provider failed to report results within the specified timeout.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM \_ E \_ kein \_ Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="9be87-541"><span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**WBEM\_E\_NO\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-542">2147750025 (0x80041089)</span><span class="sxs-lookup"><span data-stu-id="9be87-542">2147750025 (0x80041089)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-543">Der Benutzer hat versucht, eine Instanz ohne definierten Schlüssel zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="9be87-543">User attempted to put an instance with no defined key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM \_ E- \_ Anbieter \_ deaktiviert**</span><span class="sxs-lookup"><span data-stu-id="9be87-544"><span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**WBEM\_E\_PROVIDER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-545">2147750026 (0x8004108a)</span><span class="sxs-lookup"><span data-stu-id="9be87-545">2147750026 (0x8004108A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-546">Der Benutzer hat versucht, eine Anbieter Instanz zu registrieren, aber der com-Server für die Anbieter Instanz wurde entladen.</span><span class="sxs-lookup"><span data-stu-id="9be87-546">User attempted to register a provider instance but the COM server for the provider instance was unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**wbechaos \_ E- \_ Registrierung \_ zu \_ breit**</span><span class="sxs-lookup"><span data-stu-id="9be87-547"><span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-548">2147753985 (0x80042001)</span><span class="sxs-lookup"><span data-stu-id="9be87-548">2147753985 (0x80042001)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-549">Die Anbieter Registrierung überschneidet sich mit der System Ereignis Domäne.</span><span class="sxs-lookup"><span data-stu-id="9be87-549">Provider registration overlaps with the system event domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**wbechaos \_ E \_ \_ zu \_ präzise Registrierung**</span><span class="sxs-lookup"><span data-stu-id="9be87-550"><span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**WBEMESS\_E\_REGISTRATION\_TOO\_PRECISE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-551">2147753986 (0x80042002)</span><span class="sxs-lookup"><span data-stu-id="9be87-551">2147753986 (0x80042002)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-552">In dieser Abfrage wurde keine WITHIN-Klausel verwendet.</span><span class="sxs-lookup"><span data-stu-id="9be87-552">A WITHIN clause was not used in this query.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**wbechaos \_ E \_ Authz \_ nicht \_ privilegiert**</span><span class="sxs-lookup"><span data-stu-id="9be87-553"><span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS\_E\_AUTHZ\_NOT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-554">2147753987 (0x80042003)</span><span class="sxs-lookup"><span data-stu-id="9be87-554">2147753987 (0x80042003)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-555">Dieser Computer verfügt nicht über die erforderlichen Domänen Berechtigungen, um die Sicherheitsfunktionen zu unterstützen, die sich auf die erstellte Abonnement Instanz beziehen.</span><span class="sxs-lookup"><span data-stu-id="9be87-555">This computer does not have the necessary domain permissions to support the security functions that relate to the created subscription instance.</span></span> <span data-ttu-id="9be87-556">Wenden Sie sich an den Domänen Administrator, um diesen Computer der Windows-Autorisierungs Zugriffs Gruppe hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9be87-556">Contact the Domain Administrator to get this computer added to the Windows Authorization Access Group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ E-Wiederholungs \_ Versuch \_ später**</span><span class="sxs-lookup"><span data-stu-id="9be87-557"><span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM\_E\_RETRY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-558">2147758081 (0x80043001)</span><span class="sxs-lookup"><span data-stu-id="9be87-558">2147758081 (0x80043001)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-559">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9be87-559">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM \_ E- \_ Ressourcen Konflikt \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-560"><span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**WBEM\_E\_RESOURCE\_CONTENTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-561">2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="9be87-561">2147758082 (0x80043002)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-562">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="9be87-562">Reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**wbemmof \_ E \_ - \_ qualifizierername erwartet \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-563"><span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF\_E\_EXPECTED\_QUALIFIER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-564">2147762177 (0x80044001)</span><span class="sxs-lookup"><span data-stu-id="9be87-564">2147762177 (0x80044001)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-565">Ein qualifizierername wurde erwartet.</span><span class="sxs-lookup"><span data-stu-id="9be87-565">Expected a qualifier name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**wbemmof \_ E \_ erwartet \_ Semi**</span><span class="sxs-lookup"><span data-stu-id="9be87-566"><span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF\_E\_EXPECTED\_SEMI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-567">2147762178 (0x80044002)</span><span class="sxs-lookup"><span data-stu-id="9be87-567">2147762178 (0x80044002)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-568">Semikolon oder "=" erwartet.</span><span class="sxs-lookup"><span data-stu-id="9be87-568">Expected semicolon or '='.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**wbemmof \_ E \_ erwartete \_ öffnende geschweifter \_ Klammer**</span><span class="sxs-lookup"><span data-stu-id="9be87-569"><span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-570">2147762179 (0x80044003)</span><span class="sxs-lookup"><span data-stu-id="9be87-570">2147762179 (0x80044003)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-571">Es wurde eine öffnende geschweiften Klammer erwartet.</span><span class="sxs-lookup"><span data-stu-id="9be87-571">Expected an opening brace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**wbemmof \_ E \_ erwartet schließende geschweifter \_ \_ Klammer**</span><span class="sxs-lookup"><span data-stu-id="9be87-572"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-573">2147762180 (0x80044004)</span><span class="sxs-lookup"><span data-stu-id="9be87-573">2147762180 (0x80044004)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-574">Fehlende schließende geschweifte Klammer oder ein ungültiges Array Element.</span><span class="sxs-lookup"><span data-stu-id="9be87-574">Missing closing brace or an illegal array element.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**wbemmof \_ E \_ erwartet Schließ \_ Ende \_ Klammer**</span><span class="sxs-lookup"><span data-stu-id="9be87-575"><span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_BRACKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-576">2147762181 (0x80044005)</span><span class="sxs-lookup"><span data-stu-id="9be87-576">2147762181 (0x80044005)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-577">Es wurde eine schließende Klammer erwartet.</span><span class="sxs-lookup"><span data-stu-id="9be87-577">Expected a closing bracket.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**wbemmof \_ E \_ erwartet Schließ \_ Ende \_ Parser**</span><span class="sxs-lookup"><span data-stu-id="9be87-578"><span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF\_E\_EXPECTED\_CLOSE\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-579">2147762182 (0x80044006)</span><span class="sxs-lookup"><span data-stu-id="9be87-579">2147762182 (0x80044006)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-580">Schließende Klammer erwartet.</span><span class="sxs-lookup"><span data-stu-id="9be87-580">Expected closing parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**wbemmof \_ E \_ \_ Ungültiger konstanter \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="9be87-581"><span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF\_E\_ILLEGAL\_CONSTANT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-582">2147762183 (0x80044007)</span><span class="sxs-lookup"><span data-stu-id="9be87-582">2147762183 (0x80044007)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-583">Numerischer Wert außerhalb des gültigen Bereichs oder Zeichen folgen ohne Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="9be87-583">Numeric value out of range or strings without quotes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**wbemmof \_ E \_ - \_ \_ Typbezeichner erwartet**</span><span class="sxs-lookup"><span data-stu-id="9be87-584"><span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF\_E\_EXPECTED\_TYPE\_IDENTIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-585">2147762184 (0x80044008)</span><span class="sxs-lookup"><span data-stu-id="9be87-585">2147762184 (0x80044008)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-586">Es wurde ein Typbezeichner erwartet.</span><span class="sxs-lookup"><span data-stu-id="9be87-586">Expected a type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**wbemmof \_ E \_ erwartet \_ offene \_ Parser**</span><span class="sxs-lookup"><span data-stu-id="9be87-587"><span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF\_E\_EXPECTED\_OPEN\_PAREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-588">2147762185 (0x80044009)</span><span class="sxs-lookup"><span data-stu-id="9be87-588">2147762185 (0x80044009)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-589">Es wurde eine öffnende Klammer erwartet.</span><span class="sxs-lookup"><span data-stu-id="9be87-589">Expected an open parenthesis.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**wbemmof \_ E \_ unbekanntes \_ Token**</span><span class="sxs-lookup"><span data-stu-id="9be87-590"><span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-591">2147762186 (0x8004400a)</span><span class="sxs-lookup"><span data-stu-id="9be87-591">2147762186 (0x8004400A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-592">Unerwartetes Token in der Datei.</span><span class="sxs-lookup"><span data-stu-id="9be87-592">Unexpected token in the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**wbemmof \_ E \_ unbekannter \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="9be87-593"><span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF\_E\_UNRECOGNIZED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-594">2147762187 (0x8004400b)</span><span class="sxs-lookup"><span data-stu-id="9be87-594">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-595">Unbekannter oder nicht unterstützter Typbezeichner.</span><span class="sxs-lookup"><span data-stu-id="9be87-595">Unrecognized or unsupported type identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**wbemmof \_ E \_ - \_ Eigenschafts \_ Name erwartet**</span><span class="sxs-lookup"><span data-stu-id="9be87-596"><span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF\_E\_EXPECTED\_PROPERTY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-597">2147762187 (0x8004400b)</span><span class="sxs-lookup"><span data-stu-id="9be87-597">2147762187 (0x8004400B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-598">Der Eigenschafts-oder Methodenname wurde erwartet.</span><span class="sxs-lookup"><span data-stu-id="9be87-598">Expected property or method name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**wbemmof \_ E \_ typedef \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="9be87-599"><span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF\_E\_TYPEDEF\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-600">2147762189 (0x8004400d)</span><span class="sxs-lookup"><span data-stu-id="9be87-600">2147762189 (0x8004400D)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-601">Typedefs und enumerierte Typen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-601">Typedefs and enumerated types are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**wbemmof \_ E \_ unerwarteter \_ Alias**</span><span class="sxs-lookup"><span data-stu-id="9be87-602"><span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF\_E\_UNEXPECTED\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-603">2147762190 (0x8004400e)</span><span class="sxs-lookup"><span data-stu-id="9be87-603">2147762190 (0x8004400E)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-604">Nur ein Verweis auf ein Klassenobjekt kann einen Alias Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9be87-604">Only a reference to a class object can have an alias value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**wbemmof \_ E \_ unerwartete \_ array- \_ Init**</span><span class="sxs-lookup"><span data-stu-id="9be87-605"><span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF\_E\_UNEXPECTED\_ARRAY\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-606">2147762191 (0x8004400f)</span><span class="sxs-lookup"><span data-stu-id="9be87-606">2147762191 (0x8004400F)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-607">Unerwartete Array Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="9be87-607">Unexpected array initialization.</span></span> <span data-ttu-id="9be87-608">Arrays müssen mit deklariert werden \[ \] .</span><span class="sxs-lookup"><span data-stu-id="9be87-608">Arrays must be declared with \[\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**wbemmof \_ E \_ ungültige \_ Zusatz \_ Syntax**</span><span class="sxs-lookup"><span data-stu-id="9be87-609"><span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF\_E\_INVALID\_AMENDMENT\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-610">2147762192 (0x80044010)</span><span class="sxs-lookup"><span data-stu-id="9be87-610">2147762192 (0x80044010)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-611">Die Syntax für den Namespace Pfad ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-611">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**wbemmof \_ E \_ ungültige \_ doppelte \_ Zusatz Änderung**</span><span class="sxs-lookup"><span data-stu-id="9be87-612"><span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF\_E\_INVALID\_DUPLICATE\_AMENDMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-613">2147762193 (0x80044011)</span><span class="sxs-lookup"><span data-stu-id="9be87-613">2147762193 (0x80044011)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-614">Doppelte Konvertierer für die Änderung.</span><span class="sxs-lookup"><span data-stu-id="9be87-614">Duplicate amendment specifiers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**wbemmof \_ E \_ ungültiges \_ pragma**</span><span class="sxs-lookup"><span data-stu-id="9be87-615"><span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF\_E\_INVALID\_PRAGMA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-616">2147762194 (0x80044012)</span><span class="sxs-lookup"><span data-stu-id="9be87-616">2147762194 (0x80044012)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-617">auf das [ \# pragma](pragma-namespace.md) muss ein gültiges Schlüsselwort folgen.</span><span class="sxs-lookup"><span data-stu-id="9be87-617">[\#pragma](pragma-namespace.md) must be followed by a valid keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**wbemmof \_ E \_ ungültige \_ Namespace \_ Syntax.**</span><span class="sxs-lookup"><span data-stu-id="9be87-618"><span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-619">2147762195 (0x80044013)</span><span class="sxs-lookup"><span data-stu-id="9be87-619">2147762195 (0x80044013)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-620">Die Syntax für den Namespace Pfad ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-620">Namespace path syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**wbemmof \_ E \_ erwartet \_ Klassen \_ Name**</span><span class="sxs-lookup"><span data-stu-id="9be87-621"><span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF\_E\_EXPECTED\_CLASS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-622">2147762196 (0x80044014)</span><span class="sxs-lookup"><span data-stu-id="9be87-622">2147762196 (0x80044014)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-623">Unerwartetes Zeichen im Klassennamen muss ein Bezeichner sein.</span><span class="sxs-lookup"><span data-stu-id="9be87-623">Unexpected character in class name must be an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**wbemmof \_ - \_ Typ \_ stimmt nicht überein.**</span><span class="sxs-lookup"><span data-stu-id="9be87-624"><span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**WBEMMOF\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-625">2147762197 (0x80044015)</span><span class="sxs-lookup"><span data-stu-id="9be87-625">2147762197 (0x80044015)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-626">Der angegebene Wert kann nicht in den entsprechenden Typ gebracht werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-626">The value specified cannot be made into the appropriate type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**wbemmof \_ E \_ \ \_ Alias \_ Name erwartet**</span><span class="sxs-lookup"><span data-stu-id="9be87-627"><span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF\_E\_EXPECTED\_ALIAS\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-628">2147762198 (0x80044016)</span><span class="sxs-lookup"><span data-stu-id="9be87-628">2147762198 (0x80044016)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-629">Auf das Dollar Zeichen muss ein Aliasname als Bezeichner folgen.</span><span class="sxs-lookup"><span data-stu-id="9be87-629">Dollar sign must be followed by an alias name as an identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**wbemmof \_ E \_ ungültige \_ Klassen \_ Deklaration.**</span><span class="sxs-lookup"><span data-stu-id="9be87-630"><span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF\_E\_INVALID\_CLASS\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-631">2147762199 (0x80044017)</span><span class="sxs-lookup"><span data-stu-id="9be87-631">2147762199 (0x80044017)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-632">Die Klassen Deklaration ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-632">Class declaration is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**wbemmof \_ E \_ ungültige \_ \_ Instanzdeklaration.**</span><span class="sxs-lookup"><span data-stu-id="9be87-633"><span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF\_E\_INVALID\_INSTANCE\_DECLARATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-634">2147762200 (0x80044018)</span><span class="sxs-lookup"><span data-stu-id="9be87-634">2147762200 (0x80044018)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-635">Die Instanzdeklaration ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-635">The instance declaration is not valid.</span></span> <span data-ttu-id="9be87-636">Er muss mit "Instanz von" beginnen.</span><span class="sxs-lookup"><span data-stu-id="9be87-636">It must start with "instance of"</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**wbemmof \_ E \_ erwartet \_ Dollar**</span><span class="sxs-lookup"><span data-stu-id="9be87-637"><span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF\_E\_EXPECTED\_DOLLAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-638">2147762201 (0x80044019)</span><span class="sxs-lookup"><span data-stu-id="9be87-638">2147762201 (0x80044019)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-639">Erwartetes Dollarzeichen.</span><span class="sxs-lookup"><span data-stu-id="9be87-639">Expected dollar sign.</span></span> <span data-ttu-id="9be87-640">Ein Alias in der Form "$Name" muss dem "as"-Schlüsselwort folgen.</span><span class="sxs-lookup"><span data-stu-id="9be87-640">An alias in the form "$name" must follow the "as" keyword.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**wbemmof \_ E \_ CimType- \_ Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="9be87-641"><span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**WBEMMOF\_E\_CIMTYPE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-642">2147762202 (0x8004401a)</span><span class="sxs-lookup"><span data-stu-id="9be87-642">2147762202 (0x8004401A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-643">Der Qualifizierer "CimType" kann nicht direkt in einer MOF-Datei angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-643">"CIMTYPE" qualifier cannot be specified directly in a MOF file.</span></span> <span data-ttu-id="9be87-644">Verwenden Sie die Standardtyp Notation.</span><span class="sxs-lookup"><span data-stu-id="9be87-644">Use standard type notation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**wbemmof \_ E \_ duplizierte \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="9be87-645"><span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF\_E\_DUPLICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-646">2147762203 (0x8004401b)</span><span class="sxs-lookup"><span data-stu-id="9be87-646">2147762203 (0x8004401B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-647">Es wurde ein doppelter Eigenschaftsname in der MOF-Datei gefunden.</span><span class="sxs-lookup"><span data-stu-id="9be87-647">Duplicate property name was found in the MOF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**wbemmof \_ E \_ ungültige \_ Namespace \_ Spezifikation**</span><span class="sxs-lookup"><span data-stu-id="9be87-648"><span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF\_E\_INVALID\_NAMESPACE\_SPECIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-649">2147762204 (0x8004401c)</span><span class="sxs-lookup"><span data-stu-id="9be87-649">2147762204 (0x8004401C)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-650">Die Namespace Syntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-650">Namespace syntax is not valid.</span></span> <span data-ttu-id="9be87-651">Verweise auf andere Server sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9be87-651">References to other servers are not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**wbemmof \_ E \_ außerhalb \_ des gültigen \_ Bereichs**</span><span class="sxs-lookup"><span data-stu-id="9be87-652"><span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF\_E\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-653">2147762205 (0x8004401d)</span><span class="sxs-lookup"><span data-stu-id="9be87-653">2147762205 (0x8004401D)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-654">Der Wert liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="9be87-654">Value out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**wbemmof \_ E \_ ungültige \_ Datei.**</span><span class="sxs-lookup"><span data-stu-id="9be87-655"><span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF\_E\_INVALID\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-656">2147762206 (0x8004401e)</span><span class="sxs-lookup"><span data-stu-id="9be87-656">2147762206 (0x8004401E)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-657">Die Datei ist keine gültige Text-MOF-Datei oder binäre MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="9be87-657">The file is not a valid text MOF file or binary MOF file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**wbemmof \_ E \_ Aliase \_ in \_ Embedded**</span><span class="sxs-lookup"><span data-stu-id="9be87-658"><span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**WBEMMOF\_E\_ALIASES\_IN\_EMBEDDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-659">2147762207 (0x8004401f)</span><span class="sxs-lookup"><span data-stu-id="9be87-659">2147762207 (0x8004401F)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-660">Eingebettete Objekte können keine Aliase sein.</span><span class="sxs-lookup"><span data-stu-id="9be87-660">Embedded objects cannot be aliases.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**wbemmof \_ E \_ NULL \_ array \_ Elem**</span><span class="sxs-lookup"><span data-stu-id="9be87-661"><span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF\_E\_NULL\_ARRAY\_ELEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-662">2147762208 (0x80044020)</span><span class="sxs-lookup"><span data-stu-id="9be87-662">2147762208 (0x80044020)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-663">NULL-Elemente in einem Array werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-663">NULL elements in an array are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**wbemmof \_ E- \_ doppelter \_ Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="9be87-664"><span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**WBEMMOF\_E\_DUPLICATE\_QUALIFIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-665">2147762209 (0x80044021)</span><span class="sxs-lookup"><span data-stu-id="9be87-665">2147762209 (0x80044021)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-666">Der Qualifizierer wurde für das Objekt mehrmals verwendet.</span><span class="sxs-lookup"><span data-stu-id="9be87-666">Qualifier was used more than once on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**Typ wbemmof \_ E \_ Erwarteter \_ \_ Typ**</span><span class="sxs-lookup"><span data-stu-id="9be87-667"><span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF\_E\_EXPECTED\_FLAVOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-668">2147762210 (0x80044022)</span><span class="sxs-lookup"><span data-stu-id="9be87-668">2147762210 (0x80044022)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-669">Es wurde ein Typ für die Konfiguration erwartet, z. b. " **starinstance**", " **desubclass**", " **EnableOverride**" oder </span><span class="sxs-lookup"><span data-stu-id="9be87-669">Expected a flavor type such as **ToInstance**, **ToSubClass**, **EnableOverride**, or **DisableOverride**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**wbemmof \_ E \_ inkompatible \_ Geschmacks \_ Typen**</span><span class="sxs-lookup"><span data-stu-id="9be87-670"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-671">2147762211 (0x80044023)</span><span class="sxs-lookup"><span data-stu-id="9be87-671">2147762211 (0x80044023)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-672">Das Kombinieren von **EnableOverride** und **DisableOverride** für denselben Qualifizierer ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9be87-672">Combining **EnableOverride** and **DisableOverride** on same qualifier is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**wbemmof \_ E \_ mehrere \_ Aliase**</span><span class="sxs-lookup"><span data-stu-id="9be87-673"><span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF\_E\_MULTIPLE\_ALIASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-674">2147762212 (0x80044024)</span><span class="sxs-lookup"><span data-stu-id="9be87-674">2147762212 (0x80044024)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-675">Ein Alias kann nicht zweimal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9be87-675">An alias cannot be used twice.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**Wbemmof \_ E \_ nicht \_ kompatibel \_ TYPES2**</span><span class="sxs-lookup"><span data-stu-id="9be87-676"><span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF\_E\_INCOMPATIBLE\_FLAVOR\_TYPES2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-677">2147762213 (0x80044025)</span><span class="sxs-lookup"><span data-stu-id="9be87-677">2147762213 (0x80044025)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-678">Die Kombination von " **restricted**" und " **deinstance** **" oder "** um" ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9be87-678">Combining **Restricted**, and **ToInstance** or **ToSubClass** is not legal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**wbemmof \_ E \_ keine \_ Arrays \_ zurückgegeben**</span><span class="sxs-lookup"><span data-stu-id="9be87-679"><span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF\_E\_NO\_ARRAYS\_RETURNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-680">2147762214 (0x80044026)</span><span class="sxs-lookup"><span data-stu-id="9be87-680">2147762214 (0x80044026)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-681">Methoden können keine Array Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9be87-681">Methods cannot return array values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**wbemmof \_ E \_ muss ein-oder ausgehend \_ sein \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-682"><span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF\_E\_MUST\_BE\_IN\_OR\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-683">2147762215 (0x80044027)</span><span class="sxs-lookup"><span data-stu-id="9be87-683">2147762215 (0x80044027)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-684">Argumente müssen einen **in** -oder **out** -Qualifizierer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9be87-684">Arguments must have an **In** or **Out** qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**wbemmof \_ E \_ ungültige \_ Flags- \_ Syntax.**</span><span class="sxs-lookup"><span data-stu-id="9be87-685"><span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF\_E\_INVALID\_FLAGS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-686">2147762216 (0x80044028)</span><span class="sxs-lookup"><span data-stu-id="9be87-686">2147762216 (0x80044028)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-687">Die Flags-Syntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-687">Flags syntax is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**wbemmof \_ E \_ - \_ Klammer \_ oder \_ \_ fehlerhafter Typ erwartet**</span><span class="sxs-lookup"><span data-stu-id="9be87-688"><span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF\_E\_EXPECTED\_BRACE\_OR\_BAD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-689">2147762217 (0x80044029)</span><span class="sxs-lookup"><span data-stu-id="9be87-689">2147762217 (0x80044029)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-690">Die abschließende geschweifter Klammer und das Semikolon für eine Klasse fehlen.</span><span class="sxs-lookup"><span data-stu-id="9be87-690">The final brace and semi-colon for a class are missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**Wbemmof \_ E \_ nicht unterstützt \_ CIMV22 \_ Qual- \_ Wert**</span><span class="sxs-lookup"><span data-stu-id="9be87-691"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_QUAL\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-692">2147762218 (0x8004402a)</span><span class="sxs-lookup"><span data-stu-id="9be87-692">2147762218 (0x8004402A)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-693">Eine CIM-Version 2,2 wird für einen qualifiziererwert nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-693">A CIM version 2.2 feature is not supported for a qualifier value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**Wbemmof \_ E \_ nicht unterstützter \_ CIMV22- \_ \_ Datentyp**</span><span class="sxs-lookup"><span data-stu-id="9be87-694"><span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF\_E\_UNSUPPORTED\_CIMV22\_DATA\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-695">2147762219 (0x8004402b)</span><span class="sxs-lookup"><span data-stu-id="9be87-695">2147762219 (0x8004402B)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-696">Der Datentyp der CIM-Version 2,2 wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9be87-696">The CIM version 2.2 data type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**wbemmof \_ E \_ ungültige \_ Delta einstance- \_ Syntax.**</span><span class="sxs-lookup"><span data-stu-id="9be87-697"><span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETEINSTANCE\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-698">2147762220 (0x8004402c)</span><span class="sxs-lookup"><span data-stu-id="9be87-698">2147762220 (0x8004402C)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-699">Die Delete instance-Syntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-699">The delete instance syntax is not valid.</span></span> <span data-ttu-id="9be87-700">Der Wert sollte `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span><span class="sxs-lookup"><span data-stu-id="9be87-700">It should be `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**wbemmof \_ E \_ ungültige \_ qualifizierersyntax. \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-701"><span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF\_E\_INVALID\_QUALIFIER\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-702">2147762221 (0x8004402d)</span><span class="sxs-lookup"><span data-stu-id="9be87-702">2147762221 (0x8004402D)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-703">Die qualifizierersyntax ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-703">The qualifier syntax is not valid.</span></span> <span data-ttu-id="9be87-704">Dort sollte `qualifiername:type=value,scope(class|instance), flavorname` stehen.</span><span class="sxs-lookup"><span data-stu-id="9be87-704">It should be `qualifiername:type=value,scope(class|instance), flavorname`.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**wbemmof \_ E- \_ Qualifizierer außerhalb des Gültigkeits \_ \_ \_ Bereichs**</span><span class="sxs-lookup"><span data-stu-id="9be87-705"><span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**WBEMMOF\_E\_QUALIFIER\_USED\_OUTSIDE\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-706">2147762222 (0x8004402e)</span><span class="sxs-lookup"><span data-stu-id="9be87-706">2147762222 (0x8004402E)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-707">Der Qualifizierer wird außerhalb seines Gültigkeits Bereichs verwendet.</span><span class="sxs-lookup"><span data-stu-id="9be87-707">The qualifier is used outside of its scope.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**wbemmof \_ E \_ Fehler beim Erstellen der temporären \_ \_ \_ Datei.**</span><span class="sxs-lookup"><span data-stu-id="9be87-708"><span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF\_E\_ERROR\_CREATING\_TEMP\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-709">2147762223 (0x8004402f)</span><span class="sxs-lookup"><span data-stu-id="9be87-709">2147762223 (0x8004402F)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-710">Fehler beim Erstellen der temporären Datei.</span><span class="sxs-lookup"><span data-stu-id="9be87-710">Error creating temporary file.</span></span> <span data-ttu-id="9be87-711">Die temporäre Datei ist eine Zwischenphase in der MOF-Kompilierung.</span><span class="sxs-lookup"><span data-stu-id="9be87-711">The temporary file is an intermediate stage in the MOF compilation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**wbemmof \_ E- \_ Fehler \_ ungültige \_ Includedatei \_**</span><span class="sxs-lookup"><span data-stu-id="9be87-712"><span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**WBEMMOF\_E\_ERROR\_INVALID\_INCLUDE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-713">2147762224 (0x80044030)</span><span class="sxs-lookup"><span data-stu-id="9be87-713">2147762224 (0x80044030)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-714">Eine in der MOF-Datei mit dem Präprozessorbefehl enthaltene Datei ist nicht gültig. [ \# ](-include.md)</span><span class="sxs-lookup"><span data-stu-id="9be87-714">A file included in the MOF by the preprocessor command [\#include](-include.md) is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9be87-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**wbemmof \_ E \_ ungültige \_ deleteclass- \_ Syntax.**</span><span class="sxs-lookup"><span data-stu-id="9be87-715"><span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF\_E\_INVALID\_DELETECLASS\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9be87-716">2147762225 (0x80044031)</span><span class="sxs-lookup"><span data-stu-id="9be87-716">2147762225 (0x80044031)</span></span>
</dt> <dt>



<span data-ttu-id="9be87-717">Die Syntax für die Präprozessorbefehle ' [ \# pragma DeleteInstance](pragma-deleteinstance.md) ' oder ' [ \# pragma deleteclass](pragma-deleteclass.md) ' ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9be87-717">The syntax for the preprocessor commands [\#pragma deleteinstance](pragma-deleteinstance.md) or [\#pragma deleteclass](pragma-deleteclass.md) is not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9be87-718">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9be87-718">Requirements</span></span>



| <span data-ttu-id="9be87-719">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9be87-719">Requirement</span></span> | <span data-ttu-id="9be87-720">Wert</span><span class="sxs-lookup"><span data-stu-id="9be87-720">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9be87-721">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9be87-721">Minimum supported client</span></span><br/> | <span data-ttu-id="9be87-722">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9be87-722">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9be87-723">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9be87-723">Minimum supported server</span></span><br/> | <span data-ttu-id="9be87-724">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9be87-724">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9be87-725">Header</span><span class="sxs-lookup"><span data-stu-id="9be87-725">Header</span></span><br/>                   | <dl> <span data-ttu-id="9be87-726"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="9be87-726"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="9be87-727">IDL</span><span class="sxs-lookup"><span data-stu-id="9be87-727">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9be87-728"><dt>Wbemcli. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9be87-728"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9be87-729">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9be87-729">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be87-730">WMI-Rückgabe Codes</span><span class="sxs-lookup"><span data-stu-id="9be87-730">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

