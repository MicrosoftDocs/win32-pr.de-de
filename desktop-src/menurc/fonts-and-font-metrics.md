---
title: Schriftarten und textmetriken
description: In diesem Thema werden die von Windows bereitgestellten Gliederungs Schriftarten, Schriftart Metrikwerte, die sich Zwischenversionen von Windows ändern können, und Anleitungen zur Verwendung von Schriftart Metriken in Ihren Desktop-Apps erläutert.
ms.assetid: B195154D-0168-4C5E-9CFB-AE7EF63D5F42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27d4eb5f34f5a88e4a0e3e866f9a14784c3895
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948731"
---
# <a name="fonts-and-text-metrics"></a>Schriftarten und textmetriken

In diesem Thema werden die von Windows bereitgestellten Gliederungs Schriftarten, Schriftart Metrikwerte, die sich Zwischenversionen von Windows ändern können, und Anleitungen zur Verwendung von Schriftart Metriken in Ihren Desktop-Apps erläutert.

-   Informationen zu den Schriftart Metriken in DirectWrite finden Sie unter [textmetriken](/windows/desktop/DirectWrite/text-metrics).
-   Ausführliche Informationen zur Verwaltung von Text in Apps mithilfe von GDI finden Sie in den Themen zu [Schriftarten und Text](/windows/desktop/gdi/fonts-and-text).

Ausführlichere Informationen zur Schriftart Verwendung und Typspezifikationen finden Sie auf der [Microsoft Typografie-Website](https://www.microsoft.com/typography/default.mspx).

## <a name="available-fonts"></a>Verfügbare Schriftarten

Die mit Windows bereitgestellten Gliederungs Schriftarten werden als OpenType-Schriftarten mit TrueType-gliedern ausgeliefert (Windows unterstützt auch OpenType-Schriftarten im CFF-Format). Listen aller von Windows bereitgestellten Schriftarten finden Sie unter [Microsoft Typografie: Schriftarten nach Produkt oder Familie](https://www.microsoft.com/typography/fonts/default.aspx). Alle Windows-Gliederungs Schriftarten entsprechen der aktuellen Version der [OpenType-Spezifikation](https://www.microsoft.com/typography/otspec/).

Eine Liste aller aktuellen und der Legacy-Benutzeroberflächen-Schriftarten finden Sie unten unter [Gesperrte Schriftart Metriken](#locked-font-metrics) .

## <a name="font-modifications"></a>Schriftart Änderungen

Um die Abwärtskompatibilität zu gewährleisten, werden Schriftarten selten aus Windows entfernt. Schriftarten werden jedoch häufig geändert. Zu den Änderungen gehören das Hinzufügen von Zeichen, das Neuzeichnen vorhandener Zeichen, das Ändern von Hinweisen oder das Hinzufügen oder Ändern der Unterstützung für erweiterte OpenType-Features und komplexe Skript

### <a name="locked-font-metrics"></a>Gesperrte Schriftart Metriken

Beachten Sie, dass einige der in Microsoft-Apps verwendeten UI-Schriftarten und Standard Schriftarten zugeordneten Werte gesperrt sind. UI-Schriftarten werden zum Rendering von Benutzeroberflächen Elementen wie Beschriftungen, Dialogfeldern und Menüs verwendet. An diesen Schriftarten werden nur sehr wenige Änderungen vorgenommen, wenn Sie eine hohe Sichtbarkeit und häufige Verwendung haben. Da die gemeldeten Werte, die diesen Schriftarten zugeordnet sind, jedoch gesperrt sind, gibt es möglicherweise Abweichungen zwischen gemeldeten und tatsächlichen Schriftart Werten.

Die folgenden gemeldeten Werte sind für die Benutzeroberfläche und die Standard Schriftarten gesperrt und werden möglicherweise nicht korrekt berichtet:

-   Diese Werte aus der Tabelle " [OS/2](https://www.microsoft.com/typography/otspec/os2.htm)" der Schriftart:
    -   xavgcharwidth
    -   stypolinegap
    -   stypoascender
    -   stypodescender
    -   Windows-upgraden
    -   Verwendung von ""
-   Der im Header der Schriftart festgelegte [unitsperem](https://www.microsoft.com/typography/otspec/head.htm) -Wert.
-   Werte aus der [Tabelle für vertikale Geräte Metriken (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
-   Die voraus Breite für einzelne Symbole

Im folgenden finden Sie eine Liste der Benutzeroberflächen Schriftarten, die mit Windows 8.1 ausgeliefert werden (von gesperrten Werten betroffen):

| Skriptname                   | Benutzeroberflächen Schriftart               |
|-------------------------------|-----------------------|
| Arabisch                        | Segoe UI              |
| Armenisch                      | Segoe UI              |
| Bangla (ehemals Bengalisch)     | Nirmala UI            |
| Bopomofo                      | Microsoft JhengHei UI |
| Braille                       | Segoe UI Symbol       |
| Buginesisch                      | Leelawadee UI         |
| Kanadische Aborigines-Silben | Gadugi                |
| Cherokee                      | Gadugi                |
| Koptisch                        | Segoe UI Symbol       |
| Chinesisch (vereinfacht)          | Microsoft YaHei UI    |
| Chinesisch (traditionell)         | Microsoft JhengHei UI |
| Kyrillisch                      | Segoe UI              |
| Devanagari                    | Nirmala UI            |
| Deseret                       | Segoe UI Symbol       |
| Ethiopic                      | Ebrima                |
| Georgisch                      | Segoe UI              |
| Glagolitisch                    | Segoe UI Symbol       |
| Go                        | Segoe UI Symbol       |
| Griechisch                         | Segoe UI              |
| Gujarati                      | Nirmala UI            |
| Gurmukhi                      | Nirmala UI            |
| Hebräisch                        | Segoe UI              |
| Alte kursiv Formatierung                    | Segoe UI Symbol       |
| Javanisch                      | Javanese-Text         |
| Japanisch                      | Meiryo-Benutzeroberfläche             |
| Kannada                       | Mirmala-Benutzeroberfläche            |
| Khmer                         | Leelawadee UI         |
| Koreanisch                        | Malgun Gothic         |
| Laotisch                           | Leelawadee UI         |
| Lateinisch                         | Segoe UI              |
| Malayalam                     | Nirmala UI            |
| Mongolisch                     | Mongolisches Baiti       |
| Myanmar                       | Myanmar Text          |
| N ' Ko                          | Ebrima                |
| Ogam                         | Segoe UI Symbol       |
| Ol Chiki                      | Nirmala UI            |
| Altes Turkisch                    | Segoe UI Symbol       |
| Odia (früher Oriya)         | Nirmala UI            |
| Osmanya                       | Ebrima                |
| Phags-pa                      | Microsoft PhagsPa     |
| Runisch                         | Segoe UI Symbol       |
| Sora sompg                  | Nirmala UI            |
| Singhalesisch                       | Nirmala UI            |
| Syrisch                        | Estrangelo Edessa     |
| Tai-Le                        | Microsoft Tai Le      |
| Neue Tai-Lue                   | Microsoft Neu-Tai-Lue |
| Tamilisch                         | Nirmala UI            |
| Telugu                        | Nirmala UI            |
| Tifinagh                      | Ebrima                |
| Thaana                        | MV Boli               |
| Thailändisch                          | Leelawadee UI         |
| Tibetisch                       | Microsoft Himalaya    |
| Vai                           | Ebrima                |
| Yi                            | Microsoft Yi Baiti    |



 

Im folgenden finden Sie eine Liste der Legacy-Benutzeroberflächen Schriftarten, die ebenfalls von gesperrten Werten betroffen sind:

| Skript Name (Legacy)          | Benutzeroberflächen Schriftart (Legacy)               |
|-------------------------------|--------------------------------|
| Bangla (ehemals Bengalisch)     | Vrinda                         |
| Kanadische Aborigines-Silben | Euphemia                       |
| Cherokee                      | Plantagenet                    |
| Chinesisch (vereinfacht)          | Microsoft YaHei und Simsun     |
| Chinesisch (traditionell)         | Mingliu und Microsoft jhenghei |
| Devanagari                    | Mangal                         |
| Europäische Sprachen            | Tahoma                         |
| Gujarati                      | Strauch                         |
| Gurmukhi                      | Raavi                          |
| Japanisch                      | Meiryo und MS Gothic UI        |
| Kannada                       | Tunga                          |
| Khmer                         | Khmer                          |
| Koreanisch                        | Gulim                          |
| Laotisch                           | Laos-Benutzeroberfläche                         |
| Malayalam                     | Kartika                        |
| Mittlere Osten (Sprachen)      | Tahoma                         |
| Odia (früher Oriya)         | Kalinga                        |
| Singhalesisch                     | Iskoola Pota                   |
| Tamilisch                         | Latha und Vijaya               |
| Telugu                        | Gautami                        |
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

### <a name="dynamic-font-metrics"></a>Dynamische Schriftart Metriken

Abgesehen von den oben aufgeführten gesperrten Metriken werden die Schriftart Werte genau gemeldet. Wenn eine Schriftart in einer neuen Version von Windows geändert wird, unterscheiden sich die dynamischen Schriftart Werte zwischen den neuen und alten. Wenn z. b. einer Schriftart ein Symbol hinzugefügt wird, können sich die Werte im Header der Schriftart ändern. Das Clipping könnte dazu führen, dass diese Werte (z. b. xmin, xmax, ymin und ymax) gesperrt sind und die Mindest-und Maximalwerte für Symbole in der Schriftart melden.

> [!IMPORTANT]
> Wenn Sie in Ihrer APP dynamische Schriftart Werte verwenden (z. b. in [**TextMetric**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)), ändern sich diese Werte, wenn die Schriftarten in zukünftigen Versionen von Windows geändert werden. Verwenden Sie diese tatsächlichen Werte nicht in Situationen, in denen Text statisch bleiben muss.

 

## <a name="guidelines-for-using-font-metrics"></a>Richtlinien zum Verwenden von Schriftart Metriken

-   Computebildschirm-Metriken und Schriftart Metriken (z. b. durchschnittliche Breite) beim Starten einer APP, und verwenden diese Werte, um Ihre APP zu entwerfen. Dadurch wird ein konsistentes Rendering bereitgestellt, und Ihr Layout antwortet auf Änderungen in Schriftarten oder auf den Schriftart Fall Back. Eine Übersicht über die Schriftart-Fall Back und die Schriftart Verknüpfung finden Sie unter [Globalisierung Schritt für Schritt: Schriftarten](https://msdn.microsoft.com/goglobal/bb688134.aspx). Weitere Informationen finden [Sie unter Verwenden von Schriftart fallback](/windows/desktop/Intl/using-font-fallback) für uniscrispezifische Informationen.
    -   Um eine Basis Metrik zu berechnen, müssen Sie repräsentativen Text für Ihre beabsichtigte Sprache/Ihr Skript Rendering.
    -   Legen Sie für Steuerelemente, die nur eine einzelne Zeile mit nicht umschließtem Text enthalten, diese an die vollständige Breite des nicht gekürzten Texts an.
    -   Bei Steuerelementen mit mehreren Zeilen wird die Gesamtlänge, dividiert durch die Zeichen Länge, angezeigt, und Sie haben eine solide Breite, mit der Sie arbeiten können. Beachten Sie, dass dies für komplexe Skripts, bei denen ein einzelnes ' Zeichen ' für den Reader mehrere Code Punkte sein kann, kniffliger ist.
-   Verwenden Sie stypoascender, stypodescender und unitsperem (aus der [Tabelle OS/2](https://www.microsoft.com/typography/otspec/os2.htm)), um den vertikalen Abstand zu berechnen. "stypoascender" wird verwendet, um den optimalen Offset von der obersten Position eines Textframes bis zur ersten Baseline zu bestimmen, und "stypodescender" bestimmt den optimalen Offset vom unteren Rand eines Textframes bis zur letzten Baseline.
-   Wenn Sie DirectWrite verwenden, erstellen Sie ein Layout mit [**idschreitetextlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout). **Idwrite tetextlayout** stellt **den** Vorgänger-  +    +  **linegap** im natürlichen Layout bereit. Sie können auf diese spezifischen Werte mit [**dwrite- \_ Schriftart \_ Metriken**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)zugreifen. Informationen zu dieser Schnittstelle finden Sie unter [Text Formatierung und Layout](/windows/desktop/DirectWrite/text-formatting-and-layout).
-   Wenn Sie GDI verwenden, Rendern Sie den Bildschirm aus, und überprüfen Sie dann das Layout (z. b. die Zeilenlänge oder die Zeichen pro Zeile), und berechnen Sie die endgültigen Layoutparameter, die beim tatsächlichen Rendering verwendet werden.
-   Erstellen Sie keine Layouts statisch basierend auf bestimmten Werten für bestimmte Versionen von Schriftarten. Die tatsächlichen Werte können sich von Release zu Release ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[**Idschreitetextlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**\_Schriftart Metriken für dwrite \_**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)
</dt> <dt>

[**Textmetrik**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)
</dt> <dt>

[unitsperem](https://www.microsoft.com/typography/otspec/head.htm)
</dt> <dt>

[OS/2-Tabelle](https://www.microsoft.com/typography/otspec/os2.htm)
</dt> <dt>

[Tabelle für vertikale Geräte Metriken (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
</dt> <dt>

[Microsoft-Typografie: Schriftarten nach Produkt oder Familie](https://www.microsoft.com/typography/fonts/default.aspx)
</dt> <dt>

**Licher**
</dt> <dt>

[Textmetriken (DirectWrite)](/windows/desktop/DirectWrite/text-metrics)
</dt> <dt>

[Schriftarten und Text (GDI)](/windows/desktop/gdi/fonts-and-text)
</dt> <dt>

[Microsoft Typografie](https://www.microsoft.com/typography/default.mspx)
</dt> </dl>

 

 