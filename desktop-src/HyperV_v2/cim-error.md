---
description: Die CIM- \_ Fehler Klasse enthält Informationen zum Fehler eines CIM-Vorgangs.
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: CIM_Error-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Error
- CIM_Error.ErrorType
- CIM_Error.OtherErrorType
- CIM_Error.OwningEntity
- CIM_Error.MessageID
- CIM_Error.Message
- CIM_Error.MessageArguments
- CIM_Error.PerceivedSeverity
- CIM_Error.ProbableCause
- CIM_Error.ProbableCauseDescription
- CIM_Error.RecommendedActions
- CIM_Error.ErrorSource
- CIM_Error.ErrorSourceFormat
- CIM_Error.OtherErrorSourceFormat
- CIM_Error.CIMStatusCode
- CIM_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59ae2527478235c14a8f856319178afe00c02a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342648"
---
# <a name="cim_error-class"></a><span data-ttu-id="f4dc1-103">CIM- \_ Fehler Klasse</span><span class="sxs-lookup"><span data-stu-id="f4dc1-103">CIM\_Error class</span></span>

<span data-ttu-id="f4dc1-104">Die **CIM- \_ Fehler** Klasse enthält Informationen zum Fehler eines CIM-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-104">The **CIM\_Error** class contains information about the failure of a CIM operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4dc1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4dc1-105">Syntax</span></span>

``` syntax
[Indication, Abstract, Version("2.22.1"), Exception, UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a><span data-ttu-id="f4dc1-106">Member</span><span class="sxs-lookup"><span data-stu-id="f4dc1-106">Members</span></span>

<span data-ttu-id="f4dc1-107">Die **CIM- \_ Fehler** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f4dc1-107">The **CIM\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="f4dc1-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4dc1-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4dc1-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f4dc1-109">Properties</span></span>

<span data-ttu-id="f4dc1-110">Die **CIM- \_ Fehler** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-110">The **CIM\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4dc1-111">**Cimstatus Code**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-111">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-112">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-114">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. DMTF- \| Fehler. Code \| 2,3 "," DSP0200. DMTF \| cimerror \| 1,3 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**Cimstatus-codedescription**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.CODE\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCodeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-115">Der CIM-Statuscode, der diese Instanz kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="f4dc1-116">Diese Eigenschaft definiert die Statuscodes, die von einem CIM-Server oder-Listener zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-116">This property defines the status codes that can be return by a CIM server or listener.</span></span>

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span data-ttu-id="f4dc1-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM \_ Err \_** -Fehler (1)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM\_ERR\_FAILED** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-118">Ein allgemeiner Fehler ist aufgetreten, der nicht von einem spezifischeren Fehlercode abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-118">A general error occurred that is not covered by a more specific error code.</span></span>

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span data-ttu-id="f4dc1-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM \_ Err- \_ Zugriff \_ verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM\_ERR\_ACCESS\_DENIED** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-120">Der Zugriff auf eine CIM-Ressource war für den Client nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-120">Access to a CIM resource was not available to the client.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span data-ttu-id="f4dc1-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM \_ Err- \_ ungültiger \_ Namespace** (3)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM\_ERR\_INVALID\_NAMESPACE** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-122">Der Ziel Namespace ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-122">The target namespace does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span data-ttu-id="f4dc1-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM \_ \_Ungültiger \_ Err-Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM\_ERR\_INVALID\_PARAMETER** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-124">Mindestens ein Parameterwert, der an die-Methode übergeben wurde, war ungültig.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-124">One or more parameter values passed to the method were invalid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span data-ttu-id="f4dc1-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM \_ Err \_ ungültige \_ Klasse** (5)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM\_ERR\_INVALID\_CLASS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-126">Die angegebene Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-126">The specified Class does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span data-ttu-id="f4dc1-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM \_ Err \_ nicht \_ gefunden** (6)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM\_ERR\_NOT\_FOUND** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-128">Das angeforderte Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-128">The requested object could not be found.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span data-ttu-id="f4dc1-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM \_ Err \_ \_ wird nicht unterstützt** (7)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM\_ERR\_NOT\_SUPPORTED** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-130">Der angeforderte Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-130">The requested operation is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span data-ttu-id="f4dc1-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM \_ Err- \_ Klasse \_ hat \_** untergeordnete Elemente (8)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM\_ERR\_CLASS\_HAS\_CHILDREN** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-132">Der Vorgang kann für diese Klasse nicht ausgeführt werden, da Sie über Instanzen verfügt.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-132">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span data-ttu-id="f4dc1-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM \_ Err- \_ Klasse \_ hat \_ Instanzen** (9)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM\_ERR\_CLASS\_HAS\_INSTANCES** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-134">Der Vorgang kann für diese Klasse nicht ausgeführt werden, da Sie über Instanzen verfügt.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-134">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span data-ttu-id="f4dc1-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM \_ Err \_ ungültige \_ Superclass** (10)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM\_ERR\_INVALID\_SUPERCLASS** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-136">Der Vorgang kann nicht ausgeführt werden, da die angegebene übergeordnete Klasse nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-136">Operation cannot be carried out since the specified superclass does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span data-ttu-id="f4dc1-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM \_ Err ist \_ bereits \_ vorhanden** (11)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM\_ERR\_ALREADY\_EXISTS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-138">Der Vorgang kann nicht ausgeführt werden, da bereits ein Objekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-138">Operation cannot be carried out because an object already exists.</span></span>

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span data-ttu-id="f4dc1-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM \_ Err \_ keine \_ solche \_ Eigenschaft** (12)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM\_ERR\_NO\_SUCH\_PROPERTY** (12)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-140">Die angegebene Eigenschaft ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-140">The specified Property does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span data-ttu-id="f4dc1-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM \_ Nicht \_ \_ überein** Stimmender Err-Typen (13)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM\_ERR\_TYPE\_MISMATCH** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-142">Der angegebene Wert ist nicht mit dem Typ kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-142">The value supplied is incompatible with the type.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span data-ttu-id="f4dc1-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM \_ Err \_ - \_ Abfrage \_ Sprache \_ wird nicht unterstützt** (14)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-144">Die Abfragesprache wird nicht erkannt oder nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-144">The query language is not recognized or supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span data-ttu-id="f4dc1-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM \_ Irre \_ ungültige \_ Abfrage** (15)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM\_ERR\_INVALID\_QUERY** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-146">Die Abfrage ist für die angegebene Abfragesprache ungültig.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-146">The query is not valid for the specified query language.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span data-ttu-id="f4dc1-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM \_ Err- \_ Methode \_ nicht \_ verfügbar** (16)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-148">Die System externe-Methode konnte nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-148">The extrinsic Method could not be executed.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span data-ttu-id="f4dc1-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM \_ Err- \_ Methode \_ nicht \_ gefunden** (17)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM\_ERR\_METHOD\_NOT\_FOUND** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-150">Die angegebene System externe-Methode ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-150">The specified extrinsic Method does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span data-ttu-id="f4dc1-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM \_ \_Unerwartete \_ Antwort von Err** (18)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM\_ERR\_UNEXPECTED\_RESPONSE** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-152">Die zurückgegebene Antwort auf den asynchronen Vorgang wurde nicht erwartet.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-152">The returned response to the asynchronous operation was not expected.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span data-ttu-id="f4dc1-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM \_ \_Ungültiges \_ Antwort \_ Ziel** (19)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-154">Das angegebene Ziel für die asynchrone Antwort ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-154">The specified destination for the asynchronous response is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span data-ttu-id="f4dc1-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM \_ Der Err- \_ Namespace ist \_ nicht \_ leer** (20).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-156">Der angegebene Namespace ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-156">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span data-ttu-id="f4dc1-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM \_ Err- \_ ungültiger \_ enumerationskontext \_** (21)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM\_ERR\_INVALID\_ENUMERATION\_CONTEXT** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-158">Der angegebene enumerationskontext ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-158">The enumeration context supplied is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span data-ttu-id="f4dc1-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM \_ \_ \_ \_ Timeout für ungültige Operation** (22)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM\_ERR\_INVALID\_OPERATION\_TIMEOUT** (22)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-160">Der angegebene Namespace ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-160">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span data-ttu-id="f4dc1-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM \_ Err \_ Pull \_ wurde \_ \_ abgebrochen** (23)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM\_ERR\_PULL\_HAS\_BEEN\_ABANDONED** (23)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-162">Der angegebene Namespace ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-162">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span data-ttu-id="f4dc1-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM \_ Err- \_ Pull \_ kann nicht \_ \_ abgebrochen werden** (24)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM\_ERR\_PULL\_CANNOT\_BE\_ABANDONED** (24)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-164">Der Versuch, einen Pull-Vorgang abzubrechen, ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-164">The attempt to abandon a pull operation has failed.</span></span>

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span data-ttu-id="f4dc1-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM \_ Err- \_ gefilterte \_ Enumeration \_ \_ wird nicht unterstützt** (25)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM\_ERR\_FILTERED\_ENUMERATION\_NOT\_SUPPORTED** (25)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-166">Gefilterte enumeratrionen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-166">Filtered Enumeratrions are not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span data-ttu-id="f4dc1-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM \_ Err- \_ Fortsetzung \_ bei \_ Fehler \_ \_ wird nicht unterstützt** (26)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM\_ERR\_CONTINUATION\_ON\_ERROR\_NOT\_SUPPORTED** (26)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-168">"Bei Fehler fortsetzen" wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-168">Continue on error is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span data-ttu-id="f4dc1-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM \_ Err- \_ Server \_ Limits \_ überschritten** (27)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM\_ERR\_SERVER\_LIMITS\_EXCEEDED** (27)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-170">Die Grenzwerte für den WBEM-Server wurden überschritten (z. b. Arbeitsspeicher, Verbindungen,...).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-170">The WBEM Server limits have been exceeded (e.g. memory, connections, ...).</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span data-ttu-id="f4dc1-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM \_ Der Err- \_ Server \_ wird \_ \_ heruntergefahren** (28).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM\_ERR\_SERVER\_IS\_SHUTTING\_DOWN** (28)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-172">Der WBEM-Server wird heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-172">The WBEM Server is shutting down.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span data-ttu-id="f4dc1-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM \_ Err \_ - \_ Abfrage \_ Funktion \_ wird nicht unterstützt** (29)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM\_ERR\_QUERY\_FEATURE\_NOT\_SUPPORTED** (29)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-174">Die angegebene Abfragefunktion wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-174">The specified Query Feature is not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f4dc1-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4dc1-176">**Cimstatus Code Description**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-176">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-177">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-178">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-179">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. DMTF- \| Fehler. Beschreibung \| 2,3 "," DSP0200. DMTF \| cimerror \| 1,3 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**Cimstatus Code**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.DESCRIPTION\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCode**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-180">Eine frei Form Zeichenfolge, die eine lesbare Beschreibung des **cimstatus Code** -Eigenschafts Werts enthält.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-180">A free-form string that contains a human-readable description of the **CIMStatusCode** property value.</span></span>

> [!Note]  
> <span data-ttu-id="f4dc1-181">Diese Beschreibung kann erweitert werden, muss jedoch mit der Definition von **cimstatus Code** konsistent sein.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-181">This description may extend, but must be consistent with the definition of **CIMStatusCode**.</span></span>

 

</dd> <dt>

<span data-ttu-id="f4dc1-182">**Errorsource**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-182">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-183">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-185">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**Errorsourceformat**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-186">Informationen, die die Entität identifizieren, die den Fehler generiert hat.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-186">Information that identifies the entity that generated the error.</span></span> <span data-ttu-id="f4dc1-187">Wenn die Entität vom CIM-Schema modelliert wird, enthält diese Eigenschaft den Pfad zu der Instanz, die als Zeichen folgen Parameter codiert ist.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-187">If the entity is modeled by the CIM Schema, this property contains the path to the instance encoded as a string parameter.</span></span> <span data-ttu-id="f4dc1-188">Andernfalls enthält die-Eigenschaft eine Zeichenfolge, die die Entität benennt, die den Fehler generiert hat.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-188">Otherwise, the property contains a string that names the entity that generated the error.</span></span> <span data-ttu-id="f4dc1-189">Das Format dieser Eigenschaft wird durch die Eigenschaft **errorsourceformat** angegeben.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-189">The format of this property is specified by the **ErrorSourceFormat** property.</span></span>

</dd> <dt>

<span data-ttu-id="f4dc1-190">**Errorsourceformat**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-190">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-191">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-192">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-193">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**Errorsource**","**CIM- \_ Fehler**.**Othererrorsourceformat**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSource**", "**CIM\_Error**.**OtherErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-194">Das Format der **errorsource** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-194">The format of the **ErrorSource** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4dc1-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-196">Das Format ist unbekannt oder kann von einer CIM-Client Anwendung nicht sinnvoll interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-196">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f4dc1-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-198">Das Format wird durch den Wert der **othererrorsourceformat** -Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-198">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="f4dc1-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**Cifibjectpath** (2)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-200">Ein CIM-Objekt Pfad gemäß Definition in der CIM-Infrastruktur Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-200">A CIM Object Path as defined in the CIM Infrastructure specification.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f4dc1-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4dc1-202">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-202">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-203">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-204">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-205">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**Othererrortype**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-205">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**OtherErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-206">Der primäre Fehlertyp.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-206">The primary error type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4dc1-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f4dc1-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span data-ttu-id="f4dc1-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Kommunikationsfehler** (2)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Communications Error** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-210">Fehler dieses Typs sind hauptsächlich mit den Prozeduren und/oder Prozessen verknüpft, die erforderlich sind, um Informationen von einem Punkt an einen anderen zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-210">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span data-ttu-id="f4dc1-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Quality of Service Fehler** (3)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Quality of Service Error** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-212">Fehler dieses Typs sind hauptsächlich mit Fehlern verknüpft, die zu eingeschränkter Funktionalität oder Leistung führen.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-212">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span>

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="f4dc1-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Fehler** (4)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-214">Ein Fehler dieses Typs ist hauptsächlich mit einem Software-oder Verarbeitungsfehler verknüpft.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-214">Error of this type are principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span data-ttu-id="f4dc1-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Fehler** (5)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-216">Fehler dieses Typs sind hauptsächlich mit einem Geräte-oder Hardwarefehler verknüpft.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-216">Errors of this type are principally associated with an equipment or hardware failure.</span></span>

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span data-ttu-id="f4dc1-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Umgebungs Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Environmental Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-218">Weitere Umgebungs Überlegungen</span><span class="sxs-lookup"><span data-stu-id="f4dc1-218">other environmental considerations.</span></span>

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span data-ttu-id="f4dc1-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Sicherheitsfehler** (7)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Security Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-220">Fehler dieses Typs sind Sicherheitsverletzungen, Erkennung von Viren und ähnlichen Problemen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-220">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span>

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span data-ttu-id="f4dc1-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Overabonnementfehler** (8)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Oversubscription Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-222">Fehler dieses Typs sind hauptsächlich mit dem Ausfall der Zuordnung ausreichender Ressourcen zum Abschluss des Vorgangs verknüpft.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-222">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span>

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span data-ttu-id="f4dc1-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>Nicht **verfügbarer Ressourcen Fehler** (9).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Unavailable Resource Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-224">Fehler dieses Typs sind hauptsächlich mit dem Fehler beim Zugriff auf eine erforderliche Ressource verbunden.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-224">Errors of this type are principally associated with the failure to access a required resource.</span></span>

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span data-ttu-id="f4dc1-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Nicht unterstützter Vorgangs Fehler** (10)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Unsupported Operation Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-226">Fehler dieses Typs sind hauptsächlich mit nicht unterstützten Anforderungen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-226">Errors of this type are principally associated with requests that are not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f4dc1-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4dc1-228">**Meldung**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-228">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-229">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-230">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-231">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**MessageId**","**CIM- \_ Fehler**.**Messagearguments**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-231">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-232">Die formatierte Meldung.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-232">The formatted message.</span></span>

> [!Note]  
> <span data-ttu-id="f4dc1-233">Diese Meldung wird erstellt, indem dynamische Elemente der **messagearguments** -Eigenschaft mit den statischen Elementen der **MessageId** -Eigenschaft kombiniert und dann zu einer Nachrichten Registrierung oder einem Katalog hinzugefügt werden, die der **owningentity**-Eigenschaft zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-233">This message is created by combining dynamic elements of the **MessageArguments** property with the static elements of the **MessageID** property, and then adding them to a message registry or catalog associated with the **OwningEntity**.</span></span>

 

</dd> <dt>

<span data-ttu-id="f4dc1-234">**Messagearguments**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-234">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-235">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f4dc1-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-236">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-237">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**MessageId**","**CIM- \_ Fehler**.**Meldung**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-237">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**Message**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-238">Ein Array, das den dynamischen Inhalt der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-238">An array that contains the dynamic content of the message.</span></span>

</dd> <dt>

<span data-ttu-id="f4dc1-239">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-239">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-240">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-241">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-242">Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**Meldung**","**CIM- \_ Fehler**.**Messagearguments**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-242">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**Message**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-243">Eine nicht transparente Zeichenfolge, die innerhalb des Gültigkeits Bereichs von owningentity das Format der Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-243">An opaque string that uniquely identifies, within the scope of the OwningEntity, the format of the Message.</span></span>

</dd> <dt>

<span data-ttu-id="f4dc1-244">**Othererrorsourceformat**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-244">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-245">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-246">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-247">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**Errorsourceformat**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-247">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-248">Eine Zeichenfolge, die den **errorsourceformat** -Wert definiert, wenn **errorsourceformat** auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-248">A string that defines the **ErrorSourceFormat** value when **ErrorSourceFormat** is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="f4dc1-249">**Othererrortype**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-249">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-250">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-251">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-252">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**ErrorType**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-252">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-253">Eine frei Form Zeichenfolge, die den **ErrorType** -Wert beschreibt, wenn der Wert auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-253">A free-form string that describes the **ErrorType** value when it is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="f4dc1-254">**Owningentity**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-254">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-255">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-257">Die eindeutige ID der Entität, die das Format der Nachricht besitzt, die von dieser Instanz beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-257">The unique ID of the entity that owns the format of the message described by this instance.</span></span>

> [!Note]  
> <span data-ttu-id="f4dc1-258">Diese Eigenschaft muss einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder eindeutigen Namen enthalten, der im Besitz der Geschäfts Entität oder des Standard Texts ist, die das Nachrichtenformat definiert hat.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-258">This property must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

 

</dd> <dt>

<span data-ttu-id="f4dc1-259">**Wahrnehmgrad**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-259">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-260">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-261">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-262">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Wahrgenommene Schweregrade ")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-262">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-263">Eine Beschreibung des Fehler schwere Grads aus der Sicht des Elements, das die Fehlermeldung gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-263">A description of the error severity from the point of view of the element that sent the error message.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4dc1-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-265">der erkannte Schweregrad der Angabe ist unbekannt oder unbestimmt.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-265">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f4dc1-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-267">Gibt an, dass der Wert des schwere Grads in der Eigenschaft **otherschwere Grad** gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-267">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="f4dc1-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informationen** (2)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-269">Informationen sollten beim Bereitstellen einer informativen Antwort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-269">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="f4dc1-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>Heruntergestuft **/Warnung** (3)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-271">Sollte verwendet werden, wenn der Benutzer die Entscheidung treffen soll, ob eine Aktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-271">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="f4dc1-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Neben** Version (4)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-273">Es ist eine Aktion erforderlich, aber die Situation ist zu diesem Zeitpunkt nicht schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-273">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="f4dc1-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Haupt** Version (5)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-275">Die Aktion ist jetzt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-275">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="f4dc1-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Kritisch** (6)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-277">Jetzt ist eine Aktion erforderlich, und der Bereich ist umfangreich (möglicherweise kommt es zu einem bevorstehenden Ausfall einer wichtigen Ressource).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-277">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="f4dc1-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>Schwerwiegend **/nicht wiederherstellbar** (7)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f4dc1-279">Es ist ein Fehler aufgetreten, aber es ist zu spät, um Abhilfemaßnahmen zu ergreifen.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-279">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f4dc1-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4dc1-281">**Probableursache**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-281">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-282">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-283">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-284">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Empfehlung. ITU \| X733. Wahrscheinliche Ursache "," Empfehlung. ITU \| M3100. probablecause "," ITU-IANA-Alarm-TC "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**Probablecaueindescription**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-284">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCauseDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-285">Eine Beschreibung der wahrscheinlichen Ursache des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-285">A description of te probable cause of the error.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f4dc1-286">**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-286">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f4dc1-287">**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-287">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="f4dc1-288">**Adapter-/Kartenfehler** (2)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-288">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="f4dc1-289">**Fehler des Anwendungs Subsystems** (3)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-289">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="f4dc1-290">**Reduzierte Bandbreite** (4)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-290">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="f4dc1-291">**Fehler bei der Verbindungs Herstellung** (5)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-291">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="f4dc1-292">**Kommunikationsprotokoll Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-292">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="f4dc1-293">**Kommunikations Subsystem-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-293">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="f4dc1-294">**Konfigurations-/Anpassungsfehler** (8)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-294">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="f4dc1-295">**Überlastung** (9)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-295">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="f4dc1-296">Beschädigte **Daten** (10)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-296">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="f4dc1-297">**Limit für CPU-Zyklen überschritten** (11)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-297">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="f4dc1-298">**DataSet/Modem-Fehler** (12)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-298">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="f4dc1-299">Herunter gestufter **Signal** (13)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-299">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="f4dc1-300">**DTE-DCE-Schnittstellen Fehler** (14)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-300">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="f4dc1-301">**Gehäuse Tür geöffnet** (15)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-301">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="f4dc1-302">**Geräte** Fehler (16)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-302">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="f4dc1-303">**Übermäßige Vibrationen** (17)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-303">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="f4dc1-304">**Datei Format Fehler** (18)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-304">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="f4dc1-305">**Feuer erkannt** (19)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-305">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="f4dc1-306">Über **Flutung erkannt** (20)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-306">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="f4dc1-307">**Rahmen Fehler** (21)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-307">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="f4dc1-308">**HVAC-Problem** (22)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-308">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="f4dc1-309">**Feuchtigkeit nicht akzeptabel** (23)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-309">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="f4dc1-310">E **/a-Gerätefehler** (24)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-310">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="f4dc1-311">**Eingabegeräte Fehler** (25)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-311">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="f4dc1-312">**LAN-Fehler** (26)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-312">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="f4dc1-313">Es wurde ein **nicht giftiger Leck erkannt** (27)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-313">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="f4dc1-314">**Fehler beim übertragen lokaler Knoten** (28)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-314">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="f4dc1-315">**Verlust von Frame** (29)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-315">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="f4dc1-316">**Verlust von Signal** (30)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-316">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="f4dc1-317">**Material Versorgung erschöpft** (31)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-317">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="f4dc1-318">**Multiplexer-Problem** (32)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-318">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="f4dc1-319">**Nicht** genügend Arbeitsspeicher (33)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-319">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="f4dc1-320">**Ausgabegeräte Fehler** (34)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-320">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="f4dc1-321">Beeinträchtigung der **Leistung** (35)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-321">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="f4dc1-322">**Energie Problem** (36)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-322">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="f4dc1-323">**Unzulässiger Druck** (37)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-323">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="f4dc1-324">**Prozessor Problem (interner Computerfehler)** (38)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-324">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="f4dc1-325">**Pump Fehler** (39)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-325">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="f4dc1-326">**Warteschlangen Größe überschritten** (40)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-326">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="f4dc1-327">**Empfangs Fehler** (41)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-327">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="f4dc1-328">**Empfänger Fehler** (42)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-328">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="f4dc1-329">**Remote Knoten-Übertragungsfehler** (43)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-329">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="f4dc1-330">**Ressource mit oder fast der Kapazität** (44)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-330">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="f4dc1-331">**Antwortzeit übertrieben** (45)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-331">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="f4dc1-332">**Datenübertragungs Rate übermäßig** hoch (46)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-332">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="f4dc1-333">**Software Fehler** (47)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-333">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="f4dc1-334">Das **Software Programm wurde abgebrochen** (48).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-334">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="f4dc1-335">**Software Programmfehler (falsche Ergebnisse)** (49)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-335">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="f4dc1-336">**Speicher Kapazitäts Problem** (50)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-336">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="f4dc1-337">**Temperatur unzulässig** (51)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-337">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="f4dc1-338">**Schwellenwert überschritten** (52)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-338">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="f4dc1-339">**Zeit Steuerungs Problem** (53)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-339">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="f4dc1-340">Es wurde ein **giftiger Leck erkannt** (54)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-340">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="f4dc1-341">**Übertragungsfehler** (55)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-341">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="f4dc1-342">Übertragungs **Fehler** (56)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-342">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="f4dc1-343">**Zugrunde liegende Ressource nicht verfügbar** (57)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-343">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="f4dc1-344">**Versions** Konflikt (58)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-344">**Version Mismatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="f4dc1-345">**Vorherige Warnung gelöscht** (59)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-345">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="f4dc1-346">**Anmeldeversuche fehlgeschlagen** (60)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-346">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="f4dc1-347">**Software Viren erkannt** (61)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-347">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="f4dc1-348">**Hardware Sicherheits** Verletzung (62)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-348">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="f4dc1-349">**Denial-of-Service erkannt** (63)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-349">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="f4dc1-350">Nicht übereinstimmende **Sicherheits** Anmelde Informationen (64)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-350">**Security Credential Mismatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="f4dc1-351">Nicht **autorisierter Zugriff** (65)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-351">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="f4dc1-352">**Alarm empfangen** (66)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-352">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="f4dc1-353">**Verlust des Zeigers** (67)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-353">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="f4dc1-354">**Nutzlast nicht überein** Stimmungen (68)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-354">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="f4dc1-355">**Übertragungsfehler** (69)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-355">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="f4dc1-356">**Übermäßige Fehler Rate** (70)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-356">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="f4dc1-357">Ablauf **Verfolgungs Problem** (71)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-357">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="f4dc1-358">**Element nicht verfügbar** (72)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-358">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="f4dc1-359">Das **Element fehlt** (73).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-359">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="f4dc1-360">**Verlust von Multiframe** (74)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-360">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="f4dc1-361">**Übertragungskanal Fehler** (75)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-361">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="f4dc1-362">**Ungültige Nachricht empfangen** (76)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-362">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="f4dc1-363">**Routing Fehler** (77)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-363">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="f4dc1-364">**Backplane-Fehler** (78)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-364">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="f4dc1-365">**Bezeichnerduplizierung** (79)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-365">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="f4dc1-366">**Fehler beim Schutz Pfad** (80).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-366">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="f4dc1-367">**Synchronisierungs Verlust oder nicht überein** stimmende (81)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-367">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="f4dc1-368">**Terminal Problem** (82)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-368">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="f4dc1-369">**Echt Zeit Taktfehler** (83)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-369">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="f4dc1-370">**Antennen Fehler** (84)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-370">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="f4dc1-371">**Akku Ladefehler** (85)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-371">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="f4dc1-372">Datenträger **Fehler** (86)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-372">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="f4dc1-373">**Frequency Spring failure-Fehler** (87)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-373">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="f4dc1-374">**Verlust der Redundanz** (88)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-374">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="f4dc1-375">**Stromversorgung-Fehler** (89)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-375">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="f4dc1-376">**Signal Qualitäts Problem** (90)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-376">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="f4dc1-377">**Akku Entladung** (91)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-377">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="f4dc1-378">**Akku Fehler** (92)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-378">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="f4dc1-379">**Kommerzielles Energie Problem** (93)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-379">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="f4dc1-380">**Lüfterfehler** (94)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-380">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="f4dc1-381">**Engine-Fehler** (95)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-381">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="f4dc1-382">**Sensor Fehler** (96)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-382">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="f4dc1-383">**Fuse-Fehler** (97)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-383">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="f4dc1-384">**Generator Fehler** (98)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-384">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="f4dc1-385">**Niedrige Akku** Kapazität (99)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-385">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="f4dc1-386">**Niedriges Benzin** (100)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-386">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="f4dc1-387">**Niedriges Wasser** (101)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-387">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="f4dc1-388">**Explosiver Gas** (102)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-388">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="f4dc1-389">**Hohe Wind** Vorgänge (103)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-389">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="f4dc1-390">**Ice-BUILDUP** (104)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-390">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="f4dc1-391">**Rauch** (105)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-391">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="f4dc1-392">Arbeits **Speicher stimmt nicht überein** (106).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-392">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="f4dc1-393">**Nicht genügend CPU-Zyklen** (107)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-393">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="f4dc1-394">**Software Umgebungs Problem** (108)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-394">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="f4dc1-395">**Fehler beim Software Download** (109).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-395">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="f4dc1-396">Das **Element wurde erneut initialisiert** (110).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-396">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="f4dc1-397">**Timeout** (111)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-397">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="f4dc1-398">**Protokollierungs Probleme** (112)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-398">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="f4dc1-399">Der **Leck wurde erkannt** (113).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-399">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="f4dc1-400">**Fehler beim Schutzmechanismus** (114).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-400">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="f4dc1-401">**Schützen von Ressourcen Fehlern** (115)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-401">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="f4dc1-402">**Daten Bank Inkonsistenz** (116)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-402">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="f4dc1-403">**Authentifizierungsfehler** (117)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-403">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="f4dc1-404">**Verletzung der Vertraulichkeit** (118)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-404">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="f4dc1-405">**Kabel Manipulations** Funktion (119)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-405">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="f4dc1-406">**Verzögerte Informationen** (120)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-406">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="f4dc1-407">**Doppelte Informationen** (121)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-407">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="f4dc1-408">**Fehlende Informationen** (122)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-408">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="f4dc1-409">**Informations Änderung** (123)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-409">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="f4dc1-410">**Informationen außerhalb der Reihenfolge** (124)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-410">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="f4dc1-411">Der **Schlüssel ist abgelaufen** (125).</span><span class="sxs-lookup"><span data-stu-id="f4dc1-411">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="f4dc1-412">**Nicht abstreitbare Fehler** (126)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-412">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="f4dc1-413">**Aktivität außerhalb der Stunden** (127)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-413">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="f4dc1-414">**Out-of-Service** (128)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-414">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="f4dc1-415">**Verfahrensfehler** (129)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-415">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="f4dc1-416">**Unerwartete Informationen** (130)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-416">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="f4dc1-417">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-417">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f4dc1-418">**Probablecauendescription**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-418">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-419">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-420">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-421">Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Fehler**.**Probableursache**")</span><span class="sxs-lookup"><span data-stu-id="f4dc1-421">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-422">Eine frei Form Zeichenfolge, die die mögliche Ursache des Fehlers beschreibt, wenn die **probablecause** -Eigenschaft auf "1" (sonstige) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-422">A free-form string that describes the probable cause of the error, when the **ProbableCause** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="f4dc1-423">**Empfehlungs Aktionen**</span><span class="sxs-lookup"><span data-stu-id="f4dc1-423">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4dc1-424">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="f4dc1-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f4dc1-425">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f4dc1-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4dc1-426">Ein Array von Freiform-Zeichen folgen, die die empfohlenen Aktionen beschreiben, die zum Beheben des Fehlers ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f4dc1-426">An array of free-form strings that describe the recommended actions to take to resolve the error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4dc1-427">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4dc1-427">Requirements</span></span>



| <span data-ttu-id="f4dc1-428">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4dc1-428">Requirement</span></span> | <span data-ttu-id="f4dc1-429">Wert</span><span class="sxs-lookup"><span data-stu-id="f4dc1-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4dc1-430">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-430">Minimum supported client</span></span><br/> | <span data-ttu-id="f4dc1-431">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f4dc1-431">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f4dc1-432">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4dc1-432">Minimum supported server</span></span><br/> | <span data-ttu-id="f4dc1-433">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4dc1-433">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f4dc1-434">Namespace</span><span class="sxs-lookup"><span data-stu-id="f4dc1-434">Namespace</span></span><br/>                | <span data-ttu-id="f4dc1-435">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f4dc1-435">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f4dc1-436">MOF</span><span class="sxs-lookup"><span data-stu-id="f4dc1-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4dc1-437"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f4dc1-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4dc1-438">DLL</span><span class="sxs-lookup"><span data-stu-id="f4dc1-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4dc1-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f4dc1-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

