---
title: Remotedesktopdienste Fehlercodes des WMI-Anbieters (wbemcli. h)
description: Fehler, die vom Remotedesktopdienste WMI-Anbieter zurückgegeben werden. Eine Liste mit anderen WMI-Fehlern finden Sie unter WMI-Fehler Konstanten.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518989"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a><span data-ttu-id="f7f50-104">Fehlercodes für den WMI-Anbieter Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="f7f50-104">Remote Desktop Services WMI provider error codes</span></span>

<span data-ttu-id="f7f50-105">In der folgenden Liste werden die WMI-Fehler aufgeführt, die vom Remotedesktopdienste WMI-Anbieter zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f7f50-105">The following list lists the WMI errors returned by the Remote Desktop Services WMI provider.</span></span> <span data-ttu-id="f7f50-106">Eine Liste mit anderen WMI-Fehlern finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="f7f50-106">For a list of other WMI errors, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="f7f50-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM \_ E \_ fehlgeschlagen**</span><span class="sxs-lookup"><span data-stu-id="f7f50-107"><span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**WBEM\_E\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-108">2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="f7f50-108">2147749889 (0x80041001)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-109">Der Methodenaufrufe ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="f7f50-109">The method call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ nicht \_ gefunden**</span><span class="sxs-lookup"><span data-stu-id="f7f50-110"><span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM\_E\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-111">2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="f7f50-111">2147749890 (0x80041002)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-112">Das Objekt konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="f7f50-112">The object could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**Fehler beim WBEM \_ E- \_ Anbieter. \_**</span><span class="sxs-lookup"><span data-stu-id="f7f50-113"><span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**WBEM\_E\_PROVIDER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-114">2147749892 (0x80041004)</span><span class="sxs-lookup"><span data-stu-id="f7f50-114">2147749892 (0x80041004)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-115">Der Anbieter ist zu einem anderen Zeitpunkt als während der Initialisierung fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="f7f50-115">The provider has failed at some time other than during initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM \_ E- \_ Typen Konflikt \_**</span><span class="sxs-lookup"><span data-stu-id="f7f50-116"><span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**WBEM\_E\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-117">2147749893 (0x80041005)</span><span class="sxs-lookup"><span data-stu-id="f7f50-117">2147749893 (0x80041005)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-118">Es ist ein Typen Konflikt aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f7f50-118">A type mismatch has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**nicht genügend \_ Arbeits \_ \_ Speicher für \_ WBEM E**</span><span class="sxs-lookup"><span data-stu-id="f7f50-119"><span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM\_E\_OUT\_OF\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-120">2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="f7f50-120">2147749894 (0x80041006)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-121">Für die Operation war nicht genügend Arbeitsspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f7f50-121">There was not enough memory for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_Ungültiger WBEM E- \_ \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="f7f50-122"><span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-123">2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="f7f50-123">2147749896 (0x80041008)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-124">Einer der Parameter für den Aufruf ist nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="f7f50-124">One of the parameters to the call is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ nicht \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="f7f50-125"><span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM\_E\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-126">2147749897 (0x80041009)</span><span class="sxs-lookup"><span data-stu-id="f7f50-126">2147749897 (0x80041009)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-127">Die Ressource, i. d. R. ein Remoteserver, ist momentan nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f7f50-127">The resource, typically a remote server, is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ \_ wird nicht unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="f7f50-128"><span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM\_E\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-129">2147749900 (0x8004100c)</span><span class="sxs-lookup"><span data-stu-id="f7f50-129">2147749900 (0x8004100C)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-130">Das Feature bzw. die Operation wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7f50-130">The feature or operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E ( \_ ungültiger \_ Namespace)**</span><span class="sxs-lookup"><span data-stu-id="f7f50-131"><span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM\_E\_INVALID\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-132">2147749902 (0x8004100e)</span><span class="sxs-lookup"><span data-stu-id="f7f50-132">2147749902 (0x8004100E)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-133">Der angegebene Namespace konnte nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="f7f50-133">The specified namespace could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**ungültiges WBEM- \_ \_ \_ Objekt**</span><span class="sxs-lookup"><span data-stu-id="f7f50-134"><span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-135">2147749903 (0x8004100f)</span><span class="sxs-lookup"><span data-stu-id="f7f50-135">2147749903 (0x8004100F)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-136">Die angegebene Instanz ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f7f50-136">The specified instance is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM \_ E- \_ Initialisierungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="f7f50-137"><span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**WBEM\_E\_INITIALIZATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-138">2147749908 (0x80041014)</span><span class="sxs-lookup"><span data-stu-id="f7f50-138">2147749908 (0x80041014)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-139">Ein Modul, z. b. ein Anbieter, konnte aus internen Gründen nicht initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f7f50-139">A module, such as a provider, failed to initialize for internal reasons.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_Ungültiger WBEM E- \_ \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="f7f50-140"><span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**WBEM\_E\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-141">2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="f7f50-141">2147749910 (0x80041016)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-142">Die angeforderte Operation ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f7f50-142">The requested operation is not valid.</span></span> <span data-ttu-id="f7f50-143">Dieser Fehler betrifft i. A. ungültige Versuche, Klassen oder Eigenschaften zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f7f50-143">This error usually applies to invalid attempts to delete classes or properties.</span></span> <span data-ttu-id="f7f50-144">Dieser Fehler wird bei dem Versuch zurückgegeben, eine Server Überschreibungs Eigenschaft durch die Gruppenrichtlinien Steuerung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f7f50-144">This error is returned on an attempt to modify a server-override property through group policy control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_ungültige WBEM E- \_ \_ Abfrage**</span><span class="sxs-lookup"><span data-stu-id="f7f50-145"><span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM\_E\_INVALID\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-146">2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="f7f50-146">2147749911 (0x80041017)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-147">Die Abfrage war syntaktisch ungültig.</span><span class="sxs-lookup"><span data-stu-id="f7f50-147">The query was not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_Ungültiger WBEM E- \_ \_ Abfragetyp \_**</span><span class="sxs-lookup"><span data-stu-id="f7f50-148"><span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**WBEM\_E\_INVALID\_QUERY\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-149">2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="f7f50-149">2147749912 (0x80041018)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-150">Die angeforderte Abfragesprache wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7f50-150">The requested query language is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E ist \_ bereits \_ vorhanden.**</span><span class="sxs-lookup"><span data-stu-id="f7f50-151"><span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM\_E\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-152">2147749913 (0x80041019)</span><span class="sxs-lookup"><span data-stu-id="f7f50-152">2147749913 (0x80041019)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-153">In einem Put-Vorgang wurde das Flag " **wbemchangeflagkreateonly** " angegeben, aber die Instanz ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f7f50-153">In a put operation, the **wbemChangeFlagCreateOnly** flag was specified, but the instance already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_ungültige WBEM E- \_ \_ Syntax**</span><span class="sxs-lookup"><span data-stu-id="f7f50-154"><span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**WBEM\_E\_INVALID\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-155">2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="f7f50-155">2147749921 (0x80041021)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-156">Die Abfrage ist nicht syntaktisch gültig.</span><span class="sxs-lookup"><span data-stu-id="f7f50-156">Query is not syntactically valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E schreibgeschützt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f7f50-157"><span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM\_E\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-158">2147749923 (0x80041023)</span><span class="sxs-lookup"><span data-stu-id="f7f50-158">2147749923 (0x80041023)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-159">Die Eigenschaft, die Sie ändern möchten, ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f7f50-159">The property that you are attempting to modify is read-only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM \_ E \_ - \_ Anbieter \_ ist nicht fähig**</span><span class="sxs-lookup"><span data-stu-id="f7f50-160"><span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**WBEM\_E\_PROVIDER\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-161">2147749924 (0x80041024)</span><span class="sxs-lookup"><span data-stu-id="f7f50-161">2147749924 (0x80041024)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-162">Der Anbieter kann den angeforderten Vorgang nicht ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7f50-162">The provider cannot perform the requested operation.</span></span> <span data-ttu-id="f7f50-163">Der Vorgang kann eine Abfrage enthalten, die zu komplex ist, eine Instanz abruft, eine Klasse erstellt, eine Klasse aktualisiert, eine Klasse löscht oder eine Klasse auflistet.</span><span class="sxs-lookup"><span data-stu-id="f7f50-163">The operation could include a query that is too complex, retrieving an instance, creating a class, updating a class, deleting a class, or enumerating a class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ unzulässig \_ null**</span><span class="sxs-lookup"><span data-stu-id="f7f50-164"><span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM\_E\_ILLEGAL\_NULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-165">2147749928 (0x80041028)</span><span class="sxs-lookup"><span data-stu-id="f7f50-165">2147749928 (0x80041028)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-166"> / Für eine Eigenschaft, die nicht NULL sein darf, wurde der Wert Nothing **null** angegeben / , z. b. eine, die durch einen [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), einen [**indizierten**](/windows/desktop/WmiSdk/optional-qualifiers)oder einen [**nicht- \_ null**](/windows/desktop/WmiSdk/optional-qualifiers) -Qualifizierer gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="f7f50-166">A value of **Nothing**/**NULL** was specified for a property that cannot be **Nothing**/**NULL**, such as one that is marked by a [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Indexed**](/windows/desktop/WmiSdk/optional-qualifiers), or [**Not\_Null**](/windows/desktop/WmiSdk/optional-qualifiers) qualifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_der Wert von WBEM E liegt \_ \_ außerhalb \_ des zulässigen \_ Bereichs.**</span><span class="sxs-lookup"><span data-stu-id="f7f50-167"><span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM\_E\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-168">2147749931 (0x8004102b)</span><span class="sxs-lookup"><span data-stu-id="f7f50-168">2147749931 (0x8004102B)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-169">Die Anforderung wurde mit einem Wert außerhalb des gültigen Bereichs vorgenommen bzw. ist mit dem Typ nicht kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f7f50-169">The request was made with an out-of-range value, or is incompatible with the type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ungültige WBEM E- \_ \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="f7f50-170"><span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM\_E\_INVALID\_METHOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-171">2147749934 (0x8004102e)</span><span class="sxs-lookup"><span data-stu-id="f7f50-171">2147749934 (0x8004102E)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-172">Der angeforderte Methode ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f7f50-172">The requested method is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_ \_ ungültige \_ Methoden \_ Parameter für WBEM E**</span><span class="sxs-lookup"><span data-stu-id="f7f50-173"><span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**WBEM\_E\_INVALID\_METHOD\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-174">2147749935 (0x8004102f)</span><span class="sxs-lookup"><span data-stu-id="f7f50-174">2147749935 (0x8004102F)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-175">Die für die Methode bereitgestellten Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="f7f50-175">The parameters provided for the method are not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f7f50-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E ( \_ ungültiger \_ Objekt \_ Pfad)**</span><span class="sxs-lookup"><span data-stu-id="f7f50-176"><span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM\_E\_INVALID\_OBJECT\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7f50-177">2147749946 (0x8004103a)</span><span class="sxs-lookup"><span data-stu-id="f7f50-177">2147749946 (0x8004103A)</span></span>
</dt> <dt>



<span data-ttu-id="f7f50-178">Der angegebene Objekt Pfad war ungültig.</span><span class="sxs-lookup"><span data-stu-id="f7f50-178">The specified object path was not valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7f50-179">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7f50-179">Requirements</span></span>



| <span data-ttu-id="f7f50-180">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7f50-180">Requirement</span></span> | <span data-ttu-id="f7f50-181">Wert</span><span class="sxs-lookup"><span data-stu-id="f7f50-181">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f50-182">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f7f50-182">Minimum supported client</span></span><br/> | <span data-ttu-id="f7f50-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7f50-183">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="f7f50-184">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f7f50-184">Minimum supported server</span></span><br/> | <span data-ttu-id="f7f50-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7f50-185">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="f7f50-186">Header</span><span class="sxs-lookup"><span data-stu-id="f7f50-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7f50-187"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7f50-187"><dt>Wbemcli.h</dt></span></span> </dl> |



 

