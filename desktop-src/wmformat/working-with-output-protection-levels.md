---
title: Arbeiten mit Ausgabeschutzebenen
description: Arbeiten mit Ausgabeschutzebenen
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Medienformat-SDK, Ausgabeschutzebenen (OPL)
- Windows Medienformat-SDK, Schutzebenen
- Advanced Systems Format (ASF), Ausgabeschutzebenen (OPL)
- ASF (Advanced Systems Format), Ausgabeschutzebenen (OPL)
- Advanced Systems Format (ASF), Schutzebenen
- ASF (Advanced Systems Format), Schutzebenen
- Advanced Systems Format (ASF), mehrere Lizenzen
- ASF (Advanced Systems Format), mehrere Lizenzen
- Digital Rights Management (DRM), Ausgabeschutzebenen (OPL)
- DRM (Digital Rights Management), Ausgabeschutzebenen (OPL)
- Digital Rights Management (DRM), Schutzebenen
- DRM (Digital Rights Management), Schutzebenen
- Digital Rights Management (DRM), Auswerten von Ausgabeschutzebenen (OPL)
- DRM (Digital Rights Management), Auswerten von Ausgabeschutzebenen (OPL)
- Digital Rights Management (DRM), mehrere Lizenzen
- DRM (Digital Rights Management), mehrere Lizenzen
- Ausgabeschutzebenen (Output Protection Levels, OPL)
- OPL (Ausgabeschutzebenen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2888891e50ec90e784bf6f4420637544854a9b600b5538e9655bc6d3028f76d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697714"
---
# <a name="working-with-output-protection-levels"></a>Arbeiten mit Ausgabeschutzebenen

Lizenzen, die mit dem Windows Media Rights Manager 10 SDK erstellt wurden, können Aktionseinschränkungen mithilfe von Ausgabeschutzebenen (Output Protection Levels, OPLs) angeben. OPLs ermöglichen einem Lizenzersteller, einige Aktionen nur auf Geräten mit bestimmten Technologien zuzulassen. Der Vorteil der Verwendung von OPLs besteht darin, dass Sie mehr Flexibilität beim Erstellen von Lizenzeinschränkungen als bei früheren Versionen erhalten. Darüber hinaus sind OPLs erweiterbar, um zukünftige Technologien zu unterstützen. Sie können solche Lizenzen in Ihren Anwendungen mithilfe der Methoden der [**IWMDRMReader2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) unterstützen.

Um Dateien zu lesen, die durch eine Lizenz geschützt sind, die OPLs angibt, müssen Sie die OPL auf die gewünschte Aktion überprüfen. Die Ausgabetechnologie, die Ihre Anwendung verwendet, muss von der OPL in der Lizenz zugelassen werden. Einige Lizenzen für geschützte Audiodaten erfordern z. B. möglicherweise die Verwendung eines sicheren Audiopfads für die Wiedergabe.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Konfigurieren des Readers zum Auswerten von Ausgabeschutzebenen

Bevor Sie OPLs für im Reader geladene Dateien überprüfen können, müssen Sie die [**IWMDRMReader2::SetEvaluateOutputLevelLicenses-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) aufrufen und **TRUE** für den *fEvaluate-Parameter* übergeben. Wenn Sie diese Methode nicht aufrufen, sind Lizenzen, die OPLs erfordern, für Ihre Anwendung nicht sichtbar.

## <a name="evaluating-copy-output-protection-levels"></a>Auswerten von Kopierausgabe-Schutzebenen

Um Ausgabeschutzebenen für die Kopieraktion abzurufen, rufen Sie die [**IWMDRMReader2::GetCopyOutputLevels-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) auf. Die Daten, die Sie vom Aufruf erhalten, werden in einer [**DRM \_ COPY \_ OPL-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) gespeichert. Die -Struktur enthält eine Basisausgabeschutzebene, die die minimale Ausgabeebene für die Kopieraktion in der Lizenz angibt. Die DRM \_ COPY \_ OPL-Struktur enthält jedoch auch zwei Listen von Technologiebezeichnern: eine für zulässige Technologien, die mit einer niedrigeren OPL als die Basis bewertet werden, und eine für Technologien, die gleich oder höher als die Basis-OPL bewertet werden, aber durch die Lizenz eingeschränkt sind. Sie müssen die Ein- und Ausschlüsse überprüfen, um sicherzustellen, dass die Technologie, die Ihre Anwendung verwendet, durch die Lizenz zugelassen wird.

## <a name="evaluating-play-output-protection-levels"></a>Auswerten von Wiedergabeausgabeschutzebenen

Um Ausgabeschutzebenen für die Wiedergabeaktion abzurufen, rufen Sie die [**IWMDRMReader2::GetPlayOutputLevels-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) auf. Die Daten, die Sie vom Aufruf erhalten, werden in einer [**DRM \_ PLAY \_ OPL-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) gespeichert. Die -Struktur enthält mehrere andere -Strukturen. Die Grundlegenden Ausgabeschutzebenen für die Wiedergabeaktion werden in einer [**DRM-STRUKTUR MIT \_ MINIMALEN \_ \_ \_ AUSGABESCHUTZEBENEn**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) **(minOPL-Member** von **DRM \_ PLAY \_ OPL)** gespeichert, die die minimale OPL definiert, die zum Wiedergeben von Inhalten in einer Vielzahl von Formaten erforderlich ist. Sie müssen den Member auf den Typ der Ausgabeformate überprüfen, die ihre Anwendung übermittelt.

Die **DRM \_ PLAY \_ OPL-Struktur** definiert zwei Arten von Einschränkungen: erforderliche Downsampling und zulässige Schutzbezeichner für die Videoausgabe.

Erforderliche Downsamplings werden als Liste von Ausgabetechnologiebezeichnern **(oplIdDownsample-Member** von **DRM \_ PLAY \_ OPL)** definiert, die bei Verwendung den Inhalt nur dann für die Wiedergabe empfangen können, wenn der Inhalt zum ersten Mal mit einer niedrigeren Bitrate abgesampelt wird.

Zulässige Schutzbezeichner für die Videoausgabe werden als Liste von Videoausgabetechnologien mit Konfigurationsinformationen für jede definiert.

## <a name="handling-multiple-licenses"></a>Behandeln mehrerer Lizenzen

Einigen Dateien sind möglicherweise mehrere Lizenzen im lokalen Lizenzspeicher zugeordnet. Wenn Sie OPLs für eine Datei auswerten, die Sie lesen, können Sie nach zusätzlichen Lizenzen suchen, indem Sie die [**IWMDRMReader2::TryNextLicense-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) aufrufen. Sie sollten weiterhin Lizenzen testen, bis Sie eine gefunden haben, die die auszuführende Aktion zulässt, oder bis TryNextLicense DRM \_ S FALSE zurückgibt, was darauf \_ hinweist, dass keine Weiteren Lizenzen vorhanden sind.

In einigen Fällen verfügt eine Datei möglicherweise über eine zugeordnete Lizenz, die eine OPL erfordert, die Ihre Anwendung nicht unterstützen kann. In einem solchen Fall ist es wichtig, nach zusätzlichen Lizenzen zu suchen, da möglicherweise eine Lizenz vorhanden ist, die keine OPLs angibt.

**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




