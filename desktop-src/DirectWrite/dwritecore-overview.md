---
title: Übersicht über DWriteCore
description: Dschreitecore ist die Projekt-Reunion-Implementierung von DirectWrite.
keywords:
- DirectWrite-Kern
- DWriteCore
ms.topic: article
ms.date: 12/09/2020
ms.openlocfilehash: 605cab8d0cd0511b5ca3b0b14d517cdc3f290573
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351038"
---
# <a name="dwritecore-overview"></a>Übersicht über DWriteCore

Dschreitecore ist die [Projekt-Reunion](/windows/apps/project-reunion/) -Implementierung von [DirectWrite](./direct-write-portal.md). DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.

In diesem Einführungs Thema wird beschrieben, was dscriptecore ist, und es wird gezeigt, wie Sie es in der Entwicklungsumgebung installieren und mit ihm programmieren.

## <a name="the-value-proposition-of-dwritecore"></a>Der Wertbeitrag von dschreitecore.

[DirectWrite](./direct-write-portal.md) selbst unterstützt eine umfangreiche Palette von Features, die es als Tool zur Schriftart Rendering in Windows für die meisten apps bereitstellt, unabhängig davon &mdash; , ob dies durch direkte Aufrufe oder über [Direct2D](../direct2d/direct2d-portal.md)erfolgt. DirectWrite enthält ein Geräte unabhängiges textlayoutsystem, hochwertige Subpixel-Text Rendering von [Microsoft ClearType](/typography/cleartype/) , Hardware beschleunigter Text, mehrstufiger Text, erweiterter [OpenType-®](/typography/opentype/) Typografiefeatures, breiten Sprachunterstützung und [GDI](../gdi/windows-gdi.md)-kompatibles Layout und Rendering. DirectWrite ist seit Windows Vista SP2 verfügbar und wurde im Laufe der Jahre erweitert, um erweiterte Features wie z. b. Variablen Schriftarten zu enthalten, mit denen Entwickler Stile, Gewichtungen und andere Attribute auf eine Schriftart mit nur einer Schriftart Ressource anwenden können.

Aufgrund der langen Lebensdauer von DirectWrite haben Entwicklungsfortschritte tendenziell ältere Versionen von Windows hinter sich gelassen. Außerdem ist der Status von DirectWrite als Premier-textrenderingtechnologie nur auf Windows beschränkt, sodass plattformübergreifende Anwendungen entweder ihren eigenen Text Rendering-Stapel schreiben oder auf Drittanbieter Lösungen basieren können.

Dbeschreib tecore löst die grundlegenden Probleme des verwaisen-und plattformübergreifenden Kompatibilitäts Problems, indem die Bibliothek aus dem System entfernt und alle möglichen unterstützten Endpunkte als Ziel verwendet werden. Zu diesem Zweck haben wir dwrite-Core in Project Reunion mit einer öffentlichen API integriert, die von allen Windows-Endpunkten bis zu Windows 8 unterstützt wird. Sie öffnet die Tür, in der Sie Sie plattformübergreifend verwenden können.

Der primäre Wert, den dwrite-Core Ihnen als Entwickler in Project Reunion bietet, besteht darin, dass er den Zugriff auf alle aktuellen DirectWrite-Features auf die gleiche Weise wie auf Windows 8 ermöglicht. Alle Features von dbeschreib tecore funktionieren in allen Versionen mit untergeordneten Versionen identisch. mit anderen Worten: alle aktuellen Features funktionieren unter Windows 8, 8,1 und allen Versionen von Windows 10, ohne dass Unterschiede in Bezug auf die Funktionsweise der Versionen auftreten können.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>Die dwrite-Core-Demo-App &mdash; dschreitecoregallery

Dwrite-Core wird anhand der Beispiel-APP [dschreitecoregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) veranschaulicht, die Sie jetzt herunterladen und untersuchen können.

## <a name="get-started-with-dwritecore"></a>Einstieg in dwrite-Core

Bei der Vorabversion von Project Reunion 0,1 wird die Installation des nuget-Pakets Project Reunion in ihren eigenen Projekten derzeit nicht unterstützt. Die derzeit unterstützte Option für Ihre eigene Programmierung mit dwrite-Core besteht darin, mit dem Projekt " [dwrite tecoregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) -Beispiel-app" zu beginnen und ihre Entwicklung auf diesem Projekt zu basieren.

Anschließend können Sie den vorhandenen Quellcode (oder Dateien) aus dem Beispiel Projekt entfernen und dem Projekt jeden neuen Quellcode (oder Dateien) hinzufügen. Weitere Informationen zum Programmieren mit dwrite Core finden Sie im Abschnitt [Programmieren mit dbeschreib tecore](#programming-with-dwritecore) weiter unten in diesem Thema.

## <a name="the-release-phases-of-dwritecore"></a>Die releasephasen von dbeschreib tecore

Das Portieren von DirectWrite auf dbeschreib tecore ist ein ausreichend großes Projekt, das mehrere Windows-Releasezyklen umfasst. Dieses Projekt ist in Phasen unterteilt, von denen jede einem Funktionsblock entspricht, der in einem Release geliefert wird.

### <a name="features-in-the-current-release-of-dwritecore"></a>Funktionen in der aktuellen Version von dbeschreib tecore

Die derzeit verfügbare Version von dbeschreib tecore enthält die grundlegenden Tools, die Sie als Entwickler für dwrite verwenden müssen, einschließlich der folgenden Features.

- Font-Enumeration.
- Schriftart-API.
- Mit.
- Rendering-APIs auf niedriger Ebene. Dies ist in der aktuellen Phase partiell &mdash; . dbeschreib tecore interagiert nicht mit [Direct2D](../direct2d/direct2d-portal.md), Sie können jedoch [**idschreiteglyphrunanalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) und [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)verwenden.
- Grundlegende textlayoutfunktionen.
- Text Rendering-APIs.
- Das Renderziel der Bitmap.
- Farb Schriftarten.
- Sonstige Optimierungen (Schriftart Cache Bereinigung, in-Memory-Schriftart Lade Tool usw.).

Die Banner Funktion in dieser Phase ist Farb Schriftarten. Mit Farb Schriftarten können Sie Ihre Schriftarten mit einer komplexeren Farb Funktionalität über einfache einzelne Farben hinaus Rendering. Mit Color Fonts können z. b. emoji und Symbol Schriftarten von Symbolleisten dargestellt werden (die letztere wird beispielsweise von Office verwendet). Farb Schriftarten wurden erstmals in Windows 8.1 eingeführt, aber das Feature wurde in Windows 10, Version 1607 (Anniversary Update), stark erweitert.

Mit der Bereinigung des Schriftart Caches und dem in-Memory-Schriftart Lade Tool können Sie ein schnelleres Laden von Schriftarten und Arbeitsspeicher Verbesserungen ermöglichen.

Mit diesen Features können Sie sofort mit der Nutzung einiger der modernen Kernfunktionen von DirectWrite, &mdash; wie z. b. variabler Schriftarten &mdash; auf Windows 8, beginnen. Diese Iterationen der Bibliothek können auch unter [Android](https://www.android.com/)und **Linux** verwendet werden. Variablen Schriftarten sind eines der wichtigsten Features für DirectWrite-Kunden. Sie wurden in Windows 10, Version 1709 (Fall Creators Update), eingeführt, sodass der Zugriff in früheren Versionen ein großer Segen für Sie als Entwickler ist.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Unsere Einladung als DirectWrite-Entwickler

Dbeschreib tecore wird zusammen mit anderen Project Reunion-Komponenten mit Offenheit für Entwickler Feedback entwickelt. Wir laden Sie ein, mit der Untersuchung von dwrite-Core zu beginnen und Einblicke oder Anforderungen für die Featureentwicklung in unserem [GitHub-Repository Project Reunion](https://github.com/microsoft/ProjectReunion/)bereitzustellen.

## <a name="programming-with-dwritecore"></a>Programmieren mit dschreitecore

Wie bereits erwähnt, ist für die Vorabversion von Project Reunion 0,1 die derzeit unterstützte Option für Ihre eigene Programmierung mit dwrite-Core, mit dem Projekt " [dwrite tecoregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) "-Beispiel-APP zu beginnen.

Ebenso wie bei [DirectWrite](./direct-write-portal.md)programmieren Sie mithilfe der com-Light-API über die [**idbeschreib tefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) -Schnittstelle mit dwrite-Core.

**Dschreitecoregallery** enthält bereits die `dwrite_core.h` Header Datei. Dieser Header definiert zuerst das Token *DWRITE_CORE* und schließt dann ein `dwrite_3.h` . Das *DWRITE_CORE* Token ist wichtig, da es alle später enthaltenen Header anweist, alle DirectWrite-APIs für Sie verfügbar zu machen. Sobald ein Projekt enthalten ist `dwrite_core.h` , können Sie Code schreiben, erstellen und ausführen.

```cppwinrt
// pch.h
...
#include <dwrite_core.h>
```

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>Neue oder andere APIs für dwrite Core

Die API-Oberfläche für die dschreitecore-API ist größtenteils identisch mit der für [DirectWrite](/windows/win32/api/_directwrite/). Es gibt jedoch eine kleine Anzahl von neuen APIs, die derzeit nur in dwrite-Core vorhanden sind.

#### <a name="create-a-restricted-factory-object"></a>Erstellen eines eingeschränkten Factory-Objekts

Die [**DWRITE_FACTORY_TYPE**](./dwrite/ne-dwrite-dwrite_factory_type.md) -Enumeration verfügt über eine neue Konstante &mdash; **DWRITE_FACTORY_TYPE_RESTRICTED**. Eine eingeschränkte Factory ist besser gesperrt als eine isolierte Factory. Es findet in keiner Weise eine Interaktion mit einem prozessübergreifenden oder permanenten Schriftart Cache. Außerdem enthält die von dieser Factory zurückgegebene System Schriftart Auflistung nur bekannte Schriftarten. Im folgenden wird erläutert, wie Sie **DWRITE_FACTORY_TYPE_RESTRICTED** ein eingeschränktes Factory-Objekt erstellen können, wenn Sie die Free-Funktion von [**dwrite Items | atefactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) aufrufen.

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCreateFactory(
    DWRITE_FACTORY_TYPE_RESTRICTED,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

Wenn Sie **DWRITE_FACTORY_TYPE_RESTRICTED** an eine ältere Version von DirectWrite übergeben, die dies nicht unterstützt, gibt **dschreitekreatefactory** **E_INVALIDARG** zurück.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Zeichnen von Glyphen in eine Bitmap des System Speichers

DirectWrite verfügt über eine Bitmap-Renderziel-Schnittstelle, die das Rendern von Glyphen in eine Bitmap im Systemspeicher unterstützt. Die einzige Möglichkeit, auf die zugrunde liegenden Pixeldaten zuzugreifen, besteht jedoch darin, GDI zu durchlaufen, sodass die API nicht plattformübergreifend verwendet werden kann. Dies kann problemlos durch Hinzufügen einer Methode zum Abrufen der Pixeldaten behoben werden.

Daher führt dwrite tecore die [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) -Schnittstelle und die zugehörige-Methode [**IDWriteBitmapRenderTarget2:: getbitmapdata**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md)ein. Diese Methode nimmt einen Parameter vom Typ (Zeiger auf) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md)auf, bei dem es sich um eine neue Struktur handelt.

Die Anwendung erstellt ein Bitmap-Renderziel durch Aufrufen von [idwrite tegdiinterop:: createbitmaprendertarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). Unter Windows kapselt ein Bitmap-Renderziel einen GDI-Speicher-DC mit einem ausgewählten GDI-geräteunabhängigen Bitmap (DIB). [Idschreitebitmaprendertarget::D rawglyphrun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) rendert Symbole zum DIB. DirectWrite rendert die Symbole selbst, ohne dass GDI durchlaufen wird. Die Anwendung kann dann den **hdc** aus dem Bitmap-Renderziel erhalten und mit [BitBLT](/windows/win32/api/wingdi/nf-wingdi-bitblt) die Pixel in ein Windows- **hdc** kopieren.

Auf nicht-Windows-Plattformen kann die Anwendung immer noch ein Bitmap-Renderziel erstellen, aber Sie kapselt lediglich ein Systemspeicher Array ohne **hdc** und kein DIB. Ohne einen **hdc** muss Ihre Anwendung eine andere Möglichkeit aufweisen, um die Bitmap-Pixel zu erhalten, damit Sie Sie kopieren oder anderweitig verwenden können. Auch unter Windows ist es manchmal sinnvoll, die eigentlichen Pixeldaten zu erhalten. im folgenden Codebeispiel wird die aktuelle Methode gezeigt.

```cppwinrt
// pch.h
#pragma once

#include <windows.h>
#include <Unknwn.h>
#include <winrt/Windows.Foundation.h>

// WinMain.cpp
#include "pch.h"
#include <dwrite_core.h>
#pragma comment(lib, "Gdi32")

class TextRenderer
{
    DWRITE_BITMAP_DATA_BGRA32 m_targetBitmapData;

public:
    void InitializeBitmapData(winrt::com_ptr<IDWriteBitmapRenderTarget> const& renderTarget)
    {
        // Query the bitmap render target for the new interface. 
        winrt::com_ptr<IDWriteBitmapRenderTarget2> renderTarget2;
        renderTarget2 = renderTarget.try_as<IDWriteBitmapRenderTarget2>();

        if (renderTarget2)
        {
            // IDWriteBitmapRenderTarget2 exists, so we can get the bitmap the easy way. 
            winrt::check_hresult(renderTarget2->GetBitmapData(OUT & m_targetBitmapData));
        }
        else
        {
            // We're using an older version that doesn't implement IDWriteBitmapRenderTarget2, 
            // so we have to get the bitmap by going through GDI. First get the bitmap handle. 
            HDC hdc = renderTarget->GetMemoryDC();
            winrt::handle dibHandle{ GetCurrentObject(hdc, OBJ_BITMAP) };
            winrt::check_bool(bool{ dibHandle });

            // Call a GDI function to fill in the DIBSECTION structure for the bitmap. 
            DIBSECTION dib;
            winrt::check_bool(GetObject(dibHandle.get(), sizeof(dib), &dib));

            m_targetBitmapData.width = dib.dsBm.bmWidth;
            m_targetBitmapData.height = dib.dsBm.bmHeight;
            m_targetBitmapData.pixels = static_cast<uint32_t*>(dib.dsBm.bmBits);
        }
    }
};

int __stdcall wWinMain(HINSTANCE, HINSTANCE, LPWSTR, int)
{
    TextRenderer textRenderer;
    winrt::com_ptr<IDWriteBitmapRenderTarget> renderTarget{ /* ... */ };
    textRenderer.InitializeBitmapData(renderTarget);
}
```

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>Weitere API-Unterschiede zwischen dwrite-Core und DirectWrite

Es gibt ein paar APIs, bei denen es sich entweder um Stubel handelt oder die sich auf nicht-Windows-Plattformen anders Verhalten. Beispielsweise gibt [idwrite tegdiinterop:: anatefontfakefromhdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) **E_NOTIMPL** auf nicht-Windows-Plattformen zurück, da es keinen **hdc** ohne [GDI](../gdi/windows-gdi.md)gibt.

Und schließlich gibt es bestimmte andere Windows-APIs, die normalerweise in Verbindung mit DirectWrite verwendet werden (Direct2D ist ein wichtiges Beispiel). Allerdings funktionieren Direct2D und dwrite tecore derzeit nicht. Wenn Sie z. b. ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mithilfe von dwrite-Core erstellen und es an [**D2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)übergeben, schlägt dieser Vorgang fehl.