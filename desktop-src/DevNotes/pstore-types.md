---
description: Die Datentypen für geschützte Speichermethoden.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: Pstore-Typen (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361922"
---
# <a name="pstore-types"></a><span data-ttu-id="ce37d-103">Pstore-Typen</span><span class="sxs-lookup"><span data-stu-id="ce37d-103">PStore Types</span></span>

<span data-ttu-id="ce37d-104">\[Geschützter Speicher (pstore) ist für die Verwendung in Windows Server 2003 und Windows XP verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce37d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ce37d-105">Sie steht nur für schreibgeschützte Vorgänge in Windows Server 2008 und Windows Vista zur Verfügung, ist aber möglicherweise in nachfolgenden Versionen nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce37d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ce37d-106">Pstore verwendet eine ältere Implementierung des Schutzes von Daten.</span><span class="sxs-lookup"><span data-stu-id="ce37d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ce37d-107">Entwicklern wird dringend empfohlen, den stärkeren Datenschutz zu nutzen, der von den Funktionen [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) und [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) bereitgestellt wird.\]</span><span class="sxs-lookup"><span data-stu-id="ce37d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ce37d-108">Die Datentypen für geschützte Speichermethoden.</span><span class="sxs-lookup"><span data-stu-id="ce37d-108">The data types for Protected Storage methods.</span></span>


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

<span data-ttu-id="ce37d-109">**PST- \_ AccessMode**</span><span class="sxs-lookup"><span data-stu-id="ce37d-109">**PST\_ACCESSMODE**</span></span>
</dt> <dd>

<span data-ttu-id="ce37d-110">Definiert den Lese-oder Schreibmodus der Zugriffs Regel.</span><span class="sxs-lookup"><span data-stu-id="ce37d-110">Defines the read or write mode of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="ce37d-111">**PST \_ accessclaustype**</span><span class="sxs-lookup"><span data-stu-id="ce37d-111">**PST\_ACCESSCLAUSETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="ce37d-112">Definiert den Klauseltyp der Zugriffs Regel.</span><span class="sxs-lookup"><span data-stu-id="ce37d-112">Defines the clause type of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="ce37d-113">**PST- \_ Taste**</span><span class="sxs-lookup"><span data-stu-id="ce37d-113">**PST\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="ce37d-114">Definiert den Schlüssel für das gespeicherte Element.</span><span class="sxs-lookup"><span data-stu-id="ce37d-114">Defines the key for the stored item.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce37d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce37d-115">Requirements</span></span>



| <span data-ttu-id="ce37d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce37d-116">Requirement</span></span> | <span data-ttu-id="ce37d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ce37d-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce37d-118">Header</span><span class="sxs-lookup"><span data-stu-id="ce37d-118">Header</span></span><br/> | <dl> <span data-ttu-id="ce37d-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce37d-119"><dt>Pstore.h</dt></span></span> </dl> |



 

 
