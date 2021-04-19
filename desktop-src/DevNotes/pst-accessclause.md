---
description: Enthält Informationen über die Access-Klausel für den geschützten Speicher.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: PST_ACCESSCLAUSE Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366897"
---
# <a name="pst_accessclause-structure"></a><span data-ttu-id="6793a-103">PST \_ accessclause-Struktur</span><span class="sxs-lookup"><span data-stu-id="6793a-103">PST\_ACCESSCLAUSE structure</span></span>

<span data-ttu-id="6793a-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6793a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6793a-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6793a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6793a-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="6793a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6793a-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="6793a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6793a-108">Enthält Informationen über die Access-Klausel für den geschützten Speicher.</span><span class="sxs-lookup"><span data-stu-id="6793a-108">Contains information about the access clause for the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="6793a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6793a-109">Syntax</span></span>


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a><span data-ttu-id="6793a-110">Member</span><span class="sxs-lookup"><span data-stu-id="6793a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="6793a-111">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="6793a-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="6793a-112">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="6793a-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="6793a-113">**Klsie Type**</span><span class="sxs-lookup"><span data-stu-id="6793a-113">**ClauseType**</span></span>
</dt> <dd>

<span data-ttu-id="6793a-114">Der Typ der Daten, auf die vom **pbclau-Data** -Member verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6793a-114">The type of data that is pointed to by the **pbClauseData** member.</span></span> <span data-ttu-id="6793a-115">Weitere Informationen finden Sie unter [**pstore-Typen**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="6793a-115">For more information, see [**PStore Types**](pstore-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="6793a-116">**cbclauabdata**</span><span class="sxs-lookup"><span data-stu-id="6793a-116">**cbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="6793a-117">Die Größe der Daten, auf die vom **pbclau-Data** -Member verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6793a-117">The size of the data that is pointed to by the **pbClauseData** member.</span></span>

</dd> <dt>

<span data-ttu-id="6793a-118">**pbclauabdata**</span><span class="sxs-lookup"><span data-stu-id="6793a-118">**pbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="6793a-119">Ein Zeiger auf die Daten der Access-Klausel.</span><span class="sxs-lookup"><span data-stu-id="6793a-119">A pointer to the access clause data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6793a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6793a-120">Requirements</span></span>



| <span data-ttu-id="6793a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6793a-121">Requirement</span></span> | <span data-ttu-id="6793a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6793a-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6793a-123">Header</span><span class="sxs-lookup"><span data-stu-id="6793a-123">Header</span></span><br/> | <dl> <span data-ttu-id="6793a-124"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="6793a-124"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6793a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6793a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6793a-126">**PST- \_ AccessRule**</span><span class="sxs-lookup"><span data-stu-id="6793a-126">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> </dl>

 

 
