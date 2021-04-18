---
description: Beschreibt eine Regel für den Zugriff auf Elemente, die im geschützten Speicher gespeichert sind.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: PST_ACCESSRULE Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371265"
---
# <a name="pst_accessrule-structure"></a><span data-ttu-id="b133a-103">PST- \_ AccessRule-Struktur</span><span class="sxs-lookup"><span data-stu-id="b133a-103">PST\_ACCESSRULE structure</span></span>

<span data-ttu-id="b133a-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b133a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b133a-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b133a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b133a-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="b133a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b133a-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="b133a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b133a-108">Beschreibt eine Regel für den Zugriff auf Elemente, die im geschützten Speicher gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="b133a-108">Describes a rule for access to items stored in protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="b133a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b133a-109">Syntax</span></span>


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a><span data-ttu-id="b133a-110">Member</span><span class="sxs-lookup"><span data-stu-id="b133a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b133a-111">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="b133a-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="b133a-112">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="b133a-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="b133a-113">**Accessmodeflags**</span><span class="sxs-lookup"><span data-stu-id="b133a-113">**AccessModeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b133a-114">Die Zugriffs Modi, auf die sich ein angegebener Satz von Zugriffs Klauseln bezieht.</span><span class="sxs-lookup"><span data-stu-id="b133a-114">The access modes to which a specified set of access clauses pertain.</span></span>



| <span data-ttu-id="b133a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b133a-115">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="b133a-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b133a-116">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="b133a-117"><dt>**PST \_ Lesen**</dt> von <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="b133a-117"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="b133a-118">Lese Zugriffsmodus.</span><span class="sxs-lookup"><span data-stu-id="b133a-118">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="b133a-119"><dt>**PST \_ Schreiben**</dt> von <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="b133a-119"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="b133a-120">Schreibzugriffs Modus.</span><span class="sxs-lookup"><span data-stu-id="b133a-120">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b133a-121">**cklauseln**</span><span class="sxs-lookup"><span data-stu-id="b133a-121">**cClauses**</span></span>
</dt> <dd>

<span data-ttu-id="b133a-122">Die Anzahl der Strukturen im **rgklauseln** -Array.</span><span class="sxs-lookup"><span data-stu-id="b133a-122">The number of structures in the **rgClauses** array.</span></span>

</dd> <dt>

<span data-ttu-id="b133a-123">**rgklauseln**</span><span class="sxs-lookup"><span data-stu-id="b133a-123">**rgClauses**</span></span>
</dt> <dd>

<span data-ttu-id="b133a-124">Ein Zeiger auf ein Array von [**PST \_ accessclause**](pst-accessclause.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="b133a-124">A pointer to an array of [**PST\_ACCESSCLAUSE**](pst-accessclause.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b133a-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b133a-125">Requirements</span></span>



| <span data-ttu-id="b133a-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b133a-126">Requirement</span></span> | <span data-ttu-id="b133a-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b133a-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b133a-128">Header</span><span class="sxs-lookup"><span data-stu-id="b133a-128">Header</span></span><br/> | <dl> <span data-ttu-id="b133a-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b133a-129"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b133a-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b133a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b133a-131">**PST- \_ accessclause**</span><span class="sxs-lookup"><span data-stu-id="b133a-131">**PST\_ACCESSCLAUSE**</span></span>](pst-accessclause.md)
</dt> <dt>

[<span data-ttu-id="b133a-132">**PST- \_ accessruleset**</span><span class="sxs-lookup"><span data-stu-id="b133a-132">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> </dl>

 

 
