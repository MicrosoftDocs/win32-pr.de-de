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
# <a name="hextounicode-ime"></a><span data-ttu-id="9d717-103">Hexin Unicode-IME</span><span class="sxs-lookup"><span data-stu-id="9d717-103">HexToUnicode IME</span></span>

<span data-ttu-id="9d717-104">Rich Edit 3,0 unterstützt das hexadeunicode-IME, das es einem Benutzer ermöglicht, mithilfe von Tastenkombinationen zwischen hexadezimalen und Unicode-Zeichen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="9d717-104">Rich Edit 3.0 supports the HexToUnicode IME, which allows a user to convert between hexadecimal and Unicode characters by using hot keys in one of two ways.</span></span>

<span data-ttu-id="9d717-105">Bei Verwendung der ersten Konvertierungsmethode gibt der Benutzer den Zeichencode in Hexadezimal Format ein und gibt dann ALT + X ein.</span><span class="sxs-lookup"><span data-stu-id="9d717-105">Using the first conversion method, the user types the character code in hexadecimal and then enters ALT+X.</span></span> <span data-ttu-id="9d717-106">Der IME ersetzt die hexadezimalen Ziffern vor der Einfügemarke durch das Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9d717-106">The IME replaces the hexadecimal digits preceding the insertion point with the Unicode character.</span></span> <span data-ttu-id="9d717-107">Wenn die aktuelle Schriftart den Zeichencode nicht unterstützt, wird eine entsprechende Schriftart ausgewählt, die diese unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9d717-107">If the current font does not support the character code, an appropriate font is chosen that does support it.</span></span> <span data-ttu-id="9d717-108">Zum Konvertieren von Unicode in Hexadezimal gibt der Benutzer UMSCHALT + ALT + X ein.</span><span class="sxs-lookup"><span data-stu-id="9d717-108">To convert from Unicode to hexadecimal, the user enters SHIFT+ALT+X.</span></span> <span data-ttu-id="9d717-109">Dieser Eintrag ersetzt das Unicode-Zeichen, das der Einfügemarke vorangestellt ist, durch die hexadezimalen Ziffern.</span><span class="sxs-lookup"><span data-stu-id="9d717-109">This entry replaces the Unicode character that precedes the insertion point with the hexadecimal digits.</span></span> <span data-ttu-id="9d717-110">Diese Methode ermöglicht es dem Benutzer insbesondere, das Zeichen zu bestimmen, das durch einen Indikator "fehlende Glyphe" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9d717-110">In particular, this method allows the user to determine the character that is indicated by a "missing glyph" indicator.</span></span> <span data-ttu-id="9d717-111">Wenn der hexadezimale Zeichencode direkt auf einige legitime (nicht Zeichen) hexadezimale Zeichen folgt, wählt der Benutzer die zu konvertierenden Ziffern aus, bevor ALT + X eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9d717-111">If the hexadecimal character code immediately follows some legitimate (noncharacter) hexadecimal characters, the user selects the specific digits to convert before typing ALT+X.</span></span> <span data-ttu-id="9d717-112">Ein Problem mit dieser ersten Methode besteht darin, dass alt + X manchmal als Tastenkombination für den Exit-Befehl verwendet wird (d. h. Exit).</span><span class="sxs-lookup"><span data-stu-id="9d717-112">A problem with this first method is that ALT+X is sometimes used as a key combination for the exit command (that is, eXit).</span></span> <span data-ttu-id="9d717-113">In Microsoft Office wird dieser Befehl z. b. nur als Option des Menüs **Datei** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d717-113">For example, in Microsoft Office, this command only appears as an option of the **File** menu.</span></span>

<span data-ttu-id="9d717-114">Die zweite Methode zur typumrechnung zwischen hexadezimalen und Unicode-Zeichen umfasst das Zahlen Pad.</span><span class="sxs-lookup"><span data-stu-id="9d717-114">The second method of converting between hexadecimal and Unicode characters involves the number pad.</span></span> <span data-ttu-id="9d717-115">Mit dieser Methode geben die Benutzer alt + numaufszahlen (mit Werten größer als 255) ein, um Unicode-Zeichen mithilfe von Dezimalwerten einzugeben.</span><span class="sxs-lookup"><span data-stu-id="9d717-115">Using this method, the user types ALT+NumPad numbers (with values greater than 255) to enter Unicode characters using decimal values.</span></span> <span data-ttu-id="9d717-116">Diese Methode ist nicht so nützlich wie die erste, da der Benutzer nicht sehen kann, welche hexadezimalen Ziffern eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="9d717-116">This method is not as useful as the first because the user cannot see what hexadecimal digits have been typed.</span></span> <span data-ttu-id="9d717-117">Außerdem kann der Benutzer die hexadezimalen Ziffern nur dann korrigieren, wenn alle Ziffern erneut eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9d717-117">Also, the user cannot correct the hexadecimal digits except by re-entering all the digits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d717-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d717-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d717-119">Informationen über den Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="9d717-119">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 



