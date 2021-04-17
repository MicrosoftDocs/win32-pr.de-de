---
title: Übersicht über den uiless-Modus
description: Übersicht über den uiless-Modus
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- Text Services-Framework (TSF), uilessmode
- TSF (Text Services Framework), uilessmode
- TSF-aktivierte Anwendungen, uilessmode
- Uilessmode
- Text Services-Framework (TSF), Kandidatenliste UIElement
- TSF (Text Dienst Framework), Kandidatenliste UIElement
- TSF-aktivierte Anwendungen, Kandidatenliste UIElement
- Kandidatenliste UIElement
- Text Services-Framework (TSF), UIElement-Tipp
- TSF (Text Dienste-Framework), UIElement-Tipp
- TSF-aktivierte Anwendungen, UIElement-Tipp
- UIElement-Tipp
- Text Dienst Framework (TSF), vordefinierte Benutzeroberflächen Elemente
- TSF (Text Services Framework), vordefinierte Benutzeroberflächen Elemente
- TSF-aktivierte Anwendungen, vordefinierte Benutzeroberflächen Elemente
- vordefinierte Benutzeroberflächen Elemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7354a88fb28fd0d6bf5f4180ac23359a2117fe7
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104551872"
---
# <a name="uiless-mode-overview"></a>Übersicht über den uiless-Modus

## <a name="how-to-create-uilessmode"></a>Erstellen von uilessmode

**Thread lose Thread für die Benutzeroberfläche:** Die Anwendung kann einen Benutzeroberflächen losen Thread durch [**itfthreadmgrex:: activateex**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) mit der ITF \_ AE \_ uielementenabledonly erstellen. Wenn threadmgr mit diesem Flag aktiviert wird, werden nur Tipps, die das UI-Element steuern können, im Thread aktiviert. Die Anwendung muss die [**itfuielementsink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) -Schnittstelle implementieren und der Schnittstelle den Thread-Manager anweisen. [**Itfuielementsink:: beginuielement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) wird aufgerufen, wenn Tip die Benutzeroberfläche anzeigt. Die Anwendung kann in pbshow param den Wert **true** zurückgeben, damit Tip die ursprüngliche Benutzeroberfläche von Tip anzeigen kann, wenn die Anwendung nicht gezeichnet werden soll. Wenn die Anwendung die Benutzeroberfläche von Tip nicht zulässt, kann Sie in "pbshow" den Wert " **false** " zurückgeben (siehe Diagramme unten). Die Anwendung kann die Benutzeroberfläche selbst zeichnen, indem Sie einige Informationen aus dem *pelement* -Parameter erhält. Dabei kann es sich um die Kandidatenliste, das sprach leisten Element oder die benutzerdefinierte Benutzeroberfläche von Tip handeln. Die Anwendung kann die Art der Benutzeroberfläche durch die Verwendung der [**itfuielement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) -Schnittstelle kennen. Wenn die Benutzeroberfläche geändert wird, wird [**itfuielementsink:: updateuielement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) aufgerufen. Die Anwendung kann die GUID von pelement->GetGuid () vergleichen, um zu ermitteln, ob das Element zurzeit von der Anwendung gezeichnet wird.

**Tipps für die Benutzeroberflächen lose Erkennung:** Tip sollte den Modus für Benutzeroberflächen weniger unterstützen, wenn er unter der Anwendung ausgeführt werden soll, die die Benutzeroberfläche von Tipps, wie z. b. Spiele Anwendungen oder Vollbildanwendungen, nicht zulassen möchte. Um die Benutzeroberfläche weniger zu beachten, muss Tip die [**itftextinputprocessorex**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) -Schnittstelle implementieren. Wenn diese Schnittstelle nicht implementiert ist, wird Tip nicht im Thread für die Benutzeroberflächen lose Modus aktiviert. Außerdem muss Tip " [**itfuielementmgr:: beginuielement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) " aufrufen, bevor eine sichtbare Benutzeroberfläche auf dem Bildschirm angezeigt wird. Mit dieser Methode wird [**itfuielementsink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) aufgerufen, um die Anwendung zu benachrichtigen. Und die Anwendung entscheidet, ob Sie angezeigt werden kann oder nicht. Wenn Tip "beginuielement ()" aufruft, muss Tip über die [**itfuielement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) -Schnittstelle für die zugehörige Benutzeroberfläche verfügen. Die Anwendung übernimmt die-Schnittstelle, um eine weitere Benutzeroberflächen spezifische Schnittstelle zum Abrufen weiterer Informationen zum Zeichnen der Benutzeroberfläche abzurufen. System vordefiniert [**ITF candidatelistuielement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) und [**itfreadinginformationuielement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) für Tip. Wenn Tip die Kandidatenliste im Thread der Benutzeroberflächen losen Modus anzeigen möchte, muss Tip eine Instanz der **itfcandidatelistuielement** -Schnittstelle erstellen und **itfuielementmgr:: beginuielement** aufrufen. Wenn [**itftextinputprocessorex:: activateex**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) aufgerufen wird, weiß Tip bereits, dass es sich bei dem Thread um eine Benutzeroberfläche handelt, sodass die zusätzliche benutzerdefinierte Benutzeroberfläche eliminiert werden kann. Es kann jedoch auch eine eigene Schnittstelle implementieren, von der aus qied erfolgen kann, und es wird versucht, eine Benachrichtigung zu erstellen. Daher können Tip und die".....................

## <a name="uielement-supporting-tip"></a>UIElement-Unterstützungs Tipp

Der Tipp, der das UIElement unterstützt, muss von GUID \_ tfcat \_ tipcap \_ uielementaktivierte kategorisiert werden. Der Tipp in GUID \_ tfcat \_ tipcap \_ uielementaktivierten muss [**itfuielementmgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) verwenden, um eine beliebige Benutzeroberfläche anzuzeigen, damit die Anwendung die Sichtbarkeit der Benutzeroberfläche steuern kann.

**Status von UIElement anzeigen/ausblenden:** Status anzeigen/ausblenden, der durch [**itfuielement:: Show**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) oder [**itfuielement:: isshow**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) -Methode angegeben wird, ist der tatsächliche sichtbare Status. Sie steht nicht im Zusammenhang mit der Verfügbarkeit von UIElement. "UIElement" sollte immer verfügbar sein, wenn der Status "anzeigen" vorhanden ist. Der Status anzeigen ist für die Anwendung steuerbar. Die Anwendung kann plötzlich in den uiless-Modus wechseln und mit dem Zeichnen der Benutzeroberfläche beginnen, indem **itfuielement:: Show** mit **false** aufgerufen wird, um die gesamte Benutzeroberfläche von Tip auszublenden. Tip kann eine der Optionen nutzen. 1) Tip kann das UIElement in den Status "ausblenden" verschieben und mit dem Erstellen von "updateuielement" beginnen. 2) Tip kann UIElement Fertigstellen, da das Benutzeroberflächen Element das Ausblenden von Status und Tip-aufrufen enduielement () nicht unterstützt, um es abzuschließen.

## <a name="predefined-ui-elements"></a>Vordefinierte Benutzeroberflächen Elemente

**Die Kandidatenliste:** Die Kandidatenliste ist eines der wichtigsten Benutzeroberflächen Elemente für EA-Eingaben. Dieses Benutzeroberflächen Element stellt die Kandidatenliste und die entsprechende Anzahl der Kandidaten Zeichenfolgen für das Zeichnen bereit.

**Das Fenster "Lese Informationen** " Das Fenster "Lese Informationen" ist für die chinesische Tastatureingabe üblich. Diese Phase kann nicht als Kompositions Zeichenfolge in das Dokument eingefügt werden. Ein chinesischer Eingabe Prozessor öffnet ein kleines Lese Informationsfenster, in dem die Informationen zu lesen, phonetisch oder Typisierung angezeigt werden.

## <a name="the-flow-chart-of-uilessmode"></a>Flussdiagramm von uilessmode

![Diagramm, das das Flussdiagramm "U I lessmode" anzeigt.](images/tsf-uilessmode-ovw1.gif)

Nachdem der Tipp in  \* pbas von [**itfuielementmgr:: beginuielement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement)true empfangen hat, muss der Tipp updateuielement für das UIElement nicht aufrufen. Tip muss jedoch "enduielement ()" anrufen, damit [**itfuielementmgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) und die Anwendung den Status von "UIElement" nachverfolgen können. Tip muss updateuielement () aufrufen, nachdem beginuielement () in pbshow **false** zurückgegeben hat \* . Die Anwendung, die die Benutzeroberfläche zeichnen möchte, überprüft den Inhalt in beginuielement () nicht. Sie gibt lediglich den Show-Status bei beginuielement () zurück und beginnt mit der Überprüfung des Inhalts bei updateuielement (). Das updateflag der Kandidatenliste UIElement enthält z. b. alle Bits am ersten updateuielement (). Dies bedeutet, dass der Inhalt von UIElement bei beginuielement () nicht bereit sein muss.

![Das Diagramm, das anzeigt, wann das T I P "ituielementmgr:: beginuielement ()" und "beginuielement" der uielementsink der Anwendung aufruft, wird aufgerufen.](images/tsf-uilessmode-ovw2.gif)![Das Diagramm, das anzeigt, dass die Anwendung in * pbshow false zurückgibt.](images/tsf-uilessmode-ovw3.gif)![uilessmode-Flussdiagramm](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>Das UIElement der Kandidatenliste.

**Informationen zu pageingedex:** Die Anwendung, die die Kandidatenliste zeichnet, berechnet die Anzahl der Zeichen folgen pro Seite, wenn der Inhalt der Liste geändert wird (die TF- \_ cluie- \_ Zeichenfolge ist festgelegt). Es ist nicht sinnvoll, den Seitenindex zu ändern, während die Kandidatenliste für den uiless-Modus verfügbar ist. Dies bedeutet, dass sich die Liste der Tipps beim Paging Verhalten sollte, anstatt einen Bildlauf durchführen zu müssen, wenn die Auswahl auf die nächste Seite verschoben wird. Wenn der scrollvorgang bei der Auswahl verschoben wird, wird der Seitenindex geändert, und die Anwendung muss den Seitenindex neu berechnen. Das Ergebnis wird möglicherweise nicht von Tip erwartet.

**Keine Auswahl:** [**ITF candidatelistuielement:: GetSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) gibt S \_ false zurück, wenn die Kandidatenliste keine Auswahl hat. Der Rückgabewert des ersten Parametern ist ungültig.

 

 




