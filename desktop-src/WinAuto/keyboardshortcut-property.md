---
title: KeyboardShortcut (Eigenschaft)
description: Die KeyboardShortcut-Eigenschaft beschreibt eine Tastenkombination oder eine Tastenkombination, die ein angegebenes Barrierefreies Objekt aktiviert.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206786"
---
# <a name="keyboardshortcut-property"></a>KeyboardShortcut (Eigenschaft)

Die **KeyboardShortcut** -Eigenschaft beschreibt eine Tastenkombination oder eine Tastenkombination, die ein angegebenes Barrierefreies Objekt aktiviert.

Die **KeyboardShortcut** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)abgerufen.

Die abgerufene Zeichenfolge beschreibt eine *Tastenkombination* (auch als *Tastaturbeschleuniger* bezeichnet) oder eine *Zugriffstaste* (auch als *mnetmonisches* bezeichnet). Eine Zugriffstaste ist ein unterstrichenes Zeichen im Text eines Menüs, Menü Elements oder einer Bezeichnung eines Steuer Elements, z. b. einer Schaltfläche "Push".

Die abgerufene Zeichenfolge muss den Namen des Schlüssels zusammen mit den modifiziererschlüsseln enthalten. Die Zeichenfolge muss das folgende Format aufweisen, damit Clients Sie leicht analysieren können: \[ \[ modifiziererschlüssel \] + \[ ... \] + \] Key Name.

Beispiele hierfür sind alt + F, STRG + ALT + 4, Win + F1, Strg + Alt + Umschalt + Rücktaste oder einfach RÜCKTASTE.

In der folgenden Tabelle sind modifiziererschlüssel aufgelistet.



| Zusatztaste | BESCHREIBUNG                        |
|--------------|------------------------------------|
| ALT          | Alternative Modifizierertaste             |
| STRG         | Steuerelement-Modifizierertaste               |
| Schuss        | UMSCHALT-Modifizierertaste                 |
| Erringen          | WINDOWS-TASTE                   |
| FN           | Funktionstaste auf tragbaren Computern |



 

Tastenkombinationen nicht lokalisieren.

## <a name="handling-objects-that-have-both-key-types"></a>Behandeln von Objekten, die über beide Schlüsseltypen verfügen

Wenn ein Objekt über eine Tastenkombination und eine Zugriffstaste verfügt, gibt die **KeyboardShortcut** -Eigenschaft die Zugriffstaste zurück. Der Zugriffsschlüssel ist der Schlüssel, den ein Benutzer drücken würde, wenn das Objekt oder das übergeordnete Objekt den Tastaturfokus besitzt. Beispielsweise kann das Menü Element **Drucken** sowohl eine Tastenkombination (STRG + P) als auch eine Zugriffstaste (p) enthalten. Wenn ein Benutzer STRG + P drückt, während das Menü aktiv ist, geschieht nichts. Wenn ein Benutzer jedoch P drückt, während das Menü aktiv ist, wird das Dialogfeld **Drucken** der Anwendung aufgerufen. In diesem Fall ist die **KeyboardShortcut** -Eigenschaft "P", um widerzuspiegeln, was der Benutzer drücken muss, wenn das Menü den Tastaturfokus besitzt.

 

 




