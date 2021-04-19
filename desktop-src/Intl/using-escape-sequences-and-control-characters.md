---
description: Wenn eine Anwendung Zeichen folgen aus ASCII oder einer Windows (ANSI)-Codepage in Unicode konvertiert, sollte Sie Escapesequenzen Zeichen Weise in Unicode übersetzen.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Verwenden von Escapesequenzen und Steuerzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369888"
---
# <a name="using-escape-sequences-and-control-characters"></a>Verwenden von Escapesequenzen und Steuerzeichen

Wenn eine Anwendung Zeichen folgen aus ASCII oder einer [Windows (ANSI)-Codepage](code-pages.md) in Unicode konvertiert, sollte Sie Escapesequenzen Zeichen Weise in Unicode übersetzen. Wenn eine ASCII-oder eine andere 8-Bit-Textdatei in Unicode konvertiert wird, besteht die Möglichkeit, dass Sie anschließend wieder konvertiert wird. Konvertieren von Escapesequenzen in Unicode auf Zeichenbasis, anstatt Sie als einzelnes Unicode-Zeichen zu kombinieren, ist es möglich, die umgekehrte Konvertierung auszuführen, ohne dass die Escapesequenzen als solche erkannt und analysiert werden müssen. Beispielsweise sollte ESC + A zu 0x001b (ESC), 0x0041 (A) anstatt 0x411b werden.

Die ersten 32 16-Bit-Codewerte in Unicode sind für die 32-Steuerzeichen vorgesehen. Diese Spezifikation unterstützt die vorhandene Verwendung von Steuerzeichen zu Formatierungs Zwecken. Unicode-Anwendungen können diese Steuerzeichen genauso behandeln wie Ihre ASCII-Entsprechungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Sonderzeichen in Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



