---
title: Umfangreiche Bearbeitungsfunktionen
description: Umfangreiche Bearbeitungsfunktionen
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1b74069b63220a07bfb1bd5e3f5a1ad99a6c6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482456"
---
# <a name="rich-edit-functions"></a>Umfangreiche Bearbeitungsfunktionen

## <a name="in-this-section"></a>In diesem Abschnitt




| Thema | BESCHREIBUNG | 
|-------|-------------|
| <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br /> | Die <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc-Funktion</em></a> ist eine anwendungsdefinierte Rückruffunktion, die mit der EM_SETAUTOCORRECTPROC <a href="em-setautocorrectproc.md"><strong>wird.</strong></a><br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a><br /> | Die <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback-Funktion</em></a> ist eine anwendungsdefinierte Rückruffunktion, die mit den EM_STREAMIN <a href="em-streamin.md"><strong>und</strong></a> EM_STREAMOUT <a href="em-streamout.md"><strong>wird.</strong></a> Es wird verwendet, um einen Datenstrom in ein oder aus einem Rich-Edit-Steuerelement zu übertragen. Der <strong>EDITSTREAMCALLBACK-Typ</strong> definiert einen Zeiger auf diese Rückruffunktion. <em>EditStreamCallback</em> ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen. <br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br /> | Die <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx-Funktion</em></a> ist eine anwendungsdefinierte Rückruffunktion, die mit der EM_SETWORDBREAKPROCEX <a href="em-setwordbreakprocex.md"><strong>wird.</strong></a> Er bestimmt den Zeichenindex der Wörterpause oder der Zeichenklasse sowie die Wörterbruchflags der Zeichen im angegebenen Text. Der <strong>EDITWORDBREAKPROCEX-Typ</strong> definiert einen Zeiger auf diese Rückruffunktion. <em>EditWordBreakProcEx</em> ist ein Platzhalter für den anwendungsdefinierten Funktionsnamen. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMath Alphaumeric</strong></a><br /> | Ruft das mathematische alphanumerische Zeichen UTF-32 (Unicode Transformation Format) ab, das dem angegebenen BMP-Zeichen (Basic Multilingual Plane) und mathematischem Stil entspricht. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMath AlphaumericCode</strong></a><br /> | Ruft den mathematischen Stil und den aufrechten BMP-Zeichencode (Basic Multilingual Plane) ab, der dem angegebenen nachenden Byte eines mathematischen Ersatzzeichenpaars entspricht.<br /> | 
| <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphnateProc</em></a><br /> | Die <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphnateProc-Funktion</em></a> ist eine anwendungsdefinierte Rückruffunktion, die mit der EM_SETHYPHENATEINFO <a href="em-sethyphenateinfo.md"><strong>wird.</strong></a> Sie bestimmt, wie Bindestriche in einem Microsoft Rich Edit-Steuerelement erfolgen.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br /> | Übersetzt die integrierten Mathematischen, Ruby- und anderen Inlineobjekte im angegebenen Bereich in lineare Form.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br /> | Konvertiert die Mathematik im linearen Format in einem Bereich in ein integriertes Formular oder ändert das aktuelle integrierte Formular. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br /> | Übersetzt die mathematischen Zeichen im angegebenen Bereich.<br /> | 
| <a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br /> | Registriert zwei Klassennamen, REListBox20W und RECombobox20W, die zum Erstellen von Rich Edit-Listen- oder Kombinationsfeldfenstern verwendet werden können. <br /><blockquote>[!Note]<br />Für die interne Verwendung vorgesehen; wird nicht für die Verwendung in Anwendungen empfohlen. Diese Funktion wird in zukünftigen Versionen möglicherweise nicht unterstützt.</blockquote><br /> | 




 

 

