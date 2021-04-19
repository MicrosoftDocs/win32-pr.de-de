---
description: 'Der LSA- \_ \_ enumerationshandlerdatentyp wird von der LSA-Funktion verwendet, die die Treuhänder-Domänen Objekte auflistet: lsaenumeratetrusteddomainsex.'
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (ntabcapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348639"
---
# <a name="lsa_enumeration_handle"></a><span data-ttu-id="33134-103">LSA- \_ \_ enumerationshandle</span><span class="sxs-lookup"><span data-stu-id="33134-103">LSA\_ENUMERATION\_HANDLE</span></span>

<span data-ttu-id="33134-104">Der **LSA-enumerationshandlerdatentyp \_ \_** wird von der LSA-Funktion verwendet, die die [**Treuhänder-Domänen**](trusteddomain-object.md) Objekte auflistet: [**lsaenumeratetrusteddomainsex**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span><span class="sxs-lookup"><span data-stu-id="33134-104">The **LSA\_ENUMERATION\_HANDLE** data type is used by the LSA function that enumerates [**TrustedDomain**](trusteddomain-object.md) objects: [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span> <span data-ttu-id="33134-105">Diese Funktion ist so konzipiert, dass Sie mehrere Aufrufe zum Auflisten aller Objekte eines bestimmten Typs in der Datenbank durchführen können.</span><span class="sxs-lookup"><span data-stu-id="33134-105">This function is designed so that you can make multiple calls to enumerate all the objects of a given type in the database.</span></span>

<span data-ttu-id="33134-106">Beim anfänglichen enumerationsfunktions-Befehl übergeben Sie einen Zeiger auf eine **LSA- \_ enumerationshandle \_** -Variable, die mit 0 (null) initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="33134-106">On the initial enumeration function call, you pass in a pointer to an **LSA\_ENUMERATION\_HANDLE** variable that is initialized to zero.</span></span> <span data-ttu-id="33134-107">Die-Funktion aktualisiert diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="33134-107">The function updates this value.</span></span> <span data-ttu-id="33134-108">Wenn die Funktion einen Wert zurückgibt, der angibt, dass weitere Aufzählungs Objekte vorhanden sind, rufen Sie die Funktion erneut auf, und übergeben Sie den aktualisierten **LSA- \_ enumerationshandle \_** -Wert, um eine Enumeration abzurufen, die an dem Punkt fortgesetzt wird, an dem die vorherige Enumeration</span><span class="sxs-lookup"><span data-stu-id="33134-108">If the function returns a value that indicates there are more objects to enumerate, call the function again and pass in the updated **LSA\_ENUMERATION\_HANDLE** value to obtain an enumeration continuing from the point where the previous enumeration left off.</span></span>


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="33134-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33134-109">Requirements</span></span>



| <span data-ttu-id="33134-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33134-110">Requirement</span></span> | <span data-ttu-id="33134-111">Wert</span><span class="sxs-lookup"><span data-stu-id="33134-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="33134-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33134-112">Minimum supported client</span></span><br/> | <span data-ttu-id="33134-113">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33134-113">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="33134-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33134-114">Minimum supported server</span></span><br/> | <span data-ttu-id="33134-115">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33134-115">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="33134-116">Header</span><span class="sxs-lookup"><span data-stu-id="33134-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="33134-117"><dt>Ntabcapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="33134-117"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33134-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33134-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33134-119">**Lsaenumeratetrusteddomainsex**</span><span class="sxs-lookup"><span data-stu-id="33134-119">**LsaEnumerateTrustedDomainsEx**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




