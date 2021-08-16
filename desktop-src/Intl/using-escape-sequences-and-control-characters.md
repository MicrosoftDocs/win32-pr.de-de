---
description: Wenn eine Anwendung Zeichenfolgen aus ASCII oder von einer Windows -Codepage (ANSI) in Unicode konvertiert, sollte sie Escapesequenzen Zeichen für Zeichen in Unicode übersetzen.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Verwenden von Escapesequenzen und Steuerzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea89997a8f94a9fdd573b2c8360dbdd5342d38ca8bd2e7a133aa29943c07e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389919"
---
# <a name="using-escape-sequences-and-control-characters"></a>Verwenden von Escapesequenzen und Steuerzeichen

Wenn eine Anwendung Zeichenfolgen aus ASCII oder von einer [ansi-Codepage (Windows)](code-pages.md) in Unicode konvertiert, sollte sie Escapesequenzen Zeichen für Zeichen in Unicode übersetzen. Wenn eine ASCII- oder andere 8-Bit-Textdatei in Unicode konvertiert wird, besteht die Möglichkeit, dass sie anschließend wieder konvertiert wird. Wenn Escapesequenzen zeichenweise in Unicode konvertiert werden, anstatt sie als einzelnes Unicode-Zeichen zu kombinieren, ist es möglich, die umgekehrte Konvertierung durchzuführen, ohne die Escapesequenzen als solche erkennen und analysieren zu müssen. Beispielsweise sollte ESC+A 0x001B (ESC), 0x0041 (A) und nicht 0x411B werden.

Die ersten 32 16-Bit-Codewerte in Unicode sind für die 32 Steuerzeichen vorgesehen. Diese Spezifikation unterstützt die vorhandene Verwendung von Steuerzeichen zu Formatierungszwecken. Unicode-Anwendungen können diese Steuerzeichen genauso behandeln wie ihre ASCII-Entsprechungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Sonderzeichen in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



