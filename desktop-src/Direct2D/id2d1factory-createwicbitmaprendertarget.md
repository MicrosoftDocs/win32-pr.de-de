---
title: ID2D1Factory-Methode für die Methode "deewicbitmaprendertarget"
description: Erstellt ein Renderziel, das in eine WIC-Bitmap (Microsoft Windows Imaging Component) gerendert wird.
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- Methoden von "kreatewicbitmaprendertarget" Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 4025028582c254e7a5724a575ef0d7f1c7d91570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369993"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a><span data-ttu-id="b700a-104">ID2D1Factory:: | atewicbitmaprendertarget-Methoden</span><span class="sxs-lookup"><span data-stu-id="b700a-104">ID2D1Factory::CreateWicBitmapRenderTarget methods</span></span>

<span data-ttu-id="b700a-105">Erstellt ein Renderziel, das in eine WIC-Bitmap (Microsoft Windows Imaging Component) gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b700a-105">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b700a-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="b700a-106">Overload list</span></span>



| <span data-ttu-id="b700a-107">Methode</span><span class="sxs-lookup"><span data-stu-id="b700a-107">Method</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="b700a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b700a-108">Description</span></span>                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b700a-109">[**"Kreatewicbitmaprendertarget" (IWICBitmap \* , D2D1- \_ \_ Renderziel \_ Eigenschaften \* , ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="b700a-109">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES\*,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget))</span></span> | <span data-ttu-id="b700a-110">Erstellt ein Renderziel, das in eine WIC-Bitmap (Microsoft Windows Imaging Component) gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b700a-110">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |
| <span data-ttu-id="b700a-111">[**"Kreatewicbitmaprendertarget" (IWICBitmap \* , D2D1 \_ \_ Renderziel \_ Eigenschaften&, ID2D1RenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span><span class="sxs-lookup"><span data-stu-id="b700a-111">[**CreateWicBitmapRenderTarget(IWICBitmap\*,D2D1\_RENDER\_TARGET\_PROPERTIES&,ID2D1RenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))</span></span>  | <span data-ttu-id="b700a-112">Erstellt ein Renderziel, das in eine WIC-Bitmap (Microsoft Windows Imaging Component) gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b700a-112">Creates a render target that renders to a Microsoft Windows Imaging Component (WIC) bitmap.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b700a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b700a-113">Remarks</span></span>

<span data-ttu-id="b700a-114">Die Anwendung sollte einmal Renderziele erstellen und Sie für die Lebensdauer der Anwendung oder bis zum D2DERR-Erstellungs [**\_ \_ Ziel**](direct2d-error-codes.md) Fehler erhalten.</span><span class="sxs-lookup"><span data-stu-id="b700a-114">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="b700a-115">Wenn Sie diesen Fehler erhalten, müssen Sie das Renderziel (und alle erstellten Ressourcen) neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b700a-115">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

<span data-ttu-id="b700a-116">**Hinweis**   Diese Methode wird auf Windows Phone nicht unterstützt und schlägt fehl, wenn Sie auf einem Gerät mit dem Fehlercode 0x8899000b aufgerufen wird (für diesen Vorgang ist kein Hardware-renderinggerät verfügbar).</span><span class="sxs-lookup"><span data-stu-id="b700a-116">**Note**   This method isn't supported on Windows Phone and will fail when called on a device with error code 0x8899000b ( There is no hardware rendering device available for this operation ).</span></span> <span data-ttu-id="b700a-117">Da der Windows Phone-Emulator Warp-Rendering unterstützt, schlägt diese Methode fehl, wenn Sie im Emulator mit einem anderen Fehlercode aufgerufen wird, 0x88982f80 (wincodec \_ Err \_ unsupportedpixelformat).</span><span class="sxs-lookup"><span data-stu-id="b700a-117">Because the Windows Phone Emulator supports WARP rendering, this method will fail when called on the emulator with a different error code, 0x88982f80 (wincodec\_err\_unsupportedpixelformat).</span></span>

## <a name="requirements"></a><span data-ttu-id="b700a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b700a-118">Requirements</span></span>



| <span data-ttu-id="b700a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b700a-119">Requirement</span></span> | <span data-ttu-id="b700a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b700a-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b700a-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b700a-121">Library</span></span><br/> | <dl> <span data-ttu-id="b700a-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b700a-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="b700a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b700a-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b700a-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b700a-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b700a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b700a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b700a-126">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="b700a-126">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

