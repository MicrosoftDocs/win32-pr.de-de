---
title: Sprachleiste (Textdienste)
description: Sprachleiste
ms.assetid: 82b92567-fdc1-488c-b395-4cb95257955c
keywords:
- Textdienstframework (TSF), Sprachleiste
- TSF (Textdienstframework),Sprachleiste
- Textdienste, Sprachleiste
- Sprachleiste
- Textdienstframework (TSF), Schaltflächen
- TSF (Textdienstframework),Schaltflächen
- Textdienste,Schaltflächen
- Textdienstframework (TSF), Menüs
- TSF (Textdienstframework),Menüs
- Textdienste,Menüs
- Schaltflächenstile
- Menüschaltflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9ea3224e29028955e1d838356d39a9e12417c267dc84bfac6b88b6d1293b3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952118"
---
# <a name="language-bar-text-services"></a>Sprachleiste (Textdienste)

## <a name="implementing-the-language-bar-object"></a>Implementieren des Sprachleistenobjekts

Um das Hinzufügen eines Elements zur Sprachleiste zu unterstützen, muss ein Textdienst ein Objekt implementieren, das die [ITfSource-Schnittstelle](/windows/desktop/api/msctf/nn-msctf-itfsource) und eines der [ITfLangBarItem-Steuerelementelemente](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritem) unterstützt. Wenn das Element installiert ist, installiert die Sprachleiste eine [ITfLangBarItemSink-Senke,](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemsink) indem [ITfSource::AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) mit IID \_ ITfLangBarItemSink des Elements aufruft. Das Element verwendet die **ITfLangBarItemSink-Schnittstelle,** um die Sprachleiste über Änderungen zu benachrichtigen, z. B. wenn das Element ausgeblendet, angezeigt, aktiviert oder deaktiviert ist.

Vier Arten von Sprachleistenelementen können installiert werden, und jede der erforderlichen Schnittstellen wird aus **ITfLangBarItem erstellt.** Im Folgenden finden Sie mögliche **ITfLangBarItem-Steuerelementelemente.**



|   Element            |    Beschreibung                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schaltfläche        | Eine Sprachleistenschaltfläche fungiert als Befehlsschaltfläche, Umschaltsteuerelement oder Menü auf der Sprachleiste. Das -Objekt muss die ITfLangBarItemButton-Schnittstelle unterstützen.                   |
| Ballon       | Ein Sprachleistensprechblasen fungiert als Popupbenachrichtigung auf der Sprachleiste. Das -Objekt muss die ITfLangBarItemBalloon-Schnittstelle unterstützen.                                       |
| Bitmap        | Eine Sprachleistenbitmap fungiert als statisches Element auf der Sprachleiste, die eine Bitmap anzeigt. Das -Objekt muss die ITfLangBarItemBitmap-Schnittstelle unterstützen.                       |
| Bitmapschaltfläche | Eine Bitmapschaltfläche der Sprachleiste fungiert als Schaltflächenelement auf der Sprachleiste, in der Text und eine Bitmap angezeigt werden. Das -Objekt muss die ITfLangBarItemBitmapButton-Schnittstelle unterstützen. |



 

## <a name="button-styles"></a>Schaltflächenstile

Ein Schaltflächenelement kann wie folgt funktionieren. Die Funktion des Schaltflächenelements wird durch die Flags bestimmt, die im **dwStyle-Member** der [TF \_ LANGBARITEMINFO-Struktur](/windows/desktop/api/ctfutb/ns-ctfutb-tf_langbariteminfo) in der [ITfLangBarItem::GetInfo-Methode festgelegt](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritem-getinfo) sind.



|    Element           |    Beschreibung                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schaltfläche        | Die Schaltfläche fungiert als Standardbefehlsschaltfläche. Dieses Schaltflächenformat wird durch den TF \_ LBI \_ STYLE \_ BTN \_ BUTTON-Stil identifiziert. ITfLangBarItemButton::OnClick wird aufgerufen, wenn auf das Element geklickt wird. ITfLangBarItemButton::InitMenu und ITfLangBarItemButton::OnMenuSelect werden nicht verwendet.                                                                                                   |
| Umschaltfläche | Die Schaltfläche fungiert als Ein-/Aus-Steuerelement, das einen klickten Zustand ähnlich wie ein Kontrollkästchen verwalten kann. Dieses Schaltflächenformat wird durch den TF \_ LBI \_ STYLE \_ BTN \_ TOGGLE-Stil identifiziert. ITfLangBarItemButton::OnClick wird aufgerufen, wenn auf das Element geklickt wird. ITfLangBarItemButton::InitMenu und ITfLangBarItemButton::OnMenuSelect werden nicht verwendet.                                                  |
| Menü          | Die Schaltfläche fungiert als Dropdownmenü. Dieses Schaltflächenformat wird durch den TF \_ LBI \_ STYLE \_ BTN \_ MENU-Stil identifiziert. ITfLangBarItemButton::InitMenu wird aufgerufen, wenn auf die Schaltfläche geklickt wird. Wenn der Benutzer ein Element im Menü auswählt, ruft die Sprachleiste ITfLangBarItemButton::OnMenuSelect mit dem Bezeichner des ausgewählten Menüelements auf. ITfLangBarItemButton::OnClickis wird nicht verwendet. |



 

## <a name="implementing-a-menu-button"></a>Implementieren einer Menüschaltfläche

Wenn der Benutzer auf eine Menüschaltfläche klickt, ruft die Sprachleiste [ITfLangBarItemButton::InitMenu auf.](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) Das Element fügt dem Menü Elemente mithilfe der [ITfMenu-Schnittstelle](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) hinzu, die an InitMenu übergeben wird.

Um dem Menü ein Untermenü hinzuzufügen, rufen Sie [ITfMenu::AddMenuItem](/windows/desktop/api/Ctfutb/nf-ctfutb-itfmenu-addmenuitem) mit TF \_ LBMENUF \_ SUBMENU auf. Wenn dies erfolgt ist, wird im *ppMenu-Parameter* von AddMenuItem ein neues **ITfMenu-Objekt** zurückgegeben, das das Untermenü darstellt. Dieses neue Menüobjekt wird verwendet, um dem Untermenü Elemente hinzuzufügen.

Wenn der Benutzer ein Element im Menü auswählt, ruft die Sprachleiste [ITfLangBarItemButton::OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) mit dem Bezeichner des ausgewählten Menüelements auf.

## <a name="adding-items-to-the-language-bar"></a>Hinzufügen von Elementen zur Sprachleiste

Ein Textdienst sollte seine Elemente der Sprachleiste hinzufügen, wenn seine [ITfTextInputProcessor::Activate-Methode](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-activate) aufgerufen wird, und diese entfernen, wenn dessen [ITfTextInputProcessor::D eactivate](/windows/desktop/api/msctf/nf-msctf-itftextinputprocessor-deactivate) aufgerufen wird.

Um der Sprachleiste ein Element hinzuzufügen, ruft der Textdienst eine [ITfLangBarItemMgr-Schnittstelle](/windows/desktop/api/ctfutb/nn-ctfutb-itflangbaritemmgr) ab, indem er ITfThreadMgr::QueryInterface mit IID \_ ITfLangBarItemMgr aufruft. Der Textdienst ruft dann [ITfLangBarItemMgr::AddItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-additem) mit dem Zeiger auf das Sprachleistenelementobjekt auf.

Der Textdienst muss das Element entfernen, wenn es deaktiviert wird. Der Textdienst verwendet entweder dieselbe **ITfLangBarItemMgr-Schnittstelle,** die zum Hinzufügen der Elemente verwendet wird, oder erhält eine andere Instanz der Schnittstelle. Der Textdienst ruft dann [ITfLangBarItemMgr::RemoveItem mit](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-removeitem) dem Schnittstellenzeiger des zu entfernenden Elements auf.

## <a name="extending-system-language-bar-items"></a>Erweitern von Systemsprachleistenelementen

TSF bietet die Möglichkeit, vorhandenen Sprachleistenmenüs Menüelemente hinzuzufügen. Dadurch kann ein Textdienst Dem Menü eines anderen Textdiensts Elemente hinzufügen, ohne der Symbolleiste eine separate Schaltfläche hinzufügen zu müssen. Dadurch können die Menüelemente auch in logische Gruppen organisiert werden. Beispielsweise kann ein Textdienst, der dem Standard-Sprachtextdienst zusätzliche Funktionen bietet, dem Menü des Sprachtextdiensts Elemente hinzufügen, anstatt eine eigene Menüschaltfläche auf oberster Ebene hinzuzufügen.

Ein Textdienst stellt eine Sprachleisten-Menüerweiterung bereit, indem ein Objekt implementiert wird, das die [ITfSystemLangBarItemSink-Schnittstelle](/windows/desktop/api/ctfutb/nn-ctfutb-itfsystemlangbaritemsink) unterstützt. Diese Schnittstelle funktioniert genau wie die [ITfLangBarItemButton-Schnittstelle](/windows/desktop/api/Ctfutb/nn-ctfutb-itflangbaritembutton) für eine Menüschaltfläche. Wenn das Menü angezeigt wird, ruft der zu erweiternde Textdienst [ITfSystemLangBarItemSink::InitMenu auf.](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu) Die Erweiterung fügt dem Menü Elemente hinzu, indem sie die [ITfMenu-Schnittstelle](/windows/desktop/api/ctfutb/nn-ctfutb-itfmenu) verwendet, die an **InitMenu übergeben wird.** Wenn der Benutzer ein von der Erweiterung hinzugefügtes Element auswählt, ruft der zu erweiternde Textdienst [ITfSystemLangBarItemSink::OnMenuSelect](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-onmenuselect) mit dem Bezeichner des ausgewählten Menüelements auf.

Um eine Sprachleisten-Menüerweiterung zu installieren, schließt der Textdienst die folgenden Schritte ab.

1.  Rufen Sie die **ITfLangBarItem-Schnittstelle** für das zu erweiternde Element ab, indem Sie [ITfLangBarItemMgr::GetItem](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem) mit der **GUID** für das zu erweiternde Element aufrufen.
2.  Rufen Sie **die ITfSource-Schnittstelle** für das zu erweiternde Element ab, indem Sie ITfLangBarItem::QueryInterface mit IID \_ ITfSource aufrufen.
3.  Rufen [Sie ITfSource::AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) mit IID ITfSystemLangBarItemSink und dem Zeiger auf das \_ **ITfSystemLangBarItemSink-Objekt** auf. Wenn ITfSource::AdviseSink fehlschlägt, unterstützt der Textdienst keine Menüerweiterungen.

[ITfSource::UnadviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink)**ITfSource::AdviseSink**

## <a name="supporting-language-bar-menu-extensions"></a>Unterstützung von Sprachleisten-Menüerweiterungen

Ein Textdienst kann anderen Textdiensten das Hinzufügen von Elementen zu den Sprachleistenmenüs ermöglichen, wie oben gezeigt. Der Textdienst, der seine GUID veröffentlichen muss, damit das Element durch Aufrufen von [ITfLangBarItemMgr::GetItem erhalten werden kann.](/windows/desktop/api/ctfutb/nf-ctfutb-itflangbaritemmgr-getitem)

Zur Unterstützung von Menüerweiterungen muss der Textdienst die [ITfSource-Schnittstelle](/windows/desktop/api/msctf/nn-msctf-itfsource) unterstützen. Mit den folgenden Schritten wird die Unterstützung für eine oder mehrere Menüerweiterungen aktiviert.

1.  Wenn [ITfSource::AdviseSink](/windows/desktop/api/msctf/nf-msctf-itfsource-advisesink) mit IID \_ ITfSystemLangBarItemSink aufgerufen wird, muss der Textdienst die **ITfSystemLangBarItemSink-Schnittstelle** speichern und einen Cookiewert zurückgeben, der die Erweiterung identifiziert.
2.  Wenn [ITfLangBarItemButton::InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) aufgerufen wird, ruft der Textdienst die [ITfSystemLangBarItemSink::InitMenu-Methode](/windows/desktop/api/ctfutb/nf-ctfutb-itfsystemlangbaritemsink-initmenu) der Erweiterung auf. Der Textdienst muss eine Möglichkeit implementieren, um die von der Erweiterung hinzugefügten Menüelemente zu identifizieren, im Gegensatz zu den Elementen, die vom Textdienst selbst hinzugefügt werden.
3.  Wenn [ITfLangBarItemButton::OnMenuSelect](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onmenuselect) mit einem Menüelementbezeichner aufgerufen wird, der zu einer Erweiterung gehört, ruft der Textdienst die **ITfSystemLangBarItemSink::OnMenuSelect-Methode** der Erweiterung auf.
4.  Wenn [ITfSource::UnadviseSink mit](/windows/desktop/api/msctf/nf-msctf-itfsource-unadvisesink) dem entsprechenden Cookie aufgerufen wird, entfernt der Textdienst die Menüerweiterung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einrichten von Textdienstframework](how-to-set-up-tsf.md)
</dt> <dt>

[Sprachleiste (Anwendungen)](language-bar-app.md)
</dt> </dl>

 

 
