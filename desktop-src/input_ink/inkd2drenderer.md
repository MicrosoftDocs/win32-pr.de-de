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
ms.openlocfilehash: 51383770b8eb0c5dca5efbb5f1756bee81ece506c0e92337e9df9a60eb0a8aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726730"
---
# <a name="inkd2drenderer-class"></a>InkD2DRenderer-Klasse

Implementiert die [**IInkD2DRenderer-Schnittstelle.**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer)

Ein [**IInkD2DRenderer-Objekt**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) ermöglicht das Rendern von Freihandstrichen im angegebenen Direct2D-Gerätekontext einer Universellen Windows-App anstelle des Standardmäßigen [**InkCanvas-Steuerelements.**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)

## <a name="members"></a>Member

Die **InkD2DRenderer-Klasse** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **InkD2DRenderer** verfügt auch über diese Typen von Membern:

- [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **InkD2DRenderer-Klasse** verfügt über diese Methoden.

| Methode                              | Beschreibung                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Rendert den Ink-Strich im angegebenen Direct2D-Gerätekontext der App.<br/> |

## <a name="creationaccess-functions"></a>\\Erstellungszugriffsfunktionen

Rufen Sie [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) mit dem Klassenbezeichner <strong>InkD2DRenderer</strong> auf, um einen Verweis auf das Objekt abzurufen.

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Beispiele

Dieser Codeausschnitt aus der Datei "SceneComposer.cpp" des [Beispiels Für komplexes Öffnen](/samples/microsoft/windows-universal-samples/complexink/) veranschaulicht das Rendern einer Sammlung von Ink-Strichen in einen Direct2D-Gerätekontext.

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

Dieser Codeausschnitt aus der Datei "InkRenderer.cpp" des [Beispiels "Komplexes Zeichnen"](/samples/microsoft/windows-universal-samples/complexink/) zeigt die Render-Methode (im vorherigen Codeausschnitt aufgerufen), die die [**Draw-Methode**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) zum Rendern der Striche aufruft.

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
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                  |
| Header<br/>                   | <dl> <dt>Inkrenderer.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Inkrenderer.idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer ist als 4044e60c-7b01-4671-a97c-04e0210a07a5 definiert.<br/>         |

## <a name="related-topics"></a>Zugehörige Themen

[Ink-Renderer,](ink-renderer.md) [Stift- und Stiftinteraktionen,](/windows/uwp/design/input/pen-and-stylus-interactions) [Ink-Analysebeispiel,](/samples/microsoft/windows-universal-samples/inkanalysis/) [Einfaches Beispiel für Dasken,](/samples/microsoft/windows-universal-samples/simpleink/) [Komplexes Beispiel für Diekung](/samples/microsoft/windows-universal-samples/complexink/)
