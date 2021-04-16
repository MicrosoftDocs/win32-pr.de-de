---
description: In jeder Hauptversion von Windows gibt es Schriftarten, die zur Unterstützung internationaler Sprachen und Skripts hinzugefügt werden.
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: Internationale Schriftart Enumeration und-Auswahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e5d0d07a0953f72f097f8578f5e32b3ee49093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350278"
---
# <a name="international-font-enumeration-and-selection"></a>Internationale Schriftart Enumeration und-Auswahl

In jeder Hauptversion von Windows gibt es Schriftarten, die zur Unterstützung internationaler Sprachen und Skripts hinzugefügt werden. Verweisen Sie [in Windows auf Skript-und Schriftart Unterstützung in Windows](https://msdn.microsoft.com/globalization/mt791278) , um die Schriftarten zu unterstützen, die in jeder Windows-Version seit Windows 2000 hinzugefügt wurden, sowie die unterstützten Skripts, Regionen und Sprachen.

## <a name="enumfontfamiliesex"></a>Enumfontfamiliesex

Um internationale Schriftarten in Ihrer Anwendung aufzulisten, können Sie die [**enumfontfamiliesex**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) -Funktion verwenden. Mit **enumfontfamiliesex** können Sie Schriftarten auf der Grundlage des Schriftart namens und des Zeichensatzes auflisten, indem Sie einen Zeiger auf eine [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur übergeben, die den Schriftart Namen und die Informationen zum charset enthält. Um **enumfontfamiliesex** aufzurufen, können Sie entweder einen Schriftart Namen oder einen Zeichensatz angeben, oder Sie können nach dem verfügbaren Element Fragen. Wenn der Schriftart Name der **LOGFONT** auf **null** festgelegt wird, werden alle Schriftart Namen aufgelistet. Wenn Sie das CharSet-Feld auf **Default \_ CharSet** festlegen, werden alle Zeichensätze aufgezählt.

Beachten Sie, dass Zeichensätzen ein Legacy Konzept sind, das den Pre-Unicode-Zeichensätzen entspricht. Zurzeit gibt es keinen Mechanismus zum Auflisten von Schriftarten, die beliebige Skripts oder Zeichen Bereiche in Unicode unterstützen. Die [**newtextmetricex**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa) -Struktur, die von [**enumfontfamexproc**](/previous-versions//dd162618(v=vs.85)) übergeben wird, enthält die [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) -Struktur, die ausführlichere Deklarationen enthält, die der Schriftart Entwickler für die Codepages und die von der Schriftart unterstützten Unicode-Bereiche bereitstellt. Um genau zu bestimmen, welche Zeichen Bereiche eine bestimmte Schriftart unterstützt, wählen Sie die Schriftart in einen Gerätekontext aus, und nennen Sie [**getfontunicoderanges**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges). Beachten Sie, dass diese API keine zusätzlichen Unicode-Ebenen unterstützt.

## <a name="choosefont"></a>Auswahl Schriftart

Sie können die Funktion " [**choosefont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) " verwenden, um ein gemeinsames Dialogfeld anzuzeigen, in dem der Benutzer Internationale Schriftarten basierend auf dem charset auswählen kann. Sie können eines von drei Flags angeben, die basierend auf dem Charset festgelegt werden sollen, welche Schriftarten im Dialogfeld "Select-Font" angezeigt werden: **CF \_ ScriptsOnly**, **CF \_ selectScript** oder **CF \_ noscriptsel**.

Das Flag " **CF \_ ScriptsOnly** " weist die API an, Schriftarten für alle Zeichensätze aufzulisten, die kein Symbol oder OEM sind.

Wenn Sie nur Schriftarten anzeigen möchten, die ein bestimmtes Zeichensatz abdecken, müssen Sie das Flag **CF \_ selectScript** angeben. Initialisieren Sie vor dem Aufrufen von [**choosefont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))das *lfCharSet* -Feld der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur. Wenn Sie nur den Zeichensatz angeben möchten, legen Sie die anderen Felder der **LOGFONT** -Struktur auf **null** fest. Damit " **choosefont** " die **LOGFONT** -Struktur untersuchen kann, müssen Sie auch das **CF \_ inittologfontstruct** -Flag angeben.

Zum Schluss können Sie wie jedes andere Feld im Dialogfeld Schriftart auch ein leeres Skript-Listenfeld anzeigen. Diese Funktion ist nützlich, wenn der Benutzer mehrere verschiedene Schriftarten hervorgehoben hat, die mehrere Zeichensätze abdecken. In diesem Fall würden Sie " [**choosefont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) " mit dem Flag " **CF \_ noscriptsel** " aufzurufen.

Ab Windows 7 implementiert [**Choice Font**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) die Unterstützung für das Ausblenden von Schriftarten aus Schriftart Auswahllisten. **Auswahl Schriftart** listet nur die gezeigten Schriftarten auf und filtert die ausgeblendeten Schriftarten, während Schriftarten im Listenfeld angezeigt werden. Das zusätzliche Flag (**CF \_ inactivefonts**) im Flags-Member der [**choosefont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) -Struktur wird hinzugefügt, damit Sie alle installierten Schriftarten in der Schriftart Liste anzeigen können, und zwar so, als hätten Sie die **Schriftart** vor Windows 7 Verhalten. Ausführliche Informationen zu Verhaltens unterschieden in Windows 7 für die **choosefont** -Funktion finden Sie im [**Dialog Feld "Auswahl von Win32 () Win32 Common**](../win7appqual/choosefont-win32-common-dialog.md) " im [Windows 7-Cookbook zur Anwendungsqualität](../win7appqual/windows-7-application-quality-cookbook.md). Informationen zu den Unterschieden bei den Endbenutzern in Windows 7 finden Sie in der Auswahl der Funktionen " **choosetfont** " und " **Choice Font** "

Beachten Sie, dass Zeichensätzen ein Legacy Konzept sind, das den Pre-Unicode-Zeichensätzen entspricht. Zurzeit gibt es keinen Mechanismus zum Filtern von Schriftarten auf der Grundlage von Unicode-Skripts oder Zeichen Bereichen.

## <a name="font-controls-in-windows-scenic-ribbon"></a>Schriftart Steuerelemente in Windows Scenic Multifunktionsleiste

Windows 7 führt das Windows Scenic Menüband ein, das eine Reihe von Steuerelementen enthält, die auf die Schriftart Auswahl abzielen. Diese Schriftart Steuerelemente unterstützen das neue Schriftart Ausblenden von Windows 7. Sie können diese Schriftart Steuerelemente verwenden, um nur angezeigte Schriftarten aufzulisten und dem Benutzer die Auswahl der Schriftart zu ermöglichen.

> [!Note]  
> Die Unterstützung für das Ausblenden von Schriftarten ist nicht verfügbar, wenn das Windows Scenic-Menüband auf einer beliebigen Plattform vor Windows 7 ausgeführt wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Enumfontfamiliesex**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**Auswahl Schriftart**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**Chooonfont-Struktur**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Schriftart Steuerelemente in Windows Scenic Multifunktionsleiste**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**Ausgewählter Win32-Dialog Feld ()**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
