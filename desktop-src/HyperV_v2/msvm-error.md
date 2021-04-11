---
description: Enthält Informationen über den Schweregrad, die Ursache, Empfohlene Aktionen und andere Daten, die sich auf den Ausfall eines CIM-Vorgangs beziehen.
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Msvm_Error-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b3b30f1d64146db2554d097b11104df09ba018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042329"
---
# <a name="msvm_error-class"></a><span data-ttu-id="9e64d-103">MSVM- \_ Fehler Klasse</span><span class="sxs-lookup"><span data-stu-id="9e64d-103">Msvm\_Error class</span></span>

<span data-ttu-id="9e64d-104">Eine spezialisierte Klasse, die Informationen über den Schweregrad, die Ursache, Empfohlene Aktionen und andere Daten enthält, die sich auf den Ausfall eines CIM-Vorgangs beziehen.</span><span class="sxs-lookup"><span data-stu-id="9e64d-104">A specialized class that contains information about the severity, cause, recommended actions, and other data related to the failure of a CIM Operation.</span></span>

<span data-ttu-id="9e64d-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9e64d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e64d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e64d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
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

## <a name="members"></a><span data-ttu-id="9e64d-107">Member</span><span class="sxs-lookup"><span data-stu-id="9e64d-107">Members</span></span>

<span data-ttu-id="9e64d-108">Die **MSVM- \_ Fehler** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9e64d-108">The **Msvm\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="9e64d-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e64d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e64d-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9e64d-110">Properties</span></span>

<span data-ttu-id="9e64d-111">Die **MSVM- \_ Fehler** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9e64d-111">The **Msvm\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e64d-112">**Cimstatus Code**</span><span class="sxs-lookup"><span data-stu-id="9e64d-112">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-113">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9e64d-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-115">Der CIM-Statuscode, der diese Instanz kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="9e64d-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="9e64d-116">Diese Eigenschaft definiert die Statuscodes, die von einem entsprechenden CIM-Server oder-Listener zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="9e64d-116">This property defines the status codes that may be return by a conforming CIM Server or Listener.</span></span> <span data-ttu-id="9e64d-117">Nicht alle Statuscodes sind für jeden Vorgang gültig.</span><span class="sxs-lookup"><span data-stu-id="9e64d-117">Not all status codes are valid for each operation.</span></span> <span data-ttu-id="9e64d-118">Die Spezifikation für jeden Vorgang sollte die Statuscodes definieren, die von diesem Vorgang zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="9e64d-118">The specification for each operation should define the status codes that may be returned by that operation.</span></span> <span data-ttu-id="9e64d-119">Die folgenden Werte für den CIM-Statuscode sind definiert.</span><span class="sxs-lookup"><span data-stu-id="9e64d-119">The following values for CIM status code are defined.</span></span> <span data-ttu-id="9e64d-120">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-120">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="9e64d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9e64d-121">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="9e64d-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9e64d-122">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <span data-ttu-id="9e64d-123"><dt>**CIM \_ Err \_**</dt> -Fehler <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-123"><dt>**CIM\_ERR\_FAILED**</dt> <dt>1</dt></span></span> </dl>                                                                       | <span data-ttu-id="9e64d-124">Ein allgemeiner Fehler ist aufgetreten, der nicht von einem spezifischeren Fehlercode abgedeckt wird.</span><span class="sxs-lookup"><span data-stu-id="9e64d-124">A general error occurred that is not covered by a more specific error code.</span></span><br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <span data-ttu-id="9e64d-125"><dt>**CIM \_ Err- \_ Zugriff \_ verweigert**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-125"><dt>**CIM\_ERR\_ACCESS\_DENIED**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="9e64d-126">Der Zugriff auf eine CIM-Ressource war für den Client nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e64d-126">Access to a CIM resource was not available to the client.</span></span><br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <span data-ttu-id="9e64d-127"><dt>**CIM \_ Err \_ ungültiger \_ Namespace**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-127"><dt>**CIM\_ERR\_INVALID\_NAMESPACE**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="9e64d-128">Der Ziel Namespace ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-128">The target namespace does not exist.</span></span><br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <span data-ttu-id="9e64d-129"><dt>**CIM \_ \_Ungültiger \_ Parameter**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-129"><dt>**CIM\_ERR\_INVALID\_PARAMETER**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="9e64d-130">Mindestens ein Parameterwert, der an die-Methode übergeben wurde, war ungültig.</span><span class="sxs-lookup"><span data-stu-id="9e64d-130">One or more parameter values passed to the method were invalid.</span></span><br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <span data-ttu-id="9e64d-131"><dt>**CIM \_ Err \_ ungültige \_ Klasse**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-131"><dt>**CIM\_ERR\_INVALID\_CLASS**</dt> <dt>5</dt></span></span> </dl>                                                 | <span data-ttu-id="9e64d-132">Die angegebene Klasse ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-132">The specified class does not exist.</span></span><br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <span data-ttu-id="9e64d-133"><dt>**CIM \_ Err \_ nicht \_ gefunden**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-133"><dt>**CIM\_ERR\_NOT\_FOUND**</dt> <dt>6</dt></span></span> </dl>                                                             | <span data-ttu-id="9e64d-134">Das angeforderte Objekt wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-134">The requested object could not be found.</span></span><br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <span data-ttu-id="9e64d-135"><dt>**CIM \_ Err \_ nicht \_ unterstützt**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-135"><dt>**CIM\_ERR\_NOT\_SUPPORTED**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="9e64d-136">Der angeforderte Vorgang wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-136">The requested operation is not supported.</span></span><br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <span data-ttu-id="9e64d-137"><dt>**CIM \_ Err \_ - \_ Klasse \_ hat**</dt> untergeordnete <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-137"><dt>**CIM\_ERR\_CLASS\_HAS\_CHILDREN**</dt> <dt>8</dt></span></span> </dl>                                 | <span data-ttu-id="9e64d-138">Der Vorgang kann für diese Klasse nicht ausgeführt werden, da Sie über Instanzen verfügt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-138">Operation cannot be carried out on this class because it has instances.</span></span><br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <span data-ttu-id="9e64d-139"><dt>**CIM \_ Err- \_ Klasse \_ hat \_ Instanzen**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-139"><dt>**CIM\_ERR\_CLASS\_HAS\_INSTANCES**</dt> <dt>9</dt></span></span> </dl>                              | <span data-ttu-id="9e64d-140">Der Vorgang kann für diese Klasse nicht ausgeführt werden, da Sie über Instanzen verfügt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-140">Operation cannot be carried out on this class since it has instances.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <span data-ttu-id="9e64d-141"><dt>**CIM \_ Err \_ ungültige \_ Superclass**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-141"><dt>**CIM\_ERR\_INVALID\_SUPERCLASS**</dt> <dt>10</dt></span></span> </dl>                                 | <span data-ttu-id="9e64d-142">Der Vorgang kann nicht ausgeführt werden, da die angegebene übergeordnete Klasse nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e64d-142">Operation cannot be carried out since the specified superclass does not exist.</span></span><br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <span data-ttu-id="9e64d-143"><dt>**CIM \_ Err ist \_ bereits \_ vorhanden**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-143"><dt>**CIM\_ERR\_ALREADY\_EXISTS**</dt> <dt>11</dt></span></span> </dl>                                             | <span data-ttu-id="9e64d-144">Der Vorgang kann nicht ausgeführt werden, da bereits ein Objekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9e64d-144">Operation cannot be carried out because an object already exists.</span></span><br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <span data-ttu-id="9e64d-145"><dt>**CIM \_ Err \_ keine \_ solche \_ Eigenschaft**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-145"><dt>**CIM\_ERR\_NO\_SUCH\_PROPERTY**</dt> <dt>12</dt></span></span> </dl>                                      | <span data-ttu-id="9e64d-146">Die angegebene Eigenschaft ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-146">The specified Property does not exist.</span></span><br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <span data-ttu-id="9e64d-147"><dt>**CIM \_ Err \_ - \_ Typen**</dt> Konflikt <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-147"><dt>**CIM\_ERR\_TYPE\_MISMATCH**</dt> <dt>13</dt></span></span> </dl>                                                | <span data-ttu-id="9e64d-148">Der angegebene Wert ist nicht mit dem Typ kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9e64d-148">The value supplied is incompatible with the type.</span></span><br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <span data-ttu-id="9e64d-149"><dt>**CIM \_ Err- \_ Abfrage \_ Sprache \_ wird 14 nicht \_ unterstützt**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-149"><dt>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED**</dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="9e64d-150">Die Abfragesprache wird nicht erkannt oder nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-150">The query language is not recognized or supported.</span></span><br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <span data-ttu-id="9e64d-151"><dt>**CIM \_ \_Ungültige \_ Abfrage**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-151"><dt>**CIM\_ERR\_INVALID\_QUERY**</dt> <dt>15</dt></span></span> </dl>                                                | <span data-ttu-id="9e64d-152">Die Abfrage ist für die angegebene Abfragesprache ungültig.</span><span class="sxs-lookup"><span data-stu-id="9e64d-152">The query is not valid for the specified query language.</span></span><br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <span data-ttu-id="9e64d-153"><dt>**CIM \_ Err- \_ Methode \_ nicht \_ verfügbar**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-153"><dt>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE**</dt> <dt>16</dt></span></span> </dl>                          | <span data-ttu-id="9e64d-154">Die System externe-Methode konnte nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-154">The extrinsic method could not be executed.</span></span><br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <span data-ttu-id="9e64d-155"><dt>**CIM \_ Err- \_ Methode \_ nicht \_ gefunden**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-155"><dt>**CIM\_ERR\_METHOD\_NOT\_FOUND**</dt> <dt>17</dt></span></span> </dl>                                      | <span data-ttu-id="9e64d-156">Die angegebene System externe-Methode ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-156">The specified extrinsic method does not exist.</span></span><br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <span data-ttu-id="9e64d-157"><dt>**CIM \_ \_Unerwartete \_ Antwort**</dt> 18 nicht erwartet <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-157"><dt>**CIM\_ERR\_UNEXPECTED\_RESPONSE**</dt> <dt>18</dt></span></span> </dl>                              | <span data-ttu-id="9e64d-158">Die zurückgegebene Antwort auf den asynchronen Vorgang wurde nicht erwartet.</span><span class="sxs-lookup"><span data-stu-id="9e64d-158">The returned response to the asynchronous operation was not expected.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <span data-ttu-id="9e64d-159"><dt>**CIM \_ \_Ungültiges \_ Antwort \_ Ziel**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-159"><dt>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION**</dt> <dt>19</dt></span></span> </dl>  | <span data-ttu-id="9e64d-160">Das angegebene Ziel für die asynchrone Antwort ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9e64d-160">The specified destination for the asynchronous response is not valid.</span></span><br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <span data-ttu-id="9e64d-161"><dt>**CIM \_ Der Err- \_ Namespace ist \_ nicht \_ leer**</dt> <dt>20</dt> .</span><span class="sxs-lookup"><span data-stu-id="9e64d-161"><dt>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY**</dt> <dt>20</dt></span></span> </dl>                             | <span data-ttu-id="9e64d-162">Der angegebene Namespace ist nicht leer.</span><span class="sxs-lookup"><span data-stu-id="9e64d-162">The specified namespace is not empty.</span></span><br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="9e64d-163"><dt>**DMTF reserviert**</dt> <dt>21 = *Wert*</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-163"><dt>**DMTF Reserved**</dt> <dt>21 = *value* </dt></span></span> </dl>                            | <span data-ttu-id="9e64d-164">Reservierte Werte.</span><span class="sxs-lookup"><span data-stu-id="9e64d-164">Reserved values.</span></span><br/>                                                               |



 

</dd> <dt>

<span data-ttu-id="9e64d-165">**Cimstatus Code Description**</span><span class="sxs-lookup"><span data-stu-id="9e64d-165">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-166">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e64d-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-168">Eine Zeichenfolge, die eine vom Benutzer lesbare Beschreibung der **cimstatus Code** -Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="9e64d-168">A string containing a user-readable description of the **CIMStatusCode** property.</span></span> <span data-ttu-id="9e64d-169">Diese Beschreibung wird möglicherweise erweitert, muss jedoch mit der Definition von **cimstatus Code** übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9e64d-169">This description may extend, but must be consistent with, the definition of **CIMStatusCode**.</span></span> <span data-ttu-id="9e64d-170">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-170">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9e64d-171">**Errorsource**</span><span class="sxs-lookup"><span data-stu-id="9e64d-171">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-172">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e64d-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-173">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-174">Die identifizierenden Informationen der Entität (die Instanz), die den Fehler erzeugt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-174">The identifying information of the entity (the instance) generating the error.</span></span> <span data-ttu-id="9e64d-175">Wenn diese Entität im CIM-Schema modelliert ist, enthält diese Eigenschaft den Pfad der-Instanz, die als Zeichen folgen Parameter codiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e64d-175">If this entity is modeled in the CIM Schema, this property contains the path of the instance encoded as a string parameter.</span></span> <span data-ttu-id="9e64d-176">Wenn die Eigenschaft nicht modelliert ist, enthält Sie eine Identifikations Zeichenfolge, die die Entität benennt, die den Fehler generiert hat.</span><span class="sxs-lookup"><span data-stu-id="9e64d-176">If not modeled, the property contains some identifying string that names the entity that generated the error.</span></span> <span data-ttu-id="9e64d-177">Der Pfad oder die identifizierende Zeichenfolge wird gemäß der **errorsourceformat** -Eigenschaft formatiert.</span><span class="sxs-lookup"><span data-stu-id="9e64d-177">The path or identifying string is formatted per the **ErrorSourceFormat** property.</span></span> <span data-ttu-id="9e64d-178">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-178">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9e64d-179">**Errorsourceformat**</span><span class="sxs-lookup"><span data-stu-id="9e64d-179">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-180">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e64d-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-181">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-182">Das Format der **errorsource** -Eigenschaft ist basierend auf dem Wert dieser Eigenschaft interpretierbar.</span><span class="sxs-lookup"><span data-stu-id="9e64d-182">The format of the **ErrorSource** property is interpretable based on the value of this property.</span></span> <span data-ttu-id="9e64d-183">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt und immer auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-183">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)), and it is always set to 0.</span></span>



| <span data-ttu-id="9e64d-184">Wert</span><span class="sxs-lookup"><span data-stu-id="9e64d-184">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="9e64d-185">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9e64d-185">Meaning</span></span>                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9e64d-186"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-186"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="9e64d-187">Das Format ist unbekannt oder kann von einer CIM-Client Anwendung nicht sinnvoll interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-187">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span><br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9e64d-188"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="9e64d-189">Das Format wird durch den Wert der **othererrorsourceformat** -Eigenschaft definiert.</span><span class="sxs-lookup"><span data-stu-id="9e64d-189">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span><br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <span data-ttu-id="9e64d-190"><dt>**Cithbjecthandle**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-190"><dt>**CIMObjectHandle**</dt> <dt>2 </dt></span></span> </dl> | <span data-ttu-id="9e64d-191">Ein CIM-Objekt Handle, das mit der MOF-Syntax codiert wird, die für das nicht-Terminal ObjectHandle definiert ist, wird zur Identifizierung der Entität verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e64d-191">A CIM Object Handle, encoded using the MOF syntax defined for the objectHandle non-terminal, is used to identify the entity.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9e64d-192">**ErrorType**</span><span class="sxs-lookup"><span data-stu-id="9e64d-192">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-193">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e64d-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-194">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-195">Primäre Klassifizierung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="9e64d-195">Primary classification of the error.</span></span> <span data-ttu-id="9e64d-196">Die folgenden Werte sind definiert.</span><span class="sxs-lookup"><span data-stu-id="9e64d-196">The following values are defined.</span></span> <span data-ttu-id="9e64d-197">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-197">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="9e64d-198">Wert</span><span class="sxs-lookup"><span data-stu-id="9e64d-198">Value</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="9e64d-199">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9e64d-199">Meaning</span></span>                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9e64d-200"><dt>**Unbekannter**</dt> Wert <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-200"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9e64d-201"><dt>**Sonstige**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-201"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <span data-ttu-id="9e64d-202"><dt>**Kommunikationsfehler**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-202"><dt>**Communications Error**</dt> <dt>2</dt></span></span> </dl>                               | <span data-ttu-id="9e64d-203">Fehler dieses Typs sind hauptsächlich mit den Prozeduren und/oder Prozessen verknüpft, die erforderlich sind, um Informationen von einem Punkt an einen anderen zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="9e64d-203">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span><br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <span data-ttu-id="9e64d-204"><dt>**Quality of Service Fehler**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-204"><dt>**Quality of Service Error**</dt> <dt>3</dt></span></span> </dl>               | <span data-ttu-id="9e64d-205">Fehler dieses Typs sind hauptsächlich mit Fehlern verknüpft, die zu eingeschränkter Funktionalität oder Leistung führen.</span><span class="sxs-lookup"><span data-stu-id="9e64d-205">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span><br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <span data-ttu-id="9e64d-206"><dt>**Software Fehler**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-206"><dt>**Software Error**</dt> <dt>4</dt></span></span> </dl>                                                       | <span data-ttu-id="9e64d-207">Ein Fehler dieses Typs ist hauptsächlich mit einem Software-oder Verarbeitungsfehler verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9e64d-207">Error of this type are principally associated with a software or processing fault.</span></span><br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <span data-ttu-id="9e64d-208"><dt>**Hardware Fehler**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-208"><dt>**Hardware Error**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="9e64d-209">Fehler dieses Typs sind hauptsächlich mit einem Geräte-oder Hardwarefehler verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9e64d-209">Errors of this type are principally associated with an equipment or hardware failure.</span></span><br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <span data-ttu-id="9e64d-210"><dt>**Umgebungs Fehler**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-210"><dt>**Environmental Error**</dt> <dt>6</dt></span></span> </dl>                                   | <span data-ttu-id="9e64d-211">Fehler dieses Typs sind hauptsächlich einer Fehlerbedingung im Zusammenhang mit der Einrichtung oder anderen Umgebungs Überlegungen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9e64d-211">Errors of this type are principally associated with a failure condition relating to the facility, or other environmental considerations.</span></span><br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <span data-ttu-id="9e64d-212"><dt>**Sicherheitsfehler**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-212"><dt>**Security Error**</dt> <dt>7</dt></span></span> </dl>                                                       | <span data-ttu-id="9e64d-213">Fehler dieses Typs sind Sicherheitsverletzungen, Erkennung von Viren und ähnlichen Problemen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9e64d-213">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span><br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <span data-ttu-id="9e64d-214"><dt>**Overabonnementfehler**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-214"><dt>**Oversubscription Error**</dt> <dt>8</dt></span></span> </dl>                       | <span data-ttu-id="9e64d-215">Fehler dieses Typs sind hauptsächlich mit dem Ausfall der Zuordnung ausreichender Ressourcen zum Abschluss des Vorgangs verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9e64d-215">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span><br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <span data-ttu-id="9e64d-216">Nicht <dt>**verfügbarer Ressourcen Fehler**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-216"><dt>**Unavailable Resource Error**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="9e64d-217">Fehler dieses Typs sind hauptsächlich mit dem Fehler beim Zugriff auf eine erforderliche Ressource verbunden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-217">Errors of this type are principally associated with the failure to access a required resource.</span></span><br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <span data-ttu-id="9e64d-218"><dt>**Nicht unterstützter Vorgangs Fehler**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-218"><dt>**Unsupported Operation Error**</dt> <dt>10 </dt></span></span> </dl> | <span data-ttu-id="9e64d-219">Fehler dieses Typs sind hauptsächlich mit nicht unterstützten Anforderungen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="9e64d-219">Errors of this type are principally associated with requests that are not supported.</span></span><br/>                                                          |



 

</dd> <dt>

<span data-ttu-id="9e64d-220">**Meldung**</span><span class="sxs-lookup"><span data-stu-id="9e64d-220">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-221">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e64d-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-222">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-223">Die formatierte Meldung.</span><span class="sxs-lookup"><span data-stu-id="9e64d-223">The formatted message.</span></span> <span data-ttu-id="9e64d-224">Diese Meldung wird erstellt, indem der dynamische Inhalt der Nachricht, die in **messagearguments** beschrieben wird, auf die Format Zeichenfolge angewendet wird, die innerhalb des Gültigkeits Bereichs von **owningentity** durch **MessageId** eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9e64d-224">This message is constructed by applying the dynamic content of the message, described in **MessageArguments**, to the format string uniquely identified, within the scope of the **OwningEntity**, by **MessageID**.</span></span> <span data-ttu-id="9e64d-225">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-225">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9e64d-226">**Messagearguments**</span><span class="sxs-lookup"><span data-stu-id="9e64d-226">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-227">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9e64d-227">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-228">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-229">Ein Array, das den dynamischen Inhalt der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="9e64d-229">An array containing the dynamic content of the message.</span></span> <span data-ttu-id="9e64d-230">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-230">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9e64d-231">**MessageId**</span><span class="sxs-lookup"><span data-stu-id="9e64d-231">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-232">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e64d-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-233">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-234">Eine nicht transparente Zeichenfolge, die innerhalb des Gültigkeits Bereichs von **owningentity** das Format der Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9e64d-234">An opaque string that uniquely identifies, within the scope of the **OwningEntity**, the format of the message.</span></span> <span data-ttu-id="9e64d-235">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-235">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9e64d-236">**Othererrorsourceformat**</span><span class="sxs-lookup"><span data-stu-id="9e64d-236">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-237">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e64d-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-238">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-239">Eine Zeichenfolge, die "andere" Werte für **errorsourceformat** definiert.</span><span class="sxs-lookup"><span data-stu-id="9e64d-239">A string defining "Other" values for **ErrorSourceFormat**.</span></span> <span data-ttu-id="9e64d-240">Dieser Wert muss auf einen Wert ungleich NULL festgelegt werden, wenn **errorsourceformat** auf den Wert 1 (Other) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9e64d-240">This value must be set to a non-NULL value when **ErrorSourceFormat** is set to a value of 1 (Other).</span></span> <span data-ttu-id="9e64d-241">Für alle anderen Werte von **errorsourceformat** muss der Wert dieser Zeichenfolge auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-241">For all other values of **ErrorSourceFormat**, the value of this string must be set to **Null**.</span></span> <span data-ttu-id="9e64d-242">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-242">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9e64d-243">**Othererrortype**</span><span class="sxs-lookup"><span data-stu-id="9e64d-243">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-244">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e64d-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-245">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-246">Eine Zeichenfolge, die den **ErrorType** beschreibt, wenn 1, (Other), als **ErrorType** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e64d-246">A string that describes the **ErrorType** when 1, (Other), is specified as the **ErrorType**.</span></span> <span data-ttu-id="9e64d-247">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-247">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9e64d-248">**Owningentity**</span><span class="sxs-lookup"><span data-stu-id="9e64d-248">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-249">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e64d-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-250">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-251">Eine Zeichenfolge, die die Entität eindeutig identifiziert, die die Definition des Format der in dieser Instanz beschriebenen Meldung besitzt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-251">A string that uniquely identifies the entity that owns the definition of the format of the message described in this instance.</span></span> <span data-ttu-id="9e64d-252">**Owningentity** muss einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder anderweitig eindeutigen Namen enthalten, der im Besitz des Geschäfts Entitäts-oder Standard Texts ist, der das Format definiert.</span><span class="sxs-lookup"><span data-stu-id="9e64d-252">**OwningEntity** must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity or standards body defining the format.</span></span> <span data-ttu-id="9e64d-253">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-253">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9e64d-254">**Wahrnehmgrad**</span><span class="sxs-lookup"><span data-stu-id="9e64d-254">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-255">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e64d-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-256">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-257">Ein Enumerationswert, der den Schweregrad des Fehlers aus der Sicht des Notifizierers beschreibt: 2-niedrig sollte für nicht kritische Probleme wie z. b. ungültige Parameter, falsche Verwendung, nicht unterstützte Funktionalität verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-257">An enumerated value that describes the severity of the error from the notifier's point of view: 2 - Low should be used for noncritical issues such as invalid parameters, incorrect usage, unsupported functionality.</span></span> <span data-ttu-id="9e64d-258">3-Mittel sollte verwendet werden, um anzugeben, dass eine Aktion erforderlich ist, aber die Situation ist zu diesem Zeitpunkt nicht schwerwiegend.</span><span class="sxs-lookup"><span data-stu-id="9e64d-258">3 - Medium should be used to indicate action is needed, but the situation is not serious at this time.</span></span> <span data-ttu-id="9e64d-259">4-High sollte verwendet werden, um anzugeben, dass jetzt eine Aktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9e64d-259">4 - High should be used to indicate action is needed now.</span></span> <span data-ttu-id="9e64d-260">5-schwerwiegend sollte verwendet werden, um einen Datenverlust oder nicht BEHEB baren System-oder Dienst Fehler anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9e64d-260">5 - Fatal should be used to indicate a loss of data or unrecoverable system or service failure.</span></span> <span data-ttu-id="9e64d-261">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-261">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9e64d-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9e64d-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (2)</span><span class="sxs-lookup"><span data-stu-id="9e64d-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Mittel** (3)</span><span class="sxs-lookup"><span data-stu-id="9e64d-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (4)</span><span class="sxs-lookup"><span data-stu-id="9e64d-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>Schwer **wiegend (5** )</span><span class="sxs-lookup"><span data-stu-id="9e64d-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Fatal** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9e64d-267">**Probableursache**</span><span class="sxs-lookup"><span data-stu-id="9e64d-267">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-268">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e64d-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-269">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-270">Ein Enumerationswert, der die mögliche Ursache des Fehlers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-270">An enumerated value that describes the probable cause of the error.</span></span> <span data-ttu-id="9e64d-271">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-271">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9e64d-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="9e64d-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="9e64d-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Adapter-/Kartenfehler** (2)</span><span class="sxs-lookup"><span data-stu-id="9e64d-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Adapter/Card Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Fehler des Anwendungs Subsystems** (3)</span><span class="sxs-lookup"><span data-stu-id="9e64d-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Application Subsystem Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Reduzierte Bandbreite** (4)</span><span class="sxs-lookup"><span data-stu-id="9e64d-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Bandwidth Reduced** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Fehler bei der Verbindungs Herstellung** (5)</span><span class="sxs-lookup"><span data-stu-id="9e64d-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Connection Establishment Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Kommunikationsprotokoll Fehler** (6)</span><span class="sxs-lookup"><span data-stu-id="9e64d-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Communications Protocol Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Kommunikations Subsystem-Fehler** (7)</span><span class="sxs-lookup"><span data-stu-id="9e64d-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Communications Subsystem Failure** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Konfigurations-/Anpassungsfehler** (8)</span><span class="sxs-lookup"><span data-stu-id="9e64d-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Configuration/Customization Error** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Überlastung** (9)</span><span class="sxs-lookup"><span data-stu-id="9e64d-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestion** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>Beschädigte **Daten** (10)</span><span class="sxs-lookup"><span data-stu-id="9e64d-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Corrupt Data** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**Limit für CPU-Zyklen überschritten** (11)</span><span class="sxs-lookup"><span data-stu-id="9e64d-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**CPU Cycles Limit Exceeded** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**DataSet/Modem-Fehler** (12)</span><span class="sxs-lookup"><span data-stu-id="9e64d-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Dataset/Modem Error** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>Herunter gestufter **Signal** (13)</span><span class="sxs-lookup"><span data-stu-id="9e64d-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Degraded Signal** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE-Schnittstellen Fehler** (14)</span><span class="sxs-lookup"><span data-stu-id="9e64d-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE Interface Error** (14)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Gehäuse Tür geöffnet** (15)</span><span class="sxs-lookup"><span data-stu-id="9e64d-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Enclosure Door Open** (15)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Geräte** Fehler (16)</span><span class="sxs-lookup"><span data-stu-id="9e64d-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Equipment Malfunction** (16)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Übermäßige Vibrationen** (17)</span><span class="sxs-lookup"><span data-stu-id="9e64d-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Excessive Vibration** (17)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**Datei Format Fehler** (18)</span><span class="sxs-lookup"><span data-stu-id="9e64d-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**File Format Error** (18)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Feuer erkannt** (19)</span><span class="sxs-lookup"><span data-stu-id="9e64d-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire Detected** (19)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>Über **Flutung erkannt** (20)</span><span class="sxs-lookup"><span data-stu-id="9e64d-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Flood Detected** (20)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Rahmen Fehler** (21)</span><span class="sxs-lookup"><span data-stu-id="9e64d-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Framing Error** (21)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC-Problem** (22)</span><span class="sxs-lookup"><span data-stu-id="9e64d-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC Problem** (22)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Feuchtigkeit nicht akzeptabel** (23)</span><span class="sxs-lookup"><span data-stu-id="9e64d-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Humidity Unacceptable** (23)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>E **/a-Gerätefehler** (24)</span><span class="sxs-lookup"><span data-stu-id="9e64d-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**I/O Device Error** (24)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Eingabegeräte Fehler** (25)</span><span class="sxs-lookup"><span data-stu-id="9e64d-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Input Device Error** (25)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**LAN-Fehler** (26)</span><span class="sxs-lookup"><span data-stu-id="9e64d-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**LAN Error** (26)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>Es wurde ein **nicht giftiger Leck erkannt** (27)</span><span class="sxs-lookup"><span data-stu-id="9e64d-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Non-Toxic Leak Detected** (27)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Fehler beim übertragen lokaler Knoten** (28)</span><span class="sxs-lookup"><span data-stu-id="9e64d-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Local Node Transmission Error** (28)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Verlust von Frame** (29)</span><span class="sxs-lookup"><span data-stu-id="9e64d-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Loss of Frame** (29)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Verlust von Signal** (30)</span><span class="sxs-lookup"><span data-stu-id="9e64d-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Loss of Signal** (30)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**31.31. Material ist erschöpft** (31)</span><span class="sxs-lookup"><span data-stu-id="9e64d-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 Material Supply Exhausted** (31)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Multiplexer-Problem** (32)</span><span class="sxs-lookup"><span data-stu-id="9e64d-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Multiplexer Problem** (32)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Nicht** genügend Arbeitsspeicher (33)</span><span class="sxs-lookup"><span data-stu-id="9e64d-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Out of Memory** (33)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Ausgabegeräte Fehler** (34)</span><span class="sxs-lookup"><span data-stu-id="9e64d-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Output Device Error** (34)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>Beeinträchtigung der **Leistung** (35)</span><span class="sxs-lookup"><span data-stu-id="9e64d-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Performance Degraded** (35)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Energie Problem** (36)</span><span class="sxs-lookup"><span data-stu-id="9e64d-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Power Problem** (36)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Unzulässiger Druck** (37)</span><span class="sxs-lookup"><span data-stu-id="9e64d-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressure Unacceptable** (37)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Prozessor Problem (interner Computerfehler)** (38)</span><span class="sxs-lookup"><span data-stu-id="9e64d-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Processor Problem (Internal Machine Error)** (38)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Pump Fehler** (39)</span><span class="sxs-lookup"><span data-stu-id="9e64d-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Pump Failure** (39)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Warteschlangen Größe überschritten** (40)</span><span class="sxs-lookup"><span data-stu-id="9e64d-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Queue Size Exceeded** (40)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Empfangs Fehler** (41)</span><span class="sxs-lookup"><span data-stu-id="9e64d-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Receive Failure** (41)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Empfänger Fehler** (42)</span><span class="sxs-lookup"><span data-stu-id="9e64d-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Receiver Failure** (42)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Remote Knoten-Übertragungsfehler** (43)</span><span class="sxs-lookup"><span data-stu-id="9e64d-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Remote Node Transmission Error** (43)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Ressource mit oder fast der Kapazität** (44)</span><span class="sxs-lookup"><span data-stu-id="9e64d-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Resource at or Nearing Capacity** (44)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Antwortzeit übertrieben** (45)</span><span class="sxs-lookup"><span data-stu-id="9e64d-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Response Time Excessive** (45)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Datenübertragungs Rate übermäßig** hoch (46)</span><span class="sxs-lookup"><span data-stu-id="9e64d-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Retransmission Rate Excessive** (46)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Fehler** (47)</span><span class="sxs-lookup"><span data-stu-id="9e64d-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (47)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>Das **Software Programm wurde abgebrochen** (48).</span><span class="sxs-lookup"><span data-stu-id="9e64d-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Software Program Abnormally Terminated** (48)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Software Programmfehler (falsche Ergebnisse)** (49)</span><span class="sxs-lookup"><span data-stu-id="9e64d-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Software Program Error (Incorrect Results)** (49)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Speicher Kapazitäts Problem** (50)</span><span class="sxs-lookup"><span data-stu-id="9e64d-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperatur unzulässig** (51)</span><span class="sxs-lookup"><span data-stu-id="9e64d-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperature Unacceptable** (51)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Schwellenwert überschritten** (52)</span><span class="sxs-lookup"><span data-stu-id="9e64d-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Threshold Crossed** (52)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Zeit Steuerungs Problem** (53)</span><span class="sxs-lookup"><span data-stu-id="9e64d-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Timing Problem** (53)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>Es wurde ein **giftiger Leck erkannt** (54)</span><span class="sxs-lookup"><span data-stu-id="9e64d-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Toxic Leak Detected** (54)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Übertragungsfehler** (55)</span><span class="sxs-lookup"><span data-stu-id="9e64d-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Transmit Failure** (55)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>Übertragungs **Fehler** (56)</span><span class="sxs-lookup"><span data-stu-id="9e64d-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Transmitter Failure** (56)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Zugrunde liegende Ressource nicht verfügbar** (57)</span><span class="sxs-lookup"><span data-stu-id="9e64d-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Underlying Resource Unavailable** (57)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Versions** Konflikt (58)</span><span class="sxs-lookup"><span data-stu-id="9e64d-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Version Mismatch** (58)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Vorherige Warnung gelöscht** (59)</span><span class="sxs-lookup"><span data-stu-id="9e64d-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**60-Anmeldeversuche fehlgeschlagen** (60)</span><span class="sxs-lookup"><span data-stu-id="9e64d-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//60 Login Attempts Failed** (60)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Software Viren erkannt** (61)</span><span class="sxs-lookup"><span data-stu-id="9e64d-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Software Virus Detected** (61)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Hardware Sicherheits** Verletzung (62)</span><span class="sxs-lookup"><span data-stu-id="9e64d-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Hardware Security Breached** (62)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denial-of-Service erkannt** (63)</span><span class="sxs-lookup"><span data-stu-id="9e64d-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denial of Service Detected** (63)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>Nicht übereinstimmende **Sicherheits** Anmelde Informationen (64)</span><span class="sxs-lookup"><span data-stu-id="9e64d-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Security Credential Mismatch** (64)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>Nicht **autorisierter Zugriff** (65)</span><span class="sxs-lookup"><span data-stu-id="9e64d-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Unauthorized Access** (65)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarm empfangen** (66)</span><span class="sxs-lookup"><span data-stu-id="9e64d-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarm Received** (66)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Verlust des Zeigers** (67)</span><span class="sxs-lookup"><span data-stu-id="9e64d-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Loss of Pointer** (67)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Nutzlast nicht überein** Stimmungen (68)</span><span class="sxs-lookup"><span data-stu-id="9e64d-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Payload Mismatch** (68)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Übertragungsfehler** (69)</span><span class="sxs-lookup"><span data-stu-id="9e64d-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Transmission Error** (69)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Übermäßige Fehler Rate** (70)</span><span class="sxs-lookup"><span data-stu-id="9e64d-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Excessive Error Rate** (70)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>Ablauf **Verfolgungs Problem** (71)</span><span class="sxs-lookup"><span data-stu-id="9e64d-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Trace Problem** (71)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Element nicht verfügbar** (72)</span><span class="sxs-lookup"><span data-stu-id="9e64d-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Element Unavailable** (72)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>Das **Element fehlt** (73).</span><span class="sxs-lookup"><span data-stu-id="9e64d-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Element Missing** (73)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Verlust von Multiframe** (74)</span><span class="sxs-lookup"><span data-stu-id="9e64d-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Loss of Multi Frame** (74)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Übertragungskanal Fehler** (75)</span><span class="sxs-lookup"><span data-stu-id="9e64d-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Broadcast Channel Failure** (75)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Ungültige Nachricht empfangen** (76)</span><span class="sxs-lookup"><span data-stu-id="9e64d-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Invalid Message Received** (76)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Routing Fehler** (77)</span><span class="sxs-lookup"><span data-stu-id="9e64d-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Routing Failure** (77)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Backplane-Fehler** (78)</span><span class="sxs-lookup"><span data-stu-id="9e64d-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Backplane Failure** (78)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Bezeichnerduplizierung** (79)</span><span class="sxs-lookup"><span data-stu-id="9e64d-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Identifier Duplication** (79)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Fehler beim Schutz Pfad** (80).</span><span class="sxs-lookup"><span data-stu-id="9e64d-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Protection Path Failure** (80)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Synchronisierungs Verlust oder nicht überein** stimmende (81)</span><span class="sxs-lookup"><span data-stu-id="9e64d-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Sync Loss or Mismatch** (81)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Terminal Problem** (82)</span><span class="sxs-lookup"><span data-stu-id="9e64d-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Terminal Problem** (82)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Echt Zeit Taktfehler** (83)</span><span class="sxs-lookup"><span data-stu-id="9e64d-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Real Time Clock Failure** (83)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Antennen Fehler** (84)</span><span class="sxs-lookup"><span data-stu-id="9e64d-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Antenna Failure** (84)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Akku Ladefehler** (85)</span><span class="sxs-lookup"><span data-stu-id="9e64d-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Battery Charging Failure** (85)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>Datenträger **Fehler** (86)</span><span class="sxs-lookup"><span data-stu-id="9e64d-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Disk Failure** (86)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Frequency Spring failure-Fehler** (87)</span><span class="sxs-lookup"><span data-stu-id="9e64d-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Frequency Hopping Failure** (87)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Verlust der Redundanz** (88)</span><span class="sxs-lookup"><span data-stu-id="9e64d-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Loss of Redundancy** (88)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Stromversorgung-Fehler** (89)</span><span class="sxs-lookup"><span data-stu-id="9e64d-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Power Supply Failure** (89)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Signal Qualitäts Problem** (90)</span><span class="sxs-lookup"><span data-stu-id="9e64d-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Signal Quality Problem** (90)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**91 Akku Entladung** (91)</span><span class="sxs-lookup"><span data-stu-id="9e64d-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 Battery Discharging** (91)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Akku Fehler** (92)</span><span class="sxs-lookup"><span data-stu-id="9e64d-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Battery Failure** (92)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Kommerzielles Energie Problem** (93)</span><span class="sxs-lookup"><span data-stu-id="9e64d-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Commercial Power Problem** (93)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Lüfterfehler** (94)</span><span class="sxs-lookup"><span data-stu-id="9e64d-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Fan Failure** (94)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Engine-Fehler** (95)</span><span class="sxs-lookup"><span data-stu-id="9e64d-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Engine Failure** (95)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Sensor Fehler** (96)</span><span class="sxs-lookup"><span data-stu-id="9e64d-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Sensor Failure** (96)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Fuse-Fehler** (97)</span><span class="sxs-lookup"><span data-stu-id="9e64d-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Fuse Failure** (97)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Generator Fehler** (98)</span><span class="sxs-lookup"><span data-stu-id="9e64d-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Generator Failure** (98)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Niedrige Akku** Kapazität (99)</span><span class="sxs-lookup"><span data-stu-id="9e64d-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Low Battery** (99)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Niedriges Benzin** (100)</span><span class="sxs-lookup"><span data-stu-id="9e64d-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Low Fuel** (100)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Niedriges Wasser** (101)</span><span class="sxs-lookup"><span data-stu-id="9e64d-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Low Water** (101)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Explosiver Gas** (102)</span><span class="sxs-lookup"><span data-stu-id="9e64d-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Explosive Gas** (102)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**Hohe Wind** Vorgänge (103)</span><span class="sxs-lookup"><span data-stu-id="9e64d-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**High Winds** (103)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice-BUILDUP** (104)</span><span class="sxs-lookup"><span data-stu-id="9e64d-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice Buildup** (104)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Rauch** (105)</span><span class="sxs-lookup"><span data-stu-id="9e64d-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Smoke** (105)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>Arbeits **Speicher stimmt nicht überein** (106).</span><span class="sxs-lookup"><span data-stu-id="9e64d-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Memory Mismatch** (106)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Nicht genügend CPU-Zyklen** (107)</span><span class="sxs-lookup"><span data-stu-id="9e64d-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Out of CPU Cycles** (107)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Software Umgebungs Problem** (108)</span><span class="sxs-lookup"><span data-stu-id="9e64d-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Software Environment Problem** (108)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Fehler beim Software Download** (109).</span><span class="sxs-lookup"><span data-stu-id="9e64d-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Software Download Failure** (109)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>Das **Element wurde erneut initialisiert** (110).</span><span class="sxs-lookup"><span data-stu-id="9e64d-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Element Reinitialized** (110)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)</span><span class="sxs-lookup"><span data-stu-id="9e64d-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Protokollierungs Probleme** (112)</span><span class="sxs-lookup"><span data-stu-id="9e64d-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Logging Problems** (112)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>Der **Leck wurde erkannt** (113).</span><span class="sxs-lookup"><span data-stu-id="9e64d-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Leak Detected** (113)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Fehler beim Schutzmechanismus** (114).</span><span class="sxs-lookup"><span data-stu-id="9e64d-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Protection Mechanism Failure** (114)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**115 schützen von Ressourcen Fehlern** (115)</span><span class="sxs-lookup"><span data-stu-id="9e64d-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Protecting Resource Failure** (115)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Daten Bank Inkonsistenz** (116)</span><span class="sxs-lookup"><span data-stu-id="9e64d-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Database Inconsistency** (116)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Authentifizierungsfehler** (117)</span><span class="sxs-lookup"><span data-stu-id="9e64d-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Authentication Failure** (117)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Verletzung der Vertraulichkeit** (118)</span><span class="sxs-lookup"><span data-stu-id="9e64d-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Breach of Confidentiality** (118)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Kabel Manipulations** Funktion (119)</span><span class="sxs-lookup"><span data-stu-id="9e64d-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Cable Tamper** (119)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Verzögerte Informationen** (120)</span><span class="sxs-lookup"><span data-stu-id="9e64d-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Delayed Information** (120)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Doppelte Informationen** (121)</span><span class="sxs-lookup"><span data-stu-id="9e64d-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Duplicate Information** (121)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Fehlende Informationen** (122)</span><span class="sxs-lookup"><span data-stu-id="9e64d-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Information Missing** (122)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Informations Änderung** (123)</span><span class="sxs-lookup"><span data-stu-id="9e64d-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Information Modification** (123)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Informationen außerhalb der Reihenfolge** (124)</span><span class="sxs-lookup"><span data-stu-id="9e64d-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Information Out of Sequence** (124)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>Der **Schlüssel ist abgelaufen** (125).</span><span class="sxs-lookup"><span data-stu-id="9e64d-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Key Expired** (125)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Nicht abstreitbare Fehler** (126)</span><span class="sxs-lookup"><span data-stu-id="9e64d-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Non-Repudiation Failure** (126)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Aktivität außerhalb der Stunden** (127)</span><span class="sxs-lookup"><span data-stu-id="9e64d-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Out of Hours Activity** (127)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Out-of-Service** (128)</span><span class="sxs-lookup"><span data-stu-id="9e64d-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Out of Service** (128)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Verfahrensfehler** (129)</span><span class="sxs-lookup"><span data-stu-id="9e64d-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Procedural Error** (129)</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Unerwartete Informationen** (130)</span><span class="sxs-lookup"><span data-stu-id="9e64d-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Unexpected Information** (130 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9e64d-403">**Probablecauendescription**</span><span class="sxs-lookup"><span data-stu-id="9e64d-403">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-404">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9e64d-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-405">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-406">Eine Zeichenfolge, die die mögliche Ursache des Fehlers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-406">A string that describes the probable cause of the error.</span></span> <span data-ttu-id="9e64d-407">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-407">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="9e64d-408">**Empfehlungs Aktionen**</span><span class="sxs-lookup"><span data-stu-id="9e64d-408">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e64d-409">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="9e64d-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9e64d-410">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9e64d-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e64d-411">Eine Zeichenfolge, die empfohlene Maßnahmen zum Beheben des Fehlers beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-411">A string that describes recommended actions to take to resolve the error.</span></span> <span data-ttu-id="9e64d-412">Diese Eigenschaft wird vom [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="9e64d-412">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e64d-413">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e64d-413">Remarks</span></span>

<span data-ttu-id="9e64d-414">Der Zugriff auf die **MSVM- \_ Fehler** Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="9e64d-414">Access to the **Msvm\_Error** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9e64d-415">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9e64d-415">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e64d-416">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e64d-416">Requirements</span></span>



| <span data-ttu-id="9e64d-417">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e64d-417">Requirement</span></span> | <span data-ttu-id="9e64d-418">Wert</span><span class="sxs-lookup"><span data-stu-id="9e64d-418">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e64d-419">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e64d-419">Minimum supported client</span></span><br/> | <span data-ttu-id="9e64d-420">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e64d-420">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9e64d-421">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e64d-421">Minimum supported server</span></span><br/> | <span data-ttu-id="9e64d-422">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e64d-422">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e64d-423">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e64d-423">Namespace</span></span><br/>                | <span data-ttu-id="9e64d-424">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9e64d-424">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9e64d-425">MOF</span><span class="sxs-lookup"><span data-stu-id="9e64d-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e64d-426"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-426"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e64d-427">DLL</span><span class="sxs-lookup"><span data-stu-id="9e64d-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e64d-428"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9e64d-428"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9e64d-429">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e64d-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e64d-430">**CIM- \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="9e64d-430">**CIM\_Error**</span></span>](cim-error.md)
</dt> <dt>

<span data-ttu-id="9e64d-431">[**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e64d-431">[**CIM\_Error**](/previous-versions//cc150671(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9e64d-432">Verwaltungs Klassen für virtuelle Systeme</span><span class="sxs-lookup"><span data-stu-id="9e64d-432">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

