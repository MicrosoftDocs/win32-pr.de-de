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
# <a name="using-null-terminated-strings"></a><span data-ttu-id="4d423-103">Verwenden von auf NULL endenden Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="4d423-103">Using Null-terminated Strings</span></span>

<span data-ttu-id="4d423-104">Ihre Unicode-Anwendungen sollten bei der Verwendung von mit NULL endenden Zeichen folgen immer NULL in Tchar umwandeln.</span><span class="sxs-lookup"><span data-stu-id="4d423-104">Your Unicode applications should always cast zero to TCHAR when using null-terminated strings.</span></span> <span data-ttu-id="4d423-105">Der Code 0x0000 ist das Unicode-Zeichen folgen Abschluss Zeichen für eine NULL-terminierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4d423-105">The code 0x0000 is the Unicode string terminator for a null-terminated string.</span></span> <span data-ttu-id="4d423-106">Ein einzelnes Null-Byte ist für diesen Code nicht ausreichend, da viele Unicode-Zeichen NULL-Bytes als das hohe oder das niedrige Byte enthalten.</span><span class="sxs-lookup"><span data-stu-id="4d423-106">A single null byte is not sufficient for this code, because many Unicode characters contain null bytes as either the high or the low byte.</span></span> <span data-ttu-id="4d423-107">Ein Beispiel hierfür ist der Buchstabe A, bei dem der Zeichencode 0x0041 ist.</span><span class="sxs-lookup"><span data-stu-id="4d423-107">An example is the letter A, for which the character code is 0x0041.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d423-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d423-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d423-109">Verwenden von Sonderzeichen in Unicode</span><span class="sxs-lookup"><span data-stu-id="4d423-109">Using Special Characters in Unicode</span></span>](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



