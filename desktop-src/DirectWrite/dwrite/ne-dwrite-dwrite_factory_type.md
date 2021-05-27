---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Gibt den Typ des DirectWrite-Factoryobjekts an.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
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
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 51cfbb274d681bb35b806f49aef13cc4a220ee26
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550305"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="d5e0a-103">DWRITE_FACTORY_TYPE-Enumeration (dwrite.h)</span><span class="sxs-lookup"><span data-stu-id="d5e0a-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="d5e0a-104">Gibt den Typ des DirectWrite-Factoryobjekts an.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5e0a-105">Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="d5e0a-106">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="d5e0a-107">Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="d5e0a-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5e0a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5e0a-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a><span data-ttu-id="d5e0a-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d5e0a-109">Constants</span></span>

| <span data-ttu-id="d5e0a-110">Name</span><span class="sxs-lookup"><span data-stu-id="d5e0a-110">Name</span></span> | <span data-ttu-id="d5e0a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5e0a-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="d5e0a-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="d5e0a-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="d5e0a-113">Gibt an, dass die DirectWrite-Factory eine freigegebene Factory ist und die Wiederverwendung zwischengespeicherter Schriftartdaten über mehrere Prozesskomponenten hinweg ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="d5e0a-114">Solche Factorys nutzen auch prozessübergreifende Komponenten zum Zwischenspeichern von Schriftarten, um eine bessere Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="d5e0a-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="d5e0a-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="d5e0a-116">Gibt an, dass das DirectWrite-Factoryobjekt isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="d5e0a-117">Objekte, die aus der isolierten Factory erstellt wurden, interagieren nicht mit dem internen DirectWrite-Zustand anderer Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="d5e0a-118">DWRITE_FACTORY_TYPE_ISOLATED2</span><span class="sxs-lookup"><span data-stu-id="d5e0a-118">DWRITE_FACTORY_TYPE_ISOLATED2</span></span> | <span data-ttu-id="d5e0a-119">Gibt an, dass das DirectWrite-Factoryobjekt eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-119">Indicates that the DirectWrite factory object is restricted.</span></span> <span data-ttu-id="d5e0a-120">Objekte, die aus einer eingeschränkten Factory erstellt werden, verwenden oder ändern weder den internen Zustand noch zwischengespeicherte Daten, die von anderen Factorys verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-120">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="d5e0a-121">Darüber hinaus enthält die Systemschriftartenauflistung nur bekannte Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-121">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="d5e0a-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5e0a-122">Examples</span></span>

<span data-ttu-id="d5e0a-123">Weitere Informationen finden Sie im [Übersichtsthema DWriteCore](../dwritecore-overview.md) und in der [Beispiel-App DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="d5e0a-123">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e0a-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d5e0a-124">Remarks</span></span>

<span data-ttu-id="d5e0a-125">Ein DirectWrite-Factoryobjekt enthält Informationen über seinen internen Zustand, z. B. die Registrierung des Schriftartladeprogramm und zwischengespeicherte Schriftartdaten.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-125">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="d5e0a-126">In den meisten Fällen sollten Sie das freigegebene Factoryobjekt verwenden, da es mehreren Komponenten, die DirectWrite verwenden, ermöglicht, interne DirectWrite-Zustandsinformationen freizugeben, wodurch die Speicherauslastung reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-126">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="d5e0a-127">Es gibt jedoch Fälle, in denen es wünschenswert ist, die Auswirkungen einer Komponente auf den Rest des Prozesses zu reduzieren, z. B. ein Plug-In aus einer nicht vertrauenswürdigen Quelle, indem sie in der Sandbox gespeichert und von den restlichen Prozesskomponenten isolieren wird.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-127">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="d5e0a-128">In solchen Fällen sollten Sie eine isolierte Factory für die Sandboxkomponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-128">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="d5e0a-129">Eine eingeschränkte Factory ist stärker gesperrt als eine isolierte Factory.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-129">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="d5e0a-130">Es interagiert in irgendeiner Weise nicht mit einem prozessübergreifenden oder beständigen Schriftartcache.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-130">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="d5e0a-131">Darüber hinaus enthält die von dieser Factory zurückgegebene Auflistung von Systemschriftarten nur bekannte Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="d5e0a-131">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="d5e0a-132">Wenn Sie **DWRITE_FACTORY_TYPE_ISOLATED2** DWrite-Version übergeben, die älter als DWriteCore ist, gibt [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) **E_INVALIDARG.**</span><span class="sxs-lookup"><span data-stu-id="d5e0a-132">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e0a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5e0a-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d5e0a-134">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="d5e0a-134">**Minimum supported client**</span></span> | <span data-ttu-id="d5e0a-135">Windows 10, Project Reunion [Win32-Apps]</span><span class="sxs-lookup"><span data-stu-id="d5e0a-135">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="d5e0a-136">**Header**</span><span class="sxs-lookup"><span data-stu-id="d5e0a-136">**Header**</span></span> | <span data-ttu-id="d5e0a-137">dwrite.h (include dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="d5e0a-137">dwrite.h (include dwrite_core.h)</span></span> |