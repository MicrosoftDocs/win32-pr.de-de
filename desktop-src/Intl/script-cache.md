---
description: Definiert einen uniscrikcache für Schriftart Metrik.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350074"
---
# <a name="script_cache"></a><span data-ttu-id="8827b-103">Skript \_ Cache</span><span class="sxs-lookup"><span data-stu-id="8827b-103">SCRIPT\_CACHE</span></span>

<span data-ttu-id="8827b-104">Definiert einen uniscrikcache für Schriftart Metrik.</span><span class="sxs-lookup"><span data-stu-id="8827b-104">Defines a Uniscribe font metric cache.</span></span>


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a><span data-ttu-id="8827b-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8827b-105">Remarks</span></span>

<span data-ttu-id="8827b-106">Dies ist eine nicht transparente Struktur.</span><span class="sxs-lookup"><span data-stu-id="8827b-106">This is an opaque structure.</span></span> <span data-ttu-id="8827b-107">Die Anwendung muss eine Skript \_ Cache Variable für jeden verwendeten Zeichenstil zuordnen und beibehalten.</span><span class="sxs-lookup"><span data-stu-id="8827b-107">The application must allocate and retain one SCRIPT\_CACHE variable for each character style used.</span></span> <span data-ttu-id="8827b-108">Die Variable muss mit **null** initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8827b-108">The variable must be initialized to **NULL**.</span></span>

<span data-ttu-id="8827b-109">Viele Skriptfunktionen nehmen eine Kombination aus einem Hardware Geräte-Kontext Handle und einer Skript \_ Cache Variable auf.</span><span class="sxs-lookup"><span data-stu-id="8827b-109">Many script functions take a combination of a hardware device context handle and a SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="8827b-110">Uniscriversucht zunächst, mithilfe der Skript Cache Variable auf Schriftart Daten zuzugreifen \_ .</span><span class="sxs-lookup"><span data-stu-id="8827b-110">Uniscribe first attempts to access font data by using the SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="8827b-111">Der Hardware Gerätekontext wird nur überprüft, wenn die erforderlichen Daten nicht bereits zwischengespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="8827b-111">It only inspects the hardware device context if the required data is not already cached.</span></span>

<span data-ttu-id="8827b-112">Das Hardware Gerätekontext Handle kann als **null** an unischreiber übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8827b-112">The hardware device context handle can be passed to Uniscribe as **NULL**.</span></span> <span data-ttu-id="8827b-113">Wenn die von unischreiber benötigten Daten bereits zwischengespeichert sind, wird auf den Gerätekontext nicht zugegriffen, und der Vorgang wird normal fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="8827b-113">If data required by Uniscribe is already cached, the device context is not accessed, and the operation continues normally.</span></span>

<span data-ttu-id="8827b-114">Wenn der Gerätekontext als **null** und unischreiber aus irgendeinem Grund darauf zugreifen muss, gibt uniscriden Fehlercode E \_ Pending zurück.</span><span class="sxs-lookup"><span data-stu-id="8827b-114">If the device context is passed as **NULL** and Uniscribe needs to access it for any reason, Uniscribe returns the error code E\_PENDING.</span></span> <span data-ttu-id="8827b-115">Dieser Code wird schnell zurückgegeben, sodass die Anwendung zeitaufwändige [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) -Aufrufe vermeiden kann.</span><span class="sxs-lookup"><span data-stu-id="8827b-115">This code is returned quickly, allowing the application to avoid time-consuming [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) calls.</span></span>

## <a name="examples"></a><span data-ttu-id="8827b-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8827b-116">Examples</span></span>

<span data-ttu-id="8827b-117">Das folgende Beispiel gilt für alle Funktionen, die eine Skript \_ Cache Variable und ein optionales Handle für einen Hardware Gerätekontext akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="8827b-117">The following example applies to all functions that take a SCRIPT\_CACHE variable and an optional handle to a hardware device context.</span></span>


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a><span data-ttu-id="8827b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8827b-118">Requirements</span></span>



| <span data-ttu-id="8827b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8827b-119">Requirement</span></span> | <span data-ttu-id="8827b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8827b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8827b-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8827b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8827b-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8827b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8827b-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8827b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8827b-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8827b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8827b-125">Header</span><span class="sxs-lookup"><span data-stu-id="8827b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8827b-126"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8827b-126"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8827b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8827b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8827b-128">Unischreiber</span><span class="sxs-lookup"><span data-stu-id="8827b-128">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="8827b-129">Uniscristrukturen</span><span class="sxs-lookup"><span data-stu-id="8827b-129">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="8827b-130">Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="8827b-130">Caching</span></span>](caching.md)
</dt> </dl>

 

 
