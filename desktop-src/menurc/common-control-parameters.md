---
title: Allgemeine Steuerelement Parameter
description: Im folgenden wird die allgemeine Syntax für eine Control Resource-Definition-Anweisung beschrieben.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314913"
---
# <a name="common-control-parameters"></a>Allgemeine Steuerelement Parameter

Im folgenden wird die allgemeine Syntax für eine Control Resource-Definition-Anweisung beschrieben. Die Bedeutung der einzelnen Parameter ist unten angegeben. Gelegentlich verwendet eine-Anweisung einen-Parameter anders, oder es kann ein Parameter ignoriert werden. Die Anweisungs spezifische Variation wird in der Dokumentation für die-Anweisung beschrieben.

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Text, der mit dem-Steuerelement angezeigt werden soll. Der Text wird im-Steuerelement oder neben dem-Steuerelement positioniert.

Dieser Parameter muss NULL oder mehr Zeichen enthalten, die in doppelten Anführungszeichen (") eingeschlossen sind. Zeichen folgen werden automatisch mit null-terminierter und in die resultierende Ressourcen Datei in Unicode konvertiert.

Standardmäßig sind die zwischen den doppelten Anführungszeichen aufgelisteten Zeichen ANSI-Zeichen, und Escapesequenzen werden als Byte-Escapesequenzen interpretiert. Wenn der Zeichenfolge das Präfix "L" vorangestellt ist, ist die Zeichenfolge eine Zeichenfolge mit breit Zeichen, und Escapesequenzen werden als 2-Byte-Escapesequenzen interpretiert, die Unicode-Zeichen angeben Wenn im Text ein doppeltes Anführungszeichen erforderlich ist, müssen Sie das doppelte Anführungszeichen zweimal einschließen.

Ein kaufmännisches und-Zeichen (&) im Text gibt an, dass das folgende Zeichen als mnetmonisches Zeichen für das-Steuerelement verwendet wird. Wenn das Steuerelement angezeigt wird, wird das kaufmännische und-Zeichen nicht angezeigt, aber das mnetmonische Zeichen wird unterstrichen. Der Benutzer kann das Steuerelement auswählen, indem er die Taste drückt, die dem unterstrichenen mnetmonischen Zeichen entspricht. Um das kaufmännische und-Zeichen als Zeichen in einer Zeichenfolge zu verwenden, fügen Sie zwei kaufmännische und-Zeichen (&&) ein.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Name*
</dt> <dd>

Steuerelement Bei diesem Wert muss es sich um eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich 0 bis 65.535 oder um einen einfachen arithmetischen Ausdruck handeln, der zu einem Wert in diesem Bereich ausgewertet wird.

</dd> <dt>

<span id="x"></span><span id="X"></span>*Stuben*
</dt> <dd>

X-Koordinate des linken Rands des Steuer Elements relativ zur linken Seite des Dialog Felds. Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich zwischen 0 und 65.535 sein. Die Koordinate befindet sich in Dialogfeld Einheiten und ist relativ zum Ursprung des Dialog Felds, Fensters oder Steuer Elements, das das angegebene Steuerelement enthält.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Teenie*
</dt> <dd>

Y-Koordinate des oberen Rands des Steuer Elements relativ zum oberen Rand des Dialog Felds. Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich zwischen 0 und 65.535 sein. Die Koordinate befindet sich in Dialog Einheiten relativ zum Ursprung des Dialog Felds, Fensters oder Steuer Elements, das das angegebene Steuerelement enthält.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Breite*
</dt> <dd>

Breite des Steuer Elements. Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich zwischen 1 und 65.535 sein. Die Breite liegt bei Einheiten von 1/4 Zeichen.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Flugh*
</dt> <dd>

Die Höhe des Steuer Elements. Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich zwischen 1 und 65.535 sein. Die Höhe ist in Einheiten von 1/8 Zeichen.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Vorbild*
</dt> <dd>

Steuerelement Stile. Verwenden Sie den bitweisen or ( \| )-Operator, um Stile zu kombinieren. Weitere Informationen finden Sie unter [Fenster Stile](../winmsg/window-styles.md).

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*Erweiterter Stil*
</dt> <dd>

Erweiterte Fenster Stile. Sie müssen *Style* angeben, um den *erweiterten Stil* anzugeben. Weitere Informationen finden Sie unter [**ExStyle**](exstyle-statement.md).

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*
</dt> <dd>

Numerischer Ausdruck, der die ID angibt, mit der das Steuerelement während der [**WM- \_ Hilfe**](../shell/wm-help.md) verarbeitet wird.

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*
</dt> <dd>

Steuerelement spezifische Daten für das Steuerelement. Wenn ein Dialogfeld erstellt wird und ein Steuerelement in diesem Dialogfeld, das Steuerelement spezifische Daten enthält, erstellt wird, wird ein Zeiger auf diese Daten über den *LPARAM* der [**WM \_ Create**](../winmsg/wm-create.md) -Meldung für dieses Steuerelement an die Fenster Prozedur des Steuer Elements übermittelt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Horizontale Dialog Einheiten sind 1/4 der Dialogfeld Basis-breiten Einheit. Vertikale Einheiten sind 1/8 der Dialogfeld Basis-Höheneinheit. Die aktuellen Dialogfeld Basiseinheiten werden aus der Höhe und Breite der aktuellen System Schriftart berechnet. Die [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) -Funktion gibt die Dialog Basiseinheiten in Pixel zurück. Die Koordinaten sind relativ zum Ursprung des Dialog Felds.

 

 