---
description: Ruft das Handle für die automatisch Ausblend Ende appbar ab, die einem Bildschirmrand zugeordnet ist. Diese Meldung erweitert "dem \_ getautohidebar", indem Sie einen bestimmten Monitor zur Verwendung in mehreren Überwachungssituationen angeben.
title: ABM_GETAUTOHIDEBAREX Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982972"
---
# <a name="abm_getautohidebarex-message"></a><span data-ttu-id="b63b4-104">ABM \_ getautohidebarex-Meldung</span><span class="sxs-lookup"><span data-stu-id="b63b4-104">ABM\_GETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="b63b4-105">Ruft das Handle für die automatisch Ausblend Ende appbar ab, die einem Bildschirmrand zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b63b4-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="b63b4-106">Diese Meldung erweitert " [**dem \_ getautohidebar**](abm-getautohidebar.md) ", indem Sie einen bestimmten Monitor zur Verwendung in mehreren Überwachungssituationen angeben.</span><span class="sxs-lookup"><span data-stu-id="b63b4-106">This message extends [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="b63b4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b63b4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b63b4-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="b63b4-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="b63b4-109">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die den Bildschirmrand und-Monitor angibt.</span><span class="sxs-lookup"><span data-stu-id="b63b4-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge and monitor.</span></span> <span data-ttu-id="b63b4-110">Sie müssen die Member **CBSIZE**, **uedge** und **RC** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b63b4-110">You must specify the **cbSize**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b63b4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b63b4-111">Return value</span></span>

<span data-ttu-id="b63b4-112">Gibt das Handle für die automatisch Ausblend-appbar zurück.</span><span class="sxs-lookup"><span data-stu-id="b63b4-112">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="b63b4-113">Der Rückgabewert ist **null** , wenn ein Fehler auftritt oder wenn dem angegebenen Rand des angegebenen Monitors keine Automatisches Ausblenden-appbar zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b63b4-113">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge of the given monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="b63b4-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b63b4-114">Requirements</span></span>



| <span data-ttu-id="b63b4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b63b4-115">Requirement</span></span> | <span data-ttu-id="b63b4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b63b4-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b63b4-117">Header</span><span class="sxs-lookup"><span data-stu-id="b63b4-117">Header</span></span><br/> | <dl> <span data-ttu-id="b63b4-118"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b63b4-118"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b63b4-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b63b4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b63b4-120">**ABM \_ getautohidebar**</span><span class="sxs-lookup"><span data-stu-id="b63b4-120">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="b63b4-121">**ABM-Bild-auf \_**</span><span class="sxs-lookup"><span data-stu-id="b63b4-121">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="b63b4-122">**ABM \_ .**</span><span class="sxs-lookup"><span data-stu-id="b63b4-122">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




