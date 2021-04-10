---
description: Win32 \_ privilegesstatus&\# 8194; Die WMI-Klasse meldet Informationen zu den Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind. Sie kann zurückgegeben werden, wenn ein Vorgang fehlgeschlagen ist oder wenn eine teilweise aufgefüllte Instanz zurückgegeben wurde.
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: Win32_PrivilegesStatus-Klasse (cimwin32-WMI-Anbieter)
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
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab399ce08374a954b3bbc015cfee7b4d20167b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861168"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a><span data-ttu-id="1096c-104">Win32_PrivilegesStatus-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="1096c-104">Win32_PrivilegesStatus class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1096c-105">Die **Win32 \_ privilegesstatus**- [WMI-Klasse](../wmisdk/retrieving-a-class.md) meldet Informationen zu den Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1096c-105">The **Win32\_PrivilegesStatus** [WMI class](../wmisdk/retrieving-a-class.md) reports information about privileges required to complete an operation.</span></span> <span data-ttu-id="1096c-106">Sie kann zurückgegeben werden, wenn ein Vorgang fehlgeschlagen ist oder wenn eine teilweise aufgefüllte Instanz zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1096c-106">It may be returned when an operation failed or when a partially populated instance has been returned.</span></span>

<span data-ttu-id="1096c-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1096c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1096c-108">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="1096c-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1096c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1096c-109">Syntax</span></span>

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
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

## <a name="members"></a><span data-ttu-id="1096c-110">Member</span><span class="sxs-lookup"><span data-stu-id="1096c-110">Members</span></span>

<span data-ttu-id="1096c-111">Die **Win32 \_ privilegesstatus** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1096c-111">The **Win32\_PrivilegesStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="1096c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1096c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1096c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1096c-113">Properties</span></span>

<span data-ttu-id="1096c-114">Die **Win32 \_ privilegesstatus** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1096c-114">The **Win32\_PrivilegesStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1096c-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1096c-115">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1096c-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1096c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1096c-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1096c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1096c-118">Eine beliebige benutzerdefinierte Zeichenfolge, die einen Fehler-oder Betriebsstatus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1096c-118">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="1096c-119">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="1096c-119">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="1096c-120">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="1096c-120">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1096c-121">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1096c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1096c-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1096c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1096c-123">Der Vorgang, der zum Zeitpunkt eines Fehlers oder einer Anomalieerkennung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="1096c-123">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="1096c-124">In der Regel legt Windows-Verwaltungsinstrumentation (WMI) diese Eigenschaft auf den Namen einer com-API für die WMI-Methode fest, z. b. die folgende: [**IWbemServices:: kreateinstanceenum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="1096c-124">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="1096c-125">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="1096c-125">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="1096c-126">**Parameter Info**</span><span class="sxs-lookup"><span data-stu-id="1096c-126">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1096c-127">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1096c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1096c-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1096c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1096c-129">Parameter, die an einem Fehler oder einer Statusänderung beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="1096c-129">Parameters involved in an error or status change.</span></span> <span data-ttu-id="1096c-130">Wenn eine Anwendung z. b. versucht, eine Klasse abzurufen, die nicht vorhanden ist, wird diese Eigenschaft auf den Namen der angreifenden Klasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1096c-130">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="1096c-131">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="1096c-131">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="1096c-132">**PrivilegesNotHeld**</span><span class="sxs-lookup"><span data-stu-id="1096c-132">**PrivilegesNotHeld**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1096c-133">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1096c-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1096c-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1096c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1096c-135">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT-Privilegien")</span><span class="sxs-lookup"><span data-stu-id="1096c-135">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="1096c-136">Auflisten der erforderlichen Zugriffsberechtigungen für einen Vorgang fehlt.</span><span class="sxs-lookup"><span data-stu-id="1096c-136">Listing required access privileges missing to complete an operation.</span></span> <span data-ttu-id="1096c-137">Die Zugriffs Berechtigungs Typen finden Sie unter den Windows-Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="1096c-137">The types of access privileges can be found under the Windows Privileges.</span></span>

<span data-ttu-id="1096c-138">Beispiel: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="1096c-138">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="1096c-139">**Privilegigesrequired**</span><span class="sxs-lookup"><span data-stu-id="1096c-139">**PrivilegesRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1096c-140">Datentyp: **Zeichen** folgen Array</span><span class="sxs-lookup"><span data-stu-id="1096c-140">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1096c-141">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1096c-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1096c-142">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT-Privilegien")</span><span class="sxs-lookup"><span data-stu-id="1096c-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|AccessControl\|Windows NT Privileges")</span></span>
</dt> </dl>

<span data-ttu-id="1096c-143">Auflisten aller Berechtigungen, die zum Ausführen eines Vorgangs erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1096c-143">Listing of all of the privileges required to perform an operation.</span></span> <span data-ttu-id="1096c-144">Dies schließt Werte aus der **PrivilegesNotHeld** -Eigenschaft ein.</span><span class="sxs-lookup"><span data-stu-id="1096c-144">This includes values from the **PrivilegesNotHeld** property.</span></span>

<span data-ttu-id="1096c-145">Beispiel: "SE \_ Shutdown \_ Name"</span><span class="sxs-lookup"><span data-stu-id="1096c-145">Example: "SE\_SHUTDOWN\_NAME"</span></span>

</dd> <dt>

<span data-ttu-id="1096c-146">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="1096c-146">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1096c-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1096c-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1096c-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1096c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1096c-149">Identifiziert den Anbieter, der einen Fehler oder eine Statusänderung auslöst oder meldet.</span><span class="sxs-lookup"><span data-stu-id="1096c-149">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="1096c-150">Wenn ein Anbieter nicht beteiligt ist, wird diese Zeichenfolge auf "Windows-Verwaltung" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1096c-150">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="1096c-151">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="1096c-151">This property is inherited from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

</dd> <dt>

<span data-ttu-id="1096c-152">**Statuscode**</span><span class="sxs-lookup"><span data-stu-id="1096c-152">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1096c-153">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1096c-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1096c-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1096c-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1096c-155">Enthält einen Fehler-oder Informations Code für einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1096c-155">Contains an error or information code for an operation.</span></span> <span data-ttu-id="1096c-156">Dies kann ein beliebiger Wert sein, der vom Anbieter definiert wird. der Wert 0 (null) ist jedoch normalerweise reserviert, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1096c-156">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span>

<span data-ttu-id="1096c-157">Diese Eigenschaft wird von [**\_ \_ notifystatus**](../wmisdk/--notifystatus.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="1096c-157">This property is inherited from [**\_\_NotifyStatus**](../wmisdk/--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1096c-158">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1096c-158">Remarks</span></span>

<span data-ttu-id="1096c-159">Die **Win32 \_ privilegesstatus** -Klasse wird von [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="1096c-159">The **Win32\_PrivilegesStatus** class is derived from [**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1096c-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1096c-160">Requirements</span></span>



| <span data-ttu-id="1096c-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1096c-161">Requirement</span></span> | <span data-ttu-id="1096c-162">Wert</span><span class="sxs-lookup"><span data-stu-id="1096c-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1096c-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1096c-163">Minimum supported client</span></span><br/> | <span data-ttu-id="1096c-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1096c-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1096c-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1096c-165">Minimum supported server</span></span><br/> | <span data-ttu-id="1096c-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1096c-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1096c-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="1096c-167">Namespace</span></span><br/>                | <span data-ttu-id="1096c-168">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1096c-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1096c-169">MOF</span><span class="sxs-lookup"><span data-stu-id="1096c-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1096c-170"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1096c-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1096c-171">DLL</span><span class="sxs-lookup"><span data-stu-id="1096c-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1096c-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1096c-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1096c-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1096c-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1096c-174">**\_\_Erweiterdedstatus**</span><span class="sxs-lookup"><span data-stu-id="1096c-174">**\_\_ExtendedStatus**</span></span>](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
