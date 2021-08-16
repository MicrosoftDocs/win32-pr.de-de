---
title: Allgemeine Steuerelementparameter
description: Im Folgenden wird die allgemeine Syntax für eine Ressourcendefinitions-Anweisung des Steuerelements beschrieben.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbdbf707e1ee72f62c7c08cb7065f4d1a4b8f2f4c000d52f3a28c9806a21a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870561"
---
# <a name="common-control-parameters"></a>Allgemeine Steuerelementparameter

Im Folgenden wird die allgemeine Syntax für eine Ressourcendefinitions-Anweisung des Steuerelements beschrieben. Die Bedeutung der einzelnen Parameter wird unten angegeben. Gelegentlich verwendet eine Anweisung einen Parameter anders oder ignoriert möglicherweise einen Parameter. Die anweisungsspezifische Variante wird in der Dokumentation für die -Anweisung beschrieben.

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Text*
</dt> <dd>

Text, der mit dem -Steuerelement angezeigt werden soll. Der Text wird innerhalb des Steuerelements oder neben dem Steuerelement positioniert.

Dieser Parameter muss 0 (null) oder mehr Zeichen enthalten, die in doppelte Anführungszeichen () eingeschlossen sind. Zeichenfolgen werden automatisch mit NULL beendet und in der resultierenden Ressourcendatei in Unicode konvertiert.

Standardmäßig sind die zeichen, die zwischen den doppelten Anführungszeichen aufgeführt sind, ANSI-Zeichen, und Escapesequenzen werden als Byte-Escapesequenzen interpretiert. Wenn der Zeichenfolge das Präfix "L" vorangestellt ist, ist die Zeichenfolge eine Breitzeichenzeichenfolge, und Escapesequenzen werden als 2-Byte-Escapesequenzen interpretiert, die Unicode-Zeichen angeben. Wenn ein doppeltes Anführungszeichen im Text erforderlich ist, müssen Sie das doppelte Anführungszeichen zweimal verwenden.

Ein ampersand-Zeichen (&) im Text gibt an, dass das folgende Zeichen als mnemonisches Zeichen für das Steuerelement verwendet wird. Wenn das Steuerelement angezeigt wird, wird das ampersand-Zeichen nicht angezeigt, aber das mnemonische Zeichen wird unterstrichen. Der Benutzer kann das Steuerelement auswählen, indem er die Taste drückt, die dem unterstrichenen mnemonischen Zeichen entspricht. Um das ampersand-Zeichen als Zeichen in einer Zeichenfolge zu verwenden, fügen Sie zwei ampersands (&&) ein.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Steuerelement Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich von 0 bis 65.535 oder ein einfacher arithmetischer Ausdruck sein, der zu einem Wert in diesem Bereich ausgewertet wird.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

X-Koordinate der linken Seite des Steuerelements relativ zur linken Seite des Dialogfelds. Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich von 0 bis 65.535 sein. Die Koordinate befindet sich in Dialogeinheiten und ist relativ zum Ursprung des Dialogfelds, Fensters oder Steuerelements, das bzw. das das angegebene Steuerelement enthält.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Y-Koordinate der oberen Seite des Steuerelements relativ zum oberen Rand des Dialogfelds. Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich von 0 bis 65.535 sein. Die Koordinate befindet sich in Dialogeinheiten relativ zum Ursprung des Dialogfelds, Fensters oder Steuerelements, das bzw. das das angegebene Steuerelement enthält.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Breite*
</dt> <dd>

Breite des Steuerelements. Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich von 1 bis 65.535 sein. Die Breite beträgt 1/4 Zeichen.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Höhe*
</dt> <dd>

Höhe des Steuerelements. Dieser Wert muss eine 16-Bit-Ganzzahl ohne Vorzeichen im Bereich von 1 bis 65.535 sein. Die Höhe beträgt 1/8 Zeichen.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Steuerelementstile. Verwenden Sie den bitweisen OR \| ()-Operator, um Stile zu kombinieren. Weitere Informationen finden Sie unter [Fensterstile.](../winmsg/window-styles.md)

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*Erweiterter Stil*
</dt> <dd>

Erweiterte Fensterstile. Sie müssen style *angeben,* um erweiterte *Stile anzugeben.* Weitere Informationen finden Sie unter [**EXSTYLE**](exstyle-statement.md).

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*
</dt> <dd>

Numerischer Ausdruck, der die ID angibt, mit der das Steuerelement während der [**WM \_ HELP-Verarbeitung identifiziert**](../shell/wm-help.md) wird.

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*
</dt> <dd>

Steuerelementspezifische Daten für das Steuerelement. Wenn ein Dialogfeld erstellt wird und ein Steuerelement in diesem Dialogfeld mit steuerelementspezifischen Daten erstellt wird, wird ein Zeiger auf diese Daten über die *lParam-Nachricht* der [**WM \_ CREATE-Nachricht**](../winmsg/wm-create.md) für dieses Steuerelement an die Fensterprozedur des Steuerelements übergeben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Horizontale Dialogeinheiten sind 1/4 der Basisbreiteneinheit des Dialogs. Vertikale Einheiten sind 1/8 der Basishöheneinheit des Dialogs. Die aktuellen Dialogbasiseinheiten werden aus der Höhe und Breite der aktuellen Systemschriftart berechnet. Die [**GetDialogBaseUnits-Funktion**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) gibt die Basiseinheiten des Dialogs in Pixel zurück. Die Koordinaten sind relativ zum Ursprung des Dialogfelds.

 

 