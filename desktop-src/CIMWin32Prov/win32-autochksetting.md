---
description: Die Win32 \_ autochksetting-WMI-Klasse stellt die Einstellungen für den AutoCheck-Vorgang eines Datenträgers dar.
ms.assetid: 637f4d5d-f2f0-4fe0-bbde-7804156979b7
ms.tgt_platform: multiple
title: Win32_AutochkSetting-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AutochkSetting
- Win32_AutochkSetting.Caption
- Win32_AutochkSetting.Description
- Win32_AutochkSetting.SettingID
- Win32_AutochkSetting.UserInputDelay
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea3da60cd4075aa2e36285d30950d3a105d59354
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344844"
---
# <a name="win32_autochksetting-class"></a><span data-ttu-id="4828b-103">Win32 \_ autochksetting-Klasse</span><span class="sxs-lookup"><span data-stu-id="4828b-103">Win32\_AutochkSetting class</span></span>

<span data-ttu-id="4828b-104">Die **Win32 \_ autochksetting** - [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) stellt die Einstellungen für den AutoCheck-Vorgang eines Datenträgers dar.</span><span class="sxs-lookup"><span data-stu-id="4828b-104">The **Win32\_AutochkSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings for the autocheck operation of a disk.</span></span>

<span data-ttu-id="4828b-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4828b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4828b-106">Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4828b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4828b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4828b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, AMENDMENT]
class Win32_AutochkSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 UserInputDelay;
};
```

## <a name="members"></a><span data-ttu-id="4828b-108">Member</span><span class="sxs-lookup"><span data-stu-id="4828b-108">Members</span></span>

<span data-ttu-id="4828b-109">Die **Win32 \_ autochksetting** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="4828b-109">The **Win32\_AutochkSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="4828b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4828b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4828b-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4828b-111">Properties</span></span>

<span data-ttu-id="4828b-112">Die **Win32 \_ autochksetting** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4828b-112">The **Win32\_AutochkSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4828b-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4828b-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828b-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4828b-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4828b-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4828b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4828b-116">Qualifizierer: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="4828b-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4828b-117">Kurze Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4828b-117">Short textual description of the current object.</span></span>

<span data-ttu-id="4828b-118">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4828b-118">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="4828b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4828b-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828b-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4828b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4828b-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4828b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4828b-122">Textbeschreibung des aktuellen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="4828b-122">Textual description of the current object.</span></span>

<span data-ttu-id="4828b-123">Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.</span><span class="sxs-lookup"><span data-stu-id="4828b-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="4828b-124">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="4828b-124">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828b-125">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4828b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4828b-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="4828b-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4828b-127">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("SettingID"), [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4828b-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingId"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4828b-128">Eine ID, die als Teil eines Schlüssels für das aktuelle-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4828b-128">An ID that is used as part of a key for the current object.</span></span>

</dd> <dt>

<span data-ttu-id="4828b-129">**UserInputDelay**</span><span class="sxs-lookup"><span data-stu-id="4828b-129">**UserInputDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4828b-130">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4828b-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4828b-131">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="4828b-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4828b-132">Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \| autochktimeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span><span class="sxs-lookup"><span data-stu-id="4828b-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKLM\\\\CurrentControlSet\\\\Control\\\\Session Manager \| AutoChkTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="4828b-133">Die Benutzereingabe Verzögerung für die automatische Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="4828b-133">The user input delay for autocheck.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4828b-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4828b-134">Remarks</span></span>

<span data-ttu-id="4828b-135">Die **Win32 \_ autochksetting** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4828b-135">The **Win32\_AutochkSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4828b-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4828b-136">Requirements</span></span>



| <span data-ttu-id="4828b-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4828b-137">Requirement</span></span> | <span data-ttu-id="4828b-138">Wert</span><span class="sxs-lookup"><span data-stu-id="4828b-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4828b-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4828b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4828b-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4828b-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4828b-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4828b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4828b-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4828b-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4828b-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="4828b-143">Namespace</span></span><br/>                | <span data-ttu-id="4828b-144">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4828b-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4828b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="4828b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4828b-146"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4828b-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4828b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="4828b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4828b-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4828b-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4828b-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4828b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4828b-150">**CIM- \_ Einstellung**</span><span class="sxs-lookup"><span data-stu-id="4828b-150">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="4828b-151">Computer System-Hardware Klassen</span><span class="sxs-lookup"><span data-stu-id="4828b-151">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

