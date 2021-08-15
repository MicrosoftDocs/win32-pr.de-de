---
title: Übersicht über den UILess-Modus
description: Übersicht über den UILess-Modus
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- Textdienstframework (TSF), UILessMode
- TSF (Textdienstframework),UILessMode
- TSF-fähige Anwendungen, UILessMode
- UILessMode
- Textdienstframework (TSF),UiElement für Kandidatenliste
- TSF (Textdienstframework),Kandidatenliste UIElement
- TSF-fähige Anwendungen, Kandidatenliste UIElement
- CANDIDATE LIST UIElement
- Textdienstframework (TSF),UIElement TIP
- TSF (Textdienstframework),UIElement TIP
- TSF-fähige Anwendungen, UIElement TIP
- UIElement TIP
- Textdienstframework (TSF), vordefinierte Benutzeroberflächenelemente
- TSF (Textdienstframework), vordefinierte UI-Elemente
- TSF-fähige Anwendungen, vordefinierte UI-Elemente
- Vordefinierte Benutzeroberflächenelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdac8e43cc8342c50a6d232b801af0c65315fd407b9f413f2b5fdcb7074282fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949863"
---
# <a name="uiless-mode-overview"></a>Übersicht über den UILess-Modus

## <a name="how-to-create-uilessmode"></a>Erstellen von UILessMode

**Erstellen eines threadfreien Threads ohne Benutzeroberfläche:** Die Anwendung kann einen Ui Less Thread von [**ITfThreadMgrEx::ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) mit ITF \_ AE \_ UIELEMENTENABLEDONLY erstellen. Wenn ThreadMgr mit diesem Flag aktiviert wird, werden nur TIPs aktiviert, die das Ui-Element steuern können. Die Anwendung muss die [**ITfUIElementSink-Schnittstelle**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) implementieren und die Schnittstelle im Thread-Manager empfehlen. [**ITfUIElementSink::BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) wird aufgerufen, wenn TIP seine Benutzeroberfläche anzeigt. Die Anwendung kann **TRUE** im pbShow-Parameter zurückgeben, damit TIP die ursprüngliche Benutzeroberfläche von TIP anzeigen kann, wenn die Anwendung nicht zeichnen möchte. Wenn die Anwendung die Benutzeroberfläche von TIP nicht zulässt, kann sie **FALSE** in pbShow zurückgeben (siehe Diagramme unten). Die Anwendung kann die Benutzeroberfläche selbst zeichnen, indem sie einige Informationen aus dem *pElement-Parameter* erhält. Dies kann die Kandidatenliste, das Sprachleistenelement oder die benutzerdefinierte Benutzeroberfläche von TIP sein. Die Anwendung kann die Art der Benutzeroberfläche durch QIing [**ITfUIElement-Schnittstelle**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) kennen. Wenn die Benutzeroberfläche geändert wird, wird [**ITfUIElementSink::UpdateUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) aufgerufen. Die Anwendung kann die GUID von pElement->GetGUID() vergleichen, um zu wissen, ob das Element derzeit von der Anwendung gezeichnet wird.

**Machen Sie benutzeroberflächenfreie TIPPS:** TIP sollte den Benutzeroberflächenmodus unterstützen, wenn er unter der Anwendung ausgeführt werden soll, die die Benutzeroberfläche von TIP nicht zulassen soll, z. B. Spieleanwendung oder Vollbildanwendungen. Um die Benutzeroberfläche weniger zu berücksichtigen, muss TIP die [**ITfTextInputProcessorEx-Schnittstelle**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) implementieren. Wenn diese Schnittstelle nicht implementiert ist, wird TIP nicht unter dem Ui Less Mode-Thread aktiviert. Darüber hinaus muss TIP [**ITFUIElementMgr::BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) aufrufen, bevor eine sichtbare Benutzeroberfläche auf dem Bildschirm angezeigt wird. Diese Methode ruft [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) auf, um die Anwendung zu benachrichtigen. Und die Anwendung entscheidet, ob sie angezeigt werden kann oder nicht. Wenn TIP BeginUIElement() aufruft, muss TIP über die [**ITfUIElement-Schnittstelle**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) für die entsprechende Benutzeroberfläche verfügen. Die Anwendung ruft die Schnittstelle ab, um eine andere benutzeroberflächenspezifische Schnittstelle abzurufen, um weitere Informationen zum Zeichnen der Benutzeroberfläche abzurufen. Systemdefiniert [**ITfCandidateListUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) und [**ITfReadingInformationUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) für TIP. Wenn TIP die Kandidatenliste unter dem Ui-Less Mode-Thread anzeigen möchte, muss TIP eine Instanz der **ITfCandidateListUIElement-Schnittstelle** erstellen und **ITFUIElementMgr::BeginUIElement** aufrufen. Wenn [**ITfTextInputProcessorEx::ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) aufgerufen wird, weiß TIP bereits, dass der Thread weniger benutzerdefiniert ist, sodass die zusätzliche benutzerdefinierte Benutzeroberfläche entfernt werden kann. Es kann jedoch eine eigene Schnittstelle implementieren, von der aus QIed erfolgen kann, und versuchen, eine Benachrichtigung zu erstellen. Daher können TIP und die **Appli ITfUIElement-Kation** über eine Aushandlung für die benutzerdefinierte TIP-Benutzeroberfläche verfügen.

## <a name="uielement-supporting-tip"></a>UIElement Supporting TIP

Der TIP, der UIElement unterstützt, muss nach GUID \_ TFCAT \_ TIPCAP UIELEMENTENABLED kategorisiert \_ werden. Der TIP in GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTABLED muss [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) verwenden, um eine beliebige Benutzeroberfläche anzuzeigen, damit die Anwendung die Sichtbarkeit der Benutzeroberfläche steuern kann.

**Anzeigen/Ausblenden des UiElement-Status:** Der durch [**die ITfUIElement::Show-**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) oder [**ITfUIElement::IsShown-Methode**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) angegebene Status wird angezeigt. Er bezieht sich nicht auf die Verfügbarkeit von UIElement. UIElement sollte immer verfügbar sein, wenn der Status anzeigen vorhanden ist. Der Show-Status kann von der Anwendung gesteuert werden. Die Anwendung wechselt möglicherweise plötzlich in den UILess-Modus und beginnt damit, eine Benutzeroberfläche selbst zu zeichnen, indem **sie ITfUIElement::Show** mit **FALSE** aufruft, um die gesamte Benutzeroberfläche von TIP auszublenden. Dann kann TIP eine der optionen auswählen. 1) TIP kann das UIElement in den Status Ausblenden verschieben und mit dem Generieren von UpdateUIElement beginnen. 2) TIP kann UIElement beenden, da das UI-Element den Status Ausblenden nicht unterstützt und Tip EndUIElement() aufruft, um es fertig zu stellen.

## <a name="predefined-ui-elements"></a>Vordefinierte UI-Elemente

**Die Kandidatenliste:** Die Kandidatenliste ist eines der wichtigsten Benutzeroberflächenelemente für EA-Eingaben. Dieses UI-Element stellt die Kandidatenliste und die entsprechende Anzahl der Kandidatenzeichenfolgen zum Zeichnen bereit.

**Das Fenster "Leseinformationen"** Das Leseinformationsfenster ist für die chinesische Tastatureingabe üblich. Sie verfügt über die Stufe, die nicht als Kompositionszeichenfolge in das Dokument eingefügt werden kann. Ein chinesischer Eingabeprozessor öffnet ein kleines Leseinformationsfenster, in dem die Lese-, phonetischen oder Typisierungsinformationen angezeigt werden.

## <a name="the-flow-chart-of-uilessmode"></a>Das Flussdiagramm von UILessMode

![Diagramm, das das U I LessMode-Flussdiagramm zeigt.](images/tsf-uilessmode-ovw1.gif)

Nachdem der TIP **true** in \* pbShown von [**ITfUIElementMgr::BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement)empfangen hat, muss der TIP updateUIElement nicht für das UIElement aufrufen. Tip muss jedoch EndUIElement() aufrufen, damit [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) und die Anwendung den Status von UIElement nachverfolgen können. TIP muss UpdateUIElement() aufrufen, nachdem BeginUIElement() in pbShow **FALSE** zurückgegeben \* hat. Die Anwendung, die die Benutzeroberfläche zeichnen möchte, überprüft nicht den Inhalt in BeginUIElement(). Sie gibt lediglich den Anzeigestatus unter BeginUIElement() zurück und beginnt mit der Überprüfung des Inhalts unter UpdateUIElement(). Das Updateflag der Kandidatenliste UIElement verfügt beispielsweise über alle Bits im ersten UpdateUIElement(). Dies bedeutet, dass der Inhalt von UIElement unter BeginUIElement() nicht bereit sein muss.

![Diagramm, das zeigt, wenn das T I P "ITUIElementMgr::BeginUIElement()" und "BeginUIElement of Application es UIElementSink" aufruft.](images/tsf-uilessmode-ovw2.gif)![Diagramm, das zeigt, dass die Anwendung FALSE in *pbShow zurückgibt.](images/tsf-uilessmode-ovw3.gif)![Flussdiagramm "uilessmode"](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>Das UIElement der Kandidatenliste

**Informationen zu PageIndex:** Die Anwendung, die die Kandidatenliste zeichnet, berechnet die Anzahl der Zeichenfolgen pro Seite, wenn der Inhalt der Liste geändert wird (TF \_ CLUIE \_ STRING ist festgelegt). Es ist nicht sinnvoll, den Seitenindex zu ändern, während die Kandidatenliste für den UILess-Modus verfügbar ist. Dies bedeutet, dass die Tip-Kandidatenliste das Paging verhalten sollte, anstatt zu scrollen, wenn die Auswahl auf die nächste Seite verschoben wird. Wenn der Bildlauf bei der Verschiebung der Auswahl erfolgt, wird der Seitenindex geändert, und die Anwendung muss den Seitenindex neu berechnen. Das Ergebnis wird von TIP möglicherweise nicht erwartet.

**Keine Auswahl:** [**ITfCandidateListUIElement::GetSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) gibt S \_ FALSE zurück, wenn die Kandidatenliste keine Auswahl hat. Der Rückgabewert des ersten Params ist ungültig.

 

 




