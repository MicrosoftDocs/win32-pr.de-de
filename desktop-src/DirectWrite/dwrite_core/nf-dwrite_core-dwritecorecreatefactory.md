---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core.h)
description: Erstellt ein Factoryobjekt, das für die nachfolgende Erstellung einzelner DWriteCore-Objekte verwendet wird.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
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
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 3ba1b8f6e09212c1ba2f4a0093e2205acaa2e835
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548935"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a><span data-ttu-id="7698d-103">DWriteCoreCreateFactory-Funktion (dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="7698d-103">DWriteCoreCreateFactory function (dwrite_core.h)</span></span>

<span data-ttu-id="7698d-104">Erstellt ein Factoryobjekt, das für die nachfolgende Erstellung einzelner DWriteCore-Objekte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7698d-104">Creates a factory object that is used for subsequent creation of individual DWriteCore objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7698d-105">Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite verfügbar.](../direct-write-portal.md)</span><span class="sxs-lookup"><span data-stu-id="7698d-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="7698d-106">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="7698d-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="7698d-107">Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](../dwritecore-overview.md)</span><span class="sxs-lookup"><span data-stu-id="7698d-107">For more info, and code examples, see [DWriteCore overview](../dwritecore-overview.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7698d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7698d-108">Syntax</span></span>
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a><span data-ttu-id="7698d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7698d-109">Parameters</span></span>

`factoryType`

<span data-ttu-id="7698d-110">Typ: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span><span class="sxs-lookup"><span data-stu-id="7698d-110">Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b></span></span>

<span data-ttu-id="7698d-111">Ein -Wert, der angibt, ob das Factoryobjekt freigegeben, isoliert oder eingeschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="7698d-111">A value that specifies whether the factory object will be shared, isolated, or restricted.</span></span>

`iid`

<span data-ttu-id="7698d-112">Typ: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="7698d-112">Type: <b>REFIID</b></span></span>

<span data-ttu-id="7698d-113">Ein GUID-Wert, der die DirectWrite-Factoryschnittstelle identifiziert, z. B. __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span><span class="sxs-lookup"><span data-stu-id="7698d-113">A GUID value that identifies the DirectWrite factory interface, such as __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).</span></span>

`factory`

<span data-ttu-id="7698d-114">Typ: <b>IUnknown\*\*</b></span><span class="sxs-lookup"><span data-stu-id="7698d-114">Type: <b>IUnknown\*\*</b></span></span>

<span data-ttu-id="7698d-115">Eine Adresse eines Zeigers auf das neu erstellte DirectWrite-Factoryobjekt.</span><span class="sxs-lookup"><span data-stu-id="7698d-115">An address of a pointer to the newly created DirectWrite factory object.</span></span>

## <a name="return-value"></a><span data-ttu-id="7698d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7698d-116">Return value</span></span>

<span data-ttu-id="7698d-117">Typ: <b>HRESULT</b></span><span class="sxs-lookup"><span data-stu-id="7698d-117">Type: <b>HRESULT</b></span></span>

<span data-ttu-id="7698d-118">Wenn diese Methode erfolgreich ist, gibt <b xmlns:loc="http://microsoft.com/wdcml/l10n">sie</b>S_OK.</span><span class="sxs-lookup"><span data-stu-id="7698d-118">If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>.</span></span> <span data-ttu-id="7698d-119">Andernfalls wird ein <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT-Fehlercode</b> zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7698d-119">Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.</span></span>

## <a name="examples"></a><span data-ttu-id="7698d-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7698d-120">Examples</span></span>

<span data-ttu-id="7698d-121">Weitere Informationen finden [Sie im DWriteCore-Übersichtsthema](../dwritecore-overview.md) und in der [DWriteCoreGallery-Beispiel-App.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)</span><span class="sxs-lookup"><span data-stu-id="7698d-121">See the [DWriteCore overview](../dwritecore-overview.md) topic, and the [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) sample app.</span></span>

## <a name="remarks"></a><span data-ttu-id="7698d-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7698d-122">Remarks</span></span>

<span data-ttu-id="7698d-123">Dies ist funktionell identisch mit der [DWriteCreateFactory-Funktion,](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) die von der Systemversion von DirectWrite exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7698d-123">This is functionally the same as the [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) function exported by the system version of DirectWrite.</span></span> <span data-ttu-id="7698d-124">Die DWriteCore-Funktion hat einen anderen Namen, um Mehrdeutigkeiten zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="7698d-124">The DWriteCore function has a different name to avoid ambiguity.</span></span>

## <a name="requirements"></a><span data-ttu-id="7698d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7698d-125">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7698d-126">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="7698d-126">**Minimum supported client**</span></span> | <span data-ttu-id="7698d-127">Windows 10, Project Reunion [Win32-Apps]</span><span class="sxs-lookup"><span data-stu-id="7698d-127">Windows 10, Project Reunion [Win32 apps]</span></span> |
| <span data-ttu-id="7698d-128">**Header**</span><span class="sxs-lookup"><span data-stu-id="7698d-128">**Header**</span></span> | <span data-ttu-id="7698d-129">dwrite.h (include dwrite_core.h)</span><span class="sxs-lookup"><span data-stu-id="7698d-129">dwrite.h (include dwrite_core.h)</span></span> |