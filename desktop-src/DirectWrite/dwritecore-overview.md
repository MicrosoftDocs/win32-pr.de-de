---
title: Übersicht über DWriteCore
description: DWriteCore ist die Project Reunion-Implementierung von DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: e80da37bb65cddaffabd67ae9e5b40e2433e64da
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955013"
---
# <a name="dwritecore-overview"></a>Übersicht über DWriteCore

DWriteCore ist die [Project Reunion-Implementierung](/windows/apps/project-reunion/) von [DirectWrite (DirectWrite](./direct-write-portal.md) ist die DirectX-API für hochwertiges Textrendering, auflösungsunabhängige Konturschriftarten und Vollständige Unicode-Text- und Layoutunterstützung). DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.

In diesem Einführungsthema wird beschrieben, was DWriteCore ist, und es wird gezeigt, wie Sie DWriteCore in Ihrer Entwicklungsumgebung installieren und damit programmieren.

## <a name="the-value-proposition-of-dwritecore"></a>Das Wertversprechen von DWriteCore

[DirectWrite](./direct-write-portal.md) selbst unterstützt ein umfangreiches Array von Features, wodurch es für die meisten Apps unter Windows zum Tool der Wahl beim Rendern von Schriftarten wird, unabhängig davon, ob dies über direkte Aufrufe oder &mdash; [über Direct2D erfolgt.](../direct2d/direct2d-portal.md) DirectWrite umfasst ein geräteunabhängiges Textlayoutsystem, qualitativ hochwertiges Microsoft ClearType-Textrendering, hardwarebeschleunigten Text, Mehrformattext® erweiterte [OpenType®](/typography/opentype/) Typografiefeatures, Breitsprachunterstützung und [](/typography/cleartype/) [GDI-kompatibles](../gdi/windows-gdi.md)Layout und Rendering. DirectWrite ist seit Windows Vista SP2 verfügbar und hat sich im Laufe der Jahre weiterentwickelt, um erweiterte Features wie variable Schriftarten zu enthalten, mit denen Sie Stile, Gewichtungen und andere Attribute auf eine Schriftart mit nur einer Schriftartressource anwenden können.

Aufgrund der langen Lebensdauer von DirectWrite haben Fortschritte bei der Entwicklung jedoch tendenziell ältere Versionen von Windows zurückgelassen. Darüber hinaus ist der Status von DirectWrite als führende Textrenderingtechnologie nur auf Windows beschränkt, wodurch plattformübergreifende Anwendungen entweder ihren eigenen Textrenderingstapel schreiben oder sich auf Lösungen von Drittanbietern verlassen können.

DWriteCore löst die grundlegenden Probleme des Verwaistens von Versionsfeatures und der plattformübergreifenden Kompatibilität, indem die Bibliothek aus dem System entfernt und alle möglichen unterstützten Endpunkte als Ziel verwendet werden. Zu diesem Zweck haben wir DWriteCore in Project Reunion mit einer öffentlichen API integriert, die auf allen Windows-Endpunkten bis Windows 8 unterstützt wird, und ihnen die Plattformübergreifende Verwendung ermöglicht.

DWriteCore bietet Ihnen als Entwickler in Project Reunion hauptsächlich Zugriff auf alle aktuellen DirectWrite-Features bis hin zu Windows 8. Alle Features von DWriteCore funktionieren auf allen Downlevelversionen gleich. Mit anderen Worten: Alle aktuellen Features funktionieren mit Windows 8, Version 8.1 und allen Versionen von Windows 10, ohne dass es zu Ununterschieden in Bezug darauf kommt, welche Features in welchen Versionen funktionieren können.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>Die DWriteCore-Demo-App &mdash; DWriteCoreGallery

DWriteCore wird anhand der [DWriteCoreGallery-Beispiel-App](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) veranschaulicht, die Sie jetzt herunterladen und untersuchen können.

## <a name="get-started-with-dwritecore"></a>Erste Schritte mit DWriteCore

DWriteCore ist Teil von [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0). In diesem Abschnitt wird beschrieben, wie Sie Ihre Entwicklungsumgebung für die Programmierung mit DWriteCore einrichten.

### <a name="install-the-project-reunion-05-vsix"></a>Installieren von Project Reunion 0.5 VSIX

Klicken Sie in Visual Studio auf  >  **Erweiterungen Erweiterungen verwalten,** suchen Sie nach *Project Reunion*, und laden Sie die Erweiterung Project Reunion herunter. Schließen Sie Visual Studio, öffnen Sie sie erneut, und befolgen Sie die Anweisungen, um die Erweiterung zu installieren.

Weitere Informationen finden Sie unter [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)und [Erstellen von Windows-Desktop-Apps mit Project Reunion 0.5.](/windows/apps/project-reunion/#set-up-your-development-environment)

### <a name="create-a-new-project"></a>Erstellt ein neues Projekt

Erstellen Sie in Visual Studio ein neues Projekt aus der Projektvorlage **Leere App, gepackt (WinUI 3 in Desktop).** Sie finden diese Projektvorlage, indem Sie sprache auswählen: *C++*; platform: *Project Reunion*; Projekttyp: *Desktop*.

Weitere Informationen finden Sie unter [Projektvorlagen für WinUI 3.](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3)

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>Installieren des NuGet-Pakets Microsoft.ProjectReunion.DWrite

Klicken Sie in Visual Studio  auf \> **Projekt NuGet-Pakete verwalten...** Durchsuchen , geben Oder fügen Sie \>  **Microsoft.ProjectReunion.DWrite** in das Suchfeld ein, wählen Sie das Element in den Suchergebnissen aus, und klicken Sie dann auf **Installieren,** um das Paket für dieses Projekt zu installieren.

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>Alternativ können Sie mit der Beispiel-App DWriteCoreGallery beginnen.

Alternativ können Sie mit DWriteCore programmieren, indem Sie mit dem Beispiel-App-Projekt [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) beginnen und Ihre Entwicklung auf diesem Projekt erstellen. Anschließend können Sie beliebigen vorhandenen Quellcode (oder dateien) aus diesem Beispielprojekt entfernen und dem Projekt neuen Quellcode (oder neue Dateien) hinzufügen.

### <a name="use-dwritecore-in-your-project"></a>Verwenden von DWriteCore in Ihrem Projekt

Weitere Informationen zum Programmieren mit DWriteCore finden Sie im Abschnitt Programmieren mit [DWriteCore](#programming-with-dwritecore) weiter unten in diesem Thema.

## <a name="the-release-phases-of-dwritecore"></a>Die Releasephasen von DWriteCore

Das Portieren von DirectWrite zu DWriteCore ist ein ausreichend großes Projekt, das mehrere Windows-Releasezyklen umfassen kann. Dieses Projekt ist in Phasen unterteilt, die jeweils einem Teil der In einem Release bereitgestellten Funktionalität entsprechen.

### <a name="features-in-the-current-release-of-dwritecore"></a>Features in der aktuellen Version von DWriteCore

Die derzeit verfügbare Version von DWriteCore ist Teil von [Project Reunion 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0) Sie enthält die grundlegenden Tools, die Sie als Entwickler benötigen, um DWriteCore zu nutzen, einschließlich der folgenden Features.

- Schriftartenenumeration.
- Schriftart-API.
- Gestaltung.
- Rendering-APIs auf niedriger Ebene. Dies ist teilweise in der aktuellen Phase DWriteCore funktioniert nicht mit &mdash; [Direct2D,](../direct2d/direct2d-portal.md)aber Sie können [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) und [**IDWriteBitmapRenderTarget verwenden.**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)
- Grundlegende Textlayoutfunktionalität.
- Textrendering-APIs.
- Bitmaprenderingziel.
- Farbschriftarten.
- Verschiedene Optimierungen (Bereinigung des Schriftartcaches, In-Memory-Schriftartlademodul und so weiter).

Ein Bannerfeature sind Farbschriftarten. Farbschriftarten ermöglichen es Ihnen, Ihre Schriftarten mit komplexeren Farbfunktionen zu rendern, die über einfache Einzelfarben hinausgehen. Farbschriftarten sind z. B. die Möglichkeit, Emoji- und Symbolsymbolschriftarten zu rendern (letzteres wird z. B. von Office verwendet). Farbschriftarten wurden erstmals in Windows 8.1 eingeführt, aber das Feature wurde in Windows 10 Version 1607 (Anniversary Update) stark erweitert.

Die Arbeit an der Bereinigung des Schriftartcaches und des In-Memory-Schriftartlademoduls ermöglicht ein schnelleres Laden von Schriftarten und Speicherverbesserungen.

Mit diesen Features können Sie sofort damit beginnen, einige der modernen Kernfunktionen von DirectWrite zu nutzen, z. B. &mdash; variable Schriftarten &mdash; auf Windows 8. Variable Schriftarten sind eines der wichtigsten Features für DirectWrite-Kunden. sie wurden in Windows 10 Version 1709 (Fall Creators Update) eingeführt, sodass der Zugriff auf sie in früheren Versionen ein wesentlicher Vorteil für Sie als Entwickler ist.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Unsere Einladung für Sie als DirectWrite-Entwickler

DWriteCore wird zusammen mit anderen Project Reunion-Komponenten mit Entwicklerfeedback entwickelt. Wir laden Sie ein, mit dem Erkunden von DWriteCore zu beginnen und Einblicke oder Anforderungen in die Featureentwicklung in unserem [GitHub-Repository Project Reunion](https://github.com/microsoft/ProjectReunion/)bereitzustellen.

## <a name="programming-with-dwritecore"></a>Programmieren mit DWriteCore

Genau wie bei [DirectWrite programmieren](./direct-write-portal.md)Sie mit DWriteCore über die COM-Light-API über die [**IDWriteFactory-Schnittstelle.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)

Um DWriteCore zu verwenden, muss die Headerdatei eingeschlossen `dwrite_core.h` werden.

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

Die `dwrite_core.h` Headerdatei definiert zuerst das Token *DWRITE_CORE* und enthält dann die `dwrite_3.h` Headerdatei. Das *DWRITE_CORE* Token ist wichtig, da es alle nachfolgend enthaltenen Header anleitet, ihnen alle DirectWrite-APIs zur Verfügung zu stellen. Sobald Ihr Projekt enthalten `dwrite_core.h` ist, können Sie code, build und run schreiben.

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>APIs, die neu oder anders für DWriteCore sind

Die DWriteCore-API-Oberfläche ist größtenteils identisch mit der für [DirectWrite.](/windows/win32/api/_directwrite/) Es gibt jedoch eine kleine Anzahl neuer APIs, die derzeit nur in DWriteCore vorhanden sind.

#### <a name="create-a-factory-object"></a>Erstellen eines Factoryobjekts

Die [**freie DWriteCoreCreateFactory-Funktion**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) erstellt ein Factoryobjekt, das für die nachfolgende Erstellung einzelner DWriteCore-Objekte verwendet wird.

**DWriteCoreCreateFactory** ist funktionell identisch mit der [DWriteCreateFactory-Funktion,](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) die von der Systemversion von DirectWrite exportiert wurde. Die DWriteCore-Funktion hat einen anderen Namen, um Mehrdeutigkeiten zu vermeiden.

#### <a name="create-a-restricted-factory-object"></a>Erstellen eines eingeschränkten Factoryobjekts

Die [**DWRITE_FACTORY_TYPE-Enumeration**](./dwrite/ne-dwrite-dwrite_factory_type.md) verfügt über eine neue Konstante DWRITE_FACTORY_TYPE_ISOLATED2 , die eine &mdash; eingeschränkte Factory angibt. Eine eingeschränkte Factory ist stärker gesperrt als eine isolierte Factory. Es interagiert in irgendeiner Weise nicht mit einem prozessübergreifenden oder beständigen Schriftartcache. Darüber hinaus enthält die von dieser Factory zurückgegebene Auflistung von Systemschriftarten nur bekannte Schriftarten. So können Sie DWRITE_FACTORY_TYPE_ISOLATED2 verwenden, um **ein** eingeschränktes Factoryobjekt zu erstellen, wenn Sie die freie [**DWriteCoreCreateFactory-Funktion**](/windows/win32/directwrite/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) aufrufen.

```cppwinrt
// Create a factory that doesn't interact with any cross-process nor
// persistent cache state.
winrt::com_ptr<::IDWriteFactory7> spFactory;
winrt::check_hresult(
  ::DWriteCoreCreateFactory(
    DWRITE_FACTORY_TYPE_ISOLATED2,
    __uuidof(spFactory),
    reinterpret_cast<IUnknown**>(spFactory.put())
  )
);
```

Wenn Sie **DWRITE_FACTORY_TYPE_ISOLATED2** an eine ältere Version von DirectWrite übergeben, die sie nicht unterstützt, gibt **DWriteCreateFactory** **E_INVALIDARG.**

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Zeichnen von Glyphen in eine Systemspeicherbitmap

DirectWrite verfügt über eine Bitmap-Renderzielschnittstelle, die das Rendern von Glyphen in eine Bitmap im Systemspeicher unterstützt. Derzeit besteht die einzige Möglichkeit, zugriff auf die zugrunde liegenden Pixeldaten zu erhalten, in der Verwendung von GDI, sodass die API nicht plattformübergreifend verwendet werden kann. Dies lässt sich leicht beheben, indem eine Methode zum Abrufen der Pixeldaten hinzugefügt wird.

DWriteCore führt daher die [**IDWriteBitmapRenderTarget2-Schnittstelle**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) und deren [**Methode IDWriteBitmapRenderTarget2::GetBitmapData ein.**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) Diese Methode akzeptiert einen Parameter des Typs (Zeiger auf) DWRITE_BITMAP_DATA_BGRA32 [**,**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md)bei dem es sich um eine neue Struktur handelt.

Ihre Anwendung erstellt ein Bitmaprenderziel durch Aufrufen von [IDWriteGdiInterop::CreateBitmapRenderTarget.](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) Unter Windows kapselt ein Bitmaprenderingziel einen GDI-Speicherdomänencontroller mit einer in ihm ausgewählten geräteunabhängigen GDI-Bitmap (DEVICE-Independent Bitmap, DIB). [IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) rendert Glyphen im DIB. DirectWrite rendert die Glyphen selbst, ohne GDI zu durchlaufen. Ihre Anwendung kann dann den **HDC** aus dem Bitmaprenderziel abrufen und [BitBlt](/windows/win32/api/wingdi/nf-wingdi-bitblt) verwenden, um die Pixel in ein **HDC-Fenster** zu kopieren.

Auf Nicht-Windows-Plattformen kann Ihre Anwendung weiterhin ein Bitmaprenderingziel erstellen, kapselt aber einfach ein Systemspeicherarray ohne **HDC** und ohne DIB. Ohne **HDC** muss es eine andere Möglichkeit für Ihre Anwendung geben, die Bitmappixel abzurufen, damit sie sie kopieren oder anderweitig verwenden kann. Selbst unter Windows ist es manchmal nützlich, die tatsächlichen Pixeldaten abzurufen, und wir zeigen die aktuelle Vorgehensweise im folgenden Codebeispiel.

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>Andere API-Unterschiede zwischen DWriteCore und DirectWrite

Es gibt einige APIs, die entweder nur Stubs sind oder sich auf Nicht-Windows-Plattformen etwas anders verhalten. Beispielsweise gibt [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) **E_NOTIMPL** auf Nicht-Windows-Plattformen zurück, da es kein **HDC** ohne [GDI](../gdi/windows-gdi.md)gibt.

Und schließlich gibt es bestimmte andere Windows-APIs, die in der Regel zusammen mit DirectWrite verwendet werden (Direct2D ist ein bedeutendes Beispiel). Derzeit können Direct2D und DWriteCore jedoch nicht zusammenarbeiten. Wenn Sie beispielsweise ein [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mit DWriteCore erstellen und es an [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)übergeben, tritt bei diesem Aufruf ein Fehler auf.
