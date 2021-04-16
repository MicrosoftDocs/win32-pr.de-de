---
title: Win32_SessionBrokerServiceProperties-Klasse
description: Definiert die Abfrage für einen Sitzungs Broker Dienst.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste
- Win32_SessionBrokerServiceProperties Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518980"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="27672-105">Win32 \_ sessionbrokerserviceproperties-Klasse</span><span class="sxs-lookup"><span data-stu-id="27672-105">Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="27672-106">Definiert die Abfrage für einen Sitzungs Broker Dienst.</span><span class="sxs-lookup"><span data-stu-id="27672-106">Defines the query for a session broker service.</span></span>

<span data-ttu-id="27672-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27672-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="27672-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="27672-108">Syntax</span></span>

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a><span data-ttu-id="27672-109">Member</span><span class="sxs-lookup"><span data-stu-id="27672-109">Members</span></span>

<span data-ttu-id="27672-110">Die **Win32 \_ sessionbrokerserviceproperties** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="27672-110">The **Win32\_SessionBrokerServiceProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="27672-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="27672-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="27672-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27672-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="27672-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="27672-113">Methods</span></span>

<span data-ttu-id="27672-114">Die **Win32 \_ sessionbrokerserviceproperties** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="27672-114">The **Win32\_SessionBrokerServiceProperties** class has these methods.</span></span>



| <span data-ttu-id="27672-115">Methode</span><span class="sxs-lookup"><span data-stu-id="27672-115">Method</span></span>                                                                                                | <span data-ttu-id="27672-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27672-116">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27672-117">**Delta-bdbconnectionstring**</span><span class="sxs-lookup"><span data-stu-id="27672-117">**DeleteSBDbConnectionString**</span></span>](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | <span data-ttu-id="27672-118">Löscht DB-Verbindungs Zeichenfolgen (Primär und sekundär) aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="27672-118">Deletes DB connection strings (primary and secondary) from the registry.</span></span><br/> <span data-ttu-id="27672-119">**Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2:** Diese Methode ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27672-119">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/> |
| [<span data-ttu-id="27672-120">**Installbrokerdatabase**</span><span class="sxs-lookup"><span data-stu-id="27672-120">**InstallBrokerDatabase**</span></span>](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | <span data-ttu-id="27672-121">Installiert RD-Verbindungsbroker DB auf Central SQL Server</span><span class="sxs-lookup"><span data-stu-id="27672-121">Installs RD Connection Broker DB on central SQL Server</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="27672-122">**Isdbreachable**</span><span class="sxs-lookup"><span data-stu-id="27672-122">**IsDbReachable**</span></span>](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | <span data-ttu-id="27672-123">Prüft, ob DB erreichbar ist.</span><span class="sxs-lookup"><span data-stu-id="27672-123">Checks if DB is reachable</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="27672-124">**Setbrokerhamode**</span><span class="sxs-lookup"><span data-stu-id="27672-124">**SetBrokerHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | <span data-ttu-id="27672-125">Migriert Daten von der lokalen wid-Datenbank zum neuen SQL Server basierten DB.</span><span class="sxs-lookup"><span data-stu-id="27672-125">Migrates data from local WID DB to the new SQL Server based DB.</span></span> <span data-ttu-id="27672-126">Außerdem wird der Broker Server für die Verwendung des zentralen SQL Server konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="27672-126">It also configures the broker server to use the central SQL Server</span></span><br/>                                                                                        |
| [<span data-ttu-id="27672-127">**Setbrokernonhamode**</span><span class="sxs-lookup"><span data-stu-id="27672-127">**SetBrokerNonHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | <span data-ttu-id="27672-128">Migriert Daten von der zentralen SQL Server zur lokalen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="27672-128">Migrates data from central SQL Server to local DB.</span></span> <span data-ttu-id="27672-129">Außerdem wird der Broker Server für die Verwendung der lokalen Datenbank konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="27672-129">It also configures the broker server to use the local DB.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="27672-130">**"Menbdbconnectionstrings"**</span><span class="sxs-lookup"><span data-stu-id="27672-130">**SetSBDbConnectionStrings**</span></span>](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | <span data-ttu-id="27672-131">Speichert DB-Verbindungs Zeichenfolgen (Primär und sekundär) in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="27672-131">Saves DB connection strings (primary and secondary) in the registry.</span></span><br/> <span data-ttu-id="27672-132">**Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2:** Diese Methode ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27672-132">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/>     |



 

### <a name="properties"></a><span data-ttu-id="27672-133">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27672-133">Properties</span></span>

<span data-ttu-id="27672-134">Die **Win32 \_ sessionbrokerserviceproperties** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="27672-134">The **Win32\_SessionBrokerServiceProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27672-135">**Sbdbconnectionstring**</span><span class="sxs-lookup"><span data-stu-id="27672-135">**SBDbConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27672-136">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27672-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27672-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="27672-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27672-138">Vom Sitzungs Broker Dienst verwendete Daten bankverbindungs Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="27672-138">Database connection string used by Session Broker service.</span></span>

<span data-ttu-id="27672-139">**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27672-139">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="27672-140">**Sbdbsecondaryconnectionstring**</span><span class="sxs-lookup"><span data-stu-id="27672-140">**SBDbSecondaryConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27672-141">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27672-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27672-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="27672-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="27672-143">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="27672-143">Optional.</span></span> <span data-ttu-id="27672-144">Verbindungs Zeichenfolge der sekundären Datenbank, die vom Sitzungs Broker Dienst zur Unterstützung des Kennworts verwendet wird</span><span class="sxs-lookup"><span data-stu-id="27672-144">Secondary database connection string, used by Session Broker service to support password expiration.</span></span>

<span data-ttu-id="27672-145">**Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2016 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27672-145">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This property is not available prior to Windows Server 2016</span></span>

</dd> <dt>

<span data-ttu-id="27672-146">**Sbnetworkname**</span><span class="sxs-lookup"><span data-stu-id="27672-146">**SBNetworkName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27672-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="27672-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="27672-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="27672-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="27672-149">Der vom Sitzungs Broker Dienst verwendete Netzwerkname.</span><span class="sxs-lookup"><span data-stu-id="27672-149">The network name used by the session broker service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27672-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27672-150">Requirements</span></span>



| <span data-ttu-id="27672-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27672-151">Requirement</span></span> | <span data-ttu-id="27672-152">Wert</span><span class="sxs-lookup"><span data-stu-id="27672-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27672-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="27672-153">Minimum supported client</span></span><br/> | <span data-ttu-id="27672-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="27672-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="27672-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="27672-155">Minimum supported server</span></span><br/> | <span data-ttu-id="27672-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="27672-156">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="27672-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="27672-157">Namespace</span></span><br/>                | <span data-ttu-id="27672-158">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="27672-158">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="27672-159">MOF</span><span class="sxs-lookup"><span data-stu-id="27672-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27672-160"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="27672-160"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="27672-161">DLL</span><span class="sxs-lookup"><span data-stu-id="27672-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27672-162"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27672-162"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

