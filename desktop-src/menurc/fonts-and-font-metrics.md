---
title: Schriftarten und Textmetriken
description: In diesem Thema werden die von Windows bereitgestellten Konturschriftarten, Schriftartmetrikwerte, die sich zwischen Versionen von Windows ändern können, und Anleitungen zur Verwendung von Schriftartmetriken in Ihren Desktop-Apps erläutert.
ms.assetid: B195154D-0168-4C5E-9CFB-AE7EF63D5F42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5199459c7a6afd311b120bd186df000e0fd32eef828ae986caf6da8573afe8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687853"
---
# <a name="fonts-and-text-metrics"></a>Schriftarten und Textmetriken

In diesem Thema werden die von Windows bereitgestellten Konturschriftarten, Schriftartmetrikwerte, die sich zwischen Versionen von Windows ändern können, und Anleitungen zur Verwendung von Schriftartmetriken in Ihren Desktop-Apps erläutert.

-   Spezifische Informationen zu Schriftartmetriken in DirectWrite sie unter [Textmetriken](/windows/desktop/DirectWrite/text-metrics).
-   Weitere Informationen zum Verwalten von Text in Apps mithilfe von GDI finden Sie in den Themen unter [Schriftarten und Text](/windows/desktop/gdi/fonts-and-text).

Ausführlichere Informationen zur Verwendung von Schriftarten und Typspezifikationen finden Sie auf der [Microsoft-Website für Typografie.](https://www.microsoft.com/typography/default.mspx)

## <a name="available-fonts"></a>Verfügbare Schriftarten

Die mit Windows bereitgestellten Konturschriftarten werden als OpenType-Schriftarten mit TrueType-Konturen bereitgestellt (Windows unterstützt auch OpenType-Schriftarten im CFF-Format). Listen aller schriftarten, die von Windows bereitgestellt werden, finden Sie unter [Microsoft-Typografie: Schriftarten nach Produkt oder Familie](https://www.microsoft.com/typography/fonts/default.aspx). Alle Windows umrissenen Schriftarten entsprechen der neuesten Version der [OpenType-Spezifikation.](https://www.microsoft.com/typography/otspec/)

Eine Liste aller aktuellen und älteren Benutzeroberflächenschriftarten finden Sie weiter unten unter [Metriken für gesperrte](#locked-font-metrics) Schriftarten.

## <a name="font-modifications"></a>Schriftartänderungen

Um Abwärtskompatibilität zu gewährleisten, werden Schriftarten selten aus der Windows. Schriftarten werden jedoch häufig geändert. Änderungen können das Hinzufügen von Zeichen, das Neudrawing vorhandener Zeichen, das Ändern von Hinweisen oder das Hinzufügen oder Ändern der Unterstützung für erweiterte OpenType-Features und die komplexe Skriptgestaltung umfassen.

### <a name="locked-font-metrics"></a>Gesperrte Schriftartmetriken

Beachten Sie, dass einige Werte, die ui-Schriftarten und Standardschriftarten zugeordnet sind, die in Microsoft-Apps verwendet werden, gesperrt sind. Benutzeroberflächenschriftarten werden verwendet, um Benutzeroberflächenelemente wie Beschriftungen, Dialogfelder und Menüs zu rendern. Aufgrund ihrer hohen Sichtbarkeit und häufigen Verwendung werden nur sehr wenige Änderungen an diesen Schriftarten vorgenommen. Da jedoch die gemeldeten Werte, die diesen Schriftarten zugeordnet sind, gesperrt sind, können Abweichungen zwischen gemeldeten und tatsächlichen Schriftartwerten bestehen.

Die folgenden gemeldeten Werte sind für Benutzeroberflächen- und Standardschriftarten gesperrt und können ungenau gemeldet werden:

-   Diese Werte aus der [OS/2-Tabelle](https://www.microsoft.com/typography/otspec/os2.htm)der Schriftart:
    -   xAvgCharWidth
    -   sTypoLineGap
    -   sTypoAscender
    -   sTypoDescender
    -   usWinAscent
    -   usWinDescent
-   Der im Header der Schriftart festgelegte [unitsPerEm-Wert.](https://www.microsoft.com/typography/otspec/head.htm)
-   Werte aus der [Metriktabelle für vertikale Geräte (VERTICALX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
-   Die Vorbreiten für einzelne Glyphen

Im Folgenden finden Sie eine Liste der im Lieferumfang von Windows 8.1 -Schriftarten (von gesperrten Werten betroffen):

| Skriptname                   | Schriftart der Benutzeroberfläche               |
|-------------------------------|-----------------------|
| Arabisch                        | Segoe UI              |
| Armenisch                      | Segoe UI              |
| Pausla (vormalsMals ):     | Nirmala UI            |
| Bopomofo                      | Microsoft JhengHei UI |
| Braille                       | Segoe UI Symbol       |
| Buginesisch                      | Leelawadee UI         |
| Kanadierische Aboriginal-Silben | Gadugi                |
| Cherokee                      | Gadugi                |
| Koptisch                        | Segoe UI Symbol       |
| Chinesisch (vereinfacht)          | Microsoft YaHei UI    |
| Chinesisch (traditionell)         | Microsoft JhengHei UI |
| Kyrillisch                      | Segoe UI              |
| Devanagari                    | Nirmala UI            |
| Deseret                       | Segoe UI Symbol       |
| Ethiopic                      | Ebrima                |
| Georgisch                      | Segoe UI              |
| Glagolitic                    | Segoe UI Symbol       |
| Gothic                        | Segoe UI Symbol       |
| Griechisch                         | Segoe UI              |
| Gujarati                      | Nirmala UI            |
| Gurmukhi                      | Nirmala UI            |
| Hebräisch                        | Segoe UI              |
| Altes italisch                    | Segoe UI Symbol       |
| Javanisch                      | Javanischer Text         |
| Japanisch                      | Benutzeroberfläche von Überschreibbenutzeroberfläche             |
| Kannada                       | Mirmala-Benutzeroberfläche            |
| Khmer                         | Leelawadee UI         |
| Koreanisch                        | Malgun Gothic         |
| Laotisch                           | Leelawadee UI         |
| Lateinisch                         | Segoe UI              |
| Malayalam                     | Nirmala UI            |
| Mongolisch                     | Mongolisches Baiti       |
| Myanmar                       | Myanmar Text          |
| N'Ko                          | Ebrima                |
| Ogham                         | Segoe UI Symbol       |
| Ol Chiki                      | Nirmala UI            |
| Old OldIc                    | Segoe UI Symbol       |
| Odia (ehemals Orya)         | Nirmala UI            |
| Osmanya                       | Ebrima                |
| Paws-pa                      | Microsoft PhagsPa     |
| Runic                         | Segoe UI Symbol       |
| Sora Sompeng                  | Nirmala UI            |
| Singhalesisch                       | Nirmala UI            |
| Syrisch                        | Estrangelo Edessa     |
| Lette Le                        | Microsoft Tai Le      |
| Neue Lue -Lue                   | Microsoft Neu-Tai-Lue |
| Tamilisch                         | Nirmala UI            |
| Telugu                        | Nirmala UI            |
| Tifinagh                      | Ebrima                |
| Thaana                        | MV Boli               |
| Thailändisch                          | Leelawadee UI         |
| Tibetisch                       | Microsoft Himalaya    |
| Vai                           | Ebrima                |
| Yi                            | Microsoft Yi Baiti    |



 

Im Folgenden finden Sie eine Liste der älteren Schriftarten der Benutzeroberfläche, die auch von gesperrten Werten betroffen sind:

| Skriptname (Legacy)          | Schriftart der Benutzeroberfläche (Legacy)               |
|-------------------------------|--------------------------------|
| Pausla (vormalsMals ):     | Vrinda                         |
| Kanadierische Aboriginal-Silben | Euphemia                       |
| Cherokee                      | Plantagenet                    |
| Chinesisch (vereinfacht)          | Microsoft YaSim und SimSun     |
| Chinesisch (traditionell)         | MingLiU und Microsoft JhengRat |
| Devanagari                    | Mangal                         |
| Europäische Sprachen            | Tahoma                         |
| Gujarati                      | Shruti                         |
| Gurmukhi                      | Raavi                          |
| Japanisch                      | Benutzeroberfläche von Über- und Ms. Ui        |
| Kannada                       | Tunga                          |
| Khmer                         | Khmer                          |
| Koreanisch                        | Gulim                          |
| Laotisch                           | Lao-Benutzeroberfläche                         |
| Malayalam                     | Kartika                        |
| Sprachen des mittleren Ostens      | Tahoma                         |
| Odia (ehemals Orya)         | Kalinga                        |
| Singhalesen                     | Iskoola Tomba                   |
| Tamilisch                         | Latte und Vijaya               |
| Telugu                        | Gatami                        |
| Thailändisch                          | Leelawadee und Tahoma          |



 

Diese Schriftarten werden in Microsoft-Apps als Standardwerte verwendet und sind auch von gesperrten Werten betroffen:

-   Arial
-   Calibri
-   Cambria
-   Consolas
-   Courier New
-   MS Mincho
-   Times New Roman
-   Verdana

### <a name="dynamic-font-metrics"></a>Dynamische Schriftartmetriken

Ab gegensatz zu den oben aufgeführten gesperrten Metriken werden Schriftartwerte genau gemeldet. Wenn eine Schriftart in einer neuen Version von geändert Windows, unterscheiden sich dynamische Schriftartwerte zwischen der neuen und der alten. Wenn z. B. einer Schriftart ein Glyph hinzugefügt wird, können sich die Werte im Header der Schriftart ändern. Clipping kann dazu führen, dass diese Werte (einschließlich xMin, xMax, yMin und yMax und das minimale und maximale Begrenzungsfeld für Glyphen in der Schriftart) gesperrt sind und keine true-Werte melden.

> [!IMPORTANT]
> Wenn Sie dynamische Schriftartwerte in Ihrer App verwenden (z. B. werte in [**TEXTMETRIC),**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)ändern sich diese Werte, wenn Schriftarten in zukünftigen Versionen von Windows geändert werden. Verwenden Sie diese tatsächlichen Werte nicht in Situationen, in denen Text statisch bleiben muss.

 

## <a name="guidelines-for-using-font-metrics"></a>Richtlinien für die Verwendung von Schriftartmetriken

-   Berechnen Sie Bildschirmmetriken und Schriftartmetriken (z. B. durchschnittliche Breite), wenn eine App gestartet wird, und verwenden Sie diese Werte, um Ihre App zu gestalten. Dadurch wird ein konsistent genaues Rendering ermöglicht, und Ihr Layout reagiert auf Änderungen in Schriftarten oder bietet Platz für Schriftartfallbacks. Eine Übersicht über das Fallback von Schriftarten und die Verknüpfung von Schriftarten finden Sie unter [Globalisierung Schritt für Schritt: Schriftarten](https://msdn.microsoft.com/goglobal/bb688134.aspx). Informationen zu Uniscribe-spezifischen Informationen finden Sie unter [Verwenden des Schriftartfallbacks.](/windows/desktop/Intl/using-font-fallback)
    -   Um eine Basismetrik zu berechnen, rendern Sie repräsentativen Text für Ihre gewünschte Sprache/Ihr Skript.
    -   Legen Sie steuerelemente, die nur eine einzelne Zeile mit entpackten Text enthalten, so an, dass sie der vollständigen Breite des nicht gepackten Texts entsprechen.
    -   Für Steuerelemente mit mehreren Zeilen erhalten Sie die Gesamtlänge, dividieren Sie durch die Zeichenlänge, und Sie haben eine durchgezogene Breite, mit der Sie arbeiten können. Beachten Sie, dass dies für komplexe Skripts schwieriger ist, bei denen ein einzelnes "Zeichen" für den Reader mehrere Codepunkte sein kann.
-   Verwenden Sie sTypoAscender, sTypoDescender und unitsPerEm (aus der [Tabelle OS/2),](https://www.microsoft.com/typography/otspec/os2.htm)um den vertikalen Abstand zu berechnen. sTypoAscender wird verwendet, um den optimalen Offset vom oberen Rand eines Textrahmens zur ersten Baseline zu bestimmen, und sTypoDescender bestimmt den optimalen Offset vom unteren Rand eines Textrahmens zur letzten Baseline.
-   Wenn Sie DirectWrite verwenden, erstellen Sie ein Layout mit [**IDWriteTextLayout.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) **IDWriteTextLayout** stellt **ascender**  +  **descender**  +  **lineGap** im natürlichen Layout bereit. Sie können mit [**DWRITE \_ FONT \_ METRICS**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)auf diese spezifischen Werte zugreifen. Informationen zu dieser Schnittstelle finden Sie unter [Textformatierung und Layout.](/windows/desktop/DirectWrite/text-formatting-and-layout)
-   Wenn Sie GDI verwenden, rendern Sie den Bildschirm, überprüfen Sie das Layout (z. B. die Zeilenlänge oder Zeichen pro Zeile), und berechnen Sie die endgültigen Layoutparameter, die beim tatsächlichen Rendering verwendet werden.
-   Erstellen Sie Layouts nicht statisch basierend auf bestimmten Werten für bestimmte Versionen von Schriftarten. Die tatsächlichen Werte können sich von Release zu Release ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Idwritetextlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**\_DWRITE-SCHRIFTARTMETRIKEN \_**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)
</dt> <dt>

[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)
</dt> <dt>

[unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm)
</dt> <dt>

[Os/2-Tabelle](https://www.microsoft.com/typography/otspec/os2.htm)
</dt> <dt>

[Tabelle mit vertikalen Gerätemetriken (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
</dt> <dt>

[Microsoft-Typografie: Schriftarten nach Produkt oder Familie](https://www.microsoft.com/typography/fonts/default.aspx)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Textmetriken (DirectWrite)](/windows/desktop/DirectWrite/text-metrics)
</dt> <dt>

[Schriftarten und Text (GDI)](/windows/desktop/gdi/fonts-and-text)
</dt> <dt>

[Microsoft Typografie](https://www.microsoft.com/typography/default.mspx)
</dt> </dl>

 

 