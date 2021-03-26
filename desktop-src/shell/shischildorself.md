---
UID: ''
title: Shischildorself-Funktion
description: Vergleicht, ob ein Fenster gleich, ein untergeordnetes Element von oder ein Nachfolger von, einem zweiten Fenster ist.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2020
ms.locfileid: "104993303"
---
# <a name="shischildorself-function"></a><span data-ttu-id="7a7db-103">Shischildorself-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a7db-103">SHIsChildOrSelf function</span></span>

## <a name="description"></a><span data-ttu-id="7a7db-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a7db-104">Description</span></span>

<span data-ttu-id="7a7db-105">\[Diese Funktion ist über Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a7db-105">\[This function is available through Windows XP and Windows Server 2003.</span></span>
<span data-ttu-id="7a7db-106">Sie wird möglicherweise in nachfolgenden Versionen von Windows geändert oder ist nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="7a7db-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7a7db-107">Vergleicht, ob ein Fenster gleich, ein untergeordnetes Element von oder ein Nachfolger von, einem zweiten Fenster ist.</span><span class="sxs-lookup"><span data-stu-id="7a7db-107">Compares whether a window is equal to, a child of, or a descendant of, a second window.</span></span>

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a><span data-ttu-id="7a7db-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a7db-108">Parameters</span></span>

### <a name="hwndparent-in"></a><span data-ttu-id="7a7db-109">hwndParent [in]</span><span class="sxs-lookup"><span data-stu-id="7a7db-109">hwndParent [in]</span></span>

<span data-ttu-id="7a7db-110">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="7a7db-110">Type: **HWND**</span></span>

<span data-ttu-id="7a7db-111">Ein Handle für das erste Fenster.</span><span class="sxs-lookup"><span data-stu-id="7a7db-111">A handle to the first window.</span></span>

### <a name="hwnd-in"></a><span data-ttu-id="7a7db-112">HWND [in]</span><span class="sxs-lookup"><span data-stu-id="7a7db-112">hwnd [in]</span></span>

<span data-ttu-id="7a7db-113">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="7a7db-113">Type: **HWND**</span></span>

<span data-ttu-id="7a7db-114">Ein Handle für ein Fenster, das auf *hwndParent* getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a7db-114">A handle to a window to be tested against *hwndParent*.</span></span>

## <a name="returns"></a><span data-ttu-id="7a7db-115">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="7a7db-115">Returns</span></span>

<span data-ttu-id="7a7db-116">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7a7db-116">Type: **HRESULT**</span></span>

<span data-ttu-id="7a7db-117">Gibt **S_OK** zurück, wenn das von *HWND* angegebene Fenster gleich, ein untergeordnetes Element von oder ein Nachfolger des Fensters ist, das von *hwndParent* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a7db-117">Returns **S_OK** if the window specified by *hwnd* is equal to, a child of, or a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="7a7db-118">Gibt **S_FALSE** zurück, wenn das von HWND angegebene Fenster nicht gleich und kein untergeordnetes Element von ist und kein Nachfolger des Fensters ist, das von *hwndParent* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a7db-118">Returns **S_FALSE** if the window specified by hwnd is not equal to, not a child of, and not a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="7a7db-119">Der Rückgabewert ist nicht definiert, wenn ein Fenster Handle ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="7a7db-119">The return value is undefined if either window handle is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a7db-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a7db-120">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="7a7db-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7a7db-121">See also</span></span>

[<span data-ttu-id="7a7db-122">IsChild</span><span class="sxs-lookup"><span data-stu-id="7a7db-122">IsChild</span></span>](/windows/desktop/api/winuser/nf-winuser-ischild)
