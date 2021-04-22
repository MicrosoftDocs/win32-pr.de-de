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
ms.openlocfilehash: 87b0d1c2edcb836afd06d732f242b62441b9bd01
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881809"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="ce3af-103">DWRITE_FACTORY_TYPE-Enumeration (dwrite.h)</span><span class="sxs-lookup"><span data-stu-id="ce3af-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="ce3af-104">Gibt den Typ des DirectWrite-Factoryobjekts an.</span><span class="sxs-lookup"><span data-stu-id="ce3af-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce3af-105">Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce3af-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="ce3af-106">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="ce3af-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="ce3af-107">Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)</span><span class="sxs-lookup"><span data-stu-id="ce3af-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3af-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce3af-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a><span data-ttu-id="ce3af-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ce3af-109">Constants</span></span>

| <span data-ttu-id="ce3af-110">Name</span><span class="sxs-lookup"><span data-stu-id="ce3af-110">Name</span></span> | <span data-ttu-id="ce3af-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce3af-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="ce3af-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="ce3af-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="ce3af-113">Gibt an, dass die DirectWrite-Factory eine freigegebene Factory ist und die Wiederverwendung zwischengespeicherter Schriftartdaten über mehrere Prozesskomponenten hinweg ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="ce3af-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="ce3af-114">Solche Factorys nutzen auch prozessübergreifende Komponenten zum Zwischenspeichern von Schriftarten, um eine bessere Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="ce3af-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="ce3af-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="ce3af-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="ce3af-116">Gibt an, dass das DirectWrite-Factoryobjekt isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="ce3af-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="ce3af-117">Objekte, die aus der isolierten Factory erstellt wurden, interagieren nicht mit dem internen DirectWrite-Zustand anderer Komponenten.</span><span class="sxs-lookup"><span data-stu-id="ce3af-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="ce3af-118">DWRITE_FACTORY_TYPE_ISOLATED2</span><span class="sxs-lookup"><span data-stu-id="ce3af-118">DWRITE_FACTORY_TYPE_ISOLATED2</span></span> | <span data-ttu-id="ce3af-119">Gibt an, dass das DirectWrite-Factoryobjekt eingeschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="ce3af-119">Indicates that the DirectWrite factory object is restricted.</span></span> <span data-ttu-id="ce3af-120">Objekte, die aus einer eingeschränkten Factory erstellt werden, verwenden oder ändern weder den internen Zustand noch zwischengespeicherte Daten, die von anderen Factorys verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce3af-120">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="ce3af-121">Darüber hinaus enthält die Systemschriftartauflistung nur bekannte Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="ce3af-121">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="ce3af-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce3af-122">Examples</span></span>

<span data-ttu-id="ce3af-123">Weitere Informationen finden Sie im Übersichtsthema [DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) und in der [Beispiel-App DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="ce3af-123">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce3af-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce3af-124">Remarks</span></span>

<span data-ttu-id="ce3af-125">Ein DirectWrite-Factoryobjekt enthält Informationen über seinen internen Zustand, z. B. die Registrierung des Schriftartladeprogramm und zwischengespeicherte Schriftartdaten.</span><span class="sxs-lookup"><span data-stu-id="ce3af-125">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="ce3af-126">In den meisten Fällen sollten Sie das freigegebene Factoryobjekt verwenden, da es mehreren Komponenten, die DirectWrite verwenden, ermöglicht, interne DirectWrite-Zustandsinformationen freizugeben, wodurch die Speicherauslastung reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="ce3af-126">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="ce3af-127">Es gibt jedoch Fälle, in denen es wünschenswert ist, die Auswirkungen einer Komponente auf den Rest des Prozesses zu reduzieren, z. B. ein Plug-In aus einer nicht vertrauenswürdigen Quelle, indem sie in der Sandbox gespeichert und von den restlichen Prozesskomponenten isolieren wird.</span><span class="sxs-lookup"><span data-stu-id="ce3af-127">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="ce3af-128">In solchen Fällen sollten Sie eine isolierte Factory für die Sandboxkomponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="ce3af-128">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="ce3af-129">Eine eingeschränkte Factory ist stärker gesperrt als eine isolierte Factory.</span><span class="sxs-lookup"><span data-stu-id="ce3af-129">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="ce3af-130">Es interagiert in irgendeiner Weise nicht mit einem prozessübergreifenden oder beständigen Schriftartcache.</span><span class="sxs-lookup"><span data-stu-id="ce3af-130">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="ce3af-131">Darüber hinaus enthält die von dieser Factory zurückgegebene Auflistung von Systemschriftarten nur bekannte Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="ce3af-131">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="ce3af-132">Wenn Sie **DWRITE_FACTORY_TYPE_ISOLATED2** DWrite-Version übergeben, die älter als DWriteCore ist, gibt [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) **E_INVALIDARG.**</span><span class="sxs-lookup"><span data-stu-id="ce3af-132">If you pass **DWRITE_FACTORY_TYPE_ISOLATED2** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3af-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce3af-133">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ce3af-134">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="ce3af-134">**Minimum supported client**</span></span> | <span data-ttu-id="ce3af-135">Windows 10, Project Reunion [Win32-Apps]</span><span class="sxs-lookup"><span data-stu-id="ce3af-135">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="ce3af-136">**Header**</span><span class="sxs-lookup"><span data-stu-id="ce3af-136">**Header**</span></span> | <span data-ttu-id="ce3af-137">dwrite.h (include dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="ce3af-137">dwrite.h (include dwrite_core.h)</span></span> |
