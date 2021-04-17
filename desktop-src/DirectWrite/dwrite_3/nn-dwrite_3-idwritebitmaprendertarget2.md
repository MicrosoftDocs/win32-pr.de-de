---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, der zum Rendern von Glyphen verwendet werden kann.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: edc1df695424eac0bbf0d5a4951b5e9fe4ec0809
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218943"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a><span data-ttu-id="fe2cd-103">IDWriteBitmapRenderTarget2-Schnittstelle (dwrite_3. h)</span><span class="sxs-lookup"><span data-stu-id="fe2cd-103">IDWriteBitmapRenderTarget2 interface (dwrite_3.h)</span></span>

<span data-ttu-id="fe2cd-104">Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, der zum Rendern von Glyphen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fe2cd-104">Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe2cd-105">Diese API ist als Teil der dwrite-Core-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe2cd-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="fe2cd-106">DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="fe2cd-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="fe2cd-107">Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über dbeschreib tecore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span><span class="sxs-lookup"><span data-stu-id="fe2cd-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="inheritance"></a><span data-ttu-id="fe2cd-108">Vererbung</span><span class="sxs-lookup"><span data-stu-id="fe2cd-108">Inheritance</span></span>

<span data-ttu-id="fe2cd-109">Die **IDWriteBitmapRenderTarget2** -Schnittstelle erbt von [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span><span class="sxs-lookup"><span data-stu-id="fe2cd-109">The **IDWriteBitmapRenderTarget2** interface inherits from [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span></span>

## <a name="methods"></a><span data-ttu-id="fe2cd-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="fe2cd-110">Methods</span></span>

<span data-ttu-id="fe2cd-111">Die **IDWriteBitmapRenderTarget2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="fe2cd-111">The **IDWriteBitmapRenderTarget2** interface has these methods.</span></span>

| <span data-ttu-id="fe2cd-112">Methode</span><span class="sxs-lookup"><span data-stu-id="fe2cd-112">Method</span></span> | <span data-ttu-id="fe2cd-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fe2cd-113">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="fe2cd-114">IDWriteBitmapRenderTarget2:: getbitmapdata</span><span class="sxs-lookup"><span data-stu-id="fe2cd-114">IDWriteBitmapRenderTarget2::GetBitmapData</span></span>](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | <span data-ttu-id="fe2cd-115">Ruft die Pixeldaten aus einem Bitmap-Renderziel ab.</span><span class="sxs-lookup"><span data-stu-id="fe2cd-115">Retrieves the pixel data from a bitmap render target.</span></span> |

## <a name="requirements"></a><span data-ttu-id="fe2cd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe2cd-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fe2cd-117">**Unterstützte Mindestversion (Client)**</span><span class="sxs-lookup"><span data-stu-id="fe2cd-117">**Minimum supported client**</span></span> | <span data-ttu-id="fe2cd-118">Windows 10, Project Reunion 0,1-Vorabversion [Win32-Apps]</span><span class="sxs-lookup"><span data-stu-id="fe2cd-118">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="fe2cd-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="fe2cd-119">**Header**</span></span> | <span data-ttu-id="fe2cd-120">dwrite_3. h (dwrite_core. h einschließen)</span><span class="sxs-lookup"><span data-stu-id="fe2cd-120">dwrite_3.h (include dwrite_core.h)</span></span> |