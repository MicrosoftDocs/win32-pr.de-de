---
title: Win32_SessionDirectoryVMMPlugin-Klasse
description: Stellt ein VMM-Plug-in (Virtual Machine Manager) dar, das bei einem Sitzungs Broker registriert ist.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste
- Win32_SessionDirectoryVMMPlugin Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949559"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="b8087-105">Win32- \_ Klasse "sessiondirectoryvmmplugin"</span><span class="sxs-lookup"><span data-stu-id="b8087-105">Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="b8087-106">Stellt ein VMM-Plug-in (Virtual Machine Manager) dar, das bei einem Sitzungs Broker registriert ist.</span><span class="sxs-lookup"><span data-stu-id="b8087-106">Represents a virtual machine manager (VMM) plug-in registered with a session broker.</span></span>

<span data-ttu-id="b8087-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b8087-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8087-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8087-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="b8087-109">Member</span><span class="sxs-lookup"><span data-stu-id="b8087-109">Members</span></span>

<span data-ttu-id="b8087-110">Die Win32-Klasse " **\_ sessiondirectoryvmmplugin** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b8087-110">The **Win32\_SessionDirectoryVMMPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="b8087-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="b8087-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b8087-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b8087-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b8087-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="b8087-113">Methods</span></span>

<span data-ttu-id="b8087-114">Die Win32-Klasse " **\_ sessiondirectoryvmmplugin** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b8087-114">The **Win32\_SessionDirectoryVMMPlugin** class has these methods.</span></span>



| <span data-ttu-id="b8087-115">Methode</span><span class="sxs-lookup"><span data-stu-id="b8087-115">Method</span></span>                                                                             | <span data-ttu-id="b8087-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8087-116">Description</span></span>                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="b8087-117">**Getcurrentvmmplugin**</span><span class="sxs-lookup"><span data-stu-id="b8087-117">**GetCurrentVMMPlugin**</span></span>](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="b8087-118">Ruft das Plug-in mit der höchsten Priorität ab, das aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b8087-118">Gets the highest priority plug-in that is enabled.</span></span><br/> |
| [<span data-ttu-id="b8087-119">**Registervmmplugin**</span><span class="sxs-lookup"><span data-stu-id="b8087-119">**RegisterVMMPlugin**</span></span>](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | <span data-ttu-id="b8087-120">Registriert ein neues VMM-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="b8087-120">Registers a new VMM plug-in.</span></span><br/>                       |
| [<span data-ttu-id="b8087-121">**Abgeleitete**</span><span class="sxs-lookup"><span data-stu-id="b8087-121">**SetEnabled**</span></span>](setenabled-win32-sessiondirectoryvmmplugin.md)                   | <span data-ttu-id="b8087-122">Aktiviert oder deaktiviert das Plug-in.</span><span class="sxs-lookup"><span data-stu-id="b8087-122">Enables or disables the plug-in.</span></span><br/>                   |
| [<span data-ttu-id="b8087-123">**SetName**</span><span class="sxs-lookup"><span data-stu-id="b8087-123">**SetName**</span></span>](setname-win32-sessiondirectoryvmmplugin.md)                         | <span data-ttu-id="b8087-124">Legt den Namen des Plug-ins fest.</span><span class="sxs-lookup"><span data-stu-id="b8087-124">Sets the name of the plug-in.</span></span><br/>                      |
| [<span data-ttu-id="b8087-125">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="b8087-125">**SetPriority**</span></span>](setpriority-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="b8087-126">Legt die Priorität des Plug-ins fest.</span><span class="sxs-lookup"><span data-stu-id="b8087-126">Sets the priority of the plug-in.</span></span><br/>                  |
| [<span data-ttu-id="b8087-127">**Setprovider**</span><span class="sxs-lookup"><span data-stu-id="b8087-127">**SetProvider**</span></span>](setprovider-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="b8087-128">Legt den Anbieter Namen des Plug-ins fest.</span><span class="sxs-lookup"><span data-stu-id="b8087-128">Sets the provider name of the plug-in.</span></span><br/>             |
| [<span data-ttu-id="b8087-129">**Setservicelokation**</span><span class="sxs-lookup"><span data-stu-id="b8087-129">**SetServiceLocation**</span></span>](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | <span data-ttu-id="b8087-130">Legt den Speicherort des Plug-Ins für den Dienst fest.</span><span class="sxs-lookup"><span data-stu-id="b8087-130">Sets the service location of the plug-in.</span></span><br/>          |
| [<span data-ttu-id="b8087-131">**Unregistervmmplugin**</span><span class="sxs-lookup"><span data-stu-id="b8087-131">**UnregisterVMMPlugin**</span></span>](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="b8087-132">Hebt die Registrierung des Plug-Ins auf.</span><span class="sxs-lookup"><span data-stu-id="b8087-132">Unregisters the plug-in.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="b8087-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b8087-133">Properties</span></span>

<span data-ttu-id="b8087-134">Die Win32-Klasse " **\_ sessiondirectoryvmmplugin** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b8087-134">The **Win32\_SessionDirectoryVMMPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b8087-135">**Aktiviert**</span><span class="sxs-lookup"><span data-stu-id="b8087-135">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8087-136">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b8087-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b8087-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8087-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8087-138">Gibt an, ob das Plug-in aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b8087-138">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="b8087-139">**True** , wenn das Plug-in aktiviert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b8087-139">**True** if the plug-in is enabled or **false** otherwise.</span></span> <span data-ttu-id="b8087-140">Das Plug-in ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b8087-140">The plug-in is disabled by default.</span></span>

</dd> <dt>

<span data-ttu-id="b8087-141">**Priority**</span><span class="sxs-lookup"><span data-stu-id="b8087-141">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8087-142">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b8087-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b8087-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8087-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b8087-144">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b8087-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b8087-145">Die Priorität des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="b8087-145">The priority of the plug-in.</span></span> <span data-ttu-id="b8087-146">Je höher der Wert ist, desto höher ist die Priorität des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="b8087-146">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="b8087-147">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b8087-147">The priority is zero by default.</span></span>

</dd> <dt>

<span data-ttu-id="b8087-148">**sclassid**</span><span class="sxs-lookup"><span data-stu-id="b8087-148">**sClassID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8087-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8087-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8087-150">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8087-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8087-151">Der Klassen Bezeichner des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="b8087-151">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="b8087-152">**sName**</span><span class="sxs-lookup"><span data-stu-id="b8087-152">**sName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8087-153">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8087-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8087-154">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8087-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8087-155">Der Name des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="b8087-155">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="b8087-156">**sprovider**</span><span class="sxs-lookup"><span data-stu-id="b8087-156">**sProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8087-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8087-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8087-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8087-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8087-159">Der Name des Plug-in-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b8087-159">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="b8087-160">**sservicelokation**</span><span class="sxs-lookup"><span data-stu-id="b8087-160">**sServiceLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b8087-161">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b8087-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b8087-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b8087-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b8087-163">Der Dienst Speicherort, den das Plug-in kontaktieren soll.</span><span class="sxs-lookup"><span data-stu-id="b8087-163">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8087-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8087-164">Requirements</span></span>



| <span data-ttu-id="b8087-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8087-165">Requirement</span></span> | <span data-ttu-id="b8087-166">Wert</span><span class="sxs-lookup"><span data-stu-id="b8087-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8087-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8087-167">Minimum supported client</span></span><br/> | <span data-ttu-id="b8087-168">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b8087-168">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b8087-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8087-169">Minimum supported server</span></span><br/> | <span data-ttu-id="b8087-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b8087-170">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b8087-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="b8087-171">Namespace</span></span><br/>                | <span data-ttu-id="b8087-172">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b8087-172">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="b8087-173">MOF</span><span class="sxs-lookup"><span data-stu-id="b8087-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8087-174"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="b8087-174"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8087-175">DLL</span><span class="sxs-lookup"><span data-stu-id="b8087-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8087-176"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8087-176"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

