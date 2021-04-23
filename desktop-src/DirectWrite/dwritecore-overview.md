---
title: Übersicht über DWriteCore
description: DWriteCore ist die Project Reunion-Implementierung von DirectWrite.
keywords:
- DirectWrite Core
- DWriteCore
ms.topic: article
ms.date: 04/22/2021
ms.openlocfilehash: 1ebb85ae2628a2c9abce86e0ce146c0d24828267
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925674"
---
# <a name="dwritecore-overview"></a>Übersicht über DWriteCore

DWriteCore ist die [Project Reunion-Implementierung](/windows/apps/project-reunion/) von [DirectWrite (DirectWrite](./direct-write-portal.md) ist die DirectX-API für hochwertiges Textrendering, auflösungsunabhängige Gliederungsschriftarten sowie vollständige Unicode-Text- und Layoutunterstützung). DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen.

In diesem Einführungsthema wird beschrieben, was DWriteCore ist, und es wird gezeigt, wie Sie DWriteCore in Ihrer Entwicklungsumgebung installieren und damit programmieren.

## <a name="the-value-proposition-of-dwritecore"></a>Das Wertversprechen von DWriteCore

[DirectWrite](./direct-write-portal.md) selbst unterstützt eine vielzahl von Features, die es zum bevorzugten Tool für das Rendern von Schriftarten unter Windows für die meisten Apps machen, &mdash; sei es durch direkte Aufrufe oder über [Direct2D.](../direct2d/direct2d-portal.md) DirectWrite umfasst ein geräteunabhängiges Textlayoutsystem, hochwertiges Subpixel-Microsoft ClearType-Textrendering, hardwarebeschleunigenden Text, Mehrformattext, erweiterte [OpenType®](/typography/opentype/) Typografiefeatures, umfassende Sprachunterstützung und [](/typography/cleartype/) [GDI-kompatibles](../gdi/windows-gdi.md)Layout und Rendering. DirectWrite ist seit Windows Vista SP2 verfügbar und hat sich im Laufe der Jahre weiterentwickelt und umfasst erweiterte Features wie variable Schriftarten, mit denen Sie Stile, Gewichtungen und andere Attribute auf eine Schriftart mit nur einer Schriftartressource anwenden können.

Aufgrund der langen Lebensdauer von DirectWrite haben Fortschritte in der Entwicklung jedoch dazu tendiert, ältere Versionen von Windows hinter sich zu lassen. Darüber hinaus ist der Status von DirectWrite als führende Textrenderingtechnologie nur auf Windows beschränkt, sodass plattformübergreifende Anwendungen entweder ihren eigenen Textrenderingstapel schreiben oder sich auf Lösungen von Drittanbietern verlassen können.

DWriteCore löst die grundlegenden Probleme bei verwaisten Versionsfeatures und plattformübergreifender Kompatibilität, indem die Bibliothek aus dem System entfernt und alle möglichen unterstützten Endpunkte als Ziel verwendet werden. Zu diesem Zweck haben wir DWriteCore in Project Reunion mit einer öffentlichen API integriert, die auf allen Windows-Endpunkten bis hin zu Windows 8 unterstützt wird, und ihnen die Plattform für die plattformübergreifende Verwendung geöffnet.

Der Hauptwert, den DWriteCore Ihnen als Entwickler in Project Reunion bietet, besteht im Zugriff auf alle aktuellen DirectWrite-Features bis hin zu Windows 8. Alle Features von DWriteCore funktionieren in allen downlevelbasierten Versionen gleich. Anders ausgedrückt: Alle aktuellen Features funktionieren unter Windows 8, 8.1 und allen Versionen von Windows 10, ohne dass Unterschiede in Bezug darauf bestehen, welche Features in welchen Versionen funktionieren könnten.

## <a name="the-dwritecore-demo-appmdashdwritecoregallery"></a>Die DWriteCore-Demo-App &mdash; DWriteCoreGallery

DWriteCore wird mit der [DWriteCoreGallery-Beispiel-App](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) demonstriert, die Sie jetzt herunterladen und untersuchen können.

## <a name="get-started-with-dwritecore"></a>Erste Schritte mit DWriteCore

DWriteCore ist Teil von [Project Reunion 0.5.](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0) In diesem Abschnitt wird beschrieben, wie Sie Ihre Entwicklungsumgebung für die Programmierung mit DWriteCore einrichten.

### <a name="install-the-project-reunion-05-vsix"></a>Installieren von Project Reunion 0.5 VSIX

Klicken Visual Studio auf **Erweiterungen** Erweiterungen  >  **verwalten,** suchen Sie *nach Project Reunion,* und laden Sie die Projekt-Reunion-Erweiterung herunter. Schließen Und öffnen Sie Visual Studio, und befolgen Sie die Anweisungen, um die Erweiterung zu installieren.

Weitere Informationen finden Sie unter [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0)und [Erstellen von Windows-Desktop-Apps mit Project Reunion 0.5](/windows/apps/project-reunion/#set-up-your-development-environment).

### <a name="create-a-new-project"></a>Erstellen eines neuen Projekts

Erstellen Visual Studio Projektvorlage Leere App, Gepackt **(WinUI 3 in Desktop) ein** neues Projekt. Sie können diese Projektvorlage finden, indem Sie sprache auswählen: *C++*; platform: *Project Reunion*; Projekttyp: *Desktop*.

Weitere Informationen finden Sie unter [Projektvorlagen für WinUI 3.](/windows/apps/winui/winui3/winui-project-templates-in-visual-studio#project-templates-for-winui-3)

### <a name="install-the-microsoftprojectreuniondwrite-nuget-package"></a>Installieren des NuGet-Pakets Microsoft.ProjectReunion.DWrite

Klicken Visual Studio auf Projekt  NuGet-Pakete verwalten... Durchsuchen, geben oder fügen Sie \>  \>  **Microsoft.ProjectReunion.DWrite** in  das Suchfeld ein, wählen Sie das Element in den Suchergebnissen aus, und klicken Sie dann auf Installieren, um das Paket für dieses Projekt zu installieren.

### <a name="alternatively-begin-with-the-dwritecoregallery-sample-app"></a>Beginnen Sie alternativ mit der Beispiel-App DWriteCoreGallery.

Alternativ können Sie mit DWriteCore programmieren, indem Sie mit dem Beispiel-App-Projekt [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) beginnen und Ihre Entwicklung auf diesem Projekt basieren. Sie können dann beliebigen vorhandenen Quellcode (oder Dateien) aus diesem Beispielprojekt entfernen und dem Projekt neuen Quellcode (oder Dateien) hinzufügen.

### <a name="use-dwritecore-in-your-project"></a>Verwenden von DWriteCore in Ihrem Projekt

Weitere Informationen zum Programmieren mit DWriteCore finden Sie im Abschnitt [Programming with DWriteCore](#programming-with-dwritecore) weiter unten in diesem Thema.

## <a name="the-release-phases-of-dwritecore"></a>Die Releasephasen von DWriteCore

Das Portieren von DirectWrite zu DWriteCore ist ein ausreichend großes Projekt für mehrere Windows-Releasezyklen. Dieses Projekt ist in Phasen unterteilt, von denen jede einem Funktionsabschnitt entspricht, der in einem Release bereitgestellt wird.

### <a name="features-in-the-current-release-of-dwritecore"></a>Features in der aktuellen Version von DWriteCore

Die derzeit verfügbare Version von DWriteCore ist Teil von [Project Reunion 0.5](https://github.com/microsoft/ProjectReunion/releases/tag/0.5.0). Sie enthält die grundlegenden Tools, die Sie als Entwickler benötigen, um DWriteCore zu nutzen, einschließlich der folgenden Features.

- Schriftartenumeration.
- Schriftart-API.
- Gestaltung.
- Rendering-APIs auf niedriger Ebene. Dies ist in der aktuellen Phase teilweise, &mdash; da DWriteCore nicht mit [Direct2D](../direct2d/direct2d-portal.md)interoperiert, aber Sie können [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) und [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)verwenden.
- Grundlegende Textlayoutfunktionalität.
- Textrendering-APIs.
- Bitmap-Renderziel.
- Farbschriftarten.
- Verschiedene Optimierungen (Bereinigung des Schriftartcaches, In-Memory-Schriftartladeprogramm usw.)

Ein Bannerfeature sind Farbschriftarten. Mit Farbschriftarten können Sie Ihre Schriftarten mit anspruchsvolleren Farbfunktionen rendern, die über einfache Einzelfarben hinausgehen. Farbschriftarten sind z. B. die Möglichkeit, Emoji- und Symbolsymbolschriftarten zu rendern (letzteres wird z.B. von Office verwendet). Farbschriftarten wurden erstmals in Windows 8.1 eingeführt, aber das Feature wurde in Windows 10 Version 1607 (Anniversary Update) stark erweitert.

Die Arbeit an der Bereinigung des Schriftartcaches und des In-Memory-Schriftartlademoduls ermöglicht ein schnelleres Laden von Schriftarten und Arbeitsspeicherverbesserungen.

Mit diesen Features können Sie sofort beginnen, einige der modernen Kernfunktionen von DirectWrite zu nutzen, z. B. variable Schriftarten auf &mdash; &mdash; downlevelr Windows 8. Variable Schriftarten sind eines der wichtigsten Features für DirectWrite-Kunden. Sie wurden in Windows 10 Version 1709 (Fall Creators Update) eingeführt, sodass der Zugriff darauf in früheren Versionen für Sie als Entwickler einen erheblichen Vorteil ist.

## <a name="our-invitation-to-you-as-a-directwrite-developer"></a>Unsere Einladung an Sie als DirectWrite-Entwickler

DWriteCore wird zusammen mit anderen Project Reunion-Komponenten entwickelt und offen für Entwicklerfeedback. Wir laden Sie ein, DWriteCore zu erkunden und Einblicke oder Anforderungen in die Featureentwicklung in unserem [GitHub-Repository project reunion zu geben.](https://github.com/microsoft/ProjectReunion/)

## <a name="programming-with-dwritecore"></a>Programmieren mit DWriteCore

Genau wie bei [DirectWrite](./direct-write-portal.md)programmieren Sie mit DWriteCore über die COM-light-API über die [**IDWriteFactory-Schnittstelle.**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)

Um DWriteCore verwenden zu können, muss die `dwrite_core.h` Headerdatei enthalten sein.

```cppwinrt
// pch.h
...
// DWriteCore header file.
#include <dwrite_core.h>
```

Die `dwrite_core.h` Headerdatei definiert zuerst das Token *DWRITE_CORE*, und dann enthält sie die `dwrite_3.h` Headerdatei. Das *DWRITE_CORE* token ist wichtig, da es alle nachfolgend enthaltenen Header anlädt, ihnen alle DirectWrite-APIs zur Verfügung zu stellen. Sobald Ihr Projekt enthalten ist, können Sie code `dwrite_core.h` schreiben, erstellen und ausführen.

### <a name="apis-that-are-new-or-different-for-dwritecore"></a>APIs, die neu oder anders für DWriteCore sind

Die DWriteCore-API-Oberfläche ist größtenteils identisch mit der Oberfläche für [DirectWrite.](/windows/win32/api/_directwrite/) Es gibt jedoch eine kleine Anzahl neuer APIs, die sich derzeit nur in DWriteCore befinden.

#### <a name="create-a-factory-object"></a>Erstellen eines Factoryobjekts

Die freie [**DWriteCoreCreateFactory-Funktion**](/windows/win32/api/dwrite_core/nf-dwrite_core-dwritecorecreatefactory) erstellt ein Factoryobjekt, das für die nachfolgende Erstellung einzelner DWriteCore-Objekte verwendet wird.

**DWriteCoreCreateFactory** ist funktionell identisch mit der [DWriteCreateFactory-Funktion,](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) die von der Systemversion von DirectWrite exportiert wird. Die DWriteCore-Funktion hat einen anderen Namen, um Mehrdeutigkeiten zu vermeiden.

#### <a name="create-a-restricted-factory-object"></a>Erstellen eines eingeschränkten Factoryobjekts

Die [**DWRITE_FACTORY_TYPE-Enumeration**](./dwrite/ne-dwrite-dwrite_factory_type.md) verfügt über eine neue Konstante &mdash; **DWRITE_FACTORY_TYPE_ISOLATED2**, die eine eingeschränkte Factory angibt. Eine eingeschränkte Factory ist stärker gesperrt als eine isolierte Factory. Es interagiert in keiner Weise mit einem prozessübergreifenden oder persistenten Schriftartcache. Darüber hinaus enthält die von dieser Factory zurückgegebene Systemschriftartsammlung nur bekannte Schriftarten. So können Sie **DWRITE_FACTORY_TYPE_ISOLATED2** verwenden, um ein eingeschränktes Factoryobjekt zu erstellen, wenn Sie die kostenlose **DWriteCoreCreateFactory-Funktion** aufrufen.

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

Wenn Sie **DWRITE_FACTORY_TYPE_ISOLATED2** an eine ältere Version von DirectWrite übergeben, die dies nicht unterstützt, gibt **DWriteCreateFactory** **E_INVALIDARG** zurück.

#### <a name="drawing-glyphs-to-a-system-memory-bitmap"></a>Zeichnen von Glyphen in einer Systemspeicherbitmap

DirectWrite verfügt über eine Bitmap-Renderzielschnittstelle, die das Rendern von Glyphen in eine Bitmap im Systemspeicher unterstützt. Derzeit besteht die einzige Möglichkeit für den Zugriff auf die zugrunde liegenden Pixeldaten jedoch darin, GDI zu durchlaufen, sodass die API nicht plattformübergreifend verwendet werden kann. Dies lässt sich leicht beheben, indem eine Methode zum Abrufen der Pixeldaten hinzugefügt wird.

DWriteCore führt daher die [**IDWriteBitmapRenderTarget2-Schnittstelle**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) und ihre Methode [**IDWriteBitmapRenderTarget2::GetBitmapData**](./dwrite_3/nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md)ein. Diese Methode verwendet einen Parameter vom Typ (Zeiger auf) [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md), bei dem es sich um eine neue Struktur handelt.

Ihre Anwendung erstellt ein Bitmaprenderingziel durch Aufrufen von [IDWriteGdiInterop::CreateBitmapRenderTarget](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget). Unter Windows kapselt ein Bitmaprenderingziel einen GDI-Speicherdomänencontroller mit einer ausgewählten geräteunabhängigen GDI-Bitmap (DIB). [IDWriteBitmapRenderTarget::D rawGlyphRun](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) rendert Glyphen im DIB. DirectWrite rendert die Glyphen selbst, ohne GDI zu durchschreiten. Ihre Anwendung kann dann den **HDC** aus dem Bitmaprenderingziel erhalten und [BitBlt verwenden,](/windows/win32/api/wingdi/nf-wingdi-bitblt) um die Pixel in ein **HDC-Fenster zu kopieren.**

Auf Nicht-Windows-Plattformen kann Ihre Anwendung weiterhin ein Bitmaprenderingziel erstellen, kapselt aber einfach ein Systemspeicherarray ohne **HDC** und ohne DIB. Ohne einen **HDC** muss es eine andere Möglichkeit für Ihre Anwendung geben, die Bitmappixel zu erhalten, damit sie sie kopieren oder anderweitig verwenden kann. Selbst unter Windows ist es manchmal nützlich, die tatsächlichen Pixeldaten zu erhalten, und wir zeigen die aktuelle Methode dazu im folgenden Codebeispiel.

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

#### <a name="other-api-differences-between-dwritecore-and-directwrite"></a>Weitere API-Unterschiede zwischen DWriteCore und DirectWrite

Es gibt einige APIs, die entweder nur Stubs sind oder sich auf Nicht-Windows-Plattformen etwas anders verhalten. [IDWriteGdiInterop::CreateFontFaceFromHdc](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) gibt beispielsweise  E_NOTIMPL auf Nicht-Windows-Plattformen zurück, da es keine **HDC** ohne [GDI](../gdi/windows-gdi.md)gibt.

Und schließlich gibt es bestimmte andere Windows-APIs, die in der Regel zusammen mit DirectWrite verwendet werden (Direct2D ist ein gutes Beispiel). Derzeit können Direct2D und DWriteCore jedoch nicht zusammenarbeiten. Wenn Sie z. B. ein [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mit DWriteCore erstellen und an [**D2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)übergeben, erzeugt dieser Aufruf einen Fehler.
