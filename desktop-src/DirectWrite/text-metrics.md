---
title: Textmetriken
description: Zum unterstützen Ihres Layouts, der benutzerdefinierten Schriftart Auswahl und anderer metrikintensiver Vorgänge, beginnend mit Windows 8, verfügt DirectWrite über eine Reihe neuer APIs, mit denen alle Informationen zu Schriftarten ausgedrückt werden können, die Sie möglicherweise zum Entwickeln von Rich-Text-apps benötigen.
ms.assetid: 9df8c675-6f4d-4de7-916e-7dc51f5f04aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73647ae4521b23afb399a4c66c8b25cdc46ba1b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340525"
---
# <a name="text-metrics"></a>Textmetriken

Zum unterstützen Ihres Layouts, der benutzerdefinierten Schriftart Auswahl und anderer metrikintensiver Vorgänge, beginnend mit Windows 8, verfügt [DirectWrite](direct-write-portal.md) über eine Reihe neuer APIs, mit denen alle Informationen zu Schriftarten ausgedrückt werden können, die Sie möglicherweise zum Entwickeln von Rich-Text-apps benötigen.

## <a name="panose"></a>Panose

Panose ist ein visuelles Klassifizierungssystem zum Identifizieren von Schriftarten. Die Panose-Klassifizierung enthält Informationen über die Familie, den Serif-Stil, die Gewichtung, den Anteil, den Kontrast, den Strich, den Arm-Stil, die X-Höhe usw. Diese Informationen beschreiben den visuellen Stil der Schriftart. Diese Informationen sind wichtig, da Schriftarten mit ähnlichen Panose-Werten ähnlich aussehen. Dies ist in Situationen, in denen eine Schriftart nicht verfügbar ist, sehr nützlich, und die APP muss auf eine verfügbare Schriftart zurückgreifen. Wenn Sie Panose-Werte für Schriftarten vergleichen, können Sie eine Schriftart auswählen, die der ursprünglichen Schriftart visuell ähnelt.

Um auf die Panose-Informationen für eine Schriftart zuzugreifen, verwenden Sie die [**getpanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) -Methode in den [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) -und [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) -Schnittstellen. Diese Methode gibt eine [**dwrite \_ Panose**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_panose) -Enumeration zurück, die alle Panose-Informationen für diese Schriftart enthält.

## <a name="additional-metrics"></a>Zusätzliche Metriken

Ab Windows 8 unterstützt die [DirectWrite](direct-write-portal.md) -API auch eine Reihe neuer Metriken, um nützliche Informationen über die Schriftarten für Ihre APP zu erhalten. Diese neuen Metriken enthalten diese Informationen.

-   Linke, Rechte, obere und untere Symbol Metriken für das Glyphe.
-   X-und Y-Positionierung für hoch gestellt-und Index-Elemente.
-   X-und Y-Skalierungsinformationen für hoch gestellt-und Index-Elemente.
-   Gibt an, ob die Schriftart typografische Metriken aufweist.

Diese Informationen sind über die neue [**getmetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics) -Methode in den [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) -und [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) -Schnittstellen verfügbar. Diese Methode gibt eine [**dwrite- \_ Schriftart \_ METRICS1**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_font_metrics1) -Struktur zurück, die alle diese Informationen enthält.

## <a name="caret-metrics"></a>Einfügemarke

Um Textbearbeitungs-apps zu erstellen, benötigen Sie Zugriff auf Informationen zum Zeichnen der Einfügemarke, die durch den Text navigiert. Ab Windows 8 stellt [DirectWrite](direct-write-portal.md) die [**getcaretmetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics) -Methode in den [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) -und [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) -Schnittstellen für dieses Szenario bereit. **Getcaretmetrics** gibt eine Enumeration der [**dwrite- \_ caretzermetriken \_**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_caret_metrics) zurück, die Informationen über die Steigung und den Offset für die Einfügemarke entlang der Baseline enthält.

Diese Informationen sind besonders hilfreich, wenn Sie in der Lage sein sollen, ihre Einfügemarke entsprechend dem kursiv Formatierbaren Text zu hängen.

## <a name="monospaced-discoverability"></a>Auffindbarkeit von Monospaced

Apps, die es Ihren Benutzern ermöglichen, Computercode zu schreiben, verwenden häufig fest breiten Schriftarten anstelle von herkömmlichen Schriftarten. Sie können also mehr Kontrolle über die Schriftart Auswahl in apps im Zusammenhang mit der Entwicklung haben. [DirectWrite](direct-write-portal.md) gibt an, ob eine Schriftart über die API fest breiten ist. Die [**ismonospacedfont**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont) -Methode der [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) -Schnittstelle gibt einen booleschen Wert zurück, der angibt, ob die Schriftart Monospaced ist.

## <a name="font-name-matching"></a>Schriftart namens Übereinstimmung

Rich-Text-apps wie PDF-Reader müssen in der Lage sein, Schriftarten in ihren Inhalten mit Schriftarten im System abzugleichen. Sie benötigen Zugriff auf die vollständigen Namen von Schriftarten in mehreren Formaten. Sie können Schriftarten besser zuordnen, [DirectWrite](direct-write-portal.md) enthält eine Enumeration, die vollständige Benennungs Informationen zu einer Schriftart in vielen Formaten ausdrückt.

mit der dwrite-Enumeration für [**\_ Informations \_ Zeichenfolgen- \_ IDs**](/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id) können Sie den vollständigen Namen, den PostScript-Namen und den PostScript-CID-Namen einer beliebigen Schriftart im System erhalten. Diese Informationen sind hilfreich, wenn Sie Schriftarten in Ihrer APP mit den entsprechenden Schriftarten auf dem lokalen System vergleichen müssen.

## <a name="glyph-advances"></a>Glyphe-Fortschritte

Die **getglyphadvances** -Methode der [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) -Schnittstelle und der [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) -Schnittstelle übernimmt die Symbol Anzahl und die Indizes, die Sie benötigen, und gibt dann die Fortschritte für die fraglichen Symbole zurück.

## <a name="unicode-ranges"></a>Unicode-Bereiche

Apps, die ihre eigene Schriftart Auswahl verarbeiten möchten, benötigen Zugriff auf die Unicode-Bereiche, die von der Schriftart unterstützt werden. Auf diese Weise kann die APP, wenn ein Unicode-Codepunkt nicht von der Schriftart unterstützt wird, eine passende Schriftart auswählen, die das Symbol enthält. Ohne diese Informationen kann die APP eine Schriftart verwenden, die nicht alle Symbole enthält, die erforderlich sind, um die angezeigten Informationen anzuzeigen.

Die [**GetUnicodeRanges**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges) -Methode in den [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) -und [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) -Schnittstellen nimmt die maximale Anzahl der vom Client übergebenen Bereiche an und gibt die tatsächlich von der Schriftart unterstützten Bereiche zurück.

## <a name="eudc-font-collection"></a>EUDC-Schriftart Sammlung

Verwenden Sie die [**geteudcfontcollection**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefactory1-geteudcfontcollection) -Methode der [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) -Schnittstelle, um auf die EUDC-Schriftart Auflistung zuzugreifen. Diese Methode funktioniert auf dieselbe Weise wie [**getsystemfontcollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection), gibt jedoch stattdessen einen Zeiger auf eine EUDC-Schriftart Auflistung zurück.

 

 