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
- Digital Rights Management (DRM), Ausgabeschutzebenen (OUTPUT Protection Levels, OPL)
- DRM (Digital Rights Management), Ausgabeschutzebenen (OUTPUT Protection Levels, OPL)
- Digital Rights Management (DRM), Schutzebenen
- DRM (Digital Rights Management), Schutzebenen
- Digital Rights Management (DRM), Auswerten von Ausgabeschutzebenen (OPL)
- DRM (Digital Rights Management), Auswerten von Ausgabeschutzebenen (OPL)
- Digital Rights Management (DRM), mehrere Lizenzen
- DRM (Digital Rights Management), mehrere Lizenzen
- Ausgabeschutzebenen (OUTPUT Protection Levels, OPL)
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

Lizenzen, die mit dem Windows Media Rights Manager 10 SDK erstellt wurden, können Aktionseinschränkungen mithilfe von Ausgabeschutzebenen (Output Protection Levels, OPLs) angeben. OPLs ermöglichen einem Lizenzersteller, einige Aktionen nur auf Geräten mit bestimmten Technologien zu erlauben. Die Verwendung von OPLs hat den Vorteil, dass Sie mehr Flexibilität beim Erstellen von Lizenzeinschränkungen erhalten als frühere Versionen. Darüber hinaus können OPLs erweitert werden, um zukünftige Technologien zu unterstützen. Sie können solche Lizenzen in Ihren Anwendungen mithilfe der Methoden der [**IWMDRMReader2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) unterstützen.

Zum Lesen von Dateien, die durch eine Lizenz geschützt sind, die OPLs angibt, müssen Sie opl auf die gewünschte Aktion überprüfen. Die Von Ihrer Anwendung verwendete Ausgabetechnologie muss von der OPL in der Lizenz zugelassen werden. Einige Lizenzen für geschützte Audiodaten erfordern beispielsweise möglicherweise, dass Sie einen sicheren Audiopfad verwenden, um sie wieder zu verwenden.

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>Konfigurieren des Readers zum Auswerten von Ausgabeschutzebenen

Bevor Sie OPLs auf Im Reader geladene Dateien überprüfen können, müssen Sie die [**IWMDRMReader2::SetEvaluateOutputLevelLicenses-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) aufrufen und **TRUE** für den *fEvaluate-Parameter* übergeben. Wenn Sie diese Methode nicht aufrufen, sind Lizenzen, die OPLs erfordern, für Ihre Anwendung nicht sichtbar.

## <a name="evaluating-copy-output-protection-levels"></a>Auswerten von Kopierausgabeschutzebenen

Um Ausgabeschutzebenen für die Kopieraktion zu erhalten, rufen Sie [**die IWMDRMReader2::GetCopyOutputLevels-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) auf. Die Daten, die Sie vom Aufruf erhalten, werden in einer [**DRM \_ COPY \_ OPL-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) gespeichert. Die -Struktur enthält eine Basisschutzebene für die Ausgabe, die die mindeste Ausgabeebene für die Kopieraktion in der Lizenz angibt. Die DRM COPY OPL-Struktur enthält jedoch auch zwei Listen von Technologiebezeichnern: eine für zulässige Technologien, die mit einer niedrigeren OPL als die Basis bewertet werden, und eine für Technologien, die gleich oder höher als die Basis-OPL bewertet sind, aber durch die Lizenz eingeschränkt \_ \_ sind. Sie müssen die Ein- und Ausschlüsse überprüfen, um sicherzustellen, dass die Technologie, die Ihre Anwendung verwendet, von der Lizenz zugelassen wird.

## <a name="evaluating-play-output-protection-levels"></a>Auswerten von Wiedergabeausgabeschutzebenen

Um Ausgabeschutzebenen für die Wiedergabeaktion zu erhalten, rufen Sie [**die IWMDRMReader2::GetPlayOutputLevels-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) auf. Die Daten, die Sie vom Aufruf erhalten, werden in einer [**DRM \_ PLAY \_ OPL-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) gespeichert. Die -Struktur enthält mehrere andere -Strukturen. Die Basisausgabeschutzebenen für die Wiedergabeaktion werden in einer [**DRM \_ MINIMUM OUTPUT PROTECTION \_ \_ \_ LEVELS-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) **(dem minOPL-Member** von **DRM PLAY \_ \_ OPL)** gespeichert, die die mindest erforderliche OPL für die Wiedergabe von Inhalten in einer Vielzahl von Formaten definiert. Sie müssen den Member auf den Typ der Ausgabeformate überprüfen, die ihre Anwendung liefert.

Die **DRM \_ PLAY \_ OPL-Struktur** definiert zwei Arten von Einschränkungen: erforderliche Downs sampling und zulässige Videoausgabe-Schutzbezeichner.

Erforderliches Downsamping wird als Liste von Ausgabetechnologiebezeichnern **(oplIdDownsample-Member** von **DRM \_ PLAY \_ OPL)** definiert, die bei Verwendung den Inhalt nur dann zur Wiedergabe empfangen können, wenn der Inhalt zuerst auf eine niedrigere Bitrate heruntersamplet wird.

Zulässige Videoausgabeschutz-IDs werden als Liste der Videoausgabetechnologien definiert, die jeweils Konfigurationsinformationen enthalten.

## <a name="handling-multiple-licenses"></a>Behandeln mehrerer Lizenzen

Einigen Dateien sind möglicherweise mehrere Lizenzen im lokalen Lizenzspeicher zugeordnet. Wenn Sie OPLs für eine Datei auswerten, die Sie lesen, können Sie durch Aufrufen der [**IWMDRMReader2::TryNextLicense-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) nach zusätzlichen Lizenzen suchen. Sie sollten weiterhin Lizenzen testen, bis Sie eine Lizenz finden, die die durchzuführende Aktion zulässt, oder bis TryNextLicense DRM S FALSE zurückgibt, was darauf hinweist, dass keine Lizenzen mehr \_ \_ verfügbar sind.

In einigen Fällen kann eine Datei über eine zugeordnete Lizenz verfügen, die eine OPL erfordert, die Ihre Anwendung nicht unterstützen kann. In einem solchen Fall ist es wichtig, nach zusätzlichen Lizenzen zu prüfen, da möglicherweise eine Lizenz vorhanden ist, die keine OPLs an.

**Hinweis:** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren der DRM-Unterstützung**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




