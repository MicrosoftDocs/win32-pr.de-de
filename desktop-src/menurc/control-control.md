---
title: Steuerelement Steuerung
description: Definiert ein benutzerdefiniertes Steuerelement.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- Steuerelement Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948673"
---
# <a name="control-control"></a>Steuerelement Steuerung

Definiert ein benutzerdefiniertes Steuerelement.

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*klassi*
</dt> <dd>

Ein neu definierter Name, eine Zeichenfolge oder ein 16-Bit-ganz Zahl Wert ohne Vorzeichen, der die Klasse definiert. Dabei kann es sich um eine beliebige Steuerelement Klasse handeln. eine Liste der Steuerelement Klassen finden Sie in der ersten Liste, die dieser Beschreibung folgt. Wenn der Wert ein neu definierter Name ist, der von der Anwendung bereitgestellt wird, muss er eine Zeichenfolge sein, die in doppelten Anführungszeichen (") eingeschlossen ist.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Neudefinierter Name oder ganzzahliger Wert, der den Stil des angegebenen Steuer Elements angibt. Die genaue Bedeutung von *Style* hängt vom Wert der- *Klasse* ab. In den Abschnitten nach dieser Beschreibung werden die Steuerelement Klassen und die entsprechenden Stile angezeigt.

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Control-Anweisung finden Sie unter allgemeine [Steuerelement Parameter](common-control-parameters.md).

## <a name="remarks"></a>Bemerkungen

Die sechs möglichen Steuerelement Klassen werden in den folgenden Abschnitten beschrieben.

### <a name="the-button-control-class"></a>Die Button-Steuerelement Klasse

Ein Schaltflächen-Steuerelement ist ein kleines rechteckiges untergeordnetes Fenster, das der Benutzer aktivieren oder deaktivieren kann, indem er mit der Maus darauf klickt. Schaltflächen-Steuerelemente können allein oder in Gruppen verwendet werden und können entweder als bezeichnet oder ohne Text angezeigt werden. Schaltflächen Steuerelemente ändern die Darstellung normalerweise, wenn der Benutzer darauf klickt.

Die Schaltflächen Stile werden im folgenden Thema beschrieben: [Schalt](../controls/button-styles.md)Flächen Formate.

### <a name="the-combo-box-control-class"></a>Die Kombinations Feld-Steuerelement Klasse

Kombinations Feld-Steuerelemente bestehen aus einem Auswahlfeld, das einem Bearbeitungs Steuerelement plus einem Listenfeld ähnelt. Das Listenfeld wird möglicherweise jederzeit oder nach unten angezeigt, wenn der Benutzer ein "Popbox" neben dem Auswahlfeld auswählt.

Abhängig vom Format des Kombinations Felds kann der Benutzer den Inhalt des Auswahl Felds oder nicht bearbeiten. Wenn das Listenfeld sichtbar ist, wird durch das Eingeben von Zeichen in das Auswahlfeld der erste Eintrag hervorgehoben, der mit den typisierten Zeichen übereinstimmt. Umgekehrt wird beim Auswählen eines Elements im Listenfeld der ausgewählte Text im Feldauswahl angezeigt.

Die Kombinations Feld-Steuerelement Stile werden im folgenden Thema beschrieben: Kombinations [Feld-Stile](../controls/combo-box-styles.md).

### <a name="the-edit-control-class"></a>Die Edit-Steuerelement Klasse

Ein Bearbeitungs Steuerelement ist ein rechteckiges untergeordnetes Fenster, in dem der Benutzer Text von der Tastatur eingeben kann. Der Benutzer wählt das Steuerelement aus und gibt ihm den Eingabefokus, indem er auf die Maus klickt oder die Tab-Taste drückt. Der Benutzer kann Text eingeben, wenn das Steuerelement eine blinkende Einfügemarke anzeigt. Die Maus kann zum Verschieben des Cursors und zum Auswählen von zu ersetzenden Zeichen oder zum Positionieren des Cursors zum Einfügen von Zeichen verwendet werden. Mithilfe der RÜCKTASTE können Zeichen gelöscht werden.

Bearbeitungs Steuerelemente verwenden die Schriftart mit fester Größe und Unicode-Zeichen. Sie erweitern Tabstopp Zeichen in so viele Leerzeichen, wie erforderlich sind, um den Cursor auf den nächsten Tabstopp zu verschieben. Es wird davon ausgegangen, dass Tabstopps an jeder Position an acht Zeichen stehen.

Die Bearbeitungs Steuerelement Stile werden im folgenden Thema beschrieben: [Bearbeiten von Steuerelement Stilen](../controls/edit-control-styles.md).

### <a name="the-list-box-control-class"></a>Die Listenfeld-Steuerelement Klasse

Listenfeld-Steuerelemente bestehen aus einer Liste von Zeichen folgen. Das-Steuerelement wird immer dann verwendet, wenn eine Anwendung eine Liste von Namen, z. b. Dateinamen, darstellen muss, die der Benutzer anzeigen und auswählen kann. Der Benutzer kann eine Zeichenfolge auswählen, indem er mit der Maus auf die Zeichenfolge zeigt und auf eine Maustaste klickt. Wenn eine Zeichenfolge ausgewählt ist, wird Sie hervorgehoben, und eine Benachrichtigungs Meldung wird an das übergeordnete Fenster übermittelt. Eine Schiebe Leiste kann mit einem Listenfeld-Steuerelement verwendet werden, um Listen aufzulisten, die für das Steuerelement Fenster zu lang oder zu breit sind.

Die Listenfeld-Steuerelement Stile werden im folgenden Thema beschrieben: [Listenfeld Stile](../controls/list-box-styles.md).

### <a name="the-scroll-bar-control-class"></a>Die Scroll-Bar Steuerelement Klasse

Bei einem Schiebe leisten-Steuerelement handelt es sich um ein Rechteck, das einen Bild Lauf Zieh Punkt enthält und Richtungspfeile an beiden Enden aufweist. Die Bild Lauf Leiste sendet eine Benachrichtigungs Meldung an das übergeordnete Element, wenn der Benutzer im Steuerelement auf die Maus klickt. Das übergeordnete Element ist für die Aktualisierung der Thumb-Position verantwortlich. Bild Lauf leisten-Steuerelemente verfügen über die gleiche Darstellung und Funktion wie die Bild Lauf leisten, die in normalen Fenstern verwendet werden. Aber im Gegensatz zu Bild Lauf leisten können Schiebe leisten-Steuerelemente an beliebiger Stelle in einem Fenster positioniert und immer dann verwendet werden, wenn Sie scrolleingaben für ein Fenster bereitstellen möchten.

Die Stile der Scrollleiste werden im folgenden Thema beschrieben: Bild Lauf leisten- [Steuerelement Stile](../controls/scroll-bar-control-styles.md).

### <a name="the-static-control-class"></a>Die statische Steuerelement Klasse

Statische Steuerelemente sind einfache Textfelder, Felder und Rechtecke, die verwendet werden können, um andere Steuerelemente zu bezeichnen, zu Schachteln oder zu trennen. Statische Steuerelemente nehmen keine Eingaben auf und stellen keine Ausgabe bereit.

Die statischen Steuerelement Stile werden im folgenden Thema beschrieben: [statische Steuerelement Stile](../controls/static-control-styles.md).

 

 