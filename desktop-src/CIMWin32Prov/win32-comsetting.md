---
description: Die \_ WMI-Klasse für die WMI-Komprimierungen in Win32 stellt die Einstellungen dar, die einer COM-Komponente (com) oder Component Object Model einer COM-Anwendung
ms.assetid: e8cdbee8-41ab-4aff-b17b-707667138411
ms.tgt_platform: multiple
title: Win32_COMSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMSetting
- Win32_COMSetting.Caption
- Win32_COMSetting.Description
- Win32_COMSetting.SettingID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ec7932117d1ff0bc058d2b9a131f77ff9e040bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214076"
---
# <a name="win32_comsetting-class"></a><span data-ttu-id="4ee6c-103">Win32- \_ comsetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="4ee6c-103">Win32\_COMSetting class</span></span>

<span data-ttu-id="4ee6c-104">Die [WMI-Klasse für die WMI](/windows/desktop/WmiSdk/retrieving-a-class) - **\_ Komprimierungen in Win32** stellt die Einstellungen dar, die einer COM-Komponente (com) oder Component Object Model einer COM-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4ee6c-104">The **Win32\_COMSetting** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings associated with a Component Object Model (COM) component or COM application.</span></span>

<span data-ttu-id="4ee6c-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4ee6c-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee6c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ee6c-107">Syntax</span></span>

``` syntax
[abstract, UUID("{E5D8A560-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
};
```

## <a name="members"></a><span data-ttu-id="4ee6c-108">Member</span><span class="sxs-lookup"><span data-stu-id="4ee6c-108">Members</span></span>

<span data-ttu-id="4ee6c-109">Die **Win32- \_ comsetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4ee6c-109">The **Win32\_COMSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="4ee6c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ee6c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ee6c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4ee6c-111">Properties</span></span>

<span data-ttu-id="4ee6c-112">Die **Win32- \_ comsetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-112">The **Win32\_COMSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ee6c-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4ee6c-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ee6c-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ee6c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ee6c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ee6c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ee6c-116">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4ee6c-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4ee6c-117">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-117">Short textual description of the current object.</span></span>

<span data-ttu-id="4ee6c-118">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ee6c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ee6c-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ee6c-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ee6c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ee6c-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ee6c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ee6c-122">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-122">Textual description of the current object.</span></span>

<span data-ttu-id="4ee6c-123">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ee6c-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="4ee6c-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ee6c-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4ee6c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ee6c-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4ee6c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4ee6c-127">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4ee6c-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4ee6c-128">Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-128">Identifier by which the current object is known.</span></span>

<span data-ttu-id="4ee6c-129">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-129">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ee6c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ee6c-130">Remarks</span></span>

<span data-ttu-id="4ee6c-131">Die **Win32- \_ comsetting** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4ee6c-131">The **Win32\_COMSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee6c-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4ee6c-132">Requirements</span></span>



| <span data-ttu-id="4ee6c-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ee6c-133">Requirement</span></span> | <span data-ttu-id="4ee6c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4ee6c-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee6c-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4ee6c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4ee6c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ee6c-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4ee6c-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4ee6c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4ee6c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ee6c-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ee6c-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ee6c-139">Namespace</span></span><br/>                | <span data-ttu-id="4ee6c-140">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4ee6c-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4ee6c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="4ee6c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ee6c-142"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6c-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ee6c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="4ee6c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ee6c-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ee6c-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ee6c-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ee6c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee6c-146">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="4ee6c-146">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="4ee6c-147">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ee6c-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

