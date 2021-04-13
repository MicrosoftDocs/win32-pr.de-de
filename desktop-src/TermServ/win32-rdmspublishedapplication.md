---
title: Win32_RDMSPublishedApplication-Klasse
description: Verwaltet eine veröffentlichte Anwendung.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSPublishedApplication-Klasse Remotedesktopdienste
- Win32_RDMSPublishedApplication Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341127"
---
# <a name="win32_rdmspublishedapplication-class"></a><span data-ttu-id="fa0b3-105">Win32- \_ rdmspublishedappliationklasse</span><span class="sxs-lookup"><span data-stu-id="fa0b3-105">Win32\_RDMSPublishedApplication class</span></span>

<span data-ttu-id="fa0b3-106">Verwaltet eine veröffentlichte Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-106">Manages a published application.</span></span>

<span data-ttu-id="fa0b3-107">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa0b3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa0b3-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a><span data-ttu-id="fa0b3-109">Member</span><span class="sxs-lookup"><span data-stu-id="fa0b3-109">Members</span></span>

<span data-ttu-id="fa0b3-110">Die **Win32 \_ rdmspublishedappliationklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="fa0b3-110">The **Win32\_RDMSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="fa0b3-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa0b3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa0b3-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fa0b3-112">Properties</span></span>

<span data-ttu-id="fa0b3-113">Die **Win32 \_ rdmspublishedappliationklasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-113">The **Win32\_RDMSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa0b3-114">**Appalias**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-115">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-116">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-117">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa0b3-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-118">Ruft den Alias der Anwendung ab und legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-118">Gets and sets the alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-119">**AppPath**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-119">**AppPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-121">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-122">Ruft den Pfad der Anwendung ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-122">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-123">**Commandlinesesetting**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-123">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-124">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-125">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-126">Ruft die Befehlszeilen Einstellung für die Anwendung ab und legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-126">Gets and sets the command line setting for the application.</span></span>

<span data-ttu-id="fa0b3-127">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="fa0b3-127">This property can be set to one of the following values:</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="fa0b3-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**Donotallow** (0)</span><span class="sxs-lookup"><span data-stu-id="fa0b3-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="fa0b3-129">Befehlszeilenargumente dürfen nicht zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-129">Do not allow command line arguments.</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="fa0b3-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Zulassen** (1)</span><span class="sxs-lookup"><span data-stu-id="fa0b3-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd>

<span data-ttu-id="fa0b3-131">Befehlszeilenargumente zulassen.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-131">Allow command line arguments.</span></span>

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="fa0b3-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Erforderlich** (2)</span><span class="sxs-lookup"><span data-stu-id="fa0b3-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa0b3-133">Erfordert Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-133">Require command line arguments.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="fa0b3-134">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-134">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-136">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-137">Ruft den anzeigen amen der Anwendung ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-137">Gets and sets the display name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-138">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-138">**Folder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-139">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-140">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-141">Ruft den Pfad der Anwendung ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-141">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-142">**Iconcontent**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-142">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-143">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="fa0b3-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-144">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-145">Ruft ein Array ab, das das Anwendungssymbol enthält, oder legt dieses fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-145">Gets and sets an array that contains the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-146">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-146">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-147">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-149">Ruft den Index für das Anwendungssymbol ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-149">Gets and sets the index for the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-150">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-150">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-151">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-152">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-153">Ruft den Pfad zum Symbol für diese Anwendung ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-153">Gets and sets the path to the icon for this application.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-154">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-154">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-155">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-156">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-157">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fa0b3-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-158">Ruft den Namen des Anwendungs Pools der Anwendung ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-158">Gets and sets the name of the application pool of the application.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-159">**"Requirements dcommandline"**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-159">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-160">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-161">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-161">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-162">Ruft die Befehlszeilenargumente ab, die für die Anwendung erforderlich sind, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-162">Gets and sets the command line arguments that are required for the application</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-164">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-165">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-166">Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fa0b3-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-167">Ruft den Sicherheits Deskriptor ab, der den Zugriff auf die Anwendung steuert, im SDDL-Format (Security Deskriptor Definition Language), oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-167">Gets and sets the security descriptor that controls access to the application, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-168">**Showinportal**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-168">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-169">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="fa0b3-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-171">Gibt an, ob die Anwendung in terminaldiensteWebzugriff (TS Webzugriff) angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-171">Indicates whether to display the application in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="fa0b3-172">" **True** ", um die Anwendung in TS Webzugriff anzuzeigen. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-172">**TRUE** to display the application in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b3-173">**VirtualPath**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-173">**VirtualPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa0b3-174">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fa0b3-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="fa0b3-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fa0b3-176">Ruft den virtuellen Pfad der Anwendung ab und legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-176">Gets and sets the virtual path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa0b3-177">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa0b3-177">Requirements</span></span>



| <span data-ttu-id="fa0b3-178">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa0b3-178">Requirement</span></span> | <span data-ttu-id="fa0b3-179">Wert</span><span class="sxs-lookup"><span data-stu-id="fa0b3-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0b3-180">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fa0b3-180">Minimum supported client</span></span><br/> | <span data-ttu-id="fa0b3-181">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="fa0b3-181">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fa0b3-182">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fa0b3-182">Minimum supported server</span></span><br/> | <span data-ttu-id="fa0b3-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa0b3-183">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fa0b3-184">Namespace</span><span class="sxs-lookup"><span data-stu-id="fa0b3-184">Namespace</span></span><br/>                | <span data-ttu-id="fa0b3-185">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="fa0b3-185">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fa0b3-186">MOF</span><span class="sxs-lookup"><span data-stu-id="fa0b3-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa0b3-187"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b3-187"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa0b3-188">DLL</span><span class="sxs-lookup"><span data-stu-id="fa0b3-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa0b3-189"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b3-189"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fa0b3-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa0b3-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa0b3-191">Remotedesktop Management Services-Anbieter</span><span class="sxs-lookup"><span data-stu-id="fa0b3-191">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

