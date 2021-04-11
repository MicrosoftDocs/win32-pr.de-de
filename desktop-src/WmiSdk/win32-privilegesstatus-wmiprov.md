---
description: Win32 \_ privilegesstatus &\# 8194; Die WMI-Klasse meldet Informationen zu den Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind. Sie kann zurückgegeben werden, wenn ein Vorgang fehlgeschlagen ist oder wenn eine teilweise aufgefüllte Instanz zurückgegeben wurde.
ms.assetid: 85bda855-1488-4d7a-99ed-798e9859fef7
ms.tgt_platform: multiple
title: Win32_PrivilegesStatus-Klasse (WMI)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 658803be4e70849531bf52e7368e4e9cbcc2f0a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218473"
---
# <a name="win32_privilegesstatus-class-wmi"></a><span data-ttu-id="dc052-104">Win32_PrivilegesStatus-Klasse (WMI)</span><span class="sxs-lookup"><span data-stu-id="dc052-104">Win32_PrivilegesStatus class (WMI)</span></span>

<span data-ttu-id="dc052-105">Die **Win32 \_ privilegesstatus**-[WMI-Klasse](retrieving-a-class.md) meldet Informationen zu den Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind.   </span><span class="sxs-lookup"><span data-stu-id="dc052-105">The **Win32\_PrivilegesStatus**   [WMI class](retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="dc052-106">Sie kann zurückgegeben werden, wenn ein Vorgang fehlgeschlagen ist oder wenn eine teilweise aufgefüllte Instanz zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="dc052-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="dc052-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc052-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dc052-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="dc052-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc052-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc052-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}")]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a><span data-ttu-id="dc052-110">Member</span><span class="sxs-lookup"><span data-stu-id="dc052-110">Members</span></span>

<span data-ttu-id="dc052-111">Die **Win32 \_ privilegesstatus** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="dc052-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="dc052-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc052-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc052-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="dc052-113">Properties</span></span>

<span data-ttu-id="dc052-114">Die **Win32 \_ privilegesstatus** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc052-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc052-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dc052-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc052-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc052-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc052-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc052-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc052-118">Eine beliebige benutzerdefinierte Zeichenfolge, die einen Fehler-oder Betriebsstatus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="dc052-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="dc052-119">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](--extendedstatus.md)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc052-119">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc052-120">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="dc052-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc052-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc052-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc052-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc052-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc052-123">Der Vorgang, der zum Zeitpunkt eines Fehlers oder einer Anomalieerkennung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="dc052-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="dc052-124">In der Regel legt Windows-Verwaltungsinstrumentation (WMI) diese Eigenschaft auf den Namen einer com-API für die WMI-Methode fest, z. b. die folgende: [**IWbemServices:: kreateinstanceenum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="dc052-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="dc052-125">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](--extendedstatus.md)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc052-125">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc052-126">**Parameter Info**</span><span class="sxs-lookup"><span data-stu-id="dc052-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc052-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc052-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc052-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc052-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc052-129">Parameter, die an einem Fehler oder einer Statusänderung beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="dc052-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="dc052-130">Wenn eine Anwendung z. b. versucht, eine Klasse abzurufen, die nicht vorhanden ist, wird diese Eigenschaft auf den Namen der angreifenden Klasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dc052-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="dc052-131">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](--extendedstatus.md)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc052-131">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc052-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="dc052-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc052-133">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="dc052-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc052-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc052-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc052-135">Auflisten der erforderlichen Zugriffsberechtigungen für einen Vorgang fehlt.</span><span class="sxs-lookup"><span data-stu-id="dc052-135">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="dc052-136">Die Zugriffs Berechtigungs Typen finden Sie unter den Windows-Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="dc052-136">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="dc052-137">Beispiel: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="dc052-137">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="dc052-138">**Privilegigesrequired**</span><span class="sxs-lookup"><span data-stu-id="dc052-138">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc052-139">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="dc052-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc052-140">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc052-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc052-141">Auflisten aller Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dc052-141">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="dc052-142">Dies schließt Werte aus der **PrivilegesNotHeld** -Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="dc052-142">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="dc052-143">Beispiel: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="dc052-143">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="dc052-144">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="dc052-144">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc052-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dc052-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc052-146">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc052-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc052-147">Identifiziert den Anbieter, der einen Fehler oder eine Statusänderung auslöst oder meldet.</span><span class="sxs-lookup"><span data-stu-id="dc052-147">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="dc052-148">Wenn ein Anbieter nicht beteiligt ist, wird diese Zeichenfolge auf "Windows-Verwaltung" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dc052-148">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="dc052-149">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](--extendedstatus.md)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc052-149">This property is inherited from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc052-150">**Statuscode**</span><span class="sxs-lookup"><span data-stu-id="dc052-150">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc052-151">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc052-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc052-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="dc052-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc052-153">Enthält einen Fehler-oder Informations Code für einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="dc052-153">Contains an error or information code for an operation.</span></span> <span data-ttu-id="dc052-154">Dies kann ein beliebiger Wert sein, der vom Anbieter definiert wird. der Wert 0 (null) ist jedoch normalerweise reserviert, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="dc052-154">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="dc052-155">Diese Eigenschaft wird von [**\_ \_ notifystatus**](--notifystatus.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="dc052-155">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc052-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc052-156">Remarks</span></span>

<span data-ttu-id="dc052-157">Die **Win32 \_ privilegesstatus** -Klasse wird von [**\_ \_ ExtendedStatus**](--extendedstatus.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="dc052-157">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc052-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc052-158">Requirements</span></span>



| <span data-ttu-id="dc052-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc052-159">Requirement</span></span> | <span data-ttu-id="dc052-160">Wert</span><span class="sxs-lookup"><span data-stu-id="dc052-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dc052-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc052-161">Minimum supported client</span></span><br/> | <span data-ttu-id="dc052-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc052-162">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="dc052-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc052-163">Minimum supported server</span></span><br/> | <span data-ttu-id="dc052-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc052-164">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="dc052-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="dc052-165">Namespace</span></span><br/>                | <span data-ttu-id="dc052-166">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="dc052-166">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="dc052-167">MOF</span><span class="sxs-lookup"><span data-stu-id="dc052-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc052-168"><dt>WMI. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="dc052-168"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc052-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc052-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc052-170">**\_\_Erweiterdedstatus**</span><span class="sxs-lookup"><span data-stu-id="dc052-170">**\_\_ExtendedStatus**</span></span>](--extendedstatus.md)
</dt> </dl>

 

 




