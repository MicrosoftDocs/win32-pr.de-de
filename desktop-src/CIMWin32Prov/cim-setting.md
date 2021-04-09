---
description: Die CIM \_ -Einstellungs Klasse stellt Konfigurations bezogene und operative Parameter für ein oder mehrere verwaltete Systemelemente dar.
ms.assetid: 57c46b00-96c4-4df1-82ad-01f7b4f75ced
ms.tgt_platform: multiple
title: CIM_Setting-Klasse (cimwin32-WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f1081bd93c95dfa90b6a4dfa6a87339e8e3172a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861020"
---
# <a name="cim_setting-class-cimwin32-wmi-providers"></a><span data-ttu-id="54ab4-103">CIM_Setting-Klasse (cimwin32-WMI-Anbieter)</span><span class="sxs-lookup"><span data-stu-id="54ab4-103">CIM_Setting class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="54ab4-104">Die **CIM- \_ Einstellungs** Klasse stellt Konfigurations bezogene und operative Parameter für ein oder mehrere verwaltete Systemelemente dar.</span><span class="sxs-lookup"><span data-stu-id="54ab4-104">The **CIM\_Setting** class represents configuration-related and operational parameters for one or more managed system elements.</span></span> <span data-ttu-id="54ab4-105">Einem verwalteten System Element können mehrere Einstellungs Objekte zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="54ab4-105">A managed system element can have multiple setting objects associated with it.</span></span> <span data-ttu-id="54ab4-106">Die aktuellen Betriebswerte für die Parameter eines Elements werden durch Eigenschaften im-Element selbst oder durch Eigenschaften in seinen Zuordnungen reflektiert.</span><span class="sxs-lookup"><span data-stu-id="54ab4-106">The current operational values for an element's parameters are reflected by properties in the element itself or by properties in its associations.</span></span> <span data-ttu-id="54ab4-107">Diese Eigenschaften müssen nicht mit den Werten übereinstimmen, die im Einstellungs Objekt vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="54ab4-107">These properties do not have to be the same values present in the setting object.</span></span> <span data-ttu-id="54ab4-108">Beispielsweise kann ein Modem eine Einstellungs Baudrate von 56 Kilobyte pro Sekunde aufweisen, aber mit 19,2 Kilobyte pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="54ab4-108">For example, a modem may have a setting baud rate of 56 kilobytes per second, but be operating at 19.2 kilobytes per second.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54ab4-109">Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="54ab4-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="54ab4-110">WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="54ab4-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="54ab4-111">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="54ab4-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="54ab4-112">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="54ab4-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ab4-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="54ab4-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C572-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="54ab4-114">Member</span><span class="sxs-lookup"><span data-stu-id="54ab4-114">Members</span></span>

<span data-ttu-id="54ab4-115">Die **CIM- \_ Einstellungs** Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="54ab4-115">The **CIM\_Setting** class has these types of members:</span></span>

-   [<span data-ttu-id="54ab4-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54ab4-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54ab4-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54ab4-117">Properties</span></span>

<span data-ttu-id="54ab4-118">Die **CIM- \_ Einstellungs** Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="54ab4-118">The **CIM\_Setting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54ab4-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="54ab4-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ab4-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54ab4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54ab4-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ab4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54ab4-122">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="54ab4-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="54ab4-123">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="54ab4-123">Short textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="54ab4-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54ab4-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ab4-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54ab4-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54ab4-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ab4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54ab4-127">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="54ab4-127">Textual description of the current object.</span></span>

</dd> <dt>

<span data-ttu-id="54ab4-128">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="54ab4-128">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ab4-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54ab4-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54ab4-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ab4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54ab4-131">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="54ab4-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="54ab4-132">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="54ab4-132">Identifier by which the current object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54ab4-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54ab4-133">Remarks</span></span>

<span data-ttu-id="54ab4-134">Diese Klasse wird von WMI nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="54ab4-134">WMI does not implement this class.</span></span> <span data-ttu-id="54ab4-135">Informationen zu WMI-Klassen, die von **CIM- \_ Einstellungen** abgeleitet sind, finden Sie unter [Win32](win32-provider.md)</span><span class="sxs-lookup"><span data-stu-id="54ab4-135">For WMI classes derived from **CIM\_Setting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="54ab4-136">Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="54ab4-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="54ab4-137">Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="54ab4-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="54ab4-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54ab4-138">Requirements</span></span>



| <span data-ttu-id="54ab4-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54ab4-139">Requirement</span></span> | <span data-ttu-id="54ab4-140">Wert</span><span class="sxs-lookup"><span data-stu-id="54ab4-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54ab4-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54ab4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="54ab4-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54ab4-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54ab4-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54ab4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="54ab4-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54ab4-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54ab4-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="54ab4-145">Namespace</span></span><br/>                | <span data-ttu-id="54ab4-146">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="54ab4-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54ab4-147">MOF</span><span class="sxs-lookup"><span data-stu-id="54ab4-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54ab4-148"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="54ab4-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54ab4-149">DLL</span><span class="sxs-lookup"><span data-stu-id="54ab4-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54ab4-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54ab4-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

