---
description: Gibt den Satz von Zugriffsregeln für die geschützten Speicherdaten an.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: PST_ACCESSRULESET Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371689"
---
# <a name="pst_accessruleset-structure"></a><span data-ttu-id="7dd62-103">PST- \_ accessruleset-Struktur</span><span class="sxs-lookup"><span data-stu-id="7dd62-103">PST\_ACCESSRULESET structure</span></span>

<span data-ttu-id="7dd62-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7dd62-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="7dd62-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7dd62-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="7dd62-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="7dd62-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="7dd62-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="7dd62-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="7dd62-108">Gibt den Satz von Zugriffsregeln für die geschützten Speicherdaten an.</span><span class="sxs-lookup"><span data-stu-id="7dd62-108">Identifies the set of access rules for the protected storage data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd62-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dd62-109">Syntax</span></span>


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a><span data-ttu-id="7dd62-110">Member</span><span class="sxs-lookup"><span data-stu-id="7dd62-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="7dd62-111">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="7dd62-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="7dd62-112">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="7dd62-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="7dd62-113">**crules**</span><span class="sxs-lookup"><span data-stu-id="7dd62-113">**cRules**</span></span>
</dt> <dd>

<span data-ttu-id="7dd62-114">Die Anzahl der Regeln im **rgrules** -Array.</span><span class="sxs-lookup"><span data-stu-id="7dd62-114">The number of rules in the **rgRules** array.</span></span>

</dd> <dt>

<span data-ttu-id="7dd62-115">**rgrules**</span><span class="sxs-lookup"><span data-stu-id="7dd62-115">**rgRules**</span></span>
</dt> <dd>

<span data-ttu-id="7dd62-116">Ein Zeiger auf ein Array von [**PST- \_ AccessRule**](pst-accessrule.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="7dd62-116">A pointer to an array of [**PST\_ACCESSRULE**](pst-accessrule.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7dd62-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7dd62-117">Requirements</span></span>



| <span data-ttu-id="7dd62-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7dd62-118">Requirement</span></span> | <span data-ttu-id="7dd62-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7dd62-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd62-120">Header</span><span class="sxs-lookup"><span data-stu-id="7dd62-120">Header</span></span><br/> | <dl> <span data-ttu-id="7dd62-121"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd62-121"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dd62-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7dd62-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd62-123">**PST- \_ AccessRule**</span><span class="sxs-lookup"><span data-stu-id="7dd62-123">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> <dt>

[<span data-ttu-id="7dd62-124">**"Kreatesubtype"**</span><span class="sxs-lookup"><span data-stu-id="7dd62-124">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> </dl>

 

 
