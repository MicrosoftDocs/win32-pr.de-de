---
description: Stellt ein Tablet dar, das mit dem Computer verbunden ist.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: ITablet-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356289"
---
# <a name="itablet-interface"></a><span data-ttu-id="b3722-103">ITablet-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b3722-103">ITablet interface</span></span>

<span data-ttu-id="b3722-104">Stellt ein Tablet dar, das mit dem Computer verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b3722-104">Represents a tablet attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="b3722-105">Member</span><span class="sxs-lookup"><span data-stu-id="b3722-105">Members</span></span>

<span data-ttu-id="b3722-106">Die **iTablet** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b3722-106">The **ITablet** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b3722-107">**Außerdem gibt** es die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b3722-107">**ITablet** also has these types of members:</span></span>

-   [<span data-ttu-id="b3722-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="b3722-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b3722-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="b3722-109">Methods</span></span>

<span data-ttu-id="b3722-110">Die **iTablet** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b3722-110">The **ITablet** interface has these methods.</span></span>



| <span data-ttu-id="b3722-111">Methode</span><span class="sxs-lookup"><span data-stu-id="b3722-111">Method</span></span>                                                                 | <span data-ttu-id="b3722-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3722-112">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3722-113">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="b3722-113">**CreateContext**</span></span>](itablet-createcontext.md)                         | <span data-ttu-id="b3722-114">Erstellt ein Kontext Objekt, das das angegebene Tablet-Gerät beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b3722-114">Creates a context object that describes the specified tablet device.</span></span><br/>       |
| <span data-ttu-id="b3722-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b3722-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span></span>                                 | <span data-ttu-id="b3722-116">Ruft das angegebene [**itabletcursor**](itabletcursor.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="b3722-116">Retrieves the specified [**ITabletCursor**](itabletcursor.md) object.</span></span><br/>     |
| [<span data-ttu-id="b3722-117">**Getcurrsorcount**</span><span class="sxs-lookup"><span data-stu-id="b3722-117">**GetCursorCount**</span></span>](itablet-getcursorcount.md)                       | <span data-ttu-id="b3722-118">Ruft die Anzahl der dem Tablet zugeordneten Cursor Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="b3722-118">Retrieves the number of cursor objects associated with the tablet.</span></span><br/>         |
| [<span data-ttu-id="b3722-119">**Getdefaultcontextsettings**</span><span class="sxs-lookup"><span data-stu-id="b3722-119">**GetDefaultContextSettings**</span></span>](itablet-getdefaultcontextsettings.md) | <span data-ttu-id="b3722-120">Ruft die Standardkontext Einstellungen für das Tablet ab.</span><span class="sxs-lookup"><span data-stu-id="b3722-120">Retrieves the default context settings for the tablet.</span></span><br/>                     |
| [<span data-ttu-id="b3722-121">**Gethardwarecaps**</span><span class="sxs-lookup"><span data-stu-id="b3722-121">**GetHardwareCaps**</span></span>](itablet-gethardwarecaps.md)                     | <span data-ttu-id="b3722-122">Ruft einen Wert ab, der die Funktionen der Tablet-Hardware darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3722-122">Retrieves a value that represents the capabilities of the tablet hardware.</span></span><br/> |
| [<span data-ttu-id="b3722-123">**Getmaxinputrect**</span><span class="sxs-lookup"><span data-stu-id="b3722-123">**GetMaxInputRect**</span></span>](itablet-getmaxinputrect.md)                     | <span data-ttu-id="b3722-124">Ruft ein Rechteck ab, das den maximalen Eingabebereich des Tablets darstellt.</span><span class="sxs-lookup"><span data-stu-id="b3722-124">Retrieves a rectangle that represents maximum input area of the tablet.</span></span><br/>    |
| [<span data-ttu-id="b3722-125">**GetName**</span><span class="sxs-lookup"><span data-stu-id="b3722-125">**GetName**</span></span>](itablet-getname.md)                                     | <span data-ttu-id="b3722-126">Ruft eine Zeichenfolge ab, die den Namen des Tablettgeräts enthält.</span><span class="sxs-lookup"><span data-stu-id="b3722-126">Retrieves a string containing the name of the tablet device.</span></span><br/>               |
| [<span data-ttu-id="b3722-127">**Getplugandplayid**</span><span class="sxs-lookup"><span data-stu-id="b3722-127">**GetPlugAndPlayId**</span></span>](itablet-getplugandplayid.md)                   | <span data-ttu-id="b3722-128">Ruft eine Zeichenfolge ab, die die Plug & Play ID für das Tablet-Gerät enthält.</span><span class="sxs-lookup"><span data-stu-id="b3722-128">Retrieves a string containing the Plug and Play ID for the tablet device.</span></span><br/>  |
| <span data-ttu-id="b3722-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b3722-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span></span>               | <span data-ttu-id="b3722-130">Ruft die Metrikdaten für eine angegebene Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="b3722-130">Retrieves the metrics data for a specified property.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="b3722-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3722-131">Remarks</span></span>

<span data-ttu-id="b3722-132">Entwickler sollten diese Schnittstelle nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3722-132">Developers should not use this interface.</span></span>

<span data-ttu-id="b3722-133">Im folgenden Code wird beschrieben, wie die **iTablet** -Schnittstelle definiert wird.</span><span class="sxs-lookup"><span data-stu-id="b3722-133">The following code describes how the **ITablet** interface is defined.</span></span>

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a><span data-ttu-id="b3722-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3722-134">Requirements</span></span>



| <span data-ttu-id="b3722-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3722-135">Requirement</span></span> | <span data-ttu-id="b3722-136">Wert</span><span class="sxs-lookup"><span data-stu-id="b3722-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3722-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3722-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b3722-138">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b3722-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b3722-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3722-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b3722-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b3722-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b3722-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b3722-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3722-142"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3722-142"><dt>Wisptis.exe</dt></span></span> </dl> |



 

