---
description: Win32 \_ pagefilesetting&\# 8194; WMI-Klasse stellt die Einstellungen einer Auslagerungs Datei dar.
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Win32_PageFileSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339703"
---
# <a name="win32_pagefilesetting-class"></a><span data-ttu-id="6619f-103">Win32- \_ pagefilesetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="6619f-103">Win32\_PageFileSetting class</span></span>

<span data-ttu-id="6619f-104">Die **Win32 \_ pagefilesetting**- [WMI-Klasse](../wmisdk/retrieving-a-class.md) stellt die Einstellungen einer Auslagerungs Datei dar.</span><span class="sxs-lookup"><span data-stu-id="6619f-104">The **Win32\_PageFileSetting** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings of a page file.</span></span> <span data-ttu-id="6619f-105">Informationen, die in Objekten enthalten sind, die von dieser Klasse instanziiert werden, geben die Auslagerungs Datei Parameter an, die beim Systemstart erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6619f-105">Information contained within objects instantiated from this class specify the page file parameters used when the file is created at system startup.</span></span> <span data-ttu-id="6619f-106">Die Eigenschaften in dieser Klasse können geändert und bis zum Start verzögert werden.</span><span class="sxs-lookup"><span data-stu-id="6619f-106">The properties in this class can be modified and deferred until startup.</span></span> <span data-ttu-id="6619f-107">Diese Einstellungen unterscheiden sich vom Lauf Zeit Zustand einer Auslagerungs Datei, die durch die zugeordnete [**Win32- \_ PageFileUsage**](win32-pagefileusage.md)-Klasse ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="6619f-107">These settings are different from the run-time state of a page file expressed through the associated class [**Win32\_PageFileUsage**](win32-pagefileusage.md).</span></span>

<span data-ttu-id="6619f-108">Um eine Instanz dieser Klasse zu erstellen, aktivieren Sie die Berechtigung **secreatepagefileprivilege** .</span><span class="sxs-lookup"><span data-stu-id="6619f-108">To create an instance of this class, enable the **SeCreatePagefilePrivilege** privilege.</span></span> <span data-ttu-id="6619f-109">Weitere Informationen finden Sie unter [**Berechtigungs Konstanten**](../wmisdk/privilege-constants.md) und [Ausführen privilegierter Vorgänge](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="6619f-109">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="6619f-110">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6619f-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6619f-111">Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="6619f-111">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6619f-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="6619f-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="6619f-113">Member</span><span class="sxs-lookup"><span data-stu-id="6619f-113">Members</span></span>

<span data-ttu-id="6619f-114">Die **Win32-Klasse \_ pagefilesetting** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6619f-114">The **Win32\_PageFileSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="6619f-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6619f-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6619f-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6619f-116">Properties</span></span>

<span data-ttu-id="6619f-117">Die **Win32-Klasse \_ pagefilesetting** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6619f-117">The **Win32\_PageFileSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6619f-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6619f-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6619f-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6619f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6619f-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6619f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6619f-121">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="6619f-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6619f-122">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6619f-122">Short textual description of the current object.</span></span>

<span data-ttu-id="6619f-123">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6619f-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="6619f-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6619f-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6619f-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6619f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6619f-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6619f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6619f-127">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="6619f-127">Textual description of the current object.</span></span>

<span data-ttu-id="6619f-128">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6619f-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="6619f-129">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="6619f-129">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6619f-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6619f-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6619f-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6619f-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6619f-132">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("Megabytes")</span><span class="sxs-lookup"><span data-stu-id="6619f-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="6619f-133">Anfängliche Größe der Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="6619f-133">Initial size of the page file.</span></span>

<span data-ttu-id="6619f-134">Beispiel: 139</span><span class="sxs-lookup"><span data-stu-id="6619f-134">Example: 139</span></span>

</dd> <dt>

<span data-ttu-id="6619f-135">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="6619f-135">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6619f-136">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6619f-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6619f-137">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6619f-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6619f-138">Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ Memory Management \| PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("Megabytes")</span><span class="sxs-lookup"><span data-stu-id="6619f-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="6619f-139">Maximale Größe der Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="6619f-139">Maximum size of the page file.</span></span>

<span data-ttu-id="6619f-140">Beispiel: 178</span><span class="sxs-lookup"><span data-stu-id="6619f-140">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="6619f-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="6619f-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6619f-142">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6619f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6619f-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6619f-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6619f-144">Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="6619f-144">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="6619f-145">Der Pfad und der Dateiname der Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="6619f-145">Path and file name of the page file.</span></span>

<span data-ttu-id="6619f-146">Beispiel: "C: \\PAGEFILE.SYS"</span><span class="sxs-lookup"><span data-stu-id="6619f-146">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="6619f-147">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="6619f-147">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6619f-148">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6619f-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6619f-149">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6619f-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6619f-150">Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6619f-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6619f-151">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="6619f-151">Identifier by which the current object is known.</span></span>

<span data-ttu-id="6619f-152">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="6619f-152">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6619f-153">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6619f-153">Remarks</span></span>

<span data-ttu-id="6619f-154">Die **Win32- \_ pagefilesetting** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="6619f-154">The **Win32\_PageFileSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6619f-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6619f-155">Requirements</span></span>



| <span data-ttu-id="6619f-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6619f-156">Requirement</span></span> | <span data-ttu-id="6619f-157">Wert</span><span class="sxs-lookup"><span data-stu-id="6619f-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6619f-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6619f-158">Minimum supported client</span></span><br/> | <span data-ttu-id="6619f-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6619f-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6619f-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6619f-160">Minimum supported server</span></span><br/> | <span data-ttu-id="6619f-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6619f-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6619f-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="6619f-162">Namespace</span></span><br/>                | <span data-ttu-id="6619f-163">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6619f-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6619f-164">MOF</span><span class="sxs-lookup"><span data-stu-id="6619f-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6619f-165"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6619f-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6619f-166">DLL</span><span class="sxs-lookup"><span data-stu-id="6619f-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6619f-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6619f-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6619f-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6619f-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6619f-169">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="6619f-169">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="6619f-170">Betriebssystemklassen</span><span class="sxs-lookup"><span data-stu-id="6619f-170">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
