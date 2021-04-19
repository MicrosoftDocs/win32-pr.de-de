---
description: Die in der folgenden Tabelle aufgeführten Funktionen übersetzen Zeichen folgen aus einem Zeichen folgertyp in einen anderen.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Übersetzung zwischen Zeichen folgen Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349442"
---
# <a name="translation-between-string-types"></a><span data-ttu-id="ed11f-103">Übersetzung zwischen Zeichen folgen Typen</span><span class="sxs-lookup"><span data-stu-id="ed11f-103">Translation Between String Types</span></span>

<span data-ttu-id="ed11f-104">Die in der folgenden Tabelle aufgeführten Funktionen übersetzen Zeichen folgen aus einem Zeichen folgertyp in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="ed11f-104">The functions listed in the following table translate character strings from one string type to another.</span></span>



| <span data-ttu-id="ed11f-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="ed11f-105">Function</span></span>                                           | <span data-ttu-id="ed11f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed11f-106">Description</span></span>                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="ed11f-107">**FoldString**</span><span class="sxs-lookup"><span data-stu-id="ed11f-107">**FoldString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | <span data-ttu-id="ed11f-108">Übersetzt eine Zeichenfolge in eine andere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ed11f-108">Translates one character string to another.</span></span>             |
| [<span data-ttu-id="ed11f-109">**LCMapString**</span><span class="sxs-lookup"><span data-stu-id="ed11f-109">**LCMapString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | <span data-ttu-id="ed11f-110">Ordnet eine Zeichenfolge nach dem Gebiets Schema zu.</span><span class="sxs-lookup"><span data-stu-id="ed11f-110">Maps a character string by locale.</span></span>                      |
| [<span data-ttu-id="ed11f-111">**Zu Unicode**</span><span class="sxs-lookup"><span data-stu-id="ed11f-111">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)              | <span data-ttu-id="ed11f-112">Übersetzt einen virtuellen Schlüsselcode in ein Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ed11f-112">Translates a virtual key code into a Unicode character.</span></span> |
| [<span data-ttu-id="ed11f-113">**MultiByteToWideChar muss**</span><span class="sxs-lookup"><span data-stu-id="ed11f-113">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | <span data-ttu-id="ed11f-114">Ordnet eine Multibytezeichenfolge einer Unicode-Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="ed11f-114">Maps a multibyte string to a Unicode string.</span></span>            |
| [<span data-ttu-id="ed11f-115">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="ed11f-115">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | <span data-ttu-id="ed11f-116">Ordnet eine Unicode-Zeichenfolge einer Multibytezeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="ed11f-116">Maps a Unicode string to a multibyte string.</span></span>            |



 

<span data-ttu-id="ed11f-117">Die Funktionen [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) und [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) sind besonders nützlich für Anwendungen, die mehrere Zeichen folgen Typen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ed11f-117">The [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) functions are particularly useful for applications that support several string types.</span></span> <span data-ttu-id="ed11f-118">ANSI C definiert auch die Konvertierungs Funktionen **wcstomb** und **mbstowcs**, aber Sie können nur in den und aus dem von der Standard-C-Bibliothek unterstützten Zeichensatz konvertieren.</span><span class="sxs-lookup"><span data-stu-id="ed11f-118">ANSI C also defines the conversion functions **wcstombs** and **mbstowcs**, but they can only convert to and from the character set supported by the standard C library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed11f-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed11f-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed11f-120">Unicode in der Windows-API</span><span class="sxs-lookup"><span data-stu-id="ed11f-120">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
