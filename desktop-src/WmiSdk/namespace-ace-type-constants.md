---
description: Das typanfeld in einem Zugriffs Steuerungs Eintrag (Access Control Entry, ACE), der bestimmt, ob der ACE ein ACE ist, der den Zugriff zulässt oder verweigert.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Namespace-ACE-Typkonstanten (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371496"
---
# <a name="namespace-ace-type-constants"></a><span data-ttu-id="084ac-103">Namespace-ACE-Typkonstanten</span><span class="sxs-lookup"><span data-stu-id="084ac-103">Namespace ACE Type Constants</span></span>

<span data-ttu-id="084ac-104">Das **typanfeld** in einem Zugriffs Steuerungs Eintrag (Access Control Entry, ACE), der bestimmt, ob der ACE ein ACE ist, der den Zugriff zulässt oder verweigert.</span><span class="sxs-lookup"><span data-stu-id="084ac-104">The **Type** field in an access control entry (ACE) that determines whether the ACE is an ACE that allows access or denies access.</span></span>

<dl> <dt>

<span data-ttu-id="084ac-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Ließen**</span><span class="sxs-lookup"><span data-stu-id="084ac-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="084ac-106">0</span><span class="sxs-lookup"><span data-stu-id="084ac-106">0</span></span>
</dt> <dt>



<span data-ttu-id="084ac-107">Der ACE ermöglicht den Zugriff auf den-Namespace.</span><span class="sxs-lookup"><span data-stu-id="084ac-107">The ACE allows access to the namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="084ac-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Men**</span><span class="sxs-lookup"><span data-stu-id="084ac-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Deny**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="084ac-109">1</span><span class="sxs-lookup"><span data-stu-id="084ac-109">1</span></span>
</dt> <dt>



<span data-ttu-id="084ac-110">Der ACE verweigert den Zugriff auf den-Namespace.</span><span class="sxs-lookup"><span data-stu-id="084ac-110">The ACE denies access to the namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="084ac-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="084ac-111">Requirements</span></span>



| <span data-ttu-id="084ac-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="084ac-112">Requirement</span></span> | <span data-ttu-id="084ac-113">Wert</span><span class="sxs-lookup"><span data-stu-id="084ac-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="084ac-114">Header</span><span class="sxs-lookup"><span data-stu-id="084ac-114">Header</span></span><br/> | <dl> <span data-ttu-id="084ac-115"><dt>WinNT. h</dt></span><span class="sxs-lookup"><span data-stu-id="084ac-115"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="084ac-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="084ac-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="084ac-117">WMI-Sicherheits Konstanten</span><span class="sxs-lookup"><span data-stu-id="084ac-117">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="084ac-118">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="084ac-118">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="084ac-119">Einrichten der Vererbung der Namespace Sicherheit</span><span class="sxs-lookup"><span data-stu-id="084ac-119">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="084ac-120">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="084ac-120">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




