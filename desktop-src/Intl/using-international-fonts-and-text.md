---
description: In jeder Hauptversion von Windows werden Schriftarten hinzugefügt, um internationale Sprachen und Skripts zu unterstützen.
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: Internationale Schriftartenenumeration und -auswahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b28e2dca3937f3513a930f157a364d466f761ed54a53d09c3e2b8b1c89bb30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146883"
---
# <a name="international-font-enumeration-and-selection"></a>Internationale Schriftartenenumeration und -auswahl

In jeder Hauptversion von Windows werden Schriftarten hinzugefügt, um internationale Sprachen und Skripts zu unterstützen. Informationen zu den Schriftarten, die seit Windows 2000 in jeder Windows-Version hinzugefügt wurden, sowie die unterstützten Skripts, Regionen und Sprachen finden Sie unter Skript- und Schriftartunterstützung [in Windows.](https://msdn.microsoft.com/globalization/mt791278)

## <a name="enumfontfamiliesex"></a>EnumFontFamiliesEx

Zum Aufzählen von internationalen Schriftarten in Ihrer Anwendung können Sie die [**EnumFontFamiliesEx-Funktion**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) verwenden. **Mit EnumFontFamiliesEx** können Sie Schriftarten basierend auf dem Namen der Schriftart und dem Zeichensatz aufzählen, indem Sie einen Zeiger auf eine [**LOGFONT-Struktur**](/windows/win32/api/wingdi/ns-wingdi-logfonta) übergeben, die den Schriftartnamen und Zeichensatzinformationen enthält. Zum Aufrufen **von EnumFontFamiliesEx** können Sie entweder einen Schriftartnamen oder ein Zeichensatz angeben oder nach dem verfügbaren Namen fragen. Wenn Sie den Schriftartnamen von **LOGFONT** auf **NULL** festlegen, werden alle Schriftartnamen aufzählt. Wenn Sie das Zeichensatzfeld **auf DEFAULT \_ CHARSET** festlegen, werden alle Zeichensets aufzählt.

Beachten Sie, dass Zeichensätze ein Legacybegriff sind, der Prä-Unicode-Zeichensätzen entspricht. Derzeit gibt es keinen Mechanismus zum Aufzählen von Schriftarten, die beliebige Skripts oder Zeichenbereiche in Unicode unterstützen. Die von [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85)) übergebene [**NEWTEXTMETRICEX-Struktur**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa) enthält die [**FONTSIGNATURE-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) die detailliertere Deklarationen enthält, die vom Schriftartentwickler bereitgestellt werden, um zu erfahren, welche Codepages und welche Unicode-Bereiche die Schriftart unterstützt. Um genauer zu bestimmen, welche Zeichenbereiche eine bestimmte Schriftart unterstützt, wählen Sie die Schriftart in einem Gerätekontext aus, und rufen [**Sie GetFontUnicodeRanges auf.**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges) Beachten Sie, dass diese API keine ergänzenden Unicode-Ebenen unterstützt.

## <a name="choosefont"></a>Wählen SieFont aus.

Sie können die [**Funktion ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) verwenden, um ein allgemeines Dialogfeld anzuzeigen, in dem der Benutzer internationale Schriftarten basierend auf dem Zeichensatz auswählen kann. Sie können eines von drei Flags angeben, um basierend auf charset festzulegen, welche Schriftarten im Dialogfeld ChooseFont angezeigt werden: **CF \_ SCRIPTSONLY**, **CF \_ SELECTSCRIPT** oder **CF \_ NOSCRIPTSEL**.

Das **CF \_ SCRIPTSONLY-Flag** weist die API an, Schriftarten für alle Zeichensätze auflisten, die nicht Symbol oder OEM sind.

Wenn Sie nur Schriftarten anzeigen möchten, die ein bestimmtes Zeichensatz abdecken, müssen Sie das **Flag CF \_ SELECTSCRIPT angeben.** Initialisieren Sie vor dem Aufruf von [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))das *lfCharSet-Feld* der [**LOGFONT-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-logfonta) Wenn Sie nur das Zeichensatz angeben möchten, legen Sie die anderen Felder der **LOGFONT-Struktur** auf **NULL fest.** Damit **ChooseFont die** **LOGFONT-Struktur** betrachten kann, müssen Sie auch das **CF \_ INITTOLOGFONTSTRUCT-Flag** angeben.

Schließlich können Sie wie bei jedem anderen Feld im Dialogfeld Schriftart auch ein leeres Skriptlistenfeld anzeigen. Diese Funktion ist nützlich, wenn der Benutzer mehrere verschiedene Schriftarten hervorgehoben hat, die sich über mehrere Zeichensets erstreckt. In diesem Fall würden Sie [**ChooseFont mit**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) dem **CF \_ NOSCRIPTSEL-Flag** aufrufen.

Ab Windows 7 implementiert [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) Unterstützung für das Ausblenden von Schriftarten in Schriftartauswahllisten. **Wählen SieFont** aus, um nur die angezeigten Schriftarten auflisten und die ausgeblendeten Schriftarten herausfiltern, während Schriftarten im Listenfeld angezeigt werden. Das zusätzliche Flag (**CF \_ INACTIVEFONTS**) im Flags-Member der [**ChooseFont-Struktur**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) wird hinzugefügt, damit Sie alle installierten Schriftarten in der Schriftartenliste anzeigen können, wie **sich ChooseFont** vor Windows 7 verhalten hat. Details zu Verhaltensunterschieden in Windows 7 für die **ChooseFont-Funktion** finden Sie unter [**ChooseFont() Win32 Common Dialog**](../win7appqual/choosefont-win32-common-dialog.md) im [Windows 7 Application Quality Cookbook](../win7appqual/windows-7-application-quality-cookbook.md). Informationen zu den Unterschieden bei der Endbenutzererfahrung finden Sie in der **ChooseFont-Funktion** und der **CHOOSEFONT-Struktur** in Windows 7.

Beachten Sie, dass Zeichensätze ein Legacybegriff sind, der Prä-Unicode-Zeichensätzen entspricht. Derzeit gibt es keinen Mechanismus zum Filtern von Schriftarten basierend auf Unicode-Skripts oder Zeichenbereichen.

## <a name="font-controls-in-windows-scenic-ribbon"></a>Schriftartsteuerelemente im Windows Menüband

Windows 7 führt das Windows Menüband ein, das eine Reihe von Steuerelementen für die Schriftartauswahl enthält. Diese Schriftartsteuerelemente unterstützen das neue Windows 7-Schriftarten-Hiding-Verhalten. Sie können diese Schriftartsteuerelemente verwenden, um nur angezeigte Schriftarten auflisten und dem Benutzer die Auswahl der Schriftart zu ermöglichen.

> [!Note]  
> Die Unterstützung für das Ausblenden von Schriftarten ist nicht verfügbar, wenn das menüband Windows-Menüband auf einer beliebigen Plattform vor Windows 7 ausgeführt wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**Wählen SieFont aus.**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**CHOOSEFONT-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Schriftartsteuerelemente im Windows Menüband**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**Allgemeines Dialogfeld "ChooseFont() Win32"**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
