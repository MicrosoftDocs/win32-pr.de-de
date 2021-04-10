---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Gibt den Typ des DirectWrite-factoryobjekts an.
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
ms.openlocfilehash: 603b2ae525ddc6472a3b8581627f2877e06d1aac
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2020
ms.locfileid: "104040028"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a><span data-ttu-id="8ad01-103">DWRITE_FACTORY_TYPE-Enumeration (dwrite. h)</span><span class="sxs-lookup"><span data-stu-id="8ad01-103">DWRITE_FACTORY_TYPE enumeration (dwrite.h)</span></span>

<span data-ttu-id="8ad01-104">Gibt den Typ des DirectWrite-factoryobjekts an.</span><span class="sxs-lookup"><span data-stu-id="8ad01-104">Specifies the type of DirectWrite factory object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ad01-105">Diese API ist als Teil der dwrite-Core-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8ad01-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="8ad01-106">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="8ad01-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="8ad01-107">Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über dbeschreib tecore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="8ad01-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ad01-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ad01-108">Syntax</span></span>
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_RESTRICTED
} ;
```

## <a name="constants"></a><span data-ttu-id="8ad01-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="8ad01-109">Constants</span></span>

| <span data-ttu-id="8ad01-110">Name</span><span class="sxs-lookup"><span data-stu-id="8ad01-110">Name</span></span> | <span data-ttu-id="8ad01-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ad01-111">Description</span></span> |
| ---- |:---- |
| <span data-ttu-id="8ad01-112">DWRITE_FACTORY_TYPE_SHARED</span><span class="sxs-lookup"><span data-stu-id="8ad01-112">DWRITE_FACTORY_TYPE_SHARED</span></span> | <span data-ttu-id="8ad01-113">Gibt an, dass die DirectWrite-Factory eine freigegebene Factory ist und die Wiederverwendung von zwischengespeicherten Schriftart Daten über mehrere Prozess interne Komponenten hinweg ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8ad01-113">Indicates that the DirectWrite factory is a shared factory and that it allows for the reuse of cached font data across multiple in-process components.</span></span> <span data-ttu-id="8ad01-114">Diese Factorys nutzen auch prozessübergreifende Schriftart Caching-Komponenten, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="8ad01-114">Such factories also take advantage of cross process font caching components for better performance.</span></span> |
| <span data-ttu-id="8ad01-115">DWRITE_FACTORY_TYPE_ISOLATED</span><span class="sxs-lookup"><span data-stu-id="8ad01-115">DWRITE_FACTORY_TYPE_ISOLATED</span></span> | <span data-ttu-id="8ad01-116">Gibt an, dass das DirectWrite-Factoryobjekt isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="8ad01-116">Indicates that the DirectWrite factory object is isolated.</span></span> <span data-ttu-id="8ad01-117">Objekte, die aus der isolierten Factory erstellt werden, interagieren nicht mit dem internen DirectWrite-Status anderer Komponenten.</span><span class="sxs-lookup"><span data-stu-id="8ad01-117">Objects created from the isolated factory do not interact with internal DirectWrite state from other components.</span></span> |
| <span data-ttu-id="8ad01-118">DWRITE_FACTORY_TYPE_RESTRICTED</span><span class="sxs-lookup"><span data-stu-id="8ad01-118">DWRITE_FACTORY_TYPE_RESTRICTED</span></span> | <span data-ttu-id="8ad01-119">Objekte, die aus einer eingeschränkten Factory erstellt werden, verwenden weder den internen Zustand noch die von anderen Factorys verwendeten zwischengespeicherten Daten.</span><span class="sxs-lookup"><span data-stu-id="8ad01-119">Objects created from a restricted factory don't use nor modify internal state or cached data used by other factories.</span></span> <span data-ttu-id="8ad01-120">Außerdem enthält die System Schriftart Auflistung nur bekannte Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="8ad01-120">In addition, the system font collection contains only well-known fonts.</span></span>|

## <a name="examples"></a><span data-ttu-id="8ad01-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ad01-121">Examples</span></span>

<span data-ttu-id="8ad01-122">Weitere Informationen finden Sie im Thema [Übersicht über dbeschreib tecore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) und in der Beispiel-App für [dwrite-coregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .</span><span class="sxs-lookup"><span data-stu-id="8ad01-122">See the [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ad01-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ad01-123">Remarks</span></span>

<span data-ttu-id="8ad01-124">Ein DirectWrite-Factoryobjekt enthält Informationen über den internen Zustand, z. b. die Schriftart Lade Modul Registrierung und zwischengespeicherte Schriftart Daten.</span><span class="sxs-lookup"><span data-stu-id="8ad01-124">A DirectWrite factory object contains information about its internal state, such as font loader registration and cached font data.</span></span> <span data-ttu-id="8ad01-125">In den meisten Fällen sollten Sie das freigegebene Factoryobjekt verwenden, da es mehreren Komponenten ermöglicht, die DirectWrite verwenden, um interne DirectWrite-Zustandsinformationen freizugeben, wodurch die Speicherauslastung reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="8ad01-125">In most cases you should use the shared factory object, because it allows multiple components that use DirectWrite to share internal DirectWrite state information, thereby reducing memory usage.</span></span> <span data-ttu-id="8ad01-126">Es gibt jedoch Fälle, in denen es wünschenswert ist, die Auswirkungen einer Komponente auf den restlichen Prozess zu reduzieren, z. b. ein Plug-in aus einer nicht vertrauenswürdigen Quelle, durch Sandkasten und deren Isolierung von den restlichen Prozesskomponenten.</span><span class="sxs-lookup"><span data-stu-id="8ad01-126">However, there are cases when it is desirable to reduce the impact of a component on the rest of the process, such as a plug-in from an untrusted source,  by sandboxing and isolating it from the rest of the process components.</span></span> <span data-ttu-id="8ad01-127">In solchen Fällen sollten Sie eine isolierte Factory für die Sandbox Komponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ad01-127">In such cases, you should use an isolated factory for the sandboxed component.</span></span>

<span data-ttu-id="8ad01-128">Eine eingeschränkte Factory ist besser gesperrt als eine isolierte Factory.</span><span class="sxs-lookup"><span data-stu-id="8ad01-128">A restricted factory is more locked down than an isolated factory.</span></span> <span data-ttu-id="8ad01-129">Es findet in keiner Weise eine Interaktion mit einem prozessübergreifenden oder permanenten Schriftart Cache.</span><span class="sxs-lookup"><span data-stu-id="8ad01-129">It doesn't interact with a cross-process nor persistent font cache in any way.</span></span> <span data-ttu-id="8ad01-130">Außerdem enthält die von dieser Factory zurückgegebene System Schriftart Auflistung nur bekannte Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="8ad01-130">In addition, the system font collection returned from this factory includes only well-known fonts.</span></span> <span data-ttu-id="8ad01-131">Wenn Sie **DWRITE_FACTORY_TYPE_RESTRICTED** an eine Version von dwrite übergeben, die älter als dwrite-Core ist, gibt [dschreitekreatefactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) **E_INVALIDARG** zurück.</span><span class="sxs-lookup"><span data-stu-id="8ad01-131">If you pass **DWRITE_FACTORY_TYPE_RESTRICTED** to a version of DWrite that's older than DWriteCore, then [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) returns **E_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ad01-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ad01-132">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8ad01-133">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="8ad01-133">**Minimum supported client**</span></span> | <span data-ttu-id="8ad01-134">Windows 10, Project Reunion 0,1-Vorabversion [Win32-Apps]</span><span class="sxs-lookup"><span data-stu-id="8ad01-134">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="8ad01-135">**Header**</span><span class="sxs-lookup"><span data-stu-id="8ad01-135">**Header**</span></span> | <span data-ttu-id="8ad01-136">dwrite. h (Include dwrite_core. h)</span><span class="sxs-lookup"><span data-stu-id="8ad01-136">dwrite.h (include dwrite_core.h)</span></span> |
