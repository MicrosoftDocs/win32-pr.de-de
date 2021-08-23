---
description: Rich Edit 3.0 unterstützt die HexToUnicode-IME, mit der ein Benutzer zwischen Hexadezimal- und Unicode-Zeichen konvertieren kann, indem hot-Schlüssel auf zwei Arten verwendet werden.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: HexToUnicode IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a57ce56821f200c9fd9ff80560908f5a72ecfdb0f51ce981e1aff40ce785b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068150"
---
# <a name="hextounicode-ime"></a>HexToUnicode IME

Rich Edit 3.0 unterstützt die HexToUnicode-IME, mit der ein Benutzer zwischen Hexadezimal- und Unicode-Zeichen konvertieren kann, indem hot-Schlüssel auf zwei Arten verwendet werden.

Mit der ersten Konvertierungsmethode gibt der Benutzer den Zeichencode hexadezimal ein und gibt dann ALT+X ein. Die IME ersetzt die Hexadezimalziffern vor der Einfügemarke durch das Unicode-Zeichen. Wenn die aktuelle Schriftart den Zeichencode nicht unterstützt, wird eine entsprechende Schriftart ausgewählt, die ihn unterstützt. Zum Konvertieren von Unicode in hexadezimale Werte gibt der Benutzer UMSCHALT+ALT+X ein. Dieser Eintrag ersetzt das Unicode-Zeichen, das der Einfügemarke vorangestellt ist, durch die Hexadezimalziffern. Insbesondere ermöglicht diese Methode dem Benutzer, das Zeichen zu bestimmen, das durch einen "fehlenden Symbol"-Indikator angegeben wird. Wenn der Hexadezimalzeichencode unmittelbar auf einige legitime Hexadezimalzeichen (nicht Zeichen) folgt, wählt der Benutzer die zu konvertierenden Ziffern aus, bevor er ALT+X eingibt. Ein Problem bei dieser ersten Methode ist, dass ALT+X manchmal als Schlüsselkombination für den Exitbefehl (d. h. eXit) verwendet wird. In Microsoft Office wird dieser Befehl beispielsweise nur als Option im Menü **Datei** angezeigt.

Die zweite Methode zum Konvertieren zwischen Hexadezimal- und Unicode-Zeichen umfasst das Zahlenpad. Mit dieser Methode gibt der Benutzer ALT+NumPad-Zahlen (mit Werten größer als 255) ein, um Unicode-Zeichen mit Dezimalwerten einzugeben. Diese Methode ist nicht so nützlich wie die erste, da der Benutzer nicht sehen kann, welche Hexadezimalziffern eingegeben wurden. Außerdem kann der Benutzer die Hexadezimalziffern nur korrigieren, wenn er alle Ziffern erneut eingibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Eingabemethoden-Manager](about-input-method-manager.md)
</dt> </dl>

 

 



