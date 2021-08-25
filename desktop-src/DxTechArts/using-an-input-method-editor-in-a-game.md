---
title: Verwenden eines Eingabemethode-Editors in einem Spiel
description: In diesem Artikel wird erläutert, wie Sie ein einfaches IME-Bearbeitungssteuer steuerelement in einer Microsoft DirectX-Vollbildanwendung implementieren können.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8cb5869579da97aeea465b572082a23a963e9db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471966"
---
# <a name="using-an-input-method-editor-in-a-game"></a>Verwenden eines Eingabemethode-Editors in einem Spiel

> [!Note]  
> In diesem Artikel wird die Arbeit mit dem Windows XP Input Method Editor (IME) beschrieben. Es wurden Änderungen am IME für Windows Vista vorgenommen, die in diesem Artikel nicht vollständig beschrieben werden. Weitere Informationen zu Änderungen am IME für Windows Vista finden Sie unter Input Method Editors (IME) in Windows Vista – An Ever-Expanding View of Internationalization on the Microsoft Global Development and Computing Portal (Eingabemethode-Editoren (IME) in [Windows Vista – An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) on the Microsoft Global Development and Computing Portal(In diesem Artikel finden Sie unter Input Method [Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in Ever-Expanding Vista).

 

Ein Eingabemethode-Editor (ImE) ist ein Programm, das eine einfache Texteingabe mithilfe einer Standardtastatur für ostasiatische Sprachen wie Chinesisch, Japanisch, Koreanisch und andere Sprachen mit komplexen Zeichen ermöglicht. Mit IMEs kann ein Benutzer beispielsweise komplexe Zeichen in einem Textprozessor eingeben, oder ein Spieler eines großen Multiplayer-Onlinespiels kann mit Freunden in komplexen Zeichen chatten.

In diesem Artikel wird erläutert, wie Sie ein einfaches IME-Bearbeitungssteuer steuerelement in einer Microsoft DirectX-Vollbildanwendung implementieren können. Anwendungen, die DXUT nutzen, erhalten automatisch IME-Funktionen. Für Anwendungen, die das Framework nicht verwenden, wird in diesem Artikel beschrieben, wie Sie einem Bearbeitungssteuersteuer steuerelement IME-Unterstützung hinzufügen.

Inhalte:

-   [Standardmäßiges IME-Verhalten](#default-ime-behavior)
-   [Verwenden von IMEs mit DXUT](#using-imes-with-dxut)
-   [Überschreiben des Standardmäßigen IME-Verhaltens](#overriding-the-default-ime-behavior)
-   [Funktionen](#functions)
-   [Meldungen](#ime-messages)
-   [Beispiele](#examples)
    -   [CHT IME Version 4.2, 4.3 und 4.4](#cht-ime-version-42-43-and-44)
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
    -   [Eingabe locale Indicator](#input-locale-indicator)
    -   [Kompositionsfenster](#composition-window)
    -   [Lese- und Windows](#reading-and-candidate-windows)
-   [Einschränkungen](#limitations)
-   [Registrierungsinformationen](#registry-information)
-   [Anhang A: CHT-Versionen pro Betriebssystem](#appendix-a-cht-versions-per-operating-system)
-   [Weitere Informationen](#further-information)
-   [GetReadingString](#getreadingstring)
-   [ShowReadingWindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>Standardmäßiges IME-Verhalten

IMEs ordnen Tastatureingaben phonetischen Komponenten oder anderen Sprachelementen zu, die für eine ausgewählte Sprache spezifisch sind. In einem typischen Szenario gibt der Benutzer Schlüssel ein, die die Aussprache eines komplexen Zeichens darstellen. Wenn der IME die Aussprache als gültig erkennt, wird dem Benutzer eine Liste von Wort- oder Ausdruckskandidaten angezeigt, aus denen der Benutzer eine endgültige Auswahl treffen kann. Das ausgewählte Wort wird dann über eine Reihe von Microsoft Windows [**WM \_ CHAR-Nachrichten**](/windows/desktop/inputdev/wm-char) an die Anwendung gesendet. Da der IME auf einer Ebene unterhalb der Anwendung funktioniert, indem Tastatureingaben abgefangen werden, ist das Vorhandensein eines IME für die Anwendung transparent. Fast alle Windows anwendungen können IMEs problemlos nutzen, ohne sich ihrer Existenz bewusst zu sein und ohne dass eine spezielle Codierung erforderlich ist.

Ein typischer IME zeigt mehrere Fenster an, um den Benutzer durch den Zeicheneintrag zu führen, wie in den folgenden Beispielen gezeigt.

![ime zeigt mehrere Fenster an](images/ime-elements.png)

| Fenstertyp                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                 | IME-Ausgabe                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| A. Lesefenster                                 | Enthält Tastatureingaben. ändert sich in der Regel nach jeder Tastatureingabe.                                                                                                                                                                                                                                              | Lesen der Zeichenfolge                               |
| B. Kompositionsfenster                             | Enthält die Auflistung von Zeichen, die der Benutzer mit dem IME zusammengesetzt hat. Diese Zeichen werden vom IME am Anfang der Anwendung gezeichnet. Wenn der Benutzer den IME benachrichtigt, dass die Kompositionszeichenfolge zufriedenstellend ist, sendet der IME die Kompositionszeichenfolge dann über eine Reihe von WM CHAR-Nachrichten an die \_ Anwendung. | Kompositionszeichenfolge                           |
| C. Kandidatenfenster                               | Wenn der Benutzer eine gültige Aussprache eingegeben hat, zeigt der IME eine Liste von Kandidatenzeichen an, die alle mit der angegebenen Aussprache übereinstimmen. Der Benutzer wählt dann das beabsichtigte Zeichen aus dieser Liste aus, und der IME fügt dieses Zeichen der Kompositionsfensteranzeige hinzu.                                                    | Das nächste Zeichen in der Kompositionszeichenfolge |
| D: [Eingabe locale indicator (Eingabe locale](/windows/desktop/Intl/nls-terminology) indicator) | Zeigt die Sprache an, die der Benutzer für die Tastatureingabe ausgewählt hat. Dieser Indikator ist in die Taskleiste Windows eingebettet. Die Eingabesprache kann ausgewählt werden, indem Sie die Optionen "Regional" und "Language" Systemsteuerung klicken und dann auf der Registerkarte Sprachen auf Details klicken.                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>Verwenden von IMEs mit DXUT

In DXUT implementiert die CDXUTIMEEditBox-Klasse IME-Funktionen. Diese Klasse wird von der CDXUTEditBox-Klasse abgeleitet, dem grundlegenden Bearbeitungssteuerfeld, das vom Framework bereitgestellt wird. CDXUTIMEEditBox erweitert dieses Bearbeitungssteuerfeld, um IMEs zu unterstützen, indem die CDXUTIMEEditBox-Methoden überschrieben werden. Die Klassen sind so konzipiert, dass Entwickler lernen können, was sie aus dem Framework benötigen, um IME-Unterstützung in ihren eigenen Bearbeitungssteuerelementen zu implementieren. Im restlichen Teil dieses Themas wird erläutert, wie das Framework und insbesondere CDXUTIMEEditBox ein einfaches Bearbeitungssteuerfeld überschreibt, um IME-Funktionen zu implementieren.

Die meisten IME-spezifischen Variablen in CDXUTIMEEditBox werden als statisch deklariert, da viele IME-Puffer und -Zustände für den Prozess spezifisch sind. Beispielsweise verfügt ein Prozess nur über einen Puffer für die Kompositionszeichenfolge. Auch wenn der Prozess über zehn Bearbeitungssteuerelemente verfügt, verwenden sie alle denselben Kompositionszeichenfolgenpuffer. Der Kompositionszeichenfolgenpuffer für CDXUTIMEEditBox ist daher statisch und verhindert, dass die Anwendung unnötigen Speicherplatz benötigt.

CDXUTIMEEditBox wird im folgenden DXUT-Code implementiert:

(SDK-Stamm) \\ Beispiele \\ für C++ \\ Common \\ DXUTgui.cpp

## <a name="overriding-the-default-ime-behavior"></a>Überschreiben des Standardmäßigen IME-Verhaltens

Normalerweise verwendet ein IME Windows Standard-Prozeduren, um ein Fenster zu erstellen (siehe [Verwenden Windows](/windows/desktop/winmsg/using-windows)). Unter normalen Umständen führt dies zu zufriedenstellenden Ergebnissen. Wenn die Anwendung jedoch im Vollbildmodus dargestellt wird, wie es bei Spielen üblich ist, funktionieren Standardfenster nicht mehr und werden möglicherweise nicht mehr über der Anwendung angezeigt. Um dieses Problem zu beheben, muss die Anwendung die IME-Fenster selbst zeichnen, anstatt sich auf Windows zu verlassen, um diese Aufgabe auszuführen.

Wenn das standardmäßige ImE-Fenstererstellungsverhalten nicht die für eine Anwendung benötigten Informationen bietet, kann die Anwendung die ImE-Fensterbehandlung überschreiben. Eine Anwendung kann dies erreichen, indem sie IME-bezogene Nachrichten verarbeitet und die IMM-API [(Input Method Manager)](/windows/desktop/Intl/input-method-manager) aufruft.

Wenn ein Benutzer mit einem IME interagiert, um komplexe Zeichen eineingaben zu können, sendet der IMM Nachrichten an die Anwendung, um sie über wichtige Ereignisse zu benachrichtigen, z. B. das Starten einer Komposition oder das Anzeigen des Kandidatenfensters. Eine Anwendung ignoriert diese Nachrichten in der Regel und übergibt sie an den Standardnachrichtenhandler, wodurch der IME sie behandelt. Wenn die Anwendung anstelle des Standardhandlers die Nachrichten verarbeitet, steuert sie genau, was bei jedem DER IME-Ereignisse geschieht. Häufig ruft der Meldungshandler den Inhalt der verschiedenen IME-Fenster ab, indem er die IMM-API aufruft. Sobald die Anwendung über diese Informationen verfügt, kann sie die IME-Fenster selbst ordnungsgemäß zeichnen, wenn sie auf der Anzeige gerendert werden muss.

## <a name="functions"></a>Functions

Ein IME muss die Lesezeichenfolge erhalten, das Lesefenster ausblenden und die Ausrichtung des Lesefensters erhalten. In dieser Tabelle sind die Funktionen pro IME-Version aufgeführt:



|                    | Abrufen der Lesezeichenfolge                                                | Ausblenden des Lesefensters                       | Ausrichtung des Lesefensters                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| **Vor Version 6.0** | A. Direktes Lesen von privaten IME-Daten im Fensterzugriff. Siehe "4-Struktur" | Fangen Sie private IME-Nachrichten ab. Siehe "3 Nachrichten" | Überprüfen Sie die Registrierungsinformationen. Siehe "5 Registrierungsinformationen" |
| **Nach Version 6.0**  | [GetReadingString](#getreadingstring)                                 | [ShowReadingWindow](#showreadingwindow)     | [GetReadingString](#getreadingstring)                      |



 

## <a name="messages"></a>Meldungen

Die folgenden Meldungen müssen nicht für neuere IME verarbeitet werden, die [ShowReadingWindow](#showreadingwindow)() implementiert.

Die folgenden Nachrichten werden vom Anwendungsnachrichtenhandler eingeschlossen (d. h. sie werden nicht an DefWindowProc übergeben), um zu verhindern, dass das Lesefenster angezeigt wird.

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>Beispiele

Die folgenden Beispiele veranschaulichen das Lesen von Zeichenfolgeninformationen aus einer älteren IME ohne GetReadingString(). Der Code generiert die folgenden Ausgaben:



| Output              | BESCHREIBUNG                                                                                      |
|--------------|---------------------------------------------------------------------------------------|
| DWORD dwlen  | Länge der Lesezeichenfolge.                                                          |
| DWORD dwerr  | Index des Fehlerzeichens.                                                                   |
| LPWSTR wstr  | Zeiger auf die Lesezeichenfolge.                                                         |
| BOOL unicode | True gibt an, dass die Lesezeichenfolge im Unicode-Format vorliegt. Andernfalls liegt das Multibyteformat vor. |



 

### <a name="cht-ime-version-42-43-and-44"></a>CHT IME, Version 4.2, 4.3 und 4.4

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

Das IMM sendet eine WM \_ INPUTLANGCHANGE-Nachricht an das aktive Fenster einer Anwendung, nachdem das Eingabegebietsschema vom Benutzer mit einer Tastenkombination (normalerweise ALT+UMSCHALT) oder mit dem Eingabegebietsschemaindikator auf der Taskleiste oder Sprachleiste geändert wurde. Die Sprachleiste ist ein Bildschirmsteuerelement, mit dem der Benutzer einen Textdienst konfigurieren kann. (Weitere Informationen finden Sie [unter Anzeigen der Sprachleiste.)](/windows/desktop/TSF/how-to-set-up-tsf) Der folgende Screenshot zeigt eine Sprachauswahlliste, die angezeigt wird, wenn der Benutzer auf den Gebietsschemaindikator klickt.

![Sprachauswahlliste, die angezeigt wird, wenn der Benutzer auf den Gebietsschemaindikator klickt](images/ime-langselection.png)

Wenn das IMM eine WM \_ INPUTLANGCHANGE-Nachricht sendet, muss CDXUTIMEEditBox mehrere wichtige Aufgaben ausführen:

1.  Die GetKeyboardLayout-Methode wird aufgerufen, um den Eingabegebietsschemabezeichner (ID) für den Anwendungsthread zurückzugeben. Die CDXUTIMEEditBox-Klasse speichert diese ID zur späteren Verwendung in der statischen Membervariablen \_ s hklCurrent. Es ist wichtig, dass die Anwendung das aktuelle Eingabegebietsschema kennt, da die IME für jede Sprache ein eigenes verhalten hat. Der Entwickler muss möglicherweise unterschiedliche Code für verschiedene Eingabeschemas bereitstellen.
2.  CDXUTIMEEditBox initialisiert eine Zeichenfolge, die im Sprachindikator des Bearbeitungsfelds angezeigt werden soll. Dieser Indikator kann die aktive Eingabesprache anzeigen, wenn die Anwendung im Vollbildmodus ausgeführt wird und weder die Taskleiste noch die Sprachleiste sichtbar ist.
3.  Die ImmGetConversionStatus-Methode wird aufgerufen, um anzugeben, ob sich das Eingabeschema im nativen oder nicht nativen Konvertierungsmodus befindet. Im einheitlichen Konvertierungsmodus kann der Benutzer Text in der ausgewählten Sprache eingeben. Der nicht native Konvertierungsmodus bewirkt, dass die Tastatur als englische Standardtastatur fungiert. Es ist wichtig, dem Benutzer einen visuellen Hinweis darauf zu geben, in welchem Typ des Konvertierungsmodus sich der IME befindet, damit der Benutzer leicht erkennen kann, welche Zeichen beim Drücken eines Schlüssels zu erwarten sind. CDXUTIMEEditBox stellt diesen visuellen Hinweis mit einer Sprachindikatorfarbe bereit. Wenn das Eingabeschema eine IME mit nativem Konvertierungsmodus verwendet, zeichnet die CDXUTIMEEditBox-Klasse den Indikatortext mit der farbe, die durch den Parameter m \_ IndicatorImeColor definiert wird. Wenn sich die IME im nicht nativen Konvertierungsmodus befindet oder überhaupt keine IME verwendet wird, zeichnet die Klasse den Indikatortext mit der farbe, die durch den Parameter m \_ IndicatorEngColor definiert wird.
4.  CDXUTIMEEditBox überprüft das Eingabeschema und legt die statische Membervariable s \_ bInsertOnType für Koreanisch auf TRUE und für alle anderen Sprachen auf FALSE fest. Dieses Flag ist aufgrund der unterschiedlichen Verhaltensweisen koreanischer IMEs und aller anderen IMEs erforderlich. Bei der Eingabe von Zeichen in anderen Sprachen als Koreanisch wird der vom Benutzer eingegebene Text im Kompositionsfenster angezeigt, und der Benutzer kann den Inhalt der Kompositionszeichenfolge frei ändern. Der Benutzer drückt die EINGABETASTE, wenn er mit der Kompositionszeichenfolge zufrieden ist, und die Kompositionszeichenfolge wird als Reihe von WM CHAR-Nachrichten an die Anwendung \_ gesendet. Wenn ein Benutzer in koreanischen IMEs jedoch eine Taste drückt, um Text einzugeben, wird sofort ein Zeichen an die Anwendung gesendet. Wenn der Benutzer anschließend weitere Tasten drückt, um dieses Anfangszeichen zu ändern, ändert sich das Zeichen im Bearbeitungsfeld, um zusätzliche Eingaben des Benutzers widerzuspiegeln. Im Wesentlichen setzt der Benutzer Zeichen in das Bearbeitungsfeld. Diese beiden Verhaltensweisen sind so unterschiedlich, dass CDXUTIMEEditBox für jedes dieser Verhalten spezifisch codieren muss.
5.  Die statische Membermethode SetupImeApi wird aufgerufen, um Adressen von zwei Funktionen aus dem IME-Modul abzurufen: GetReadingString und ShowReadingWindow. Wenn diese Funktionen vorhanden sind, wird ShowReadingWindow aufgerufen, um das Standardlesefenster für diese IME auszublenden. Da die Anwendung das Lesefenster selbst rendert, benachrichtigt sie das IME, das Zeichnen des Standardlesefensters zu deaktivieren, damit das Vollbildrendering nicht beeinträchtigt wird.

Das IMM sendet eine WM \_ IME \_ SETCONTEXT-Nachricht, wenn ein Fenster der Anwendung aktiviert wird. Der lParam-Parameter dieser Meldung enthält ein Flag, das dem IME angibt, welche Fenster gezeichnet werden sollen und welche nicht. Da die Anwendung die gesamte Zeichnung verarbeitet, benötigt sie das IME nicht, um eines der IME-Fenster zu zeichnen. Daher legt der Nachrichtenhandler der Anwendung einfach lParam auf 0 fest und gibt zurück.

Damit Anwendungen IME unterstützen, ist eine spezielle Verarbeitung für die IME-bezogene Meldung WM \_ IME \_ SETCONTEXT erforderlich. Da Windows diese Nachricht in der Regel an die Anwendung sendet, bevor die PanoramaInitialize()-Methode aufgerufen wird, hat Panorama keine Möglichkeit, die Benutzeroberfläche für die Anzeige von Fenstern der Kandidatenliste zu verarbeiten.

Der folgende Codeausschnitt gibt an, dass Windows Anwendungen keine dem Kandidatenlistenfenster zugeordnete Benutzeroberfläche anzeigen sollen, sodass Panorama diese Benutzeroberfläche speziell behandeln kann.

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>WM \_ IME \_ STARTCOMPOSITION

Das IMM sendet eine WM \_ IME \_ STARTCOMPOSITION-Nachricht an die Anwendung, wenn eine IME-Komposition aufgrund von Tastatureingaben durch den Benutzer beginnen soll. Wenn die IME das Kompositionsfenster verwendet, wird die aktuelle Kompositionszeichenfolge in einem Kompositionsfenster angezeigt. CDXUTIMEEditBox verarbeitet diese Nachricht, indem zwei Aufgaben ausgeführt werden:

1.  CDXUTIMEEditBox löscht den Kompositionszeichenfolgenpuffer und den Attributpuffer. Diese Puffer sind statische Member von CDXUTIMEEditBox.
2.  CDXUTIMEEditBox legt die \_ statische Membervariable s bHideCaret auf TRUE fest. Dieser Member, der in der CDXUTEditBox-Basisklasse definiert ist, steuert, ob der Cursor im Bearbeitungsfeld gezeichnet werden soll, wenn das Bearbeitungsfeld gerendert wird. Das Kompositionsfenster funktioniert ähnlich wie ein Bearbeitungsfeld mit Text und Cursor. Um Verwirrung zu vermeiden, wenn das Kompositionsfenster sichtbar ist, blendet das Bearbeitungsfeld seinen Cursor aus, sodass jeweils nur ein Cursor sichtbar ist.

### <a name="wm_ime_composition"></a>WM \_ IME \_ COMPOSITION

Das IMM sendet eine WM \_ IME \_ COMPOSITION-Nachricht an die Anwendung, wenn der Benutzer eine Tastatureingabe eingibt, um die Kompositionszeichenfolge zu ändern. Der Wert von lParam gibt an, welche Art von Informationen die Anwendung aus dem Eingabemethoden-Manager (Input Method Manager, IMM) abrufen kann. Die Anwendung sollte die verfügbaren Informationen durch Aufrufen von [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) abrufen und die Informationen dann in ihrem privaten Puffer speichern, damit sie die IME-Elemente später rendern kann.

CDXUTIMEEditBox überprüft die folgenden Kompositionszeichenfolgendaten und ruft sie ab:



| [**WM \_ IME \_ COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) lParam-Flagwert | Daten                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GCS \_ COMPATTR                                                         | Kompositionsattribut          | Dieses Attribut enthält Informationen wie den Status jedes Zeichens in der Kompositionszeichenfolge (z. B. konvertiert oder nicht konvertiert). Diese Informationen sind erforderlich, da CDXUTIMEEditBox die Kompositionszeichenfolgenzeichen basierend auf ihren Attributen unterschiedlich einfärbt.                                                                                   |
| GCS \_ COMPCLAUSE                                                       | Informationen zur Kompositionsklausel | Diese Klauselinformationen werden verwendet, wenn die japanische IME aktiv ist. Wenn eine japanische Kompositionszeichenfolge konvertiert wird, können Zeichen als Klausel gruppiert werden, die in eine einzelne Entität konvertiert wird. Wenn der Benutzer den Cursor bewegt, verwendet CDXUTIMEEditBox diese Informationen, um die gesamte Klausel hervorzuheben, anstatt nur ein einzelnes Zeichen in der -Klausel zu markieren. |
| GCS \_ COMPSTR                                                          | Kompositionszeichenfolge             | Diese Zeichenfolge ist die aktuelle Zeichenfolge, die vom Benutzer zusammengesetzt wird. Dies ist auch die Zeichenfolge, die im Kompositionsfenster angezeigt wird.                                                                                                                                                                                                                                        |
| GCS \_ CURSORPOS                                                        | Position des Kompositionscursors    | Das Kompositionsfenster implementiert einen Cursor, der dem Cursor in einem Bearbeitungsfeld ähnelt. Die Anwendung kann die Cursorposition abrufen, wenn die WM IME COMPOSITION-Meldung verarbeitet \_ \_ wird, um den Cursor ordnungsgemäß zu zeichnen.                                                                                                                                            |
| GCS \_ RESULTSTR                                                        | Ergebniszeichenfolge                  | Die Ergebniszeichenfolge ist verfügbar, wenn der Benutzer den Kompositionsprozess abschließen wird. Diese Zeichenfolge sollte abgerufen werden, und die Zeichen sollten an das Bearbeitungsfeld gesendet werden.                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>WM \_ IME \_ ENDCOMPOSITION

Der IMM sendet eine WM IME ENDCOMPOSITION-Nachricht an die Anwendung, \_ \_ wenn der IME-Kompositionsvorgang beendet wird. Dies kann auftreten, wenn der Benutzer die EINGABETASTE drückt, um die Kompositionszeichenfolge zu genehmigen, oder die ESC-Taste, um die Komposition abzubricht. CDXUTIMEEditBox verarbeitet diese Nachricht, indem der Kompositionszeichenfolgenpuffer auf leer festgelegt wird. Anschließend wird bHideCaret auf FALSE festgelegt, da das Kompositionsfenster geschlossen ist und der Cursor im Bearbeitungsfeld \_ wieder sichtbar sein sollte.

Der CDXUTIMEEditBox-Meldungshandler legt auch \_ bShowReadingWindow auf FALSE fest. Dieses Flag steuert, ob die Klasse das Lesefenster zeichnet, wenn sich das Bearbeitungsfeld selbst rendert. Daher muss es beim Ende einer Komposition auf FALSE festgelegt werden.

### <a name="wm_ime_notify"></a>WM \_ IME \_ NOTIFY

Der IMM sendet eine WM \_ IME NOTIFY-Nachricht an die Anwendung, wenn \_ sich ein IME-Fenster ändert. Eine Anwendung, die das Zeichnen der IME-Fenster verarbeitet, sollte diese Meldung verarbeiten, damit sie über alle Aktualisierungen des Fensterinhalts weiß. wParam gibt den Befehl oder die Änderung an, die ausgeführt wird. CDXUTIMEEditBox verarbeitet die folgenden Befehle:




| IME-Befehl | BESCHREIBUNG | 
|-------------|-------------|
| <a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a> | Dieses Attribut enthält Informationen wie den Status der einzelnen Zeichen in der Kompositionszeichenfolge (z. B. konvertiert oder nicht konvertiert). Diese Informationen sind erforderlich, da CDXUTIMEEditBox die Kompositionszeichenfolgenzeichen je nach ihren Attributen unterschiedlich färbt. | 
| <a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a> | Wird an die Anwendung gesendet, wenn das Kandidatenfenster geöffnet oder aktualisiert werden soll. Das Kandidatenfenster wird geöffnet, wenn ein Benutzer die konvertierte Textauswahl ändern möchte. Das Fenster wird aktualisiert, wenn ein Benutzer den Auswahlindikator verschiebt oder die Seite ändert. CDXUTIMEEditBox verwendet für beide Befehle einen Meldungshandler, da die erforderlichen Aufgaben identisch sind:<br /><ol><li>CDXUTIMEEditBox legt das bShowWindow-Mitglied der Kandidatenlistenstruktur s_CandList auf TRUE fest, um anzugeben, dass das Kandidatenfenster während des Framerenderings gezeichnet werden muss.</li><li>CDXUTIMEEditBox ruft die Kandidatenliste ab, indem <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>aufgerufen wird, um zuerst die erforderliche Puffergröße abzurufen, und dann erneut, um die tatsächlichen Daten abzurufen.</li><li>Die private Kandidatenlistenstruktur, s_CandList mit den abgerufenen Kandidatendaten initialisiert wird.</li><li>Die Kandidatenzeichenfolgen werden als Array von Zeichenfolgen gespeichert.</li><li>Der Index des ausgewählten Eintrags sowie der Seitenindex werden gespeichert.</li><li>CDXUTIMEEditBox überprüft, ob der Kandidatenfensterstil vertikal oder horizontal ist. Wenn der Fensterstil horizontal ist, muss ein zusätzlicher Zeichenfolgenpuffer, das HoriCand-Member von s_CandList, mit allen Kandidatenzeichenfolgen initialisiert werden, bei dem Leerzeichen zwischen allen angrenzenden Zeichenfolgen eingefügt werden. Beim Rendern eines vertikalen Kandidatenfensters werden die einzelnen Kandidatenzeichenfolgen einzeln gezeichnet, und die y-Koordinaten werden für jede Zeichenfolge erhöht. Diese HoriCand-Zeichenfolge sollte jedoch beim Rendern eines horizontalen Kandidatenfensters verwendet werden, da das Leerzeichen die beste Möglichkeit ist, zwei angrenzende Zeichenfolgen in derselben Zeile zu trennen.</li></ol> | 
| <a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a> | Wird an die Anwendung gesendet, wenn ein Kandidatenfenster geschlossen wird. Dies geschieht, wenn ein Benutzer eine Auswahl aus der Kandidatenliste getroffen hat. CDXUTIMEEditBox verarbeitet diesen Befehl, indem das sichtbare Flag des Kandidatenfensters auf FALSE festgelegt und dann der Puffer der Kandidatenzeichenfolge entfernt wird. | 
| IMN_PRIVATE | Wird an die Anwendung gesendet, wenn der IME seine Lesezeichenfolge aktualisiert hat, weil der Benutzer Zeichen eingibt oder entfernt. Die Anwendung sollte die Lesezeichenfolge abrufen und zum Rendern speichern. CDXUTIMEEditBox verfügt über zwei Methoden zum Abrufen der Lesezeichenfolge, je nachdem, wie das Lesen von Zeichenfolgen im IME unterstützt wird: <br /><ul><li>Wenn der IME die GetReadingString-Funktion unterstützt, wird GetReadingString aufgerufen, um die Lesezeichenfolge abzurufen.</li><li>Wenn der IME GetReadingString nicht implementiert, ruft CDXUTIMEEditBox die Lesezeichenfolge aus dem Eingabekontextinhalt ab.</li></ul> | 




 

## <a name="rendering"></a>Darstellung

Das Rendern der IME-Elemente und -Fenster ist einfach. MIT CDXUTIMEEditBox kann die Basisklasse zuerst gerendert werden, da IME-Fenster über dem Bearbeitungssteuerfeld angezeigt werden sollen. Nachdem das Basisbearbeitungsfeld gerendert wurde, überprüft CDXUTIMEEditBox das Sichtbarkeitsflag jedes IME-Fensters (Indikator, Komposition, Kandidat und Lesefenster) und zeichnet das Fenster, wenn es sichtbar sein sollte. Beschreibungen der verschiedenen IME-Fenstertypen finden Sie unter Standard-IME-Verhalten.

### <a name="input-locale-indicator"></a>Eingabe locale Indicator

Der Eingabe-Locale Indicator wird vor allen anderen IME-Fenstern gerendert, da es sich um ein Element handelt, das immer angezeigt wird. Sie sollte daher unter anderen IME-Fenstern angezeigt werden. CDXUTIMEEditBox rendert den Indikator durch Aufrufen der RenderIndicator-Methode, in der die Schriftfarbe des Indikators bestimmt wird, indem die statische ImeState-Variable untersucht wird, die den aktuellen IME-Konvertierungsmodus \_ widerspiegelt. Wenn der IME aktiviert ist und die systemeigene Konvertierung aktiv ist, verwendet die Methode m \_ IndicatorImeColor als Indikatorfarbe. Wenn der IME deaktiviert ist oder sich im nicht nativen Konvertierungsmodus befindet, wird m \_ IndicatorImeColor verwendet, um den Indikatortext zu zeichnen. Standardmäßig wird das Indikatorfenster selbst rechts vom Bearbeitungsfeld gezeichnet. Anwendungen können dieses Verhalten ändern, indem sie die RenderIndicator-Methode überschreiben.

Die folgende Abbildung zeigt die verschiedenen Darstellungen eines Eingabe-Locale-Indikators für Englisch, Japanisch im alphanumerischen Konvertierungsmodus und Japanisch im nativen Konvertierungsmodus:

![Verschiedene Darstellungen eines Eingabe-Locale-Indikators für Englisch und Japanisch](images/ime-indicator.png)

### <a name="composition-window"></a>Kompositionsfenster

Das Zeichnen des Kompositionsfensters wird in der RenderComposition-Methode von CDXUTIMEEditBox behandelt. Das Kompositionsfenster wird über dem Bearbeitungsfeld angezeigt. Sie sollte an der Cursorposition des zugrunde liegenden Bearbeitungssteuer steuerelements gezeichnet werden. CDXUTIMEEditBox verarbeitet das Rendering wie folgt:

1.  Die gesamte Kompositionszeichenfolge wird mithilfe der standardkompositionszeichenfolgenfarben gezeichnet.
2.  Zeichen mit bestimmten speziellen Attributen sollten in unterschiedlichen Farben gezeichnet werden, sodass CDXUTIMEEditBox die Zeichen der Kompositionszeichenfolge überprüft und das Zeichenfolgenattribut überprüft. Wenn das Attribut unterschiedliche Farben erfordert, wird das Zeichen erneut mit den entsprechenden Farben gezeichnet.
3.  Der Cursor des Kompositionsfensters wird gezeichnet, um das Rendering zu vervollständigen.

Der Cursor sollte für koreanische IMEs blinken, aber nicht für andere IMEs. RenderComposition bestimmt anhand von Timerwerten, ob der Cursor sichtbar sein soll, wenn der koreanische IME verwendet wird.

### <a name="reading-and-candidate-windows"></a>Lese- und Windows

Die Lese- und Kandidatenfenster werden von derselben CDXUTIMEEditBox-Methode gerendert, RenderCandidateReadingWindow. Beide Fenster enthalten ein Array von Zeichenfolgen für das vertikale Layout oder eine einzelne Zeichenfolge im Fall eines horizontalen Layouts. Der Großteil des Codes in RenderCandidateReadingWindow wird verwendet, um das Fenster so zu positionieren, dass kein Teil des Fensters außerhalb des Anwendungsfensters liegt und abgeschnitten wird.

## <a name="limitations"></a>Einschränkungen

IMEs enthalten manchmal erweiterte Features, um die Eingabe von Text zu verbessern. Einige der Features in neueren IMEs sind in den folgenden Abbildungen dargestellt. Diese erweiterten Features sind in DXUT nicht vorhanden. Die Implementierung der Unterstützung für diese erweiterten Features kann eine Herausforderung darstellen, da keine Schnittstelle definiert ist, um die erforderlichen Informationen von den IMEs zu erhalten.

Erweiterte traditionelle chinesische IME mit erweiterter Kandidatenliste:

![erweiterte traditionelle chinesische Ime mit erweiterter Kandidatenliste](images/ime-advanced1.png)

Erweiterte japanische IME mit einigen Kandidateneinträgen, die zusätzlichen Text enthalten, um ihre Bedeutung zu beschreiben:

![erweiterte japanische Ime mit einigen Kandidateneinträgen, die zusätzlichen Text enthalten, um ihre Bedeutung zu beschreiben](images/ime-advanced2.png)

Erweitertes koreanisches IME, das ein Handschrifterkennungssystem enthält:

![erweitertes koreanisches Ime, das ein Handschrifterkennungssystem enthält](images/ime-advanced3.png)

## <a name="registry-information"></a>Registrierungsinformationen

Die folgenden Registrierungsinformationen werden überprüft, um die Ausrichtung des Lesefensters zu bestimmen, wenn der aktuelle IME älter als CHT New Phonetic ist, der GetReadingString() nicht implementiert.



| Schlüssel                                                           | Wert            |
|---------------------------------------------------------------|------------------|
| HKCU \\ software \\ microsoft \\ windows \\ currentversion \\ IME \_ Name | Tastaturzuordnung |



 

Where: IME \_ Name is MSTCIPH if the IME file version is 5.1 or later; andernfalls IME \_ Name is TINTLGNT.

Die Ausrichtung des Lesefensters ist horizontal, wenn eine der beiden ist:

-   Der IME ist Version 5.0, und der Tastaturzuordnungswert ist 0x22 oder 0x23
-   Der IME ist Version 5.1 oder Version 5.2, und der Tastaturzuordnungswert ist 0x22, 0x23 oder 0x24.

Wenn keine der Bedingungen erfüllt ist, ist das Lesefenster vertikal.

## <a name="appendix-a-cht-versions-per-operating-system"></a>Anhang A: CHT-Versionen pro Betriebssystem



| Betriebssystem           | CHT IME-Version |
|----------------------------|-----------------|
| Windows 98                 | 4,2             |
| Windows 2000               | 4.3             |
| Unbekannt                    | 4.4             |
| Windows ICH                 | 5.0             |
| Office XP                  | 5.1             |
| Windows XP                 | 5,2             |
| Eigenständiges Webdownload | 6.0             |



 

## <a name="further-information"></a>Weitere Informationen

Zusätzliche Informationen finden Sie unter:

-   [Installieren und Verwenden von Eingabemethoden-Editoren](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [Internationale Textanzeige](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [Das Unicode-Konsortium](https://www.unicode.org/)
-   Entwickeln von internationalem Software. Dr. International. 2nd ed. Redmond, WA: Microsoft Press, 2003.

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

\[in \] Length of lpwReadingBuf, in WCHAR. Wenn er 0 (null) ist, bedeutet dies, dass die Länge des Abfragelesepuffers gelesen wird.

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf* 
</dt> <dd>

\[out \] Gibt eine Lesezeichenfolge zurück (kein Ende 0).

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex* 
</dt> <dd>

\[out \] Gibt den Index des Fehlerzeichens in der Lesezeichenfolge zurück, falls vorhanden.

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical* 
</dt> <dd>

\[out Wenn true ist, ist das Lesen der \] Benutzeroberfläche vertikal. Andernfalls horizontal puMaxReadingLen.

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen* 
</dt> <dd>

\[out \] Die Länge der Lese-UI. Die maximale Leselänge ist nicht festgelegt. Es hängt nicht nur vom Tastaturlayout ab, sondern auch vom Eingabemodus (z. B. interner Code, Ersatzzeicheneingabe).

</dd> </dl>

**Rückgabewerte**

Die Länge der Lesezeichenfolge.

**Anmerkungen**

Wenn der Rückgabewert größer als der Wert von uReadingBufLen ist, sind alle Ausgabeparameter nicht definiert.

Diese Funktion wird in CHT IME 6.0 oder höher implementiert und kann von GetProcAddress auf einem IME-Modulhandle bezogen werden. Das IME-Modulhandle kann von ImmGetIMEFileName und LoadLibrary bezogen werden.

**Anforderungen**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**
</dt> <dd>

Deklariert in Imm.h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Importieren der Bibliothek**
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

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Importieren der Bibliothek**
</dt> <dd>

Verwenden Sie Imm.lib.

</dd> </dl>
