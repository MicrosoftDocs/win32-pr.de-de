---
description: Wird verwendet, um detaillierte Status-und Fehlerinformationen zu melden.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: __ExtendedStatus-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350169"
---
# <a name="__extendedstatus-class"></a><span data-ttu-id="b9437-103">\_\_ExtendedStatus-Klasse</span><span class="sxs-lookup"><span data-stu-id="b9437-103">\_\_ExtendedStatus class</span></span>

<span data-ttu-id="b9437-104">Die " **\_ \_ ExtendedStatus** "-System Klasse wird verwendet, um detaillierte Status-und Fehlerinformationen zu melden.</span><span class="sxs-lookup"><span data-stu-id="b9437-104">The **\_\_ExtendedStatus** system class is used to report detailed status and error information.</span></span>

<span data-ttu-id="b9437-105">Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b9437-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b9437-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b9437-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9437-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9437-107">Syntax</span></span>

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="b9437-108">Member</span><span class="sxs-lookup"><span data-stu-id="b9437-108">Members</span></span>

<span data-ttu-id="b9437-109">Die **\_ \_ ExtendedStatus** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b9437-109">The **\_\_ExtendedStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="b9437-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9437-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9437-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b9437-111">Properties</span></span>

<span data-ttu-id="b9437-112">Die **\_ \_ ExtendedStatus** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9437-112">The **\_\_ExtendedStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9437-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b9437-113">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9437-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9437-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9437-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9437-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9437-116">Eine beliebige benutzerdefinierte Zeichenfolge, die einen Fehler-oder Betriebsstatus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b9437-116">Any user-defined string that describes an error or operational status.</span></span>

</dd> <dt>

<span data-ttu-id="b9437-117">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="b9437-117">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9437-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9437-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9437-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9437-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9437-120">Der Vorgang, der zum Zeitpunkt eines Fehlers oder einer Anomalieerkennung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="b9437-120">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="b9437-121">In der Regel legt Windows-Verwaltungsinstrumentation (WMI) diese Eigenschaft auf den Namen einer com-API für die WMI-Methode fest, z. b. die folgende: [**IWbemServices:: kreateinstanceenum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="b9437-121">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

</dd> <dt>

<span data-ttu-id="b9437-122">**Parameter Info**</span><span class="sxs-lookup"><span data-stu-id="b9437-122">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9437-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9437-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9437-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9437-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9437-125">Parameter, die an einem Fehler oder einer Statusänderung beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="b9437-125">Parameters involved in an error or status change.</span></span> <span data-ttu-id="b9437-126">Wenn eine Anwendung z. b. versucht, eine Klasse abzurufen, die nicht vorhanden ist, wird diese Eigenschaft auf den Namen der angreifenden Klasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9437-126">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

</dd> <dt>

<span data-ttu-id="b9437-127">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="b9437-127">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9437-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b9437-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9437-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9437-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9437-130">Identifiziert den Anbieter, der einen Fehler oder eine Statusänderung auslöst oder meldet.</span><span class="sxs-lookup"><span data-stu-id="b9437-130">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="b9437-131">Wenn ein Anbieter nicht beteiligt ist, wird diese Zeichenfolge auf "Windows-Verwaltung" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9437-131">If a provider is not involved, this string is set to "Windows Management".</span></span>

</dd> <dt>

<span data-ttu-id="b9437-132">**Statuscode**</span><span class="sxs-lookup"><span data-stu-id="b9437-132">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9437-133">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b9437-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9437-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b9437-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b9437-135">Enthält einen Fehler-oder Informations Code für einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b9437-135">Contains an error or information code for an operation.</span></span> <span data-ttu-id="b9437-136">Dies kann ein beliebiger Wert sein, der vom Anbieter definiert wird. der Wert 0 (null) ist jedoch normalerweise reserviert, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b9437-136">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="b9437-137">Diese Eigenschaft wird von [**\_ \_ notifystatus**](--notifystatus.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b9437-137">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9437-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9437-138">Remarks</span></span>

<span data-ttu-id="b9437-139">Die **\_ \_ ExtendedStatus** -Klasse wird von der [**\_ \_ notifystatus**](--notifystatus.md) -Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b9437-139">The **\_\_ExtendedStatus** class is derived from the [**\_\_NotifyStatus**](--notifystatus.md) class.</span></span>

<span data-ttu-id="b9437-140">Verwenden Sie die **\_ \_ ExtendedStatus** -Klasse, um Informationen zu melden, die komplexer sind als ein einfacher Ergebniscode.</span><span class="sxs-lookup"><span data-stu-id="b9437-140">Use the **\_\_ExtendedStatus** class to report information that is more complex than a simple result code.</span></span> <span data-ttu-id="b9437-141">Anbieter können Ihre eigenen Klassen von **\_ \_ ExtendedStatus** ableiten, wenn Sie weitere Eigenschaften benötigen, um die Fehler zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b9437-141">Providers can derive their own classes from **\_\_ExtendedStatus** if they require more properties to describe the errors.</span></span>

<span data-ttu-id="b9437-142">Die **Statuscode** -Eigenschaft, die von der übergeordneten [**\_ \_ notifystatus**](--notifystatus.md) -Klasse geerbt wurde, ist eine Ganzzahl ohne Vorzeichen, die den Fehler-oder Statuswert darstellt.</span><span class="sxs-lookup"><span data-stu-id="b9437-142">The **StatusCode** property, inherited from the [**\_\_NotifyStatus**](--notifystatus.md) parent class, is an unsigned integer that represents the error or status value.</span></span> <span data-ttu-id="b9437-143">Wenn Instanzen dieser Klasse von einem dynamischen Anbieter von einer Methode zurückgegeben werden, werden die Eigenschaften " **Statuscode** " und " **Beschreibung** " vom Anbieter festgelegt, und die anderen Eigenschaften werden von WMI festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9437-143">When instances of this class are returned from a method by a dynamic provider, the **StatusCode** and **Description** properties are set by the provider, and the other properties are set by WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="b9437-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9437-144">Examples</span></span>

<span data-ttu-id="b9437-145">Das folgende Codebeispiel stammt aus dem [FND: Behandeln von Configuration Manager asynchronen Fehlern mithilfe von WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript-Codebeispiel in der TechNet Gallery, beschreibt die Verwendung von **\_ \_ ExtendedStatus** zum Abrufen von Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="b9437-145">The following code sample, taken from the [FND:How to Handle Configuration Manager Asynchronous Errors by Using WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript code example on TechNet Gallery, describes using **\_\_ExtendedStatus** to retrieve error information.</span></span>


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a><span data-ttu-id="b9437-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9437-146">Requirements</span></span>



| <span data-ttu-id="b9437-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9437-147">Requirement</span></span> | <span data-ttu-id="b9437-148">Wert</span><span class="sxs-lookup"><span data-stu-id="b9437-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b9437-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9437-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b9437-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9437-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b9437-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9437-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b9437-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9437-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="b9437-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9437-153">Namespace</span></span><br/>                | <span data-ttu-id="b9437-154">Alle WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="b9437-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="b9437-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9437-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9437-156">**\_\_Notifystatus**</span><span class="sxs-lookup"><span data-stu-id="b9437-156">**\_\_NotifyStatus**</span></span>](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[<span data-ttu-id="b9437-157">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="b9437-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

