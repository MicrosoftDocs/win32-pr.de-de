---
description: Ihre Unicode-Anwendungen sollten immer 0 (null) in TCHAR umgewandelt werden, wenn NULL-endende Zeichenfolgen verwendet werden.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Verwenden von Zeichenfolgen mit NULL-Terminierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a5f27048bde2af75eca28626a562473ceffcc66f3f2f23509beca4fba06ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631780"
---
# <a name="using-null-terminated-strings"></a>Verwenden von Zeichenfolgen mit NULL-Terminierung

Ihre Unicode-Anwendungen sollten immer 0 (null) in TCHAR umgewandelt werden, wenn NULL-endende Zeichenfolgen verwendet werden. Der Code 0x0000 ist das Unicode-Zeichenfolgenabschlusszeichen für eine auf NULL endende Zeichenfolge. Ein einzelnes NULL-Byte ist für diesen Code nicht ausreichend, da viele Unicode-Zeichen NULL-Bytes entweder als das hohe oder das niedrige Byte enthalten. Ein Beispiel ist der Buchstabe A, für den der Zeichencode 0x0041 ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Sonderzeichen in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



