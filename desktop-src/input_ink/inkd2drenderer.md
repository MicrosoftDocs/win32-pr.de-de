---
description: Implementiert die IInkD2DRenderer-Schnittstelle.
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
title: InkD2DRenderer-Klasse
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkD2DRenderer
api_type:
- COM
api_location:
- Inkrenderer.idl
ms.openlocfilehash: 1649d52c2e9098513c115daaf295c4005e890b8e
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104218955"
---
# <a name="inkd2drenderer-class"></a><span data-ttu-id="be872-103">InkD2DRenderer-Klasse</span><span class="sxs-lookup"><span data-stu-id="be872-103">InkD2DRenderer class</span></span>

<span data-ttu-id="be872-104">Implementiert die [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="be872-104">Implements the [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) interface.</span></span>

<span data-ttu-id="be872-105">Ein [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) -Objekt ermöglicht das Rendern von frei Hand Strichen auf den festgelegten Direct2D-Gerätekontext einer universellen Windows-APP anstelle des standardmäßigen [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) -Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="be872-105">An [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

## <a name="members"></a><span data-ttu-id="be872-106">Member</span><span class="sxs-lookup"><span data-stu-id="be872-106">Members</span></span>

<span data-ttu-id="be872-107">Die **InkD2DRenderer** -Klasse erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="be872-107">The **InkD2DRenderer** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="be872-108">**InkD2DRenderer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="be872-108">**InkD2DRenderer** also has these types of members:</span></span>

- [<span data-ttu-id="be872-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="be872-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="be872-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="be872-110">Methods</span></span>

<span data-ttu-id="be872-111">Die **InkD2DRenderer** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="be872-111">The **InkD2DRenderer** class has these methods.</span></span>

| <span data-ttu-id="be872-112">Methode</span><span class="sxs-lookup"><span data-stu-id="be872-112">Method</span></span>                              | <span data-ttu-id="be872-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be872-113">Description</span></span>                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="be872-114">**Draw**</span><span class="sxs-lookup"><span data-stu-id="be872-114">**Draw**</span></span>](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | <span data-ttu-id="be872-115">Rendert den frei Hand Strich in den festgelegten Direct2D-Gerätekontext der app.</span><span class="sxs-lookup"><span data-stu-id="be872-115">Renders the ink stroke to the designated Direct2D device context of the app.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="be872-116">Zugriffs Funktionen für die Erstellung \\</span><span class="sxs-lookup"><span data-stu-id="be872-116">Creation\\Access Functions</span></span>

<span data-ttu-id="be872-117">Rufen Sie [<strong>cokreateinstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dem Klassen Bezeichner <strong>InkD2DRenderer</strong> auf, um einen Verweis auf das Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="be872-117">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkD2DRenderer</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a><span data-ttu-id="be872-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="be872-118">Examples</span></span>

<span data-ttu-id="be872-119">Dieser Code Ausschnitt aus der Datei "scenecomposer. cpp" des [komplexen Freihand](/samples/microsoft/windows-universal-samples/complexink/) -Beispiels veranschaulicht das Rendern einer Auflistung von Hand Strichen in einen Direct2D-Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="be872-119">This snippet from the "SceneComposer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) demonstrates the rendering of a collection of ink strokes to a Direct2D device context.</span></span>

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

<span data-ttu-id="be872-120">Dieser Code Ausschnitt aus der Datei "inkrenderer. cpp" des [komplexen Freihand](/samples/microsoft/windows-universal-samples/complexink/) -Beispiels zeigt die Rendermethode (die im vorherigen Code Ausschnitt aufgerufen wurde), die die [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) -Methode zum Rendern der Striche aufruft.</span><span class="sxs-lookup"><span data-stu-id="be872-120">This snippet from the "InkRenderer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) shows the Render method (called in the previous snippet) that calls the [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) method for rendering the strokes.</span></span>

```C++
void InkRenderer::Render(
    Platform::Collections::Vector<
        Windows::UI::Input::Inking::InkStroke^>^ strokes,
        Microsoft::WRL::ComPtr<ID2D1DeviceContext> d2dContext)
{
    HRESULT hr = S_OK;
    if (_spInkD2DRenderer != nullptr)
    {
        if (strokes != nullptr && strokes->Size > 0)
        {
            // Cast the stroke collection into IUnknown to call Inkd2dRenderer
            ComPtr<IUnknown> spUnkStrokes = 
                reinterpret_cast<IUnknown*>(reinterpret_cast<__abi_IUnknown*>(strokes));
            hr = _spInkD2DRenderer->Draw(d2dContext.Get(), spUnkStrokes.Get(), false);
            if (FAILED(hr))
            {
                DX::ThrowIfFailed(hr);
            }
        }
    }
}
```

## <a name="requirements"></a><span data-ttu-id="be872-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be872-121">Requirements</span></span>

| <span data-ttu-id="be872-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be872-122">Requirement</span></span> | <span data-ttu-id="be872-123">Wert</span><span class="sxs-lookup"><span data-stu-id="be872-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="be872-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be872-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be872-125">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be872-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be872-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be872-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be872-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="be872-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="be872-128">Header</span><span class="sxs-lookup"><span data-stu-id="be872-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="be872-129"><dt>Inkrenderer. h</dt></span><span class="sxs-lookup"><span data-stu-id="be872-129"><dt>Inkrenderer.h</dt></span></span> </dl>   |
| <span data-ttu-id="be872-130">IDL</span><span class="sxs-lookup"><span data-stu-id="be872-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be872-131"><dt>Inkrenderer. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be872-131"><dt>Inkrenderer.idl</dt></span></span> </dl> |
| <span data-ttu-id="be872-132">IID</span><span class="sxs-lookup"><span data-stu-id="be872-132">IID</span></span><br/>                      | <span data-ttu-id="be872-133">IID \_ IInkD2DRenderer ist als 4044e60c-7b01-4671-a97c-04e0210a07a5 definiert.</span><span class="sxs-lookup"><span data-stu-id="be872-133">IID\_IInkD2DRenderer is defined as 4044e60c-7b01-4671-a97c-04e0210a07a5</span></span><br/>         |

## <a name="related-topics"></a><span data-ttu-id="be872-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be872-134">Related topics</span></span>

<span data-ttu-id="be872-135">[Ink-Renderer](ink-renderer.md), [Stift-und tablettstiftinteraktionen](/windows/uwp/design/input/pen-and-stylus-interactions), Handschrift [Analyse Beispiel](/samples/microsoft/windows-universal-samples/inkanalysis/), [einfaches Beispiel](/samples/microsoft/windows-universal-samples/simpleink/)für das Beispiel, Beispiel für [komplexe](/samples/microsoft/windows-universal-samples/complexink/) Erfassung</span><span class="sxs-lookup"><span data-stu-id="be872-135">[Ink renderer](ink-renderer.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
