---
description: Rich Edit 3,0 unterstützt das hexadeunicode-IME, das es einem Benutzer ermöglicht, mithilfe von Tastenkombinationen zwischen hexadezimalen und Unicode-Zeichen zu konvertieren.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: Hexin Unicode-IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530314"
---
# <a name="hextounicode-ime"></a>Hexin Unicode-IME

Rich Edit 3,0 unterstützt das hexadeunicode-IME, das es einem Benutzer ermöglicht, mithilfe von Tastenkombinationen zwischen hexadezimalen und Unicode-Zeichen zu konvertieren.

Bei Verwendung der ersten Konvertierungsmethode gibt der Benutzer den Zeichencode in Hexadezimal Format ein und gibt dann ALT + X ein. Der IME ersetzt die hexadezimalen Ziffern vor der Einfügemarke durch das Unicode-Zeichen. Wenn die aktuelle Schriftart den Zeichencode nicht unterstützt, wird eine entsprechende Schriftart ausgewählt, die diese unterstützt. Zum Konvertieren von Unicode in Hexadezimal gibt der Benutzer UMSCHALT + ALT + X ein. Dieser Eintrag ersetzt das Unicode-Zeichen, das der Einfügemarke vorangestellt ist, durch die hexadezimalen Ziffern. Diese Methode ermöglicht es dem Benutzer insbesondere, das Zeichen zu bestimmen, das durch einen Indikator "fehlende Glyphe" angegeben wird. Wenn der hexadezimale Zeichencode direkt auf einige legitime (nicht Zeichen) hexadezimale Zeichen folgt, wählt der Benutzer die zu konvertierenden Ziffern aus, bevor ALT + X eingegeben wird. Ein Problem mit dieser ersten Methode besteht darin, dass alt + X manchmal als Tastenkombination für den Exit-Befehl verwendet wird (d. h. Exit). In Microsoft Office wird dieser Befehl z. b. nur als Option des Menüs **Datei** angezeigt.

Die zweite Methode zur typumrechnung zwischen hexadezimalen und Unicode-Zeichen umfasst das Zahlen Pad. Mit dieser Methode geben die Benutzer alt + numaufszahlen (mit Werten größer als 255) ein, um Unicode-Zeichen mithilfe von Dezimalwerten einzugeben. Diese Methode ist nicht so nützlich wie die erste, da der Benutzer nicht sehen kann, welche hexadezimalen Ziffern eingegeben wurden. Außerdem kann der Benutzer die hexadezimalen Ziffern nur dann korrigieren, wenn alle Ziffern erneut eingegeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über den Eingabemethoden-Manager](about-input-method-manager.md)
</dt> </dl>

 

 



