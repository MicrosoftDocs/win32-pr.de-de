---
description: Die CIM \_ versioncompatibilitycheck-Klasse gibt an, ob es zulässig ist, den nächsten Zustand eines Software Elements zu erstellen.
ms.assetid: 3a04c489-e44e-44c7-8945-d6047ba0d6df
ms.tgt_platform: multiple
title: CIM_VersionCompatibilityCheck-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck
- CIM_VersionCompatibilityCheck.CheckID
- CIM_VersionCompatibilityCheck.Caption
- CIM_VersionCompatibilityCheck.Description
- CIM_VersionCompatibilityCheck.CheckMode
- CIM_VersionCompatibilityCheck.Name
- CIM_VersionCompatibilityCheck.TargetOperatingSystem
- CIM_VersionCompatibilityCheck.Version
- CIM_VersionCompatibilityCheck.SoftwareElementID
- CIM_VersionCompatibilityCheck.SoftwareElementState
- CIM_VersionCompatibilityCheck.AllowDownVersion
- CIM_VersionCompatibilityCheck.AllowMultipleVersions
- CIM_VersionCompatibilityCheck.Reinstall
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 00a37d52add8c9697371fd0ee8d0a24d9c487f61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958339"
---
# <a name="cim_versioncompatibilitycheck-class"></a><span data-ttu-id="b167e-103">CIM \_ versioncompatibilitycheck-Klasse</span><span class="sxs-lookup"><span data-stu-id="b167e-103">CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="b167e-104">Die **CIM \_ versioncompatibilitycheck** -Klasse gibt an, ob es zulässig ist, den nächsten Zustand eines Software Elements zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b167e-104">The **CIM\_VersionCompatibilityCheck** class specifies whether it is permissible to create the next state of a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b167e-105">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="b167e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b167e-106">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b167e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b167e-107">Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b167e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b167e-108">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="b167e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b167e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b167e-109">Syntax</span></span>

``` syntax
[UUID("{D368CA4A-DB31-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VersionCompatibilityCheck : CIM_Check
{
  string  CheckID;
  string  Caption;
  string  Description;
  boolean CheckMode;
  string  Name;
  uint16  TargetOperatingSystem;
  string  Version;
  string  SoftwareElementID;
  uint16  SoftwareElementState;
  boolean AllowDownVersion;
  boolean AllowMultipleVersions;
  boolean Reinstall;
};
```

## <a name="members"></a><span data-ttu-id="b167e-110">Member</span><span class="sxs-lookup"><span data-stu-id="b167e-110">Members</span></span>

<span data-ttu-id="b167e-111">Die **CIM \_ versioncompatibilitycheck** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b167e-111">The **CIM\_VersionCompatibilityCheck** class has these types of members:</span></span>

-   [<span data-ttu-id="b167e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="b167e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b167e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b167e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b167e-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="b167e-114">Methods</span></span>

<span data-ttu-id="b167e-115">Die **CIM \_ versioncompatibilitycheck** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b167e-115">The **CIM\_VersionCompatibilityCheck** class has these methods.</span></span>



| <span data-ttu-id="b167e-116">Methode</span><span class="sxs-lookup"><span data-stu-id="b167e-116">Method</span></span>                                                                 | <span data-ttu-id="b167e-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b167e-117">Description</span></span>                                                   |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="b167e-118">**Invoke**</span><span class="sxs-lookup"><span data-stu-id="b167e-118">**Invoke**</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md) | <span data-ttu-id="b167e-119">Führt eine bestimmte Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="b167e-119">Takes a particular action.</span></span> <span data-ttu-id="b167e-120">Wird nicht von WMI implementiert.</span><span class="sxs-lookup"><span data-stu-id="b167e-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b167e-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b167e-121">Properties</span></span>

<span data-ttu-id="b167e-122">Die **CIM \_ versioncompatibilitycheck** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b167e-122">The **CIM\_VersionCompatibilityCheck** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b167e-123">**AllowDownVersion**</span><span class="sxs-lookup"><span data-stu-id="b167e-123">**AllowDownVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-124">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b167e-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b167e-126">Wenn der Wert **true** ist, kann das Softwareelement in seinen nächsten Zustand übergehen, unabhängig davon, ob eine höhere oder eine höhere Version des Software Elements bereits in der Umgebung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b167e-126">If **TRUE**, the software element can transition to its next state whether or not if a higher or latter version of the software element already exists in the environment.</span></span>

</dd> <dt>

<span data-ttu-id="b167e-127">**Allowmultipleversions**</span><span class="sxs-lookup"><span data-stu-id="b167e-127">**AllowMultipleVersions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-128">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b167e-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b167e-130">Steuert die Fähigkeit, mehrere Versionen eines Produkts auf einem System zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b167e-130">Controls the ability to configure multiple versions of a product on a system.</span></span>

</dd> <dt>

<span data-ttu-id="b167e-131">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b167e-131">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b167e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-133">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b167e-134">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b167e-134">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b167e-135">Eine kurze Textbeschreibung des Subjekts.</span><span class="sxs-lookup"><span data-stu-id="b167e-135">A short textual description of the subject.</span></span>

<span data-ttu-id="b167e-136">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b167e-136">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b167e-137">**CheckId**</span><span class="sxs-lookup"><span data-stu-id="b167e-137">**CheckID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b167e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b167e-140">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b167e-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b167e-141">Bezeichner, der in Verbindung mit anderen Schlüsseln zum eindeutigen Identifizieren der Überprüfung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b167e-141">Identifier used in conjunction with other keys to uniquely identify the check.</span></span>

<span data-ttu-id="b167e-142">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b167e-142">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b167e-143">**Checkmode**</span><span class="sxs-lookup"><span data-stu-id="b167e-143">**CheckMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-144">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b167e-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-145">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b167e-146">Wenn der Wert **true** ist, wird erwartet, dass die Bedingung in der Umgebung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b167e-146">If **TRUE**, the condition is expected to exist in the environment.</span></span> <span data-ttu-id="b167e-147">Beispielsweise wird erwartet, dass eine Datei auf einem System ausgeführt wird, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b167e-147">For example, a file is expected to be on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **TRUE**.</span></span>

<span data-ttu-id="b167e-148">Wenn der Wert **false** ist, wird erwartet, dass die Bedingung nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b167e-148">If **FALSE**, the condition is not expected to exist.</span></span> <span data-ttu-id="b167e-149">Eine Datei befindet sich z. b. nicht in einem System, daher sollte die [**Aufruf**](invoke-method-in-class-cim-check.md) Methode **false** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b167e-149">For example, a file is not on a system, so the [**Invoke**](invoke-method-in-class-cim-check.md) method should return **FALSE**.</span></span>

<span data-ttu-id="b167e-150">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b167e-150">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b167e-151">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b167e-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-152">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b167e-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-153">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b167e-154">Eine Beschreibung der-Objekte.</span><span class="sxs-lookup"><span data-stu-id="b167e-154">A description of the objects.</span></span>

<span data-ttu-id="b167e-155">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b167e-155">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b167e-156">**Name**</span><span class="sxs-lookup"><span data-stu-id="b167e-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-157">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b167e-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-158">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b167e-159">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Name**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b167e-159">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Name**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b167e-160">Der Name, der zum Identifizieren des Software Elements verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b167e-160">Name used to identify the software element</span></span>

<span data-ttu-id="b167e-161">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b167e-161">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b167e-162">**Neuinstallation**</span><span class="sxs-lookup"><span data-stu-id="b167e-162">**Reinstall**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-163">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b167e-163">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-164">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b167e-165">Wenn der Wert **true** ist, kann das Softwareelement in seinen nächsten Zustand übergehen, unabhängig davon, ob ein Softwareelement derselben Version bereits in der Umgebung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b167e-165">If **TRUE**, the software element can transition to its next state whether or not a software element of the same version already exists in the environment.</span></span>

</dd> <dt>

<span data-ttu-id="b167e-166">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="b167e-166">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-167">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b167e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-168">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b167e-169">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b167e-169">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementID**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b167e-170">Dies ist ein Bezeichner für dieses Softwareelement.</span><span class="sxs-lookup"><span data-stu-id="b167e-170">This is an identifier for this software element.</span></span>

<span data-ttu-id="b167e-171">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b167e-171">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> <dt>

<span data-ttu-id="b167e-172">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="b167e-172">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-173">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b167e-173">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-174">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b167e-175">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM- \_ Taste**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b167e-175">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**SoftwareElementState**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b167e-176">Der Softwareelement Zustand eines Software Elements.</span><span class="sxs-lookup"><span data-stu-id="b167e-176">The software element state of a software element.</span></span>

<span data-ttu-id="b167e-177">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b167e-177">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="b167e-178"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Bereitstellbar** (0)</span><span class="sxs-lookup"><span data-stu-id="b167e-178"><span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="b167e-179"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installier Bar** (1)</span><span class="sxs-lookup"><span data-stu-id="b167e-179"><span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="b167e-180"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Ausführbare Datei** (2)</span><span class="sxs-lookup"><span data-stu-id="b167e-180"><span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="b167e-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>Wird **ausgeführt** (3)</span><span class="sxs-lookup"><span data-stu-id="b167e-181"><span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b167e-182">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="b167e-182">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-183">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b167e-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-184">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b167e-185">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". Informationen zur DMTF- \| Software Komponente \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="b167e-185">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**TargetOperatingSystem**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="b167e-186">Ziel Betriebssystem des Software Elements.</span><span class="sxs-lookup"><span data-stu-id="b167e-186">Target operating system of the software element.</span></span>

<span data-ttu-id="b167e-187">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b167e-187">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b167e-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="b167e-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b167e-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)</span><span class="sxs-lookup"><span data-stu-id="b167e-189"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="b167e-190"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="b167e-190"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-191">Mac OS</span><span class="sxs-lookup"><span data-stu-id="b167e-191">Mac OS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="b167e-192"><span id="ATTUNIX"></span><span id="attunix"></span>**Attunix** (3)</span><span class="sxs-lookup"><span data-stu-id="b167e-192"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-193">ATT UNIX</span><span class="sxs-lookup"><span data-stu-id="b167e-193">ATT UNIX</span></span>

</dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="b167e-194"><span id="DGUX"></span><span id="dgux"></span>**Dgux** (4)</span><span class="sxs-lookup"><span data-stu-id="b167e-194"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="b167e-195"><span id="DECNT"></span><span id="decnt"></span>**Decnt** (5)</span><span class="sxs-lookup"><span data-stu-id="b167e-195"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="b167e-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital UNIX** (6)</span><span class="sxs-lookup"><span data-stu-id="b167e-196"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="b167e-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="b167e-197"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-198">Öffnen von VMS</span><span class="sxs-lookup"><span data-stu-id="b167e-198">Open VMS</span></span>

</dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="b167e-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="b167e-199"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-200">HP-UX</span><span class="sxs-lookup"><span data-stu-id="b167e-200">HP-UX</span></span>

</dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="b167e-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="b167e-201"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="b167e-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="b167e-202"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="b167e-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="b167e-203"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="b167e-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="b167e-204"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="b167e-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="b167e-205"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-206">Microsoft Virtual Machine (VM) für Java</span><span class="sxs-lookup"><span data-stu-id="b167e-206">Microsoft Virtual Machine (VM) for Java</span></span>

</dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="b167e-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="b167e-207"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="b167e-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="b167e-208"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-209">Windows 3. x</span><span class="sxs-lookup"><span data-stu-id="b167e-209">Windows 3.x</span></span>

</dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="b167e-210"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="b167e-210"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-211">Windows 95</span><span class="sxs-lookup"><span data-stu-id="b167e-211">Windows 95</span></span>

</dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="b167e-212"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="b167e-212"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-213">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b167e-213">Windows 98</span></span>

</dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="b167e-214"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="b167e-214"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-215">Windows NT</span><span class="sxs-lookup"><span data-stu-id="b167e-215">Windows NT</span></span>

</dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="b167e-216"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="b167e-216"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-217">Windows CE</span><span class="sxs-lookup"><span data-stu-id="b167e-217">Windows CE</span></span>

</dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="b167e-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="b167e-218"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-219">NCR 3000</span><span class="sxs-lookup"><span data-stu-id="b167e-219">NCR 3000</span></span>

</dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="b167e-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="b167e-220"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="b167e-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="b167e-221"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="b167e-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="b167e-222"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="b167e-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Abhängige UNIX** -(24)</span><span class="sxs-lookup"><span data-stu-id="b167e-223"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="b167e-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="b167e-224"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="b167e-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="b167e-225"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="b167e-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequenent** (27)</span><span class="sxs-lookup"><span data-stu-id="b167e-226"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="b167e-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="b167e-227"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="b167e-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="b167e-228"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="b167e-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Sonnen Betriebssystem** (30)</span><span class="sxs-lookup"><span data-stu-id="b167e-229"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="b167e-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="b167e-230"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="b167e-231"><span id="ASERIES"></span><span id="aseries"></span>**Aseries** (32)</span><span class="sxs-lookup"><span data-stu-id="b167e-231"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-232">Eine Reihe</span><span class="sxs-lookup"><span data-stu-id="b167e-232">A Series</span></span>

</dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="b167e-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Tandemnsk** (33)</span><span class="sxs-lookup"><span data-stu-id="b167e-233"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-234">Tandem NSK</span><span class="sxs-lookup"><span data-stu-id="b167e-234">Tandem NSK</span></span>

</dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="b167e-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Tandemnt** (34)</span><span class="sxs-lookup"><span data-stu-id="b167e-235"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-236">Tandem NT</span><span class="sxs-lookup"><span data-stu-id="b167e-236">Tandem NT</span></span>

</dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="b167e-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="b167e-237"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-238">BS2000/OSD</span><span class="sxs-lookup"><span data-stu-id="b167e-238">BS2000/OSD</span></span>

</dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="b167e-239"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="b167e-239"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="b167e-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="b167e-240"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="b167e-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="b167e-241"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="b167e-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="b167e-242"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="b167e-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interaktives UNIX** (40)</span><span class="sxs-lookup"><span data-stu-id="b167e-243"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="b167e-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**Bsdunix** (41)</span><span class="sxs-lookup"><span data-stu-id="b167e-244"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-245">BSD UNIX</span><span class="sxs-lookup"><span data-stu-id="b167e-245">BSD UNIX</span></span>

</dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="b167e-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="b167e-246"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="b167e-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="b167e-247"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="b167e-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="b167e-248"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="b167e-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="b167e-249"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-250">Mac OS 9</span><span class="sxs-lookup"><span data-stu-id="b167e-250">Mac OS 9</span></span>

</dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="b167e-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Mach-Kernel** (46)</span><span class="sxs-lookup"><span data-stu-id="b167e-251"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="b167e-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="b167e-252"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="b167e-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="b167e-253"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="b167e-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="b167e-254"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="b167e-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Ixworks** (50)</span><span class="sxs-lookup"><span data-stu-id="b167e-255"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="b167e-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="b167e-256"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="b167e-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)</span><span class="sxs-lookup"><span data-stu-id="b167e-257"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="b167e-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="b167e-258"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="b167e-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="b167e-259"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="b167e-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTStep** (55)</span><span class="sxs-lookup"><span data-stu-id="b167e-260"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="b167e-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="b167e-261"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd>

<span data-ttu-id="b167e-262">Palm OS</span><span class="sxs-lookup"><span data-stu-id="b167e-262">Palm OS</span></span>

</dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="b167e-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="b167e-263"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="b167e-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="b167e-264"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="b167e-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (59)</span><span class="sxs-lookup"><span data-stu-id="b167e-265"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="b167e-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="b167e-266"><span id="VSE"></span><span id="vse"></span>**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="b167e-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="b167e-267"><span id="TPF"></span><span id="tpf"></span>**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b167e-268">**Version**</span><span class="sxs-lookup"><span data-stu-id="b167e-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b167e-269">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b167e-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b167e-270">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="b167e-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b167e-271">Qualifizierer [**: weiter**](/windows/desktop/WmiSdk/standard-qualifiers) gegeben ("[**CIM \_ Softwareelement**](cim-softwareelement.md).**Version**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF ". DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="b167e-271">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_SoftwareElement**](cim-softwareelement.md).**Version**"), [**CIM\_key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="b167e-272">Version des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="b167e-272">Version of the operation.</span></span>

<span data-ttu-id="b167e-273">Die Version des Vorgangs sollte eine der folgenden Formen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="b167e-273">The version of the operation should be in one of the following forms:</span></span>

-   <span data-ttu-id="b167e-274"><major>.<minor>.<revision></span><span class="sxs-lookup"><span data-stu-id="b167e-274"><major>.<minor>.<revision></span></span>
-   <span data-ttu-id="b167e-275"><major>.<minor><letter><revision></span><span class="sxs-lookup"><span data-stu-id="b167e-275"><major>.<minor><letter><revision></span></span>

<span data-ttu-id="b167e-276">Diese Eigenschaft wird von der [**CIM- \_ Überprüfung**](cim-check.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="b167e-276">This property is inherited from [**CIM\_Check**](cim-check.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b167e-277">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b167e-277">Remarks</span></span>

<span data-ttu-id="b167e-278">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b167e-278">WMI does not implement this class.</span></span>

<span data-ttu-id="b167e-279">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="b167e-279">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b167e-280">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b167e-280">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b167e-281">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b167e-281">Requirements</span></span>



| <span data-ttu-id="b167e-282">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b167e-282">Requirement</span></span> | <span data-ttu-id="b167e-283">Wert</span><span class="sxs-lookup"><span data-stu-id="b167e-283">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b167e-284">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b167e-284">Minimum supported client</span></span><br/> | <span data-ttu-id="b167e-285">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b167e-285">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b167e-286">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b167e-286">Minimum supported server</span></span><br/> | <span data-ttu-id="b167e-287">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b167e-287">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b167e-288">Namespace</span><span class="sxs-lookup"><span data-stu-id="b167e-288">Namespace</span></span><br/>                | <span data-ttu-id="b167e-289">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b167e-289">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b167e-290">MOF</span><span class="sxs-lookup"><span data-stu-id="b167e-290">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b167e-291"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b167e-291"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b167e-292">DLL</span><span class="sxs-lookup"><span data-stu-id="b167e-292">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b167e-293"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b167e-293"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b167e-294">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b167e-294">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b167e-295">**CIM- \_ Überprüfung**</span><span class="sxs-lookup"><span data-stu-id="b167e-295">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

