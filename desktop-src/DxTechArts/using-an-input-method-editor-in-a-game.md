---
title: Verwenden eines Eingabemethoden-Editors in einem Spiel
description: In diesem Artikel wird erläutert, wie Sie ein einfaches IME-Bearbeitungssteuerelement in einer Microsoft DirectX-Vollbildanwendung implementieren können.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119c5933aae14e2d3e45085dafa241a4dcb11e1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118675"
---
# <a name="using-an-input-method-editor-in-a-game"></a>Verwenden eines Eingabemethoden-Editors in einem Spiel

> [!Note]  
> In diesem Artikel wird die Arbeit mit dem Eingabemethoden-Editor (INPUT Method Editor, IME) von Windows XP ausführlich beschrieben. Es wurden Änderungen am IME für Windows Vista vorgenommen, die in diesem Artikel nicht vollständig beschrieben werden. Weitere Informationen zu Änderungen am IME für Windows Vista finden Sie unter [Eingabemethoden-Editoren (INPUT Method Editors, IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista – Eine Ever-Expanding Ansicht der Internationalisierung](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) im globalen Entwicklungs- und Computingportal von Microsoft.

 

Ein Eingabemethoden-Editor (IME) ist ein Programm, das eine einfache Texteingabe mithilfe einer Standardtastatur für ostasiatische Sprachen wie Chinesisch, Japanisch, Koreanisch und andere Sprachen mit komplexen Zeichen ermöglicht. Beispielsweise kann ein Benutzer mit IMEs komplexe Zeichen in einer Textverarbeitung eingeben, oder ein Spieler eines umfangreichen Multiplayer-Onlinespiels kann mit Freunden in komplexen Zeichen chatten.

In diesem Artikel wird erläutert, wie Sie ein einfaches IME-Bearbeitungssteuerelement in einer Microsoft DirectX-Vollbildanwendung implementieren können. Anwendungen, die DXUT nutzen, erhalten automatisch IME-Funktionen. Für Anwendungen, die das Framework nicht verwenden, wird in diesem Artikel beschrieben, wie Sie einem Bearbeitungssteuerelement IME-Unterstützung hinzufügen.

Inhalte:

-   [Ime-Standardverhalten](#default-ime-behavior)
-   [Verwenden von IMEs mit DXUT](#using-imes-with-dxut)
-   [Überschreiben des STANDARD-IME-Verhaltens](#overriding-the-default-ime-behavior)
-   [Funktionen](#functions)
-   [Meldungen](#ime-messages)
-   [Beispiele](#examples)
    -   [CHT IME, Version 4.2, 4.3 und 4.4](#cht-ime-version-42-43-and-44)
    -   [CHT IME Version 5.0](#cht-ime-version-50)
    -   [CHT IME Version 5.1, 5.2 und CHS IME Version 5.3](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [CHS IME Version 4.1](#chs-ime-version-41)
    -   [CHS IME Version 4.2](#chs-ime-version-42)
-   [IME-Nachrichten](#ime-messages)
    -   [WM \_ INPUTLANGCHANGE](#wm_inputlangchange)
    -   [WM \_ IME \_ STARTCOMPOSITION](/windows)
    -   [WM \_ IME \_ COMPOSITION](/windows)
    -   [WM \_ IME \_ ENDCOMPOSITION](/windows)
    -   [WM \_ IME \_ NOTIFY](/windows)
-   [Darstellung](#rendering)
    -   [Eingabe-Gebietsschemaindikator](#input-locale-indicator)
    -   [Kompositionsfenster](#composition-window)
    -   [Lesen und Kandidatenfenster](#reading-and-candidate-windows)
-   [Einschränkungen](#limitations)
-   [Registrierungsinformationen](#registry-information)
-   [Anhang A: CHT-Versionen pro Betriebssystem](#appendix-a-cht-versions-per-operating-system)
-   [Weitere Informationen](#further-information)
-   [GetReadingString](#getreadingstring)
-   [ShowReadingWindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>Ime-Standardverhalten

IMEs ordnen Tastatureingaben phonetischen Komponenten oder anderen Sprachelementen zu, die für eine ausgewählte Sprache spezifisch sind. In einem typischen Szenario gibt der Benutzer Schlüssel ein, die die Aussprache eines komplexen Zeichens darstellen. Wenn die IME die Aussprache als gültig erkennt, wird dem Benutzer eine Liste von Wort- oder Ausdruckskandidaten angezeigt, aus der der Benutzer eine endgültige Auswahl treffen kann. Das ausgewählte Wort wird dann über eine Reihe von Microsoft Windows [**WM \_ CHAR-Nachrichten**](/windows/desktop/inputdev/wm-char) an die Anwendung gesendet. Da die IME auf einer Ebene unterhalb der Anwendung funktioniert, indem Tastatureingaben abgefangen werden, ist das Vorhandensein einer IME für die Anwendung transparent. Fast alle Windows-Anwendungen können IMEs problemlos nutzen, ohne sich ihrer Existenz bewusst zu sein und ohne dass eine spezielle Codierung erforderlich ist.

Eine typische IME zeigt mehrere Fenster an, um den Benutzer durch den Zeicheneintrag zu führen, wie in den folgenden Beispielen gezeigt.

![ime zeigt mehrere Fenster an.](images/ime-elements.png)

| Fenstertyp                                       | Beschreibung                                                                                                                                                                                                                                                                                                                 | IME-Ausgabe                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| A. Lesefenster                                 | Enthält Tastatureingaben von der Tastatur. ändert sich in der Regel nach jeder Tastatureingabe.                                                                                                                                                                                                                                              | Lesen einer Zeichenfolge                               |
| B. Kompositionsfenster                             | Enthält die Auflistung von Zeichen, die der Benutzer mit der IME zusammengesetzt hat. Diese Zeichen werden vom IME über der Anwendung gezeichnet. Wenn der Benutzer die IME benachrichtigt, dass die Kompositionszeichenfolge zufriedenstellend ist, sendet der IME die Kompositionszeichenfolge über eine Reihe von WM CHAR-Nachrichten an die \_ Anwendung. | Kompositionszeichenfolge                           |
| C. Kandidatenfenster                               | Wenn der Benutzer eine gültige Aussprache eingegeben hat, zeigt die IME eine Liste der Kandidatenzeichen an, die alle mit der angegebenen Aussprache übereinstimmen. Der Benutzer wählt dann das gewünschte Zeichen aus dieser Liste aus, und die IME fügt dieses Zeichen der Anzeige des Kompositionsfensters hinzu.                                                    | das nächste Zeichen in der Kompositionszeichenfolge |
| D: [Indikator für das Eingabeschema](/windows/desktop/Intl/nls-terminology) | Zeigt die Sprache an, die der Benutzer für die Tastatureingabe ausgewählt hat. Dieser Indikator ist in die Windows-Taskleiste eingebettet. Die Eingabesprache kann ausgewählt werden, indem Sie die Systemsteuerung Regionale optionen und Sprachoptionen öffnen und dann auf der Registerkarte Sprachen auf Details klicken.                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>Verwenden von IMEs mit DXUT

In DXUT implementiert die CDXUTIMEEditBox-Klasse IME-Funktionen. Diese Klasse wird von der CDXUTEditBox-Klasse abgeleitet, dem grundlegenden Bearbeitungssteuerelement, das vom Framework bereitgestellt wird. CDXUTIMEEditBox erweitert dieses Bearbeitungssteuerelement, um IMEs zu unterstützen, indem die CDXUTIMEEditBox-Methoden überschrieben werden. Die Klassen sind auf diese Weise konzipiert, damit Entwickler lernen können, was sie aus dem Framework nutzen müssen, um IME-Unterstützung in ihren eigenen Bearbeitungssteuerelementen zu implementieren. Im weiteren Verlauf dieses Themas wird erläutert, wie das Framework und insbesondere CDXUTIMEEditBox ein grundlegendes Bearbeitungssteuerelement überschreiben, um IME-Funktionen zu implementieren.

Die meisten IME-spezifischen Variablen in CDXUTIMEEditBox werden als statisch deklariert, da viele IME-Puffer und -Zustände für den Prozess spezifisch sind. Beispielsweise verfügt ein Prozess nur über einen Puffer für die Kompositionszeichenfolge. Selbst wenn der Prozess über zehn Bearbeitungssteuerelemente verfügt, verwenden sie alle denselben Kompositionszeichenfolgenpuffer. Der Kompositionszeichenfolgenpuffer für CDXUTIMEEditBox ist daher statisch und verhindert, dass die Anwendung unnötigen Speicherplatz einnimmt.

CDXUTIMEEditBox wird im folgenden DXUT-Code implementiert:

(SDK-Stamm) \\ Beispiele \\ für \\ C++ Common \\ DXUTgui.cpp

## <a name="overriding-the-default-ime-behavior"></a>Überschreiben des STANDARD-IME-Verhaltens

Normalerweise verwendet ein IME Standardmäßige Windows-Prozeduren, um ein Fenster zu erstellen (siehe [Verwenden von Windows](/windows/desktop/winmsg/using-windows)). Unter normalen Umständen führt dies zu zufriedenstellenden Ergebnissen. Wenn die Anwendung jedoch wie bei Spielen üblich im Vollbildmodus angezeigt wird, funktionieren Standardfenster nicht mehr und werden möglicherweise nicht über der Anwendung angezeigt. Um dieses Problem zu beheben, muss die Anwendung die IME-Fenster selbst zeichnen, anstatt sich auf Windows zu verlassen, um diese Aufgabe auszuführen.

Wenn das Standardmäßige ImE-Fenstererstellungsverhalten nicht bereitstellt, was eine Anwendung erfordert, kann die Anwendung die Ime-Fensterverarbeitung überschreiben. Eine Anwendung kann dies erreichen, indem sie IME-bezogene Nachrichten verarbeitet und die IMM-API [(Input Method Manager)](/windows/desktop/Intl/input-method-manager) aufruft.

Wenn ein Benutzer mit einer IME interagiert, um komplexe Zeichen einzugeben, sendet das IMM Nachrichten an die Anwendung, um sie über wichtige Ereignisse zu benachrichtigen, z. B. das Starten einer Komposition oder das Anzeigen des Kandidatenfensters. Eine Anwendung ignoriert diese Nachrichten in der Regel und übergibt sie an den Standardnachrichtenhandler, wodurch der IME sie verarbeitet. Wenn die Anwendung anstelle des Standardhandlers die Nachrichten verarbeitet, steuert sie genau, was bei den einzelnen IME-Ereignissen geschieht. Häufig ruft der Nachrichtenhandler den Inhalt der verschiedenen IME-Fenster ab, indem er die IMM-API aufruft. Sobald die Anwendung über diese Informationen verfügt, kann sie die IME-Fenster selbst ordnungsgemäß zeichnen, wenn sie auf der Anzeige gerendert werden muss.

## <a name="functions"></a>Functions

Eine IME muss die Lesezeichenfolge abrufen, das Lesefenster ausblenden und die Ausrichtung des Lesefensters abrufen. Diese Tabelle zeigt die Funktionen pro IME-Version:



|                    | Abrufen von Lesezeichenfolgen                                                | Ausblenden des Lesefensters                       | Ausrichtung des Lesefensters                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| **Vor Version 6.0** | A. Direktes Lesen des Fensterzugriffs auf private IME-Daten. Siehe "4-Struktur" | Fangen Sie private IME-Nachrichten ab. Siehe "3 Nachrichten" | Untersuchen Sie die Registrierungsinformationen. Weitere Informationen finden Sie unter "5 Registrierungsinformationen". |
| **Nach Version 6.0**  | [GetReadingString](#getreadingstring)                                 | [ShowReadingWindow](#showreadingwindow)     | [GetReadingString](#getreadingstring)                      |



 

## <a name="messages"></a>Meldungen

Die folgenden Meldungen müssen nicht für neuere IME verarbeitet werden, die [ShowReadingWindow ()](#showreadingwindow)implementiert.

Die folgenden Meldungen werden vom Anwendungsmeldungshandler abgefangen (d. h. sie werden nicht an DefWindowProc übergeben), um zu verhindern, dass das Lesefenster angezeigt wird.

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>Beispiele

Die folgenden Beispiele veranschaulichen, wie Zeichenfolgeninformationen aus einer älteren IME gelesen werden, die nicht über GetReadingString() verfügen. Der Code generiert die folgenden Ausgaben:



| Output              | BESCHREIBUNG                                                                                      |
|--------------|---------------------------------------------------------------------------------------|
| DWORD dwlen  | Länge der Lesezeichenfolge.                                                          |
| DWORD dwerr  | Index des Fehlerzeichens.                                                                   |
| LPWSTR wstr  | Zeiger auf die Lesezeichenfolge.                                                         |
| BOOL-Unicode | True gibt an, dass die Lesezeichenfolge im Unicode-Format vor liegt. Andernfalls liegt das Multibyteformat vor. |



 

### <a name="cht-ime-version-42-43-and-44"></a>CHT IME Version 4.2, 4.3 und 4.4

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a>CHT IME Version 5.0

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a>CHT IME Version 5.1, 5.2 und CHS IME Version 5.3

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a>CHS IME Version 4.1

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a>CHS IME Version 4.2

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a>IME-Nachrichten

Eine Vollbildanwendung muss die folgenden IME-bezogenen Nachrichten ordnungsgemäß verarbeiten:

### <a name="wm_inputlangchange"></a>WM \_ INPUTLANGCHANGE

Der IMM sendet eine WM INPUTLANGCHANGE-Nachricht an das aktive Fenster einer Anwendung, nachdem das Eingabe-Locale vom Benutzer mit einer Tastenkombination (in der Regel ALT+UMSCHALT) oder mit dem Eingabe-Locale-Indikator auf der Taskleiste oder Sprachleiste geändert \_ wurde. Die Sprachleiste ist ein Steuerelement auf dem Bildschirm, mit dem der Benutzer einen Textdienst konfigurieren kann. (Weitere Informationen [finden Sie unter Anzeigen der Sprachleiste.)](/windows/desktop/TSF/how-to-set-up-tsf) Der folgende Screenshot zeigt eine Sprachauswahlliste, die angezeigt wird, wenn der Benutzer auf den Indikator für das Locale klickt.

![Sprachauswahlliste, die angezeigt wird, wenn der Benutzer auf den Locale Indicator klickt](images/ime-langselection.png)

Wenn der IMM eine WM \_ INPUTLANGCHANGE-Nachricht sendet, muss CDXUTIMEEditBox mehrere wichtige Aufgaben ausführen:

1.  Die GetKeyboardLayout-Methode wird aufgerufen, um den Eingabe-Locale Identifier (ID) für den Anwendungsthread zurück zu geben. Die CDXUTIMEEditBox-Klasse speichert diese ID zur späteren Verwendung in der statischen \_ Membervariablen "hklCurrent". Es ist wichtig, dass die Anwendung das aktuelle Eingabe-Locale kennt, da der IME für jede Sprache über ein eigenes eigenes Verhalten verfügt. Der Entwickler muss möglicherweise anderen Code für verschiedene Eingabe-Locales bereitstellen.
2.  CDXUTIMEEditBox initialisiert eine Zeichenfolge, die im Sprachindikator des Bearbeitungsfelds angezeigt werden soll. Dieser Indikator kann die aktive Eingabesprache anzeigen, wenn die Anwendung im Vollbildmodus ausgeführt wird und weder die Taskleiste noch die Sprachleiste sichtbar sind.
3.  Die ImmGetConversionStatus-Methode wird aufgerufen, um anzugeben, ob sich das Eingabe-Locale im nativen oder nicht nativen Konvertierungsmodus befindet. Im nativen Konvertierungsmodus kann der Benutzer Text in der ausgewählten Sprache eingeben. Im nicht nativen Konvertierungsmodus wird die Tastatur als standardmäßige englische Tastatur verwendet. Es ist wichtig, dem Benutzer einen visuellen Hinweis zu geben, in welchem Konvertierungsmodus sich der IME befindet, damit der Benutzer leicht erkennen kann, welche Zeichen beim Drücken eines Schlüssels zu erwarten sind. CDXUTIMEEditBox stellt diesen visuellen Hinweis mit einer Sprachindikatorfarbe zur Verfügung. Wenn das Eingabeschema einen IME mit nativem Konvertierungsmodus verwendet, zeichnet die CDXUTIMEEditBox-Klasse den Indikatortext mit der Farbe, die durch den Parameter m \_ IndicatorImeColor definiert wird. Wenn sich der IME im nicht nativen Konvertierungsmodus befindet oder überhaupt kein IME verwendet wird, zeichnet die Klasse den Indikatortext mit der Farbe, die durch den Parameter m \_ IndicatorEngColor definiert wird.
4.  CDXUTIMEEditBox überprüft das Eingabe-Locale und legt die statische Membervariable bInsertOnType auf TRUE für Koreanisch und FALSE für alle \_ anderen Sprachen fest. Dieses Flag ist aufgrund der unterschiedlichen Verhaltensweisen von koreanischen IMEs und allen anderen IMEs erforderlich. Wenn Sie Zeichen in anderen Sprachen als Koreanisch eingeben, wird der vom Benutzer eingegebene Text im Kompositionsfenster angezeigt, und der Benutzer kann den Inhalt der Kompositionszeichenfolge frei ändern. Der Benutzer drückt die EINGABETASTE, wenn er mit der Kompositionszeichenfolge zufrieden ist, und die Kompositionszeichenfolge wird als Eine Reihe von WM CHAR-Nachrichten an die \_ Anwendung gesendet. Wenn ein Benutzer in koreanischen IMEs jedoch eine Taste zum Eingeben von Text drückt, wird sofort ein Zeichen an die Anwendung gesendet. Wenn der Benutzer anschließend weitere Tasten drückt, um dieses Anfangszeichen zu ändern, ändert sich das Zeichen im Bearbeitungsfeld, um zusätzliche Eingaben des Benutzers widerzudrücken. Im Wesentlichen besteht der Benutzer im Verfassen von Zeichen im Bearbeitungsfeld. Diese beiden Verhaltensweisen sind so unterschiedlich, dass CDXUTIMEEditBox für jedes dieser Verhalten speziell codiert werden muss.
5.  Die statische Membermethode SetupImeApi wird aufgerufen, um Adressen von zwei Funktionen aus dem IME-Modul abzurufen: GetReadingString und ShowReadingWindow. Wenn diese Funktionen vorhanden sind, wird ShowReadingWindow aufgerufen, um das Standardlesefenster für diesen IME auszublenden. Da die Anwendung das Lesefenster selbst rendert, benachrichtigt sie den IME, das Zeichnen des Standardlesefensters zu deaktivieren, damit es das Rendering im Vollbildmodus nicht beeinträchtigt.

Der IMM sendet eine WM \_ IME \_ SETCONTEXT-Nachricht, wenn ein Fenster der Anwendung aktiviert wird. Der lParam-Parameter dieser Meldung enthält ein Flag, das dem IME angibt, welche Fenster gezeichnet werden sollen und welche nicht. Da die Anwendung die ganze Zeichnung übernimmt, benötigt sie den IME nicht, um eines der IME-Fenster zu zeichnen. Daher legt der Meldungshandler der Anwendung einfach lParam auf 0 fest und gibt zurück.

Damit Anwendungen IME unterstützen können, ist eine spezielle Verarbeitung für die IME-bezogene Nachricht WM \_ IME \_ SETCONTEXT erforderlich. Da Windows diese Nachricht in der Regel vor dem Aufruf der PanoramaInitialize()-Methode an die Anwendung sendet, hat Panorama keine Möglichkeit, die Benutzeroberfläche zum Anzeigen von Kandidatenlistenfenstern zu verarbeiten.

Der folgende Codeausschnitt gibt windows-Anwendungen an, dass keine dem Kandidatenlistenfenster zugeordnete Benutzeroberfläche angezeigt wird, sodass Panorama diese Benutzeroberfläche speziell verarbeiten kann.

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>WM \_ IME \_ STARTCOMPOSITION

Der IMM sendet eine WM \_ IME STARTCOMPOSITION-Nachricht an die Anwendung, wenn eine IME-Komposition als Folge von Tastatureingaben durch den Benutzer \_ beginnt. Wenn der IME das Kompositionsfenster verwendet, wird die aktuelle Kompositionszeichenfolge in einem Kompositionsfenster angezeigt. CDXUTIMEEditBox verarbeitet diese Nachricht durch Ausführen von zwei Aufgaben:

1.  CDXUTIMEEditBox entfernt den Kompositionszeichenfolgenpuffer und den Attributpuffer. Diese Puffer sind statische Member von CDXUTIMEEditBox.
2.  CDXUTIMEEditBox legt die \_ statische Membervariable bHideCaret auf TRUE fest. Dieser Member, der in der CDXUTEditBox-Basisklasse definiert ist, steuert, ob der Cursor im Bearbeitungsfeld gezeichnet werden soll, wenn das Bearbeitungsfeld gerendert wird. Das Kompositionsfenster funktioniert ähnlich wie ein Bearbeitungsfeld mit Text und Cursor. Um Verwirrung zu vermeiden, wenn das Kompositionsfenster sichtbar ist, blendet das Bearbeitungsfeld seinen Cursor aus, sodass immer nur ein Cursor gleichzeitig sichtbar ist.

### <a name="wm_ime_composition"></a>WM \_ IME \_ COMPOSITION

Der IMM sendet eine WM IME COMPOSITION-Nachricht an die Anwendung, wenn der Benutzer eine Tastatureingabe eingibt, \_ \_ um die Kompositionszeichenfolge zu ändern. Der Wert von lParam gibt an, welche Art von Informationen die Anwendung aus dem Eingabemethode-Manager (Input Method Manager, IMM) abrufen kann. Die Anwendung sollte die verfügbaren Informationen abrufen, indem [**sie ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) aufruft, und dann die Informationen in ihrem privaten Puffer speichern, damit sie die IME-Elemente später rendern kann.

CDXUTIMEEditBox überprüft die folgenden Kompositionszeichenfolgendaten und ruft sie ab:



| [**WM \_ IME \_ COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam-Flagwert | Daten                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_GCS-KOMPATIBILITÄTS-TR                                                         | Composition-Attribut          | Dieses Attribut enthält Informationen wie den Status der einzelnen Zeichen in der Kompositionszeichenfolge (z. B. konvertiert oder nicht konvertiert). Diese Informationen sind erforderlich, da CDXUTIMEEditBox die Kompositionszeichenfolgenzeichen je nach ihren Attributen unterschiedlich färbt.                                                                                   |
| GCS \_ COMPCLAUSE                                                       | Informationen zur Composition-Klausel | Diese Klauselinformationen werden verwendet, wenn der japanische IME aktiv ist. Wenn eine japanische Kompositionszeichenfolge konvertiert wird, können Zeichen als Eine-Klausel, die in eine einzelne Entität konvertiert wird, zusammengekettet werden. Wenn der Benutzer den Cursor verschiebt, verwendet CDXUTIMEEditBox diese Informationen, um die gesamte -Klausel anstelle eines einzelnen Zeichens innerhalb der -Klausel hervorzuheben. |
| GCS \_ COMPSTR                                                          | Kompositionszeichenfolge             | Diese Zeichenfolge ist die aktuelle Zeichenfolge, die vom Benutzer zusammengesetzt wird. Dies ist auch die Zeichenfolge, die im Kompositionsfenster angezeigt wird.                                                                                                                                                                                                                                        |
| GCS \_ CURSORPOS                                                        | Position des Kompositionscursors    | Das Kompositionsfenster implementiert einen Cursor, ähnlich wie der Cursor in einem Bearbeitungsfeld. Die Anwendung kann die Cursorposition beim Verarbeiten der WM \_ IME \_ COMPOSITION-Nachricht abrufen, um den Cursor ordnungsgemäß zu zeichnen.                                                                                                                                            |
| GCS \_ RESULTSTR                                                        | Ergebniszeichenfolge                  | Die Ergebniszeichenfolge ist verfügbar, wenn der Benutzer den Kompositionsprozess abschließen möchte. Diese Zeichenfolge sollte abgerufen und die Zeichen an das Bearbeitungsfeld gesendet werden.                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>WM \_ IME \_ ENDCOMPOSITION

Das IMM sendet eine \_ WM-IME-ENDCOMPOSITION-Nachricht \_ an die Anwendung, wenn der IME-Kompositionsvorgang beendet wird. Dies kann auftreten, wenn der Benutzer die EINGABETASTE drückt, um die Kompositionszeichenfolge zu genehmigen, oder die ESC-Taste, um die Komposition abzubrechen. CDXUTIMEEditBox verarbeitet diese Nachricht, indem der Kompositionszeichenfolgenpuffer auf leer festgelegt wird. Anschließend wird \_ s bHideCaret auf FALSE festgelegt, da das Kompositionsfenster geschlossen ist und der Cursor im Bearbeitungsfeld wieder sichtbar sein sollte.

Der CDXUTIMEEditBox-Meldungshandler legt auch \_ s bShowReadingWindow auf FALSE fest. Dieses Flag steuert, ob die Klasse das Lesefenster zeichnet, wenn das Bearbeitungsfeld selbst gerendert wird. Daher muss es auf FALSE festgelegt werden, wenn eine Komposition endet.

### <a name="wm_ime_notify"></a>WM \_ IME \_ NOTIFY

Das IMM sendet eine WM \_ IME \_ NOTIFY-Nachricht an die Anwendung, wenn sich ein IME-Fenster ändert. Eine Anwendung, die das Zeichnen der IME-Fenster verarbeitet, sollte diese Meldung verarbeiten, damit sie über alle Aktualisierungen des Fensterinhalts informiert ist. Das wParam gibt den Befehl oder die Änderung an, die stattfindet. CDXUTIMEEditBox verarbeitet die folgenden Befehle:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>IME-Befehl</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></td>
<td>Dieses Attribut enthält Informationen wie den Status jedes Zeichens in der Kompositionszeichenfolge (z. B. konvertiert oder nicht konvertiert). Diese Informationen sind erforderlich, da CDXUTIMEEditBox die Kompositionszeichenfolgenzeichen basierend auf ihren Attributen unterschiedlich einfärbt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></td>
<td>Wird an die Anwendung gesendet, wenn das Kandidatenfenster geöffnet oder aktualisiert werden soll. Das Kandidatenfenster wird geöffnet, wenn ein Benutzer die konvertierte Textauswahl ändern möchte. Das Fenster wird aktualisiert, wenn ein Benutzer den Auswahlindikator verschiebt oder die Seite ändert. CDXUTIMEEditBox verwendet einen Meldungshandler für beide Befehle, da die erforderlichen Aufgaben identisch sind:<br/>
<ol>
<li>CDXUTIMEEditBox legt das bShowWindow-Element der Kandidatenlistenstruktur s_CandList auf TRUE fest, um anzugeben, dass das Kandidatenfenster während des Framerenderings gezeichnet werden muss.</li>
<li>CDXUTIMEEditBox ruft die Kandidatenliste ab, indem <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>aufgerufen wird, um zuerst die erforderliche Puffergröße abzurufen, und dann erneut, um die tatsächlichen Daten abzurufen.</li>
<li>Die Private Candidate List-Struktur s_CandList wird mit den abgerufenen Kandidatendaten initialisiert.</li>
<li>Die Kandidatenzeichenfolgen werden als Array von Zeichenfolgen gespeichert.</li>
<li>Der Index des ausgewählten Eintrags sowie der Seitenindex wird gespeichert.</li>
<li>CDXUTIMEEditBox überprüft, ob der Stil des Kandidatenfensters vertikal oder horizontal ist. Wenn der Fensterstil horizontal ist, muss ein zusätzlicher Zeichenfolgenpuffer, der HoriCand-Member von s_CandList, mit allen Kandidatenzeichenfolgen initialisiert werden, wobei Zwischenraumzeichen zwischen allen benachbarten Zeichenfolgen eingefügt werden. Beim Rendern eines vertikalen Kandidatenfensters werden die einzelnen Kandidatenzeichenfolgen einzeln gezeichnet, wobei die y-Koordinaten für jede Zeichenfolge inkrementiert werden. Diese HoriCand-Zeichenfolge sollte jedoch beim Rendern eines horizontalen Kandidatenfensters verwendet werden, da das Leerzeichen die beste Möglichkeit ist, zwei angrenzende Zeichenfolgen in derselben Zeile zu trennen.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></td>
<td>Wird an die Anwendung gesendet, wenn ein Kandidatenfenster geschlossen wird. Dies geschieht, wenn ein Benutzer eine Auswahl aus der Kandidatenliste getroffen hat. CDXUTIMEEditBox verarbeitet diesen Befehl, indem das sichtbare Flag des Kandidatenfensters auf FALSE festgelegt wird und dann der Kandidatenzeichenfolgenpuffer löscht wird.</td>
</tr>
<tr class="even">
<td>IMN_PRIVATE</td>
<td>Wird an die Anwendung gesendet, wenn die IME ihre Lesezeichenfolge aktualisiert hat, weil der Benutzer Zeichen ein- oder entfernt hat. Die Anwendung sollte die Lesezeichenfolge abrufen und zum Rendern speichern. CDXUTIMEEditBox verfügt über zwei Methoden zum Abrufen der Lesezeichenfolge, basierend darauf, wie Lesezeichenfolgen in der IME unterstützt werden: <br/>
<ul>
<li>Wenn die IME die GetReadingString-Funktion unterstützt, wird GetReadingString aufgerufen, um die Lesezeichenfolge abzurufen.</li>
<li>Wenn die IME GetReadingString nicht implementiert, ruft CDXUTIMEEditBox die Lesezeichenfolge aus dem Inhalt des Eingabekontexts ab.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a>Darstellung

Das Rendern der IME-Elemente und -Fenster ist einfach. MIT CDXUTIMEEditBox kann die Basisklasse zuerst gerendert werden, da IME-Fenster über dem Bearbeitungssteuerelement angezeigt werden sollen. Nachdem das Basisbearbeitungsfeld gerendert wurde, überprüft CDXUTIMEEditBox das Sichtbarkeitsflag jedes IME-Fensters (Indikator, Komposition, Kandidat und Lesefenster) und zeichnet das Fenster, wenn es sichtbar sein soll. Beschreibungen der verschiedenen IME-Fenstertypen finden Sie unter Standard-IME-Verhalten.

### <a name="input-locale-indicator"></a>Eingabe-Gebietsschemaindikator

Der Eingabe-Gebietsschemaindikator wird vor allen anderen IME-Fenstern gerendert, da es sich um ein Element handelt, das immer angezeigt wird. Sie sollte daher unter anderen IME-Fenstern angezeigt werden. CDXUTIMEEditBox rendert den Indikator durch Aufrufen der RenderIndicator-Methode, bei der die Schriftfarbe des Indikators durch Untersuchen der \_ statischen ImeState-Variable bestimmt wird, die den aktuellen IME-Konvertierungsmodus widerspiegelt. Wenn die IME aktiviert ist und die native Konvertierung aktiv ist, verwendet die Methode m \_ IndicatorImeColor als Indikatorfarbe. Wenn die IME deaktiviert ist oder sich im nicht einheitlichen Konvertierungsmodus befindet, wird m \_ IndicatorImeColor verwendet, um den Indikatortext zu zeichnen. Standardmäßig wird das Indikatorfenster selbst rechts neben dem Bearbeitungsfeld gezeichnet. Anwendungen können dieses Verhalten ändern, indem sie die RenderIndicator-Methode überschreiben.

Die folgende Abbildung zeigt die verschiedenen Darstellungen eines Eingabeschemaindikators für Englisch, Japanisch im alphanumerischen Konvertierungsmodus und Japanisch im einheitlichen Konvertierungsmodus:

![unterschiedliche Darstellungen eines Eingabeschemaindikators für Englisch und Japanisch](images/ime-indicator.png)

### <a name="composition-window"></a>Kompositionsfenster

Das Zeichnen des Kompositionsfensters wird in der RenderComposition-Methode von CDXUTIMEEditBox behandelt. Das Kompositionsfenster gleitet über dem Bearbeitungsfeld. Sie sollte an der Cursorposition des zugrunde liegenden Bearbeitungssteuerelements gezeichnet werden. CDXUTIMEEditBox verarbeitet das Rendering wie folgt:

1.  Die gesamte Kompositionszeichenfolge wird mit den Standardfarben der Kompositionszeichenfolge gezeichnet.
2.  Zeichen mit bestimmten speziellen Attributen sollten in unterschiedlichen Farben gezeichnet werden, sodass CDXUTIMEEditBox die Zeichen der Kompositionszeichenfolge überprüft und das Zeichenfolgenattribut überprüft. Wenn das Attribut unterschiedliche Farben aufruft, wird das Zeichen mit den entsprechenden Farben erneut gezeichnet.
3.  Der Cursor des Kompositionsfensters wird gezeichnet, um das Rendering abzuschließen.

Der Cursor sollte für koreanische IMEs blinken, aber nicht für andere IMEs. RenderComposition bestimmt, ob der Cursor basierend auf Timerwerten sichtbar sein soll, wenn die koreanische IME verwendet wird.

### <a name="reading-and-candidate-windows"></a>Lesen und Kandidatenfenster

Die Lese- und Kandidatenfenster werden von der gleichen CDXUTIMEEditBox-Methode gerendert, RenderCandidateReadingWindow. Beide Fenster enthalten ein Array von Zeichenfolgen für das vertikale Layout oder eine einzelne Zeichenfolge im Fall eines horizontalen Layouts. Der Großteil des Codes in RenderCandidateReadingWindow wird verwendet, um das Fenster so zu positionieren, dass kein Teil des Fensters außerhalb des Anwendungsfensters liegt und abgeschnitten wird.

## <a name="limitations"></a>Einschränkungen

IMEs enthalten manchmal erweiterte Features, um die Einfache Eingabe von Text zu verbessern. Einige der Features in neueren IMEs sind in den folgenden Abbildungen dargestellt. Diese erweiterten Features sind in DXUT nicht vorhanden. Die Implementierung der Unterstützung für diese erweiterten Features kann schwierig sein, da keine Schnittstelle definiert ist, um die erforderlichen Informationen von den IMEs abzurufen.

Erweitertes traditionelles chinesisches IME mit erweiterter Kandidatenliste:

![erweitertes traditionelles Chinesisch mit erweiterter Kandidatenliste](images/ime-advanced1.png)

Erweiterte japanische IME mit einigen Kandidateneinträgen, die zusätzlichen Text enthalten, um ihre Bedeutungen zu beschreiben:

![advanced japanese ime with some candidate entries that contain additional text to describe their meanings (Erweiterte japanische Sprache mit einigen Kandidateneinträgen, die zusätzlichen Text enthalten, um ihre Bedeutungen zu beschreiben)](images/ime-advanced2.png)

Erweiterte koreanische IME, die ein Handschrifterkennungssystem enthält:

![erweiterter koreanischer Ime, der ein Handschrifterkennungssystem enthält](images/ime-advanced3.png)

## <a name="registry-information"></a>Registrierungsinformationen

Die folgenden Registrierungsinformationen werden überprüft, um die Ausrichtung des Lesefensters zu bestimmen, wenn die aktuelle IME eine ältere CHT New Phonetic-Version ist, die GetReadingString() nicht implementiert.



| Key                                                           | Wert            |
|---------------------------------------------------------------|------------------|
| HKCU \\ software \\ microsoft \\ windows \\ currentversion \\ IME \_ Name | Tastaturzuordnung |



 

Where: IME \_ Name is MSTCIPH if the IME file version is 5.1 or later; andernfalls IME Name is MSTCIPH if the IME file version is 5.1 or later; andernfalls \_ IME Name is TINTLGNT.

Die Ausrichtung des Lesefensters ist horizontal, wenn einer der folgenden Istwerte zu sehen ist:

-   Der IME ist Version 5.0, und der Wert für die Tastaturzuordnung 0x22 oder 0x23
-   Der IME ist Version 5.1 oder Version 5.2, und der Wert für die Tastaturzuordnung ist 0x22, 0x23 oder 0x24.

Wenn keine der Bedingungen erfüllt ist, ist das Lesefenster vertikal.

## <a name="appendix-a-cht-versions-per-operating-system"></a>Anhang A: CHT-Versionen pro Betriebssystem



| Operating System (Betriebssystem)           | CHT IME-Version |
|----------------------------|-----------------|
| Windows 98                 | 4,2             |
| Windows 2000               | 4.3             |
| unknown                    | 4.4             |
| Windows ME                 | 5.0             |
| Office XP                  | 5,1             |
| Windows XP                 | 5,2             |
| Eigenständige Webdownloads | 6.0             |



 

## <a name="further-information"></a>Weitere Informationen

Zusätzliche Informationen finden Sie unter:

-   [Installieren und Verwenden von Eingabemethoden-Editoren](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [Internationale Textanzeige](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [Das Unicode-Konsortium](https://www.unicode.org/)
-   Entwickeln von internationaler Software. Dr. International. 2. ed. Redmond, WA: Microsoft Press, 2003.

## <a name="getreadingstring"></a>GetReadingString

Ruft das Lesen von Zeichenfolgeninformationen ab.

**Parameter**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[im \] Eingabekontext.

</dd> <dt>

<span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*
</dt> <dd>

\[in \] Length of lpwReadingBuf, in WCHAR. Wenn der Wert 0 (null) ist, bedeutet dies, dass die Länge des Abfragelesepuffers gilt.

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf* 
</dt> <dd>

\[out \] Gibt eine Lesezeichenfolge zurück (kein Ende).

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex* 
</dt> <dd>

\[out \] Gibt den Index des Fehlerzeichens in der Lesezeichenfolge zurück, falls dies der Fehler ist.

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical* 
</dt> <dd>

\[out \] Wenn true ist, ist das Lesen der Benutzeroberfläche vertikal. Andernfalls horizontal puMaxReadingLen.

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen* 
</dt> <dd>

\[out \] Die Länge der Lesebenutzeroberfläche. Die maximale Leselänge ist nicht festgelegt. Sie hängt nicht nur vom Tastaturlayout ab, sondern auch vom Eingabemodus (z. B. interner Code, Ersatzeingabe).

</dd> </dl>

**Rückgabewerte**

Die Länge der Lesezeichenfolge.

**Anmerkungen**

Wenn der Rückgabewert größer als der Wert von uReadingBufLen ist, sind alle Ausgabeparameter nicht definiert.

Diese Funktion ist in CHT IME 6.0 oder höher implementiert und kann von GetProcAddress auf einem IME-Modulhandle erworben werden. Das IME-Modulhandle kann von ImmGetIMEFileName und LoadLibrary erworben werden.

**Anforderungen**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**
</dt> <dd>

Deklariert in Imm.h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Bibliothek importieren**
</dt> <dd>

Verwenden Sie Imm.lib.

</dd> </dl>

## <a name="showreadingwindow"></a>ShowReadingWindow

Blendet das Lesefenster ein (oder blendet es aus).

**Parameter**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[im \] Eingabekontext.

</dd> <dt>

<span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow* 
</dt> <dd>

\[in \] Auf TRUE festlegen, um das Lesefenster anzuzeigen (oder FALSE, um es auszublenden).

</dd> </dl>

**Rückgabewerte**

**Anmerkungen**

Gibt TRUE zurück, wenn erfolgreich, andernfalls FALSE.

**Anforderungen**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**
</dt> <dd>

Deklariert in Imm.h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Bibliothek importieren**
</dt> <dd>

Verwenden Sie Imm.lib.

</dd> </dl>