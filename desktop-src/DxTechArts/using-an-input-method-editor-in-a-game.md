---
title: Verwenden eines Eingabemethoden-Editors in einem Spiel
description: In diesem Artikel wird erläutert, wie Sie ein einfaches Steuerelement für die IME-Bearbeitung in einer Microsoft DirectX-Vollbildanwendung implementieren können.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1519f07a4e105ae822bd13fd7acd8b29e5ad8a0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "103961530"
---
# <a name="using-an-input-method-editor-in-a-game"></a>Verwenden eines Eingabemethoden-Editors in einem Spiel

> [!Note]  
> In diesem Artikel wird das Arbeiten mit dem Windows XP-Eingabemethoden-Editor (IME) ausführlich erläutert. An der IME für Windows Vista wurden Änderungen vorgenommen, die in diesem Artikel nicht ausführlich erläutert werden. Weitere Informationen zu Änderungen am IME für Windows Vista finden Sie unter [Eingabemethoden-Editoren (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows Vista-eine Ever-Expanding Sicht der Internationalisierung](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) im Microsoft Global Development and Computing-Portal.

 

Ein Eingabemethoden-Editor (Input Method Editor, IME) ist ein Programm, das eine einfache Texteingabe mithilfe einer Standardtastatur für ostasiatische Sprachen wie Chinesisch, Japanisch, Koreanisch und andere Sprachen mit komplexen Zeichen ermöglicht. Beispielsweise kann ein Benutzer mit IMEs komplexe Zeichen in einem Textverarbeitungs Text eingeben, oder ein Spieler eines riesigen Multiplayer-Online Spiels kann mit Freunden in komplexen Zeichen chatten.

In diesem Artikel wird erläutert, wie Sie ein einfaches Steuerelement für die IME-Bearbeitung in einer Microsoft DirectX-Vollbildanwendung implementieren können. Anwendungen, die dxut nutzen, erhalten automatisch IME-Funktionen. In diesem Artikel wird beschrieben, wie Sie einem Bearbeitungs Steuerelement IME-Unterstützung hinzufügen können, wenn Sie nicht das Framework verwenden.

Inhalte:

-   [Standardmäßiges IME-Verhalten](#default-ime-behavior)
-   [Verwenden von IMEs mit dxut](#using-imes-with-dxut)
-   [Überschreiben des standardmäßigen IME-Verhaltens](#overriding-the-default-ime-behavior)
-   [Funktionen](#functions)
-   [Meldungen](#ime-messages)
-   [Beispiele](#examples)
    -   [CHT IME Version 4,2, 4,3 und 4,4](#cht-ime-version-42-43-and-44)
    -   [CHT IME Version 5,0](#cht-ime-version-50)
    -   [CHT IME Version 5,1, 5,2 und CHS IME Version 5,3](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [CHS IME Version 4,1](#chs-ime-version-41)
    -   [CHS IME Version 4,2](#chs-ime-version-42)
-   [IME-Nachrichten](#ime-messages)
    -   [WM \_ inputlangchange](#wm_inputlangchange)
    -   [WM \_ IME \_ StartComposition](/windows)
    -   [WM- \_ IME- \_ Komposition](/windows)
    -   [WM- \_ IME- \_ endkomposition](/windows)
    -   [WM- \_ IME \_ Benachrichtigen](/windows)
-   [Darstellung](#rendering)
    -   [Eingabe Gebiets Schema Indikator](#input-locale-indicator)
    -   [Kompositionsfenster](#composition-window)
    -   [Lese-und Kandidaten Fenster](#reading-and-candidate-windows)
-   [Einschränkungen](#limitations)
-   [Registrierungsinformationen](#registry-information)
-   [Anhang A: cht-Versionen pro Betriebs System](#appendix-a-cht-versions-per-operating-system)
-   [Weitere Informationen](#further-information)
-   [Getreadingstring](#getreadingstring)
-   [Showleseringwindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>Standardmäßiges IME-Verhalten

Mit dieser Option werden Tastatureingaben für phonetische Komponenten oder andere Sprachelemente, die für eine ausgewählte Sprache spezifisch sind, zugeordnet. In einem typischen Szenario gibt der Benutzerschlüssel ein, die die Aussprache eines komplexen Zeichens darstellen. Wenn das IME die Aussprache als gültig erkennt, wird dem Benutzer eine Liste von Wort-oder Ausdrucks Kandidaten angezeigt, aus der der Benutzer eine endgültige Auswahl treffen kann. Das gewählte Wort wird dann über eine Reihe von Microsoft Windows- [**WM- \_ char**](/windows/desktop/inputdev/wm-char) -Nachrichten an die Anwendung gesendet. Da der IME auf einer Ebene unterhalb der Anwendung ausgeführt wird, indem Tastatureingaben abgefangen werden, ist das vorhanden sein eines IME für die Anwendung transparent. Fast alle Windows-Anwendungen können Unes problemlos nutzen, ohne sich über Ihr vorhanden sein zu kümmern und ohne dass eine spezielle Codierung erforderlich ist.

Ein typisches IME zeigt mehrere Fenster an, die den Benutzer durch den Zeichen Eintrag leiten, wie in den folgenden Beispielen gezeigt.

![IME zeigt mehrere Fenster an](images/ime-elements.png)

| Fenstertyp                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                 | IME-Ausgabe                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| A. Lese Fenster                                 | Enthält Tastatureingaben auf der Tastatur. wird in der Regel nach jedem Tastatur Strich geändert.                                                                                                                                                                                                                                              | Lese Zeichenfolge                               |
| B. Kompositionsfenster                             | Enthält die Auflistung der Zeichen, die der Benutzer mit dem IME zusammengesetzt hat. Diese Zeichen werden vom IME auf der Grundlage der Anwendung gezeichnet. Wenn der Benutzer den IME benachrichtigt, dass die Kompositions Zeichenfolge zufriedenstellend ist, sendet der IME die Kompositions Zeichenfolge über eine Reihe von WM char-Nachrichten an die Anwendung \_ . | Kompositions Zeichenfolge                           |
| C. Kandidaten Fenster                               | Wenn der Benutzer eine gültige Aussprache eingegeben hat, zeigt der IME eine Liste von Kandidaten Zeichen an, die alle der angegebenen Aussprache entsprechen. Der Benutzer wählt dann das beabsichtigte Zeichen aus der Liste aus, und das IME fügt dieses Zeichen in der Anzeige des Kompositions Fensters hinzu.                                                    | Das nächste Zeichen in der Kompositions Zeichenfolge. |
| D: [Eingabe](/windows/desktop/Intl/nls-terminology) Gebiets Schema Indikator | Zeigt die Sprache an, die der Benutzer für die Tastatureingabe ausgewählt hat. Dieser Indikator ist in der Windows-Taskleiste eingebettet. Die Eingabe Sprache kann ausgewählt werden, indem Sie die Systemsteuerung für Regions-und Sprachoptionen öffnen und dann auf der Registerkarte Sprachen auf Details klicken.                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>Verwenden von IMEs mit dxut

In dxut implementiert die cdxutimeeditbox-Klasse die IME-Funktionalität. Diese Klasse wird von der cdxuteditbox-Klasse abgeleitet, dem grundlegenden Bearbeitungs Steuerelement, das vom Framework bereitgestellt wird. Cdxutimeeditbox erweitert das Bearbeitungs Steuerelement, sodass es durch Überschreiben der cdxutimeeditbox-Methoden unterstützt wird. Die Klassen sind auf diese Weise konzipiert, um Entwicklern zu helfen, zu erfahren, was Sie aus dem Framework zum Implementieren von IME-Unterstützung in ihren eigenen Bearbeitungs Steuerelementen benötigen. Im weiteren Verlauf dieses Themas wird erläutert, wie das Framework und cdxutimeeditbox insbesondere ein einfaches Bearbeitungs Steuerelement überschreibt, um die IME-Funktionalität zu implementieren.

Die meisten IME-spezifischen Variablen in cdxutimeeditbox werden als statisch deklariert, da viele IME-Puffer und-Zustände für den Prozess spezifisch sind. Beispielsweise verfügt ein Prozess nur über einen Puffer für die Kompositions Zeichenfolge. Auch wenn der Prozess über zehn Bearbeitungs Steuerelemente verfügt, werden alle denselben Kompositions Zeichen folgen Puffer gemeinsam nutzen. Der Kompositions Zeichen folgen Puffer für cdxutimeeditbox ist daher statisch und verhindert, dass die Anwendung unnötigen Speicherplatz in Anspruch nimmt.

Cdxutimeeditbox ist im folgenden dxut-Code implementiert:

(SDK-Stamm) \\ Beispiele \\ C++ \\ Common \\ dxutgui. cpp

## <a name="overriding-the-default-ime-behavior"></a>Überschreiben des standardmäßigen IME-Verhaltens

Normalerweise verwendet ein IME Windows-Standard Prozeduren, um ein Fenster zu erstellen (siehe [Verwenden von Windows](/windows/desktop/winmsg/using-windows)). Unter normalen Umständen ergibt dies zufriedenstellende Ergebnisse. Wenn die Anwendung jedoch im Vollbildmodus dargestellt wird, wie es bei Spielen üblich ist, funktionieren Standardfenster nicht mehr und werden möglicherweise nicht oberhalb der Anwendung angezeigt. Um dieses Problem zu beheben, muss die Anwendung das IME-Fenster selbst zeichnen, anstatt sich auf Windows zu verlassen, um diese Aufgabe auszuführen.

Wenn das standardmäßige Erstellungs Verhalten des IME-Fensters nicht bereitstellt, was eine Anwendung erfordert, kann die Anwendung die Verarbeitung des IME-Fensters überschreiben. Eine Anwendung kann dies erreichen, indem IME-bezogene Nachrichten verarbeitet und die API des [Eingabemethoden-Managers](/windows/desktop/Intl/input-method-manager) (IMM) aufgerufen wird.

Wenn ein Benutzer mit einem IME interagiert, um komplexe Zeichen einzugeben, sendet das IMM Nachrichten an die Anwendung, um Sie über wichtige Ereignisse zu benachrichtigen, z. b. das Starten einer Komposition oder das zeigen des Kandidaten Fensters. Eine Anwendung ignoriert diese Nachrichten in der Regel und übergibt sie an den Standard Nachrichten Handler, der bewirkt, dass Sie von der IME behandelt werden. Wenn die Anwendung anstelle des Standard Handlers die Nachrichten verarbeitet, steuert Sie genau, was bei den einzelnen IME-Ereignissen geschieht. Häufig ruft der Nachrichten Handler den Inhalt der verschiedenen IME-Fenster durch Aufrufen der imm-API ab. Wenn die Anwendung über diese Informationen verfügt, kann Sie die IME-Fenster selbst zeichnen, wenn Sie in der Anzeige dargestellt werden muss.

## <a name="functions"></a>Functions

Ein IME muss die Lese Zeichenfolge erhalten, das Lese Fenster ausblenden und die Ausrichtung des Lese Fensters erhalten. Diese Tabelle zeigt die Funktionen pro IME-Version:



|                    | Lesen der Zeichenfolge                                                | Ausblenden des Lese Fensters                       | Ausrichtung des Lese Fensters                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| Vor Version 6,0 | A. Das Lesen von Fenster Access private IME-Daten direkt. Siehe "4 Structure" | Private Trap-Nachrichten in Trap Siehe "3 Nachrichten" | Überprüfen Sie die Registrierungsinformationen. Weitere Informationen finden Sie unter "5 Registrierungsinformationen" |
| Nach Version 6,0  | [Getreadingstring](#getreadingstring)                                 | [Showleseringwindow](#showreadingwindow)     | [Getreadingstring](#getreadingstring)                      |



 

## <a name="messages"></a>Meldungen

Die folgenden Meldungen müssen nicht für neuere IME verarbeitet werden, die [showleseringwindow](#showreadingwindow)() implementiert.

Die folgenden Nachrichten werden vom Anwendungs Nachrichten Handler erfasst (d. h., Sie werden nicht an defwindowproc übermittelt), um zu verhindern, dass das Lese Fenster angezeigt wird.

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird veranschaulicht, wie Zeichen folgen Informationen aus dem älteren IME gelesen werden, die nicht über getreadingstring () verfügen. Der Code generiert die folgenden Ausgaben:



|              |                                                                                       |
|--------------|---------------------------------------------------------------------------------------|
| DWORD-dwlen  | Länge der Lese Zeichenfolge                                                          |
| DWORD-dwerr  | Index des Fehlers Char                                                                   |
| LPWSTR WSTR  | Zeiger auf die Lese Zeichenfolge                                                         |
| Boolescher Unicode | True gibt an, dass die Lese Zeichenfolge im Unicode-Format vorliegt. Andernfalls ist es das multibyteformat. |



 

### <a name="cht-ime-version-42-43-and-44"></a>CHT IME Version 4,2, 4,3 und 4,4

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a>CHT IME Version 5,0

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

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a>CHT IME Version 5,1, 5,2 und CHS IME Version 5,3

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

### <a name="chs-ime-version-41"></a>CHS IME Version 4,1

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

### <a name="chs-ime-version-42"></a>CHS IME Version 4,2

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

Eine Vollbildanwendung muss die folgenden IME-bezogenen Meldungen ordnungsgemäß verarbeiten:

### <a name="wm_inputlangchange"></a>WM \_ inputlangchange

Der imm sendet eine WM- \_ inputlangchange-Meldung an das aktive Fenster einer Anwendung, nachdem das Eingabe Gebiets Schema vom Benutzer mit einer Tastenkombination (normalerweise ALT + UMSCHALT) oder mit dem Eingabe Gebiets Schema Indikator auf der Taskleiste oder der sprach Leiste geändert wurde. Die sprach Leiste ist ein Steuerelement auf dem Bildschirm, mit dem der Benutzer einen Text Dienst konfigurieren kann. (Weitere Informationen finden [Sie unter Anzeigen der sprach Leiste](/windows/desktop/TSF/how-to-set-up-tsf).) Der folgende Screenshot zeigt eine Sprachauswahl Liste, die angezeigt wird, wenn der Benutzer auf den Gebiets Schema Indikator klickt.

![die Auswahlliste für die Sprache, die angezeigt wird, wenn der Benutzer auf den Gebiets Schema Indikator klickt](images/ime-langselection.png)

Wenn der imm eine "WM \_ inputlangchange"-Meldung sendet, muss cdxutimeeditbox verschiedene wichtige Aufgaben ausführen:

1.  Die GetKeyboardLayout-Methode wird aufgerufen, um den Eingabe Gebiets Schema Bezeichner (ID) für den Anwendungs Thread zurückzugeben. Die cdxutimeeditbox-Klasse speichert diese ID in der statischen Member-Variable s \_ hklcurrent zur späteren Verwendung. Es ist wichtig, dass die Anwendung das aktuelle Eingabe Gebiets Schema kennt, da der IME für jede Sprache über ein eigenes Verhalten verfügt. Der Entwickler muss möglicherweise unterschiedliche Codes für verschiedene Eingabe Gebiets Schemas bereitstellen.
2.  Cdxutimeeditbox Initialisiert eine Zeichenfolge, die im Bearbeitungsfeld-Sprachindikator angezeigt werden soll. Dieser Indikator kann die aktive Eingabe Sprache anzeigen, wenn die Anwendung im Vollbildmodus ausgeführt wird und weder die Taskleiste noch die sprach Leiste sichtbar ist.
3.  Die immgetkonversionstatus-Methode wird aufgerufen, um anzugeben, ob das Eingabe Gebiets Schema im systemeigenen oder nicht systemeigenen Konvertierungsmodus ist. Im nativen Konvertierungsmodus kann der Benutzer Text in der gewählten Sprache eingeben. Der nicht native Konvertierungsmodus fungiert als Standard-Englisch-Tastatur. Es ist wichtig, den Benutzern einen visuellen Hinweis auf den Typ des Konvertierungsmodus zu geben, in dem sich der IME befindet, sodass der Benutzer leicht erkennen kann, welche Zeichen erwartet werden, wenn er auf einen Schlüssel trifft. Cdxutimeeditbox stellt diesem visuellen Hinweis eine Sprachindikator Farbe zur Verfügung. Wenn das Eingabe Gebiets Schema einen IME mit dem nativen Konvertierungsmodus verwendet, zeichnet die cdxutimeeditbox-Klasse den Indikator Text mit der durch den m- \_ Parameter color-Parameter definierten Farbe. Wenn sich der IME im nicht systemeigenen Konvertierungsmodus befindet oder überhaupt kein IME verwendet wird, zeichnet die Klasse den Indikator Text mit der Farbe, die durch den m-Wert Order Color-Parameter definiert wird \_ .
4.  Cdxutimeeditbox überprüft das Eingabe Gebiets Schema und legt die statische Member-Variable s \_ binsertontype für Koreanisch auf true und für alle anderen Sprachen false fest. Dieses Flag ist aufgrund der unterschiedlichen Verhaltensweisen koreanischer IMEs und aller anderen IMEs erforderlich. Wenn Zeichen in anderen Sprachen als Koreanisch eingegeben werden, wird der vom Benutzer eingegebene Text im Kompositionsfenster angezeigt, und der Benutzer kann den Inhalt der Kompositions Zeichenfolge frei ändern. Der Benutzer drückt die EINGABETASTE, wenn er mit der Kompositions Zeichenfolge zufrieden ist, und die Kompositions Zeichenfolge wird als eine Reihe von WM char-Nachrichten an die Anwendung gesendet \_ . Bei koreanischen IMEs wird jedoch sofort ein Zeichen an die Anwendung gesendet, wenn ein Benutzer eine Taste drückt, um Text einzugeben. Wenn der Benutzer anschließend mehr Tasten drückt, um das erste Zeichen zu ändern, ändert sich das Zeichen im Bearbeitungsfeld, um zusätzliche Benutzereingaben widerzuspiegeln. Im Grunde stellt der Benutzer Zeichen im Bearbeitungsfeld zusammen. Diese zwei Verhaltensweisen unterscheiden sich, dass cdxutimeeditbox speziell für jeden von Ihnen codieren muss.
5.  Die statische Member-Methode setupimeapi wird aufgerufen, um Adressen von zwei Funktionen aus dem IME-Modul abzurufen: getreadingstring und showread ingwindow. Wenn diese Funktionen vorhanden sind, wird showreadingwindow aufgerufen, um das standardmäßige Lese Fenster für diesen IME auszublenden. Da die Anwendung das Lese Fenster selbst rendert, benachrichtigt Sie den IME, das Zeichnen des standardmäßigen Lese Fensters zu deaktivieren, sodass das voll Bild Rendering nicht beeinträchtigt wird.

Der imm sendet eine WM \_ IME- \_ SetContext-Nachricht, wenn ein Fenster der Anwendung aktiviert wird. Der lParam-Parameter dieser Nachricht enthält ein Flag, das für den IME angibt, welche Fenster gezeichnet werden sollen und welche nicht. Da die Anwendung die gesamte Zeichnung verarbeitet, ist es nicht erforderlich, dass der IME das IME-Fenster zeichnet. Daher legt der Nachrichten Handler der Anwendung einfach lParam auf 0 fest und gibt zurück.

Damit Anwendungen IME unterstützen können, wird für den IME-bezogenen Message-WM-"SetContext" eine spezielle Verarbeitung benötigt \_ \_ . Da Windows diese Nachricht normalerweise vor dem Aufrufen der Methode "panoramainitialize ()" an die Anwendung sendet, kann das Panorama die Benutzeroberfläche nicht zur Anzeige von Kandidatenlisten Fenstern verarbeiten.

Der folgende Code Ausschnitt gibt für Windows-Anwendungen an, dass keine Benutzeroberfläche angezeigt werden soll, die mit dem Fenster der Kandidatenliste verknüpft ist. Dadurch kann das Panorama die Benutzeroberfläche speziell verarbeiten.

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>WM \_ IME \_ StartComposition

Der imm sendet eine WM \_ IME \_ StartComposition-Meldung an die Anwendung, wenn eine IME-Komposition im Begriff ist, als Ergebnis von Tastatureingaben durch den Benutzer zu beginnen. Wenn der IME das Kompositionsfenster verwendet, wird die aktuelle Kompositions Zeichenfolge in einem Kompositionsfenster angezeigt. Cdxutimeeditbox verarbeitet diese Nachricht, indem zwei Aufgaben ausgeführt werden:

1.  Cdxutimeeditbox löscht den Zeichen folgen Puffer und den Attribut Puffer der Komposition. Diese Puffer sind statische Member von cdxutimeeditbox.
2.  Cdxutimeeditbox legt die \_ statische Member-Variable des s bhidecaret auf true fest. Dieser Member, der in der cdxuteditbox-Basisklasse definiert ist, steuert, ob der Cursor im Bearbeitungsfeld gezeichnet werden soll, wenn das Bearbeitungsfeld gerendert wird. Das Kompositionsfenster funktioniert ähnlich wie ein Bearbeitungsfeld mit Text und Cursor. Um Verwirrung zu vermeiden, wenn das Kompositionsfenster sichtbar ist, blendet das Bearbeitungsfeld den Cursor aus, sodass jeweils nur ein Cursor sichtbar ist.

### <a name="wm_ime_composition"></a>WM- \_ IME- \_ Komposition

Der imm sendet eine WM \_ IME- \_ Kompositions Meldung an die Anwendung, wenn der Benutzer eine Tastenkombination eingibt, um die Kompositions Zeichenfolge zu ändern. Der Wert von lParam gibt an, welche Art von Informationen die Anwendung vom Eingabemethoden-Manager abrufen kann. Die Anwendung muss die verfügbaren Informationen abrufen, indem Sie " [**immgetcompositionstring**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) " anruft und die Informationen dann in Ihrem privaten Puffer speichert, damit die IME-Elemente später dargestellt werden können.

Cdxutimeeditbox überprüft die folgenden Kompositions Zeichen folgen Daten und ruft Sie ab:



| [**WM \_ Wert der IME- \_ Komposition**](/windows/desktop/Intl/wm-ime-composition) lParam-Flag | Daten                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GCS- \_ compattr                                                         | Kompositions Attribut          | Dieses Attribut enthält Informationen, z. b. den Status jedes Zeichens in der Kompositions Zeichenfolge (z. b. konvertiert oder nicht konvertiert). Diese Informationen sind erforderlich, da cdxutimeeditbox die Zeichen folgen Zeichen der Komposition auf der Grundlage ihrer Attribute unterschiedlich färbt.                                                                                   |
| GCS- \_ compclause                                                       | Informationen zur Kompositions Klausel | Diese klauselinformationen werden verwendet, wenn der japanische IME aktiv ist. Wenn eine japanische Kompositions Zeichenfolge konvertiert wird, können Zeichen als eine-Klausel gruppiert werden, die in eine einzelne Entität konvertiert wird. Wenn der Benutzer den Cursor verschiebt, verwendet cdxutimeeditbox diese Informationen, um die gesamte Klausel anstelle eines einzelnen Zeichens in der-Klausel hervorzuheben. |
| GCS \_ compstr                                                          | Kompositions Zeichenfolge             | Diese Zeichenfolge ist die aktuelle Zeichenfolge, die vom Benutzer erstellt wird. Dies ist auch die im Kompositionsfenster angezeigte Zeichenfolge.                                                                                                                                                                                                                                        |
| GCS- \_ Cursor                                                        | Position des Kompositions Cursors    | Das Kompositionsfenster implementiert einen Cursor, ähnlich dem Cursor in einem Bearbeitungsfeld. Die Anwendung kann die Cursorposition bei der Verarbeitung der WM \_ IME- \_ Kompositions Nachricht abrufen, um den Cursor ordnungsgemäß zu zeichnen.                                                                                                                                            |
| GCS- \_ ResultStr                                                        | Ergebnis Zeichenfolge                  | Die Ergebnis Zeichenfolge ist verfügbar, wenn der Benutzer im Begriff ist, den Kompositionsprozess abzuschließen. Diese Zeichenfolge sollte abgerufen werden, und die Zeichen sollten an das Bearbeitungsfeld gesendet werden.                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>WM- \_ IME- \_ endkomposition

Der imm sendet eine WM- \_ IME- \_ endkompositions Meldung an die Anwendung, wenn der IME-Kompositions Vorgang beendet wird. Dies kann vorkommen, wenn der Benutzer die EINGABETASTE drückt, um die Kompositions Zeichenfolge zu genehmigen, oder die ESC-Taste, um die Komposition abzubrechen. Cdxutimeeditbox verarbeitet diese Nachricht, indem der Kompositions Zeichen folgen Puffer auf leer festgelegt wird. Anschließend wird s \_ bhidecaret auf false festgelegt, da das Kompositionsfenster geschlossen wird und der Cursor im Bearbeitungsfeld erneut sichtbar sein sollte.

Der cdxutimeeditbox-Meldungs Handler legt auch "s \_ bshowleseringwindow" auf "false" fest. Dieses Flag steuert, ob die Klasse das Lese Fenster zeichnet, wenn sich das Bearbeitungsfeld selbst rendert, sodass es auf "false" festgelegt werden muss, wenn eine Komposition endet.

### <a name="wm_ime_notify"></a>WM- \_ IME \_ Benachrichtigen

Der imm sendet eine WM- \_ IME- \_ Benachrichtigungs Meldung an die Anwendung, wenn ein IME-Fenster geändert wird. Eine Anwendung, die das Zeichnen von IME-Fenstern behandelt, sollte diese Nachricht so verarbeiten, dass Sie ein Update des Inhalts des Fensters kennt. Der wParam-Parameter gibt den Befehl oder die Änderung an, die stattfindet. Cdxutimeeditbox behandelt die folgenden Befehle:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>IME-Befehl</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></td>
<td>Dieses Attribut enthält Informationen, z. b. den Status jedes Zeichens in der Kompositions Zeichenfolge (z. b. konvertiert oder nicht konvertiert). Diese Informationen sind erforderlich, da cdxutimeeditbox die Zeichen folgen Zeichen der Komposition auf der Grundlage ihrer Attribute unterschiedlich färbt.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></td>
<td>Wird an die Anwendung gesendet, wenn das Kandidaten Fenster gerade geöffnet bzw. aktualisiert wird. Das Kandidaten Fenster wird geöffnet, wenn ein Benutzer die konvertierte Textauswahl ändern möchte. Das Fenster wird aktualisiert, wenn ein Benutzer den Auswahl Indikator verschiebt oder die Seite ändert. Cdxutimeeditbox verwendet einen Nachrichten Handler für beide Befehle, da die erforderlichen Aufgaben exakt identisch sind:<br/>
<ol>
<li>Cdxutimeeditbox legt den bshowwindow-Member der Kandidatenlisten Struktur s_CandList auf true fest, um anzugeben, dass das Kandidaten Fenster beim Frame Rendering gezeichnet werden muss.</li>
<li>Cdxutimeeditbox Ruft die Kandidatenliste durch Aufrufen von " <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>immgetcandidatelist</strong></a>" ab, um die erforderliche Puffergröße zu erhalten, und dann erneut, um die eigentlichen Daten abzurufen.</li>
<li>Die Struktur s_CandList der privaten Kandidatenliste wird mit den abgerufenen Kandidaten Daten initialisiert.</li>
<li>Die Kandidaten Zeichenfolgen werden als Array von Zeichen folgen gespeichert.</li>
<li>Der Index des ausgewählten Eintrags sowie der Seitenindex werden gespeichert.</li>
<li>Cdxutimeeditbox überprüft, ob der Stil des Kandidaten Fensters vertikal oder horizontal ist. Wenn der Fenster Stil horizontal ist, muss ein zusätzlicher Zeichen folgen Puffer, der horicand-Member von s_CandList, mit allen Kandidaten Zeichenfolgen initialisiert werden, wobei Leerzeichen zwischen allen angrenzenden Zeichen folgen eingefügt werden. Beim Rendern eines vertikalen Kandidaten Fensters werden die einzelnen Kandidaten Zeichenfolgen nacheinander gezeichnet, wobei die y-Koordinaten für jede Zeichenfolge inkrementiert werden. Diese horicand-Zeichenfolge sollte jedoch beim Rendern eines horizontalen Kandidaten Fensters verwendet werden, da das Leerzeichen die beste Möglichkeit zum Trennen zweier aufeinander folgender Zeichen folgen in derselben Zeile ist.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></td>
<td>Wird an die Anwendung gesendet, wenn ein Kandidaten Fenster im Begriff ist, zu schließen. Dies geschieht, wenn ein Benutzer eine Auswahl aus der Kandidatenliste getroffen hat. Cdxutimeeditbox verarbeitet diesen Befehl, indem das sichtbare Flag des Kandidaten Fensters auf "false" festgelegt und der Kandidaten Zeichen folgen Puffer gelöscht wird.</td>
</tr>
<tr class="even">
<td>IMN_PRIVATE</td>
<td>Wird an die Anwendung gesendet, wenn der IME seine Lese Zeichenfolge aktualisiert hat, als das Benutzer Zeichen eingegeben oder entfernt hat. Die Anwendung sollte die Lese Zeichenfolge abrufen und für das Rendering speichern. Cdxutimeeditbox verfügt über zwei Methoden zum Abrufen der Lese Zeichenfolge, die darauf basiert, wie das Lesen von Zeichen folgen im IME unterstützt wird: <br/>
<ul>
<li>Wenn der IME die getreadingstring-Funktion unterstützt, wird getreadingstring aufgerufen, um die Lese Zeichenfolge abzurufen.</li>
<li>Wenn der IME "getreadingstring" nicht implementiert, ruft cdxutimeeditbox die Lese Zeichenfolge aus dem Eingabe Kontext Inhalt ab.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a>Darstellung

Das Rendering der IME-Elemente und Windows ist einfach. Cdxutimeeditbox ermöglicht, dass die Basisklasse zuerst Rendering wird, da IME-Fenster oberhalb des Bearbeitungs Steuer Elements angezeigt werden. Nachdem das Basis Bearbeitungsfeld gerendert wurde, prüft cdxutimeeditbox das Sichtbarkeits Kennzeichen der einzelnen IME-Fenster (Indikator, Komposition, Kandidat und Lese Fenster) und zeichnet das Fenster, wenn es sichtbar sein soll. Beschreibungen der verschiedenen IME-Fenstertypen finden Sie unter Standardmäßiges IME-Verhalten.

### <a name="input-locale-indicator"></a>Eingabe Gebiets Schema Indikator

Der Eingabe Gebiets Schema Indikator wird vor allen anderen IME-Fenstern gerendert, da es sich um ein Element handelt, das immer angezeigt wird. Daher sollte Sie unter anderen IME-Fenstern angezeigt werden. Cdxutimeeditbox rendert den Indikator durch Aufrufen der renderindicator-Methode, in der die Schriftart Farbe des Indikators durch Untersuchen der statischen "s \_ ImeState"-Variablen, die den aktuellen IME-Konvertierungsmodus widerspiegelt, bestimmt wird. Wenn der IME aktiviert und die native Konvertierung aktiv ist, verwendet die-Methode m \_ indikatorimecolor als Indikator Farbe. Wenn der IME deaktiviert ist oder sich im nicht systemeigenen Konvertierungsmodus befindet, wird m- \_ indikatorimecolor zum Zeichnen des Indikator Texts verwendet. Standardmäßig wird das Indikator Fenster selbst rechts neben dem Bearbeitungsfeld gezeichnet. Anwendungen können dieses Verhalten ändern, indem Sie die renderindicator-Methode überschreiben.

Die folgende Abbildung zeigt die verschiedenen Vorkommen eines Eingabe Gebiets Schema Indikators für Englisch, Japanisch im alphanumerischen Konvertierungsmodus und Japanisch im nativen Konvertierungsmodus:

![unterschiedliche Darstellungen eines Eingabe Gebiets Schema Indikators für Englisch und Japanisch](images/ime-indicator.png)

### <a name="composition-window"></a>Kompositionsfenster

Die Zeichnung des Kompositions Fensters wird in der rendercomposition-Methode von cdxutimeeditbox behandelt. Das Kompositionsfenster schwebt über dem Bearbeitungsfeld. Er sollte an der Cursorposition des zugrunde liegenden Bearbeitungs Steuer Elements gezeichnet werden. Cdxutimeeditbox behandelt das Rendering wie folgt:

1.  Die gesamte Kompositions Zeichenfolge wird mit den Standardfarben für Kompositions Zeichenfolgen gezeichnet.
2.  Zeichen mit bestimmten speziellen Attributen sollten in unterschiedlichen Farben gezeichnet werden, daher überprüft cdxutimeeditbox die Zeichen der Kompositions Zeichenfolge und überprüft das Zeichen folgen Attribut. Wenn das Attribut verschiedene Farben aufruft, wird das Zeichen erneut mit den entsprechenden Farben gezeichnet.
3.  Der Cursor des Kompositions Fensters wird gezeichnet, um das Rendering abzuschließen.

Der Cursor sollte für koreanische IMEs blinken, aber nicht für andere IMEs. Rendercomposition bestimmt, ob der Cursor auf der Grundlage von Zeit Geber Werten sichtbar sein soll, wenn der Koreanisch-IME verwendet wird.

### <a name="reading-and-candidate-windows"></a>Lese-und Kandidaten Fenster

Die Lese-und Kandidaten Fenster werden von der gleichen cdxutimeeditbox-Methode rendercandidatereadingwindow gerendert. Beide Fenster enthalten ein Zeichen folgen Array für das vertikale Layout oder eine einzelne Zeichenfolge im Fall eines horizontalen Layouts. Der Großteil des Codes in rendercandidatereadingwindow wird verwendet, um das Fenster so zu positionieren, dass kein Teil des Fensters außerhalb des Anwendungsfensters liegt und abgeschnitten wird.

## <a name="limitations"></a>Einschränkungen

In manchen Fällen enthalten IMEs erweiterte Features, um die einfache Eingabe von Text zu verbessern. Einige der Features, die in neueren IMEs gefunden werden, sind in den folgenden Abbildungen dargestellt. Diese erweiterten Funktionen sind nicht in dxut vorhanden. Das Implementieren der Unterstützung für diese erweiterten Funktionen kann schwierig sein, da keine Schnittstelle definiert ist, um die erforderlichen Informationen aus den IMEs zu erhalten.

Erweitertes traditionelles Chinesisch (IME) mit erweiterter Kandidatenliste:

![Erweitertes traditionelles Chinesisch (IME) mit erweiterter Kandidatenliste](images/ime-advanced1.png)

Advanced Japanese IME mit einigen Kandidaten Einträgen, die zusätzlichen Text enthalten, um ihre Bedeutung zu beschreiben:

![Advanced Japanese IME mit einigen Kandidaten Einträgen, die zusätzlichen Text zum Beschreiben ihrer Bedeutung enthalten](images/ime-advanced2.png)

Advanced Korean IME, das ein handschrifterkennungssystem umfasst:

![Advanced Korean IME mit einem handschrifterkennungssystem](images/ime-advanced3.png)

## <a name="registry-information"></a>Registrierungsinformationen

Die folgenden Registrierungsinformationen werden geprüft, um die Ausrichtung des Lese Fensters zu ermitteln, wenn die aktuelle IME älter ist, die sich in der neuen Phonetic befindet, die getreadingstring () nicht implementiert.



| Schlüssel                                                           | Wert            |
|---------------------------------------------------------------|------------------|
| HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ IME \_ Name | Tastatur Zuordnung |



 

WHERE: der IME- \_ Name ist mstciph, wenn die Version der IME-Datei 5,1 oder höher ist. Andernfalls lautet der IME- \_ Name tintlgnt.

Die Ausrichtung des Lese Fensters ist horizontal, wenn Folgendes gilt:

-   Der IME ist Version 5,0, und der Wert der Tastatur Zuordnung ist 0x22 oder 0x23.
-   Der IME ist Version 5,1 oder Version 5,2, und der Wert der Tastatur Zuordnung ist 0x22, 0x23 oder 0x24.

Wenn keine der Bedingungen erfüllt ist, ist das Lesefenster vertikal.

## <a name="appendix-a-cht-versions-per-operating-system"></a>Anhang A: cht-Versionen pro Betriebs System



| Betriebssystem           | CHT IME-Version |
|----------------------------|-----------------|
| Windows 98                 | 4,2             |
| Windows 2000               | 4.3             |
| unknown                    | 4.4             |
| Windows Me                 | 5.0             |
| Office XP                  | 5,1             |
| Windows XP                 | 5,2             |
| Eigenständiges Webdownload | 6.0             |



 

## <a name="further-information"></a>Weitere Informationen

Zusätzliche Informationen finden Sie unter:

-   [Installieren und Verwenden von Eingabemethoden-Editoren](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [Internationale Text Anzeige](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [Das Unicode-Konsortium](https://www.unicode.org/)
-   Entwickeln internationaler Software. Dr. International. 2. Ed. Redmond, WA: Microsoft Press, 2003.

## <a name="getreadingstring"></a>Getreadingstring

Ruft Zeichen folgen Informationen ab.

**Parameter**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[im \] Eingabe Kontext.

</dd> <dt>

<span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*ulesingbuschlen*
</dt> <dd>

\[\]Länge von lpwleseringbuf in WCHAR. Wenn der Wert 0 (null) ist, bedeutet dies, dass die Abfrage die Pufferlänge

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwlesingbuf* 
</dt> <dd>

\[Out \] gibt Lese Zeichenfolge zurück (nicht NULL Ende).

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnerrorindex* 
</dt> <dd>

\[Out \] gibt den Index des Fehler Zeichens in der Lese Zeichenfolge zurück, falls vorhanden.

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfisvertikal* 
</dt> <dd>

\[Wenn der Wert \] true ist, ist das Lesen der Benutzeroberfläche vertikal. Andernfalls horizontal pumaxleseringlen.

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*pumaxleseringlen* 
</dt> <dd>

\[\]die Länge der Lese Benutzeroberfläche. Die maximale Leselänge ist nicht korrigiert. Es hängt nicht nur vom Tastaturlayout, sondern auch vom Eingabemodus ab (z. b. Interner Code, Ersatz Zeicheneingabe).

</dd> </dl>

**Rückgabewerte**

Die Länge der Lese Zeichenfolge.

**Anmerkungen**

Wenn der Rückgabewert größer ist als der Wert von uleseringbuslen, sind alle Ausgabeparameter nicht definiert.

Diese Funktion wird in cht IME 6,0 oder höher implementiert und kann von GetProcAddress auf einem IME-Modul Handle abgerufen werden. der IME-Modul Handle kann von "immgetimefilename" und "LoadLibrary" abgerufen werden.

**Anforderungen**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**
</dt> <dd>

In "imm. h" deklariert.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Bibliothek importieren**
</dt> <dd>

Verwenden Sie "imm. lib".

</dd> </dl>

## <a name="showreadingwindow"></a>Showleseringwindow

Lese Fenster anzeigen (oder ausblenden).

**Parameter**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[im \] Eingabe Kontext.

</dd> <dt>

<span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow* 
</dt> <dd>

\[in ist auf \] true festgelegt, um das Lese Fenster anzuzeigen (oder false, um es auszublenden).

</dd> </dl>

**Rückgabewerte**

**Anmerkungen**

Gibt true zurück, wenn erfolgreich, andernfalls false.

**Anforderungen**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Header**
</dt> <dd>

In "imm. h" deklariert.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Bibliothek importieren**
</dt> <dd>

Verwenden Sie "imm. lib".

</dd> </dl>