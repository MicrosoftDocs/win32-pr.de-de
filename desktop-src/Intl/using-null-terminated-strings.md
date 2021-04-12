---
description: Ihre Unicode-Anwendungen sollten bei der Verwendung von mit NULL endenden Zeichen folgen immer NULL in Tchar umwandeln.
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: Verwenden von auf NULL endenden Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce12079fa3d0c5a88af369a347f1cd655136ee09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218687"
---
# <a name="using-null-terminated-strings"></a>Verwenden von auf NULL endenden Zeichen folgen

Ihre Unicode-Anwendungen sollten bei der Verwendung von mit NULL endenden Zeichen folgen immer NULL in Tchar umwandeln. Der Code 0x0000 ist das Unicode-Zeichen folgen Abschluss Zeichen für eine NULL-terminierte Zeichenfolge. Ein einzelnes Null-Byte ist für diesen Code nicht ausreichend, da viele Unicode-Zeichen NULL-Bytes als das hohe oder das niedrige Byte enthalten. Ein Beispiel hierfür ist der Buchstabe A, bei dem der Zeichencode 0x0041 ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Sonderzeichen in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



