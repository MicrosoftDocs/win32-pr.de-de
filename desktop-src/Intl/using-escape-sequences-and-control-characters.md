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
# <a name="using-escape-sequences-and-control-characters"></a><span data-ttu-id="29499-103">Verwenden von Escapesequenzen und Steuerzeichen</span><span class="sxs-lookup"><span data-stu-id="29499-103">Using Escape Sequences and Control Characters</span></span>

<span data-ttu-id="29499-104">Wenn eine Anwendung Zeichen folgen aus ASCII oder einer [Windows (ANSI)-Codepage](code-pages.md) in Unicode konvertiert, sollte Sie Escapesequenzen Zeichen Weise in Unicode übersetzen.</span><span class="sxs-lookup"><span data-stu-id="29499-104">When an application converts strings from ASCII or from a [Windows (ANSI) code page](code-pages.md) to Unicode, it should translate escape sequences character-by-character into Unicode.</span></span> <span data-ttu-id="29499-105">Wenn eine ASCII-oder eine andere 8-Bit-Textdatei in Unicode konvertiert wird, besteht die Möglichkeit, dass Sie anschließend wieder konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="29499-105">When an ASCII or other 8-bit text file is converted to Unicode, there is a chance that it will subsequently be converted back.</span></span> <span data-ttu-id="29499-106">Konvertieren von Escapesequenzen in Unicode auf Zeichenbasis, anstatt Sie als einzelnes Unicode-Zeichen zu kombinieren, ist es möglich, die umgekehrte Konvertierung auszuführen, ohne dass die Escapesequenzen als solche erkannt und analysiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="29499-106">Converting escape sequences into Unicode on a character-by-character basis, instead of combining them as a single Unicode character, makes it possible to perform the reverse conversion without needing to recognize and parse the escape sequences as such.</span></span> <span data-ttu-id="29499-107">Beispielsweise sollte ESC + A zu 0x001b (ESC), 0x0041 (A) anstatt 0x411b werden.</span><span class="sxs-lookup"><span data-stu-id="29499-107">For example, ESC+A should become 0x001B (ESC), 0x0041 (A), instead of 0x411B.</span></span>

<span data-ttu-id="29499-108">Die ersten 32 16-Bit-Codewerte in Unicode sind für die 32-Steuerzeichen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="29499-108">The first 32 16-bit code values in Unicode are intended for the 32 control characters.</span></span> <span data-ttu-id="29499-109">Diese Spezifikation unterstützt die vorhandene Verwendung von Steuerzeichen zu Formatierungs Zwecken.</span><span class="sxs-lookup"><span data-stu-id="29499-109">This specification supports the existing use of control characters for formatting purposes.</span></span> <span data-ttu-id="29499-110">Unicode-Anwendungen können diese Steuerzeichen genauso behandeln wie Ihre ASCII-Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="29499-110">Unicode applications can treat these control characters in exactly the same way as they treat their ASCII equivalents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29499-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="29499-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29499-112">Verwenden von Sonderzeichen in Unicode</span><span class="sxs-lookup"><span data-stu-id="29499-112">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



