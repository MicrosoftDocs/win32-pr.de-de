---
title: Sprach Leiste (Text Dienste)
description: Sprach Leiste
ms.assetid: 82b92567-fdc1-488c-b395-4cb95257955c
keywords:
- Text Services-Framework (TSF), sprach Leiste
- TSF (Text Dienst Framework), sprach Leiste
- Text Dienste, sprach Leiste
- sprach Leiste
- Text Dienst Framework (TSF), Schaltflächen
- TSF (Text Dienst Framework), Schaltflächen
- Text Dienste, Schaltflächen
- Text Dienste-Framework (TSF), Menüs
- TSF (Text Dienste-Framework), Menüs
- Text Dienste, Menüs
- Schaltflächenstile
- Menü Schaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41d64a488406f6eefcff5fef6c11093af00bc5b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391459"
---
# <a name="language-bar-text-services"></a>Sprach Leiste (Text Dienste)

## <a name="implementing-the-language-bar-object"></a>Implementieren des Language Bar-Objekts

Um das Hinzufügen eines Elements zur sprach Leiste zu unterstützen, muss ein Text Dienst ein Objekt implementieren, das die [itfsource](/windows/desktop/api/msctf/nn-msctf-itfsource) -Schnittstelle und eines der [itflangbaritem](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem) -Steuerelement Elemente unterstützt. Wenn das Element installiert ist, installiert die sprach Leiste eine [itflangbaritemsink](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink) -Senke, indem das [itfsource:: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) -Element des Elements mit IID \_ itflangbaritemsink aufgerufen wird. Das Element verwendet die **itflangbaritemsink** -Schnittstelle, um die sprach Leiste von Änderungen zu benachrichtigen, z. b. wenn das Element ausgeblendet, angezeigt, aktiviert oder deaktiviert ist.

Es können vier Arten von sprach leisten Elementen installiert werden, und alle erforderlichen Schnittstellen werden aus **itslangbaritem** erstellt. Im folgenden finden Sie mögliche **itslangbaritem** -Steuerelemente.



|               |                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schaltfläche        | Eine sprach leisten Schaltfläche dient als Befehls Schaltfläche, UMSCHALT Steuerelement oder Menü auf der sprach Leiste. Das Objekt muss die itflangbaritembutton-Schnittstelle unterstützen.                   |
| Ballons       | Eine sprach leisten Sprechblase fungiert als Popup Benachrichtigung auf der sprach Leiste. Das Objekt muss die Schnittstelle itbolangbaritemballoon unterstützen.                                       |
| Bitmap        | Eine sprach leisten Bitmap fungiert als statisches Element auf der sprach Leiste, das eine Bitmap anzeigt. Das Objekt muss die itblangbaritembitmap-Schnittstelle unterstützen.                       |
| Bitmap-Schaltfläche | Eine Schaltfläche für eine sprach leisten-Bitmap fungiert als Schaltflächen Element auf der sprach Leiste, auf der Text und eine Bitmap angezeigt werden. Das Objekt muss die itflangbaritembitmapbutton-Schnittstelle unterstützen. |



 

## <a name="button-styles"></a>Schaltflächenstile

Ein Button-Element kann wie folgt funktionieren. Die Funktion des Schaltflächen Elements wird durch die Flags bestimmt, die im **dwstyle** -Member der [tf \_ langbariteminfo](/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo) -Struktur in der [itflangbaritem:: GetInfo](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo) -Methode festgelegt sind.



|               |                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schaltfläche        | Die Schaltfläche dient als Standard Befehls Schaltfläche. Dieser Schaltflächen Stil wird durch den Formatvorlagen Stil der TF-LBI-Formatvorlage identifiziert \_ \_ \_ \_ . Itflangbaritembutton:: OnClick wird aufgerufen, wenn auf das Element geklickt wird. Itflangbaritembutton:: InitMenu und itflangbaritembutton:: onmenuselect werden nicht verwendet.                                                                                                   |
| Umschaltfläche | Die Schaltfläche fungiert als UMSCHALT Steuerelement, das einen angeklickten Zustand beibehalten kann, ähnlich wie ein Kontrollkästchen. Dieser Schaltflächen Stil wird durch den TF \_ LBI- \_ Stil \_ BTN- \_ UMSCHALT Stil identifiziert. Itflangbaritembutton:: OnClick wird aufgerufen, wenn auf das Element geklickt wird. Itflangbaritembutton:: InitMenu und itflangbaritembutton:: onmenuselect werden nicht verwendet.                                                  |
| Menü          | Die Schaltfläche dient als Dropdown Menü. Dieser Schaltflächen Stil wird durch den Menü Stil für den TF \_ LBI- \_ Stil \_ BTN identifiziert \_ . Itflangbaritembutton:: InitMenu wird aufgerufen, wenn auf die Schaltfläche geklickt wird. Wenn der Benutzer ein Element im Menü auswählt, ruft die sprach Leiste itflangbaritembutton:: onmenuselect mit dem Bezeichner des ausgewählten Menü Elements auf. Itflangbaritembutton:: onclickis wird nicht verwendet. |



 

## <a name="implementing-a-menu-button"></a>Implementieren einer Menü Schaltfläche

Wenn der Benutzer auf eine Menü Schaltfläche klickt, ruft die sprach Leiste [itflangbaritembutton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu)auf. Das Element fügt dem Menü Elemente mithilfe der [itfmenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) -Schnittstelle hinzu, die an InitMenu übergeben wird.

Um dem Menü ein Untermenü hinzuzufügen, nennen Sie [itfmenu:: addmenuitem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) mit dem \_ unter Menü TF lbmenuf \_ . Wenn dies der Fall ist, wird ein neues **ITF Menu** -Objekt, das das Untermenü darstellt, im *ppmenu* -Parameter von addmenuitem zurückgegeben. Dieses neue Menü Objekt wird verwendet, um dem Untermenü Elemente hinzuzufügen.

Wenn der Benutzer ein Element im Menü auswählt, ruft die sprach Leiste [itflangbaritembutton:: onmenuselect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) mit dem Bezeichner des ausgewählten Menü Elements auf.

## <a name="adding-items-to-the-language-bar"></a>Hinzufügen von Elementen zur sprach Leiste

Ein Text Dienst sollte seine Elemente der sprach Leiste hinzufügen, wenn die [itftextinputprocessor:: Aktivierungs](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate) -Methode aufgerufen wird, und Sie entfernt werden, wenn [itftextinputprocessor::D eaktivierung](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate) aufgerufen wird.

Um der sprach Leiste ein Element hinzuzufügen, ruft der Text Dienst eine [itflangbaritemmgr](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr) -Schnittstelle ab, indem ITfThreadMgr:: QueryInterface mit IID \_ itflangbaritemmgr aufgerufen wird. Der Text Dienst ruft dann [itflangbaritemmgr:: AddItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem) mit dem Zeiger auf das sprach leisten Element-Objekt auf.

Der Text Dienst muss das Element entfernen, wenn es deaktiviert ist. Der Text Dienst verwendet die gleiche **itflangbaritemmgr** -Schnittstelle, die zum Hinzufügen der Elemente verwendet wird, oder ruft eine andere Instanz der Schnittstelle ab. Der Text Dienst ruft dann [itflangbaritemmgr:: RemoveItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-removeitem) mit dem Schnittstellen Zeiger des zu entfernenden Elements auf.

## <a name="extending-system-language-bar-items"></a>Erweitern von System sprach leisten Elementen

TSF bietet die Möglichkeit, vorhandenen sprach leisten Menüs Menü Elemente hinzuzufügen. Dadurch kann ein Text Dienst dem Menü eines anderen Text Dienstanbieter Elemente hinzufügen, ohne dass der Symbolleiste eine separate Schaltfläche hinzugefügt werden muss. Dadurch können die Menü Elemente auch in logische Gruppen unterteilt werden. Beispielsweise kann ein Text Dienst, der zusätzliche Funktionen für den Standard-sprach Text Dienst bereitstellt, dem sprach Text-Dienst Menü Elemente hinzufügen, anstatt seine eigene Menü Schaltfläche auf oberster Ebene hinzuzufügen.

Ein Text Dienst stellt eine sprach leisten-Menü Erweiterung bereit, indem er ein Objekt implementiert, das die [ITF systemlangbaritemsink](/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink) -Schnittstelle unterstützt. Diese Schnittstelle funktioniert genau wie die [itflangbaritembutton](/windows/desktop/api/Ctfutb/nn-ctfutb-itflangbaritembutton) -Schnittstelle für eine Menü Schaltfläche. Wenn das Menü angezeigt wird, ruft der Text Dienst, der erweitert wird, [ITF systemlangbaritemsink:: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu)auf. Die Erweiterung fügt dem Menü Elemente mithilfe der [itfmenu](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) -Schnittstelle hinzu, die an **InitMenu** übergeben wird. Wenn der Benutzer ein Element auswählt, das von der Erweiterung hinzugefügt wurde, ruft der Text Dienst, der erweitert wird, [ITF systemlangbaritemsink:: onmenuselect](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-onmenuselect) mit dem Bezeichner des ausgewählten Menü Elements auf.

Zum Installieren einer sprach leisten-Menü Erweiterung führt der Text Dienst die folgenden Schritte aus.

1.  Rufen Sie die **itflangbaritem** -Schnittstelle für das Element ab, das Sie erweitern möchten, indem Sie [itflangbaritemmgr:: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem) mit der **GUID** für das Element aufrufen, das erweitert werden soll.
2.  Rufen Sie die **itfsource** -Schnittstelle für das Element ab, das durch Aufrufen von itflangbaritem:: QueryInterface mit IID \_ itfsource erweitert werden soll.
3.  Aufrufen von [itfsource:: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) mit IID \_ itfsystemlangbaritemsink und dem Zeiger auf das **itfsystemlangbaritemsink** -Objekt. Wenn ITF Source:: AdviseSink fehlschlägt, unterstützt der Text Dienst keine Menü Erweiterungen.

[ITF Source:: unadvisesink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink)**ITF Source:: AdviseSink**

## <a name="supporting-language-bar-menu-extensions"></a>Unterstützende sprach leisten-Menü Erweiterungen

Ein Text Dienst kann anderen Text Diensten das Hinzufügen von Elementen zu den sprach leisten Menüs ermöglichen, wie oben gezeigt. Der Text Dienst, der seine GUID veröffentlichen muss, damit das Element durch Aufrufen von [itflangbaritemmgr:: GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem)abgerufen werden kann.

Um Menü Erweiterungen zu unterstützen, muss der Text Dienst die [itfsource](/windows/desktop/api/msctf/nn-msctf-itfsource) -Schnittstelle unterstützen. Die folgenden Schritte ermöglichen die Unterstützung für eine oder mehrere Menü Erweiterungen.

1.  Wenn [itfsource:: AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) mit IID \_ itfsystemlangbaritemsink aufgerufen wird, muss der Text Dienst die **itfsystemlangbaritemsink** -Schnittstelle speichern und einen Cookie-Wert zurückgeben, der die Erweiterung identifiziert.
2.  Wenn [itflangbaritembutton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) aufgerufen wird, ruft der Text Dienst die [itfsystemlangbaritemsink:: InitMenu](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu) -Methode der Erweiterung auf. Der Text Dienst muss eine Methode implementieren, um die von der Erweiterung hinzugefügten Menü Elemente im Gegensatz zu den Elementen, die durch den Text Dienst selbst hinzugefügt wurden, zu identifizieren.
3.  Wenn [itflangbaritembutton:: onmenuselect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) mit einem Menü Element Bezeichner aufgerufen wird, der zu einer Erweiterung gehört, ruft der Text Dienst die **itfsystemlangbaritemsink:: onmenuselect** -Methode der Erweiterung auf.
4.  Wenn [itfsource:: unadvisesink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink) mit dem entsprechenden Cookie aufgerufen wird, entfernt der Text Dienst die Menü Erweiterung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten des Text Dienst-Frameworks](how-to-set-up-tsf.md)
</dt> <dt>

[Sprach Leiste (Anwendungen)](language-bar-app.md)
</dt> </dl>

 

 
