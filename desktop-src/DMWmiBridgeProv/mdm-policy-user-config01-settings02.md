---
title: MDM_Policy_User_Config01_Settings02-Klasse
description: Die Benutzer Config01 Settings02-Klasse der MDM- \_ Richtlinie \_ \_ \_ konfiguriert zusätzliche Kalender in der Taskleiste.
ms.assetid: 66cfdb55-17a7-4586-86b3-70ba7dcd5637
keywords:
- MDM_Policy_User_Config01_Settings02-Klasse
- MDM_Policy_User_Config01_Settings02-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Settings02
- MDM_Policy_User_Config01_Settings02.InstanceID
- MDM_Policy_User_Config01_Settings02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8bd0099d19ec4535abf6b525a7487b810b39704
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103863"
---
# <a name="mdm_policy_user_config01_settings02-class"></a><span data-ttu-id="ad60d-105">MDM- \_ Richtlinien \_ Benutzer \_ Config01 \_ Settings02-Klasse</span><span class="sxs-lookup"><span data-stu-id="ad60d-105">MDM\_Policy\_User\_Config01\_Settings02 class</span></span>

<span data-ttu-id="ad60d-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="ad60d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ad60d-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="ad60d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ad60d-108">Die Benutzer Config01 Settings02-Klasse der MDM- \_ Richtlinie \_ \_ \_ konfiguriert zusätzliche Kalender in der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="ad60d-108">The MDM\_Policy\_User\_Config01\_Settings02 class configures additional calendars in the taskbar.</span></span>

<span data-ttu-id="ad60d-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="ad60d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad60d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad60d-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Settings02
{
  string InstanceID;
  string ParentID;
  sint32 ConfigureTaskbarCalendar;
};
```

## <a name="members"></a><span data-ttu-id="ad60d-111">Member</span><span class="sxs-lookup"><span data-stu-id="ad60d-111">Members</span></span>

<span data-ttu-id="ad60d-112">Die **\_ \_ Benutzer \_ Config01 \_ Settings02-Klasse der MDM-Richtlinie** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="ad60d-112">The **MDM\_Policy\_User\_Config01\_Settings02** class has these types of members:</span></span>

-   [<span data-ttu-id="ad60d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad60d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad60d-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad60d-114">Properties</span></span>

<span data-ttu-id="ad60d-115">Die **\_ \_ Benutzer \_ Config01 \_ Settings02-Klasse der MDM-Richtlinie** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ad60d-115">The **MDM\_Policy\_User\_Config01\_Settings02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ad60d-116">Konfigurations Kalender konfigurieren</span><span class="sxs-lookup"><span data-stu-id="ad60d-116">ConfigureTaskbarCalendar</span></span>](/windows/client-management/mdm/policy-csp-settings#settings-configuretaskbarcalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad60d-117">Datentyp: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad60d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad60d-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="ad60d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ad60d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ad60d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad60d-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad60d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad60d-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad60d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad60d-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad60d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ad60d-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ad60d-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad60d-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="ad60d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad60d-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ad60d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad60d-126">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ad60d-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad60d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad60d-127">Requirements</span></span>



| <span data-ttu-id="ad60d-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad60d-128">Requirement</span></span> | <span data-ttu-id="ad60d-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ad60d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad60d-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad60d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ad60d-131">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad60d-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad60d-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad60d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ad60d-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad60d-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ad60d-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="ad60d-134">Namespace</span></span><br/>                | <span data-ttu-id="ad60d-135">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ad60d-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ad60d-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ad60d-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad60d-137"><dt>Dmwmibridgeprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ad60d-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad60d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ad60d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad60d-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad60d-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

