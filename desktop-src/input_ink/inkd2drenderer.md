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
# <a name="inkd2drenderer-class"></a>InkD2DRenderer-Klasse

Implementiert die [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) -Schnittstelle.

Ein [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) -Objekt ermöglicht das Rendern von frei Hand Strichen auf den festgelegten Direct2D-Gerätekontext einer universellen Windows-APP anstelle des standardmäßigen [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) -Steuer Elements.

## <a name="members"></a>Member

Die **InkD2DRenderer** -Klasse erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **InkD2DRenderer** verfügt auch über die folgenden Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **InkD2DRenderer** -Klasse verfügt über diese Methoden.

| Methode                              | BESCHREIBUNG                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Rendert den frei Hand Strich in den festgelegten Direct2D-Gerätekontext der app.<br/> |

## <a name="creationaccess-functions"></a>Zugriffs Funktionen für die Erstellung \\

Rufen Sie [<strong>cokreateinstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dem Klassen Bezeichner <strong>InkD2DRenderer</strong> auf, um einen Verweis auf das Objekt abzurufen.

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Beispiele

Dieser Code Ausschnitt aus der Datei "scenecomposer. cpp" des [komplexen Freihand](/samples/microsoft/windows-universal-samples/complexink/) -Beispiels veranschaulicht das Rendern einer Auflistung von Hand Strichen in einen Direct2D-Gerätekontext.

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

Dieser Code Ausschnitt aus der Datei "inkrenderer. cpp" des [komplexen Freihand](/samples/microsoft/windows-universal-samples/complexink/) -Beispiels zeigt die Rendermethode (die im vorherigen Code Ausschnitt aufgerufen wurde), die die [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) -Methode zum Rendern der Striche aufruft.

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

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Inkrenderer. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Inkrenderer. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer ist als 4044e60c-7b01-4671-a97c-04e0210a07a5 definiert.<br/>         |

## <a name="related-topics"></a>Zugehörige Themen

[Ink-Renderer](ink-renderer.md), [Stift-und tablettstiftinteraktionen](/windows/uwp/design/input/pen-and-stylus-interactions), Handschrift [Analyse Beispiel](/samples/microsoft/windows-universal-samples/inkanalysis/), [einfaches Beispiel](/samples/microsoft/windows-universal-samples/simpleink/)für das Beispiel, Beispiel für [komplexe](/samples/microsoft/windows-universal-samples/complexink/) Erfassung
