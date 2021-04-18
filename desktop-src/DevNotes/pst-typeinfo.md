---
description: Beschreibt einen Typ oder einen Untertyp.
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: PST_TYPEINFO Struktur (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: fc78d0570ff2e5cf66a9048d64143149564a51c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372222"
---
# <a name="pst_typeinfo-structure"></a><span data-ttu-id="d57e1-103">PST- \_ TypInfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="d57e1-103">PST\_TYPEINFO structure</span></span>

<span data-ttu-id="d57e1-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d57e1-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d57e1-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d57e1-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d57e1-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="d57e1-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d57e1-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="d57e1-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d57e1-108">Beschreibt einen Typ oder einen Untertyp.</span><span class="sxs-lookup"><span data-stu-id="d57e1-108">Describes a type or a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="d57e1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d57e1-109">Syntax</span></span>


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="d57e1-110">Member</span><span class="sxs-lookup"><span data-stu-id="d57e1-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d57e1-111">**CBSIZE**</span><span class="sxs-lookup"><span data-stu-id="d57e1-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d57e1-112">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="d57e1-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d57e1-113">**szDisplayName**</span><span class="sxs-lookup"><span data-stu-id="d57e1-113">**szDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="d57e1-114">Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die den anzeigen Amen für den Typ darstellt.</span><span class="sxs-lookup"><span data-stu-id="d57e1-114">A pointer to a wide character string that represents the display name for the type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d57e1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d57e1-115">Requirements</span></span>



| <span data-ttu-id="d57e1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d57e1-116">Requirement</span></span> | <span data-ttu-id="d57e1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d57e1-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d57e1-118">Header</span><span class="sxs-lookup"><span data-stu-id="d57e1-118">Header</span></span><br/> | <dl> <span data-ttu-id="d57e1-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d57e1-119"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d57e1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d57e1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d57e1-121">**"Kreatesubtype"**</span><span class="sxs-lookup"><span data-stu-id="d57e1-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> <dt>

[<span data-ttu-id="d57e1-122">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="d57e1-122">**CreateType**</span></span>](ipstore-createtype.md)
</dt> <dt>

[<span data-ttu-id="d57e1-123">**Getsubtypeingefo**</span><span class="sxs-lookup"><span data-stu-id="d57e1-123">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)
</dt> <dt>

[<span data-ttu-id="d57e1-124">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="d57e1-124">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
