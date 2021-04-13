---
title: Arbeiten mit Ausgabe Schutz Ebenen
description: Arbeiten mit Ausgabe Schutz Ebenen
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media-Format-SDK, Ausgabe Schutz Ebenen (OPL)
- Windows Media-Format-SDK, Schutz Ebenen
- Advanced Systems Format (ASF), Ausgabe Schutz Ebenen (OPL)
- ASF (Advanced Systems Format), Ausgabe Schutz Ebenen (OPL)
- Advanced Systems Format (ASF), Schutz Ebenen
- ASF (Advanced Systems Format), Schutz Ebenen
- Advanced Systems Format (ASF), mehrere Lizenzen
- ASF (Advanced Systems Format), mehrere Lizenzen
- Digital Rights Management (DRM), Ausgabe Schutz Ebenen (OPL)
- DRM (Digital Rights Management), Ausgabe Schutz Ebenen (OPL)
- Digital Rights Management (DRM), Schutz Ebenen
- DRM (Digital Rights Management), Schutz Ebenen
- Digital Rights Management (DRM), Auswerten von Ausgabe Schutz Ebenen (OPL)
- DRM (Digital Rights Management), Auswerten von Ausgabe Schutz Ebenen (OPL)
- Digital Rights Management (DRM), mehrere Lizenzen
- DRM (Digital Rights Management), mehrere Lizenzen
- Ausgabe Schutz Ebenen (OPL)
- OPL (Ausgabe Schutz Ebenen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314219"
---
# <a name="working-with-output-protection-levels"></a>Arbeiten mit Ausgabe Schutz Ebenen

Lizenzen, die mithilfe des Windows Media Rights Manager 10 SDK erstellt wurden, können Aktions Einschränkungen mithilfe von "Output Protection Levels (opls)" angeben. Opls ermöglichen einem Lizenz Ersteller, einige Aktionen nur auf Geräten mit bestimmten Technologien zuzulassen. Die Verwendung von opls hat den Vorteil, dass Sie mehr Flexibilität bei der Erstellung von Lizenz Einschränkungen als in früheren Versionen erhalten. Außerdem sind opls erweiterbar, um zukünftige Technologien zu ermöglichen. Sie können solche Lizenzen in Ihren Anwendungen unterstützen, indem Sie die Methoden der [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) -Schnittstelle verwenden.

Um Dateien zu lesen, die durch eine Lizenz geschützt sind, die opls angibt, müssen Sie die OPL auf die gewünschte Aktion überprüfen. Die von Ihrer Anwendung verwendete Ausgabe Technologie muss von der OPL in der Lizenz zugelassen werden. Beispielsweise erfordern einige Lizenzen für geschütztes Audiomaterial, dass Sie einen sicheren Audiopfad für die Wiedergabe verwenden.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Konfigurieren des Readers zum Auswerten von Ausgabe Schutz Ebenen

Bevor Sie opls auf Dateien prüfen können, die im Reader geladen wurden, müssen Sie die [**IWMDRMReader2:: setevaluateoutputlevellicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) -Methode aufrufen und dabei **true** für den *fevaluate* -Parameter übergeben. Wenn Sie diese Methode nicht aufzurufen, sind Lizenzen, die opls erfordern, für Ihre Anwendung nicht sichtbar.

## <a name="evaluating-copy-output-protection-levels"></a>Auswerten von Schutz Ebenen für die Kopier Ausgabe

Zum Abrufen von Ausgabe Schutz Ebenen für die Kopier Aktion müssen Sie die [**IWMDRMReader2:: getcopyoutputlevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) -Methode aufrufen. Die Daten, die Sie vom-Befehl empfangen, werden in einer [**DRM- \_ \_ kopieropl**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) -Struktur gespeichert. Die-Struktur enthält eine grundlegende Ausgabe Schutz Ebene, die die minimale Ausgabe Ebene für die Kopier Aktion in der Lizenz angibt. Die DRM \_ \_ -OPL-Struktur enthält jedoch auch zwei Listen mit Technologie bezeichgern: eine für zulässige Technologien, die mit einer niedrigeren OPL als der Basis bewertet werden, und eine für Technologien, die gleich oder höher als die Basis-OPL bewertet werden, aber durch die Lizenz eingeschränkt werden. Sie müssen die Einschlüsse und Ausschlüsse überprüfen, um sicherzustellen, dass die von Ihrer Anwendung verwendete Technologie von der Lizenz zugelassen wird.

## <a name="evaluating-play-output-protection-levels"></a>Auswerten von Wiedergabe-Ausgabe Schutz Ebenen

Zum Abrufen von Ausgabe Schutz Ebenen für die Wiedergabe Aktion müssen Sie die [**IWMDRMReader2:: getplayoutputlevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) -Methode aufrufen. Die Daten, die Sie vom-Befehl empfangen, werden in einer [**DRM- \_ Wiedergabe- \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) -Struktur gespeichert. Die-Struktur enthält mehrere andere-Strukturen. Die grundlegenden Ausgabe Schutz Ebenen für die Wiedergabe Aktion werden in einer [**DRM- \_ minimalen \_ Ausgabe \_ Schutz \_ Ebenen**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) -Struktur (dem **minopl** -Member von **DRM \_ Play \_ OPL**) gespeichert, der die minimale OPL definiert, die für die Wiedergabe von Inhalten in einer Vielzahl von Formaten erforderlich ist. Sie müssen das-Element auf den Typ der Ausgabeformate überprüfen, die Ihre Anwendung bereitstellt.

Die **DRM- \_ Wiedergabe- \_ OPL** -Struktur definiert zwei Arten von Einschränkungen: erforderliche Abtast Stichproben und zulässige Video-Ausgabe Schutz Bezeichner.

Die erforderliche Downsampling ist als eine Liste von Ausgabe Technologie bezeichaten definiert (das **opliddownsample** -Element von **DRM \_ Play \_ OPL**), die den Inhalt für die Wiedergabe nur dann empfangen kann, wenn der Inhalt zuerst mit einer niedrigeren Bitrate abgetastet wird.

Zulässige Grafik-Ausgabebezeichner werden als Liste von Videoausgabe Technologien definiert, die jeweils Konfigurationsinformationen enthalten.

## <a name="handling-multiple-licenses"></a>Verarbeiten mehrerer Lizenzen

Einigen Dateien sind möglicherweise mehrere Lizenzen im lokalen Lizenz Speicher zugeordnet. Wenn Sie opls für eine Datei auswerten, die Sie lesen, können Sie durch Aufrufen der [**IWMDRMReader2:: trynextlicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) -Methode nach zusätzlichen Lizenzen suchen. Sie sollten die Lizenzen weiterhin testen, bis Sie eine gefunden haben, die die durchzuführende Aktion zulässt, oder bis "trynextlicense" DRM \_ S false zurückgibt \_ . Dies deutet darauf hin, dass keine Lizenzen mehr vorhanden sind.

In einigen Fällen kann eine Datei über eine zugehörige Lizenz verfügen, die eine OPL erfordert, die von der Anwendung nicht unterstützt wird. In einem solchen Fall ist es wichtig, eine Überprüfung auf weitere Lizenzen durchzuführen, da möglicherweise eine Lizenz vorhanden ist, die keine opls angibt.

**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




