---
description: Der anypath-Datentyp ist eine Text Zeichenfolge, die entweder einen vollständigen Pfad oder einen relativen Pfad enthält.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: Anypath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347547"
---
# <a name="anypath"></a><span data-ttu-id="1f021-103">Anypath</span><span class="sxs-lookup"><span data-stu-id="1f021-103">AnyPath</span></span>

<span data-ttu-id="1f021-104">Der anypath-Datentyp ist eine Text Zeichenfolge, die entweder einen vollständigen Pfad oder einen relativen Pfad enthält.</span><span class="sxs-lookup"><span data-stu-id="1f021-104">The AnyPath data type is a text string containing either a full path or a relative path.</span></span> <span data-ttu-id="1f021-105">Wenn Sie einen relativen Pfad angeben, können Sie einen langen Dateinamen mit dem kurzen Dateinamen einschließen, indem Sie die kurz-und lange Namen durch einen senkrechten Strich ( \| ) trennen.</span><span class="sxs-lookup"><span data-stu-id="1f021-105">When specifying a relative path, you can include a long file name with the short file name by separating the short and long names with a vertical bar (\|).</span></span> <span data-ttu-id="1f021-106">Beachten Sie, dass auf diese Weise nicht mehrere Ebenen eines Verzeichnisses oder voll qualifizierte Pfade angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="1f021-106">Note that you cannot specify multiple levels of a directory or fully qualified paths in this way.</span></span> <span data-ttu-id="1f021-107">Der Pfad kann Eigenschaften enthalten, die in eckigen Klammern () eingeschlossen sind \[ \] .</span><span class="sxs-lookup"><span data-stu-id="1f021-107">The path may contain properties enclosed within square brackets (\[ \]).</span></span>

<span data-ttu-id="1f021-108">Beispiele für gültige anypath-Daten:</span><span class="sxs-lookup"><span data-stu-id="1f021-108">Examples of valid AnyPath data:</span></span>

-   <span data-ttu-id="1f021-109">\\\\temporäre Server \\ Freigabe \\</span><span class="sxs-lookup"><span data-stu-id="1f021-109">\\\\server\\share\\temp</span></span>
-   <span data-ttu-id="1f021-110">c: \\ Temp</span><span class="sxs-lookup"><span data-stu-id="1f021-110">c:\\temp</span></span>
-   <span data-ttu-id="1f021-111">\\Temp</span><span class="sxs-lookup"><span data-stu-id="1f021-111">\\temp</span></span>
-   <span data-ttu-id="1f021-112">PROJEC ~ 1 \| Projekt Status</span><span class="sxs-lookup"><span data-stu-id="1f021-112">projec~1\|Project Status</span></span>

<span data-ttu-id="1f021-113">Beispiele für ungültige anypath-Daten:</span><span class="sxs-lookup"><span data-stu-id="1f021-113">Examples of invalid AnyPath data:</span></span>

-   <span data-ttu-id="1f021-114">c: \\ Temp \\ PROJEC ~ 1 \| c: \\ Temp ein \\ Projekt Status</span><span class="sxs-lookup"><span data-stu-id="1f021-114">c:\\temp\\projec~1\|c:\\temp one\\Project Status</span></span>
-   <span data-ttu-id="1f021-115">\\Temp- \\ PROJEC ~ 1 \| \\ Temp ein \\ Projekt Status</span><span class="sxs-lookup"><span data-stu-id="1f021-115">\\temp\\projec~1\|\\temp one\\Project Status</span></span>

 

 



