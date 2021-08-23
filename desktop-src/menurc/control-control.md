---
title: CONTROL-Steuerelement
description: Definiert ein benutzerdefiniertes Steuerelement.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- CONTROL-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 069449b5eef83cef7b7bdfac1c61aacb0ceac97cbbdd6e6fb2c139c43b3bae13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663060"
---
# <a name="control-control"></a>CONTROL-Steuerelement

Definiert ein benutzerdefiniertes Steuerelement.

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*Klasse*
</dt> <dd>

Neu definierter Name, Zeichenfolge oder ein 16-Bit-Ganzzahlwert ohne Vorzeichen, der die Klasse definiert. Dies kann eine der Steuerelementklassen sein. eine Liste der Steuerelementklassen finden Sie in der ersten Liste nach dieser Beschreibung. Wenn der Wert ein neu definierter Name ist, der von der Anwendung bereitgestellt wird, muss er eine Zeichenfolge sein, die in doppelte Anführungszeichen () eingeschlossen ist.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Neu definierter Name oder ganzzahliger Wert, der den Stil des angegebenen Steuerelements angibt. Die genaue Bedeutung des *Stils* hängt vom *Klassenwert* ab. In den Abschnitten nach dieser Beschreibung werden die Steuerelementklassen und die entsprechenden Stile angezeigt.

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Steuerelement-Anweisung finden Sie unter [Allgemeine Steuerelementparameter](common-control-parameters.md).

## <a name="remarks"></a>Hinweise

Die sechs möglichen Steuerelementklassen werden in den folgenden Abschnitten beschrieben.

### <a name="the-button-control-class"></a>Die Button-Steuerelementklasse

Ein Schaltflächen-Steuerelement ist ein kleines rechteckiges untergeordnetes Fenster, das der Benutzer aktivieren oder deaktivieren kann, indem er mit der Maus darauf klickt. Schaltflächensteuerelemente können allein oder in Gruppen verwendet werden und können entweder beschriftet oder ohne Text angezeigt werden. Schaltflächensteuerelemente ändern in der Regel die Darstellung, wenn der Benutzer darauf klickt.

Die Schaltflächenstile werden im folgenden Thema beschrieben: [Schaltflächenstile](../controls/button-styles.md).

### <a name="the-combo-box-control-class"></a>Die Combo Box-Steuerelementklasse

Kombinationsfeld-Steuerelemente bestehen aus einem Auswahlfeld, das einem Bearbeitungssteuerfeld ähnelt, sowie einem Listenfeld. Das Listenfeld kann jederzeit angezeigt werden oder verworfen werden, wenn der Benutzer ein "Popfeld" neben dem Auswahlfeld auswählt.

Je nach Format des Kombinationsfelds kann der Benutzer den Inhalt des Auswahlfelds bearbeiten. Wenn das Listenfeld angezeigt wird, wird durch die Eingabe von Zeichen in das Auswahlfeld der erste Eintrag hervorgehoben, der den typierten Zeichen entspricht. Wenn Sie dagegen ein Element im Listenfeld auswählen, wird der ausgewählte Text im Auswahlfeld angezeigt.

Die Kombinationsfeld-Steuerelementstile werden im folgenden Thema beschrieben: [Kombinationsfeldstile](../controls/combo-box-styles.md).

### <a name="the-edit-control-class"></a>Die Edit-Steuerelementklasse

Ein Bearbeitungssteuerfeld ist ein rechteckiges untergeordnetes Fenster, in das der Benutzer Text über die Tastatur eingeben kann. Der Benutzer wählt das Steuerelement aus und erhält den Eingabefokus, indem er darauf klickt oder die TAB-TASTE drückt. Der Benutzer kann Text eingeben, wenn das Steuerelement eine blinkende Einfügemarke anzeigt. Die Maus kann verwendet werden, um den Cursor zu bewegen und zeichen auszuwählen, die ersetzt werden sollen, oder um den Cursor zum Einfügen von Zeichen zu positionieren. Die RÜCKTASTE kann verwendet werden, um Zeichen zu löschen.

Bearbeitungssteuerelemente verwenden die Schriftart mit fester Tonhöhe und zeigen Unicode-Zeichen an. Sie erweitern Tabstoppzeichen in so viele Leerzeichen, wie erforderlich sind, um den Cursor zum nächsten Tabstopp zu bewegen. Tabstopps werden an jeder achten Zeichenposition angenommen.

Die Bearbeitungssteuerstile werden im folgenden Thema beschrieben: [Bearbeiten von Steuerelementstilen.](../controls/edit-control-styles.md)

### <a name="the-list-box-control-class"></a>Die List Box-Steuerelementklasse

Listenfeld-Steuerelemente bestehen aus einer Liste von Zeichenfolgen. Das -Steuerelement wird immer dann verwendet, wenn eine Anwendung eine Liste von Namen, z. B. Dateinamen, präsentieren muss, die der Benutzer anzeigen und auswählen kann. Der Benutzer kann eine Zeichenfolge auswählen, indem er mit der Maus auf die Zeichenfolge zeigen und auf eine Maustaste klickt. Wenn eine Zeichenfolge ausgewählt ist, wird sie hervorgehoben und eine Benachrichtigungsmeldung an das übergeordnete Fenster übergeben. Eine Scrollleiste kann mit einem Listenfeld-Steuerelement verwendet werden, um Listen zu scrollen, die für das Steuerelementfenster zu lang oder zu breit sind.

Die Listenfeld-Steuerelementstile werden im folgenden Thema beschrieben: [Listenfeldstile](../controls/list-box-styles.md).

### <a name="the-scroll-bar-control-class"></a>Die Scroll-Bar-Steuerelementklasse

Ein Bildlaufleisten-Steuerelement ist ein Rechteck, das einen Bildlauffinger und Richtungspfeile an beiden Enden enthält. Die Scrollleiste sendet eine Benachrichtigung an das übergeordnete Element, wenn der Benutzer im Steuerelement mit der Maus klickt. Das übergeordnete Element ist bei Bedarf für die Aktualisierung der Klammerposition verantwortlich. Bildlaufleisten-Steuerelemente haben die gleiche Darstellung und Funktion wie die Bildlaufleisten, die in normalen Fenstern verwendet werden. Im Gegensatz zu Bildlaufleisten können Bildlaufleisten-Steuerelemente jedoch an einer beliebigen Stelle innerhalb eines Fensters positioniert und bei Bedarf verwendet werden, um Bildlaufeingaben für ein Fenster zu ermöglichen.

Die Bildlaufleistenstile werden im folgenden Thema beschrieben: [Bildlaufleisten-Steuerelementstile](../controls/scroll-bar-control-styles.md).

### <a name="the-static-control-class"></a>Die statische Steuerelementklasse

Statische Steuerelemente sind einfache Textfelder, Felder und Rechtecke, die zum Beschriften, Feld oder Trennen anderer Steuerelemente verwendet werden können. Statische Steuerelemente nehmen keine Eingaben und stellen keine Ausgabe zur Verfügung.

Die statischen Steuerelementstile werden im folgenden Thema beschrieben: [Statische Steuerelementstile](../controls/static-control-styles.md).

 

 