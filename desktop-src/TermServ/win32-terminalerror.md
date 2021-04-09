---
title: Win32_TerminalError-Klasse
description: Stellt einen Terminal Fehler dar.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Win32_TerminalError-Klasse Remotedesktopdienste
- Win32_TerminalError Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103146"
---
# <a name="win32_terminalerror-class"></a><span data-ttu-id="b0d94-105">Win32 \_ terminalerror-Klasse</span><span class="sxs-lookup"><span data-stu-id="b0d94-105">Win32\_TerminalError class</span></span>

<span data-ttu-id="b0d94-106">Stellt einen Terminal Fehler dar.</span><span class="sxs-lookup"><span data-stu-id="b0d94-106">Represents a terminal error.</span></span>

<span data-ttu-id="b0d94-107">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="b0d94-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0d94-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0d94-108">Syntax</span></span>

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="b0d94-109">Member</span><span class="sxs-lookup"><span data-stu-id="b0d94-109">Members</span></span>

<span data-ttu-id="b0d94-110">Die **Win32 \_ terminalerror** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b0d94-110">The **Win32\_TerminalError** class has these types of members:</span></span>

-   [<span data-ttu-id="b0d94-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0d94-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0d94-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0d94-112">Properties</span></span>

<span data-ttu-id="b0d94-113">Die **Win32 \_ terminalerror** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b0d94-113">The **Win32\_TerminalError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0d94-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b0d94-114">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0d94-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0d94-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0d94-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0d94-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0d94-117">Eine beliebige benutzerdefinierte Zeichenfolge, die einen Fehler-oder Betriebsstatus beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b0d94-117">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="b0d94-118">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="b0d94-118">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b0d94-119">**Vorgang**</span><span class="sxs-lookup"><span data-stu-id="b0d94-119">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0d94-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0d94-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0d94-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0d94-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0d94-122">Der Vorgang, der zum Zeitpunkt eines Fehlers oder einer Anomalieerkennung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="b0d94-122">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="b0d94-123">In der Regel wird diese Eigenschaft von WMI auf den Namen der com-API für die WMI-Methode festgelegt, wie z. b. die folgende: [**IWbemServices:: kreateinstanceenum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="b0d94-123">Typically, WMI sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="b0d94-124">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="b0d94-124">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b0d94-125">**Parameter Info**</span><span class="sxs-lookup"><span data-stu-id="b0d94-125">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0d94-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0d94-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0d94-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0d94-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0d94-128">Parameter, die an einem Fehler oder einer Statusänderung beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="b0d94-128">Parameters involved in an error or status change.</span></span> <span data-ttu-id="b0d94-129">Wenn eine Anwendung z. b. versucht, eine Klasse abzurufen, die nicht vorhanden ist, wird diese Eigenschaft auf den Namen der angreifenden Klasse festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0d94-129">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="b0d94-130">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="b0d94-130">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b0d94-131">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="b0d94-131">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0d94-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0d94-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0d94-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0d94-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0d94-134">Identifiziert den Anbieter, der einen Fehler oder eine Statusänderung auslöst oder meldet.</span><span class="sxs-lookup"><span data-stu-id="b0d94-134">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="b0d94-135">Wenn ein Anbieter nicht beteiligt ist, wird diese Zeichenfolge auf "Windows-Verwaltung" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b0d94-135">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="b0d94-136">Diese Eigenschaft wird von " [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)" geerbt.</span><span class="sxs-lookup"><span data-stu-id="b0d94-136">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="b0d94-137">**Statuscode**</span><span class="sxs-lookup"><span data-stu-id="b0d94-137">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0d94-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b0d94-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0d94-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0d94-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0d94-140">Enthält einen Fehler-oder Informations Code für einen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b0d94-140">Contains an error or information code for an operation.</span></span> <span data-ttu-id="b0d94-141">Dies kann ein beliebiger Wert sein, der vom Anbieter definiert wird. der Wert 0 (null) ist jedoch normalerweise reserviert, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b0d94-141">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="b0d94-142">Diese Eigenschaft wird von [**\_ \_ notifystatus**](/windows/desktop/WmiSdk/--notifystatus)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b0d94-142">This property is inherited from [**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span></span>

</dd> <dt>

<span data-ttu-id="b0d94-143">**Terminal Name**</span><span class="sxs-lookup"><span data-stu-id="b0d94-143">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0d94-144">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b0d94-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0d94-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b0d94-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0d94-146">Der Name des endfehlers, bei dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b0d94-146">The name of the terminal sin which the error occurred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0d94-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0d94-147">Requirements</span></span>



| <span data-ttu-id="b0d94-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0d94-148">Requirement</span></span> | <span data-ttu-id="b0d94-149">Wert</span><span class="sxs-lookup"><span data-stu-id="b0d94-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0d94-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0d94-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b0d94-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0d94-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0d94-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0d94-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b0d94-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0d94-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0d94-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0d94-154">Namespace</span></span><br/>                | <span data-ttu-id="b0d94-155">Root \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b0d94-155">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b0d94-156">MOF</span><span class="sxs-lookup"><span data-stu-id="b0d94-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0d94-157"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b0d94-157"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0d94-158">DLL</span><span class="sxs-lookup"><span data-stu-id="b0d94-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0d94-159"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0d94-159"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0d94-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0d94-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d94-161">**\_\_Erweiterdedstatus**</span><span class="sxs-lookup"><span data-stu-id="b0d94-161">**\_\_ExtendedStatus**</span></span>](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

