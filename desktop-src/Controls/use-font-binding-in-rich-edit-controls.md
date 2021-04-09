---
title: Verwenden der Schriftart Bindung in Rich Edit-Steuerelementen
description: Microsoft Rich Edit 3,0 weist in Abhängigkeit von ihrem Kontext einen Zeichensatz für einfache Textzeichen zu.
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17c2f8e0e8c1b57611839a5bbf992f9af6bf65
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103858108"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>Verwenden der Schriftart Bindung in Rich Edit-Steuerelementen

Microsoft Rich Edit 3,0 weist in Abhängigkeit von ihrem Kontext einen Zeichensatz für einfache Textzeichen zu. Hier einige Beispiele:

-   Griechischen Zeichen wird ein **griechisches Zeichen \_ Satz** zugewiesen.
-   Hangul-Symbolen wird **Hangul \_ CharSet** zugewiesen.
-   Chinesischen Zeichen wird **ShiftJIS \_ CharSet** zugewiesen, wenn Kana-Zeichen in der Nähe gefunden werden, oder **GB2312 \_ CharSet** , wenn in der Nähe keine Kana gefunden werden.
-   Nicht neutralen ANSI-Zeichen wird in jedem Ereignis **ANSI \_ CharSet** zugewiesen.

> [!Note]  
> Das Rich Edit-Steuerelement verwendet intern Unicode, sodass sich diese Verwendung von Zeichensätzen von dem ursprünglichen unterscheidet, das in Schriftart Spezifikationen verwendet wird. Die [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -Struktur verfügt jedoch über einen klar definierten Speicherort für den Zeichensatz.

 

Neutralen Zeichen, wie z. b. Leerzeichen und Ziffern, wird ein Zeichensatz abhängig von ihrem Kontext zugewiesen. Beispielsweise wird dieser Zeichensatz durch ein leeres Zeichen, das von Zeichen aus demselben Zeichensatz umgeben ist, abgerufen. Den für bidirektionalen Text verwendeten neutralen und Ziffern werden Zeichensätze auf eine Weise zugewiesen, die auf dem bidirektionalen Unicode-Algorithmus basiert.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-font-binding-in-a-rich-edit-control"></a>Verwenden der Schriftart Bindung in einem Rich-Edit-Steuerelement

Nachdem Zeichensätze zugewiesen wurden, scannt Rich Edit den Text um die Einfügemarke vorwärts und rückwärts, um die nächstgelegenen Schriftarten zu finden, die für die Zeichensätze verwendet wurden. Wenn für einen Zeichensatz keine Schriftart gefunden wird, verwendet Rich Edit die Schriftart, die vom Client für diesen Zeichensatz ausgewählt wurde. Wenn der Client keine Schriftart für den Zeichensatz angegeben hat, verwendet Rich Edit die Standard Schriftart für diesen Zeichensatz. Wenn der Client eine andere Schriftart benötigt, kann er vom Client immer geändert werden, aber dieser Ansatz funktioniert meistens. Die aktuellen Standardoptionen für die Schriftart basieren auf der folgenden Tabelle. Beachten Sie, dass die Standard Schriftarten pro Prozess festgelegt sind, und es gibt separate Listen für die Verwendung der Benutzeroberfläche und für nicht-UI-Verwendung.



| Sprache                    | Name der Benutzeroberflächen Schriftart  | Größe der Benutzeroberflächen Schriftart | nicht-UI-Schriftart Name | nicht-UI-Schriftgröße |
|-----------------------------|---------------|--------------|------------------|------------------|
| West, CE, me, Vietnamese | Tahoma        | 8            | Arial            | 10               |
| Japanisch                    | MS UI-Gotik  | 9            | MS P-Gotik      | 10               |
| Koreanisch                      | Gulim         | 9            | Gulim            | 9                |
| Chinesisch (vereinfacht)          | Simsun        | 9            | SimSun           | 10               |
| Chinesisch (traditionell)         | PMingLiu      | 9            | PMingLiu         | 9                |
| Thailändisch                        | MS Sans Serif | 8            | Tahoma           | 14               |
| Symbole                     | Wingdings     | 8            | Wingdings        | 10               |
| Devanagari                  | Mangal        | 8            | Mangal           | 10               |
| Tamilisch                       | Latha         | 8            | Latha            | 10               |
| Georgisch, Armenisch          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

In der standardmäßigen Schriftart Bindungs Tabelle (Einträge haben beispielsweise einen Zeichensatz, einen Schriftart Namen und eine Größe), ermöglicht Rich Edit \_ dem ANSI-charset, eine Übereinstimmung mit mehreren Zeichensätzen zu erreichen, während der entsprechende Zeichensatz mit anderen Schriftarten von eins zu eins übereinstimmt. Genauer gilt, dass Rich Edit die ANSI-Zeichen \_ Satz Auswahl verwendet, wenn keine anderen Alternativen gefunden werden. Sie sind in der Lage, eine präzisere Granularität anzugeben, als dies der Fall ist. Weisen Sie z. b. einen bestimmten arabischen \_ Satz für arabische Ausführungen, eine bestimmte Griechisch-Schriftart für griechische Ausführungen usw. zu. Diese präzisere Granularität wird auch verwendet, wenn eine Schriftart mit dem gewünschten Zeichensatz an einer Stelle im Dokument vor dem Bereich gefunden wird, der Schriftart gebunden ist.

Beachten Sie, dass Rich Edit zurzeit kein fehlendes Symbol in einer Schriftart behandelt, die vorgibt, einen Zeichensatz zu unterstützen, aber unvollständig ist. Zum Zeitpunkt der Anzeige in einem komplexen Skript wird bei der umfassenden Bearbeitung feststellt, dass ein solches Symbol fehlt, aber es bewirkt nicht, dass der Sicherungs Speicher eine neue Schriftart verwendet. Normalerweise wird dies durch die zugrunde liegende Schriftart Verknüpfung des Betriebssystems erreicht.

## <a name="remarks"></a>Bemerkungen

**Rich Edit 4,1:** Um die Standard Schriftart für ein Skript festzulegen, müssen Sie [**EM \_ setcharformat**](em-setcharformat.md) mit [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)aufrufen, indem Sie Werte für die Member **yHeight**, **bcharset**, **bpitchandfamily**, **szfakename** und **LCID** angeben. Wenn Sie die Standard Schriftart für eine bestimmte Codepage abrufen möchten, müssen Sie außerdem [**EM \_ getcharformat**](em-getcharformat.md) mit **CHARFORMAT2** aufrufen und Werte für das **bcharset** -und das **LCID** -Element angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




