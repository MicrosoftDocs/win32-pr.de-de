---
title: Win32_SessionDirectoryCluster-Klasse
description: Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Farm in Remotedesktopverbindung Broker (RD-Verbindungsbroker) bereit.
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster-Klasse Remotedesktopdienste
- Win32_SessionDirectoryCluster Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476203"
---
# <a name="win32_sessiondirectorycluster-class"></a><span data-ttu-id="bed00-105">Win32- \_ Klasse "sessiondirectorycluster"</span><span class="sxs-lookup"><span data-stu-id="bed00-105">Win32\_SessionDirectoryCluster class</span></span>

<span data-ttu-id="bed00-106">Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Farm in Remotedesktopverbindung Broker (RD-Verbindungsbroker) bereit.</span><span class="sxs-lookup"><span data-stu-id="bed00-106">Provides properties for viewing the properties of a farm in Remote Desktop Connection Broker (RD Connection Broker).</span></span>

> [!Note]  
> <span data-ttu-id="bed00-107">In Windows Server 2008 R2 wurde der Name des Terminal Dienste-Sitzungs Brokers (TS-Sitzungs Broker) in "RD-Verbindungsbroker" geändert.</span><span class="sxs-lookup"><span data-stu-id="bed00-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="bed00-108">Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="bed00-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bed00-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bed00-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a><span data-ttu-id="bed00-110">Member</span><span class="sxs-lookup"><span data-stu-id="bed00-110">Members</span></span>

<span data-ttu-id="bed00-111">Die Win32-Klasse " **\_ sessiondirectorycluster** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bed00-111">The **Win32\_SessionDirectoryCluster** class has these types of members:</span></span>

-   [<span data-ttu-id="bed00-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bed00-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bed00-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bed00-113">Properties</span></span>

<span data-ttu-id="bed00-114">Die Win32-Klasse " **\_ sessiondirectorycluster** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bed00-114">The **Win32\_SessionDirectoryCluster** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bed00-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="bed00-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bed00-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="bed00-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bed00-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bed00-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bed00-118">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bed00-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bed00-119">Der Name der Farm in RD-Verbindungsbroker.</span><span class="sxs-lookup"><span data-stu-id="bed00-119">Name of the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="bed00-120">**Anzahl von Servern**</span><span class="sxs-lookup"><span data-stu-id="bed00-120">**NumberOfServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bed00-121">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bed00-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bed00-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bed00-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bed00-123">Anzahl der Server in der Farm in RD-Verbindungsbroker.</span><span class="sxs-lookup"><span data-stu-id="bed00-123">Number of servers in the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="bed00-124">**Singlesessionmode**</span><span class="sxs-lookup"><span data-stu-id="bed00-124">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bed00-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bed00-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bed00-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bed00-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bed00-127">Einzelner Sitzungs Modus der Farm in RD-Verbindungsbroker.</span><span class="sxs-lookup"><span data-stu-id="bed00-127">Single session mode of the farm in RD Connection Broker.</span></span>

<dt>

<span data-ttu-id="bed00-128">0</span><span class="sxs-lookup"><span data-stu-id="bed00-128">0</span></span>
</dt> <dd>

<span data-ttu-id="bed00-129">Die Farm in RD-Verbindungsbroker befindet sich nicht im Einzel Sitzungs Modus.</span><span class="sxs-lookup"><span data-stu-id="bed00-129">The farm in RD Connection Broker is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="bed00-130">1</span><span class="sxs-lookup"><span data-stu-id="bed00-130">1</span></span>
</dt> <dd>

<span data-ttu-id="bed00-131">Die Farm in RD-Verbindungsbroker befindet sich im Einzel Sitzungs Modus.</span><span class="sxs-lookup"><span data-stu-id="bed00-131">The farm in RD Connection Broker is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bed00-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bed00-132">Remarks</span></span>

<span data-ttu-id="bed00-133">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="bed00-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bed00-134">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="bed00-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bed00-135">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bed00-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bed00-136">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bed00-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bed00-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bed00-137">Requirements</span></span>



| <span data-ttu-id="bed00-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bed00-138">Requirement</span></span> | <span data-ttu-id="bed00-139">Wert</span><span class="sxs-lookup"><span data-stu-id="bed00-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bed00-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bed00-140">Minimum supported client</span></span><br/> | <span data-ttu-id="bed00-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bed00-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bed00-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bed00-142">Minimum supported server</span></span><br/> | <span data-ttu-id="bed00-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bed00-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="bed00-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="bed00-144">Namespace</span></span><br/>                | <span data-ttu-id="bed00-145">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="bed00-145">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="bed00-146">MOF</span><span class="sxs-lookup"><span data-stu-id="bed00-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bed00-147"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="bed00-147"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bed00-148">DLL</span><span class="sxs-lookup"><span data-stu-id="bed00-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bed00-149"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bed00-149"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bed00-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bed00-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed00-151">**Win32 \_ sessiondirectoriyserver**</span><span class="sxs-lookup"><span data-stu-id="bed00-151">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> <dt>

[<span data-ttu-id="bed00-152">**Win32 \_ sessiondirectoriysession**</span><span class="sxs-lookup"><span data-stu-id="bed00-152">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

