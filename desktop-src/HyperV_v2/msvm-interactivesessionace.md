---
description: Stellt einen Zugriffs Steuerungs Eintrag (ACE) dar, der den Zugriff auf die interaktive Sitzung eines virtuellen Computers bestimmt.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Msvm_InteractiveSessionACE-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355502"
---
# <a name="msvm_interactivesessionace-class"></a><span data-ttu-id="f5035-103">MSVM \_ interactivesessionace-Klasse</span><span class="sxs-lookup"><span data-stu-id="f5035-103">Msvm\_InteractiveSessionACE class</span></span>

<span data-ttu-id="f5035-104">Stellt einen *Zugriffs Steuerungs Eintrag* (ACE) dar, der den Zugriff auf die interaktive Sitzung eines virtuellen Computers bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f5035-104">Represents an *access control entry* (ACE) that determines access to the interactive session of a virtual machine.</span></span>

<span data-ttu-id="f5035-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f5035-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5035-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5035-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a><span data-ttu-id="f5035-107">Member</span><span class="sxs-lookup"><span data-stu-id="f5035-107">Members</span></span>

<span data-ttu-id="f5035-108">Die **MSVM \_ interactivesessionace** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f5035-108">The **Msvm\_InteractiveSessionACE** class has these types of members:</span></span>

-   [<span data-ttu-id="f5035-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5035-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5035-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5035-110">Properties</span></span>

<span data-ttu-id="f5035-111">Die **MSVM \_ interactivesessionace** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f5035-111">The **Msvm\_InteractiveSessionACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5035-112">**Access Type**</span><span class="sxs-lookup"><span data-stu-id="f5035-112">**AccessType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5035-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f5035-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f5035-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f5035-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5035-115">Gibt an, ob der ACE dem Vertrauens nehmer den Zugriff gewährt oder verweigert.</span><span class="sxs-lookup"><span data-stu-id="f5035-115">Indicates whether the ACE grants or denies access to the trustee.</span></span>

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

<span data-ttu-id="f5035-116">**Zugriff zulässig** (0)</span><span class="sxs-lookup"><span data-stu-id="f5035-116">**Access Allowed** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

<span data-ttu-id="f5035-117">**Zugriff verweigert** (1)</span><span class="sxs-lookup"><span data-stu-id="f5035-117">**Access Denied** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f5035-118">**Stiftungs**</span><span class="sxs-lookup"><span data-stu-id="f5035-118">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5035-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f5035-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5035-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f5035-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5035-121">Identifiziert den Sicherheits Prinzipal, dem der ACE den Zugriff gewährt oder verweigert.</span><span class="sxs-lookup"><span data-stu-id="f5035-121">Identifies the security principal that the ACE grants or denies access to.</span></span> <span data-ttu-id="f5035-122">Gültige Formate für diese Eigenschaft sind das Windows Sam-kompatible Benutzernamen Format und das Windows-SID-Zeichen folgen Format.</span><span class="sxs-lookup"><span data-stu-id="f5035-122">Valid formats for this property include the Windows SAM-compatible user name format and the Windows SID string format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5035-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5035-123">Requirements</span></span>



| <span data-ttu-id="f5035-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5035-124">Requirement</span></span> | <span data-ttu-id="f5035-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f5035-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5035-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5035-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f5035-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5035-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f5035-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5035-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f5035-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5035-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5035-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5035-130">Namespace</span></span><br/>                | <span data-ttu-id="f5035-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="f5035-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f5035-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f5035-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5035-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f5035-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5035-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f5035-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5035-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f5035-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f5035-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5035-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5035-137">**Getinteractivesessionacl**</span><span class="sxs-lookup"><span data-stu-id="f5035-137">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




