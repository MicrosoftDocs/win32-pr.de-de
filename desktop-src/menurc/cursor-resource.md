---
title: Cursor Ressource
description: Definiert eine Bitmap, die die Form des Cursors auf dem Anzeige Bildschirm oder einen animierten Cursor definiert.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Cursor Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341714"
---
# <a name="cursor-resource"></a><span data-ttu-id="1ecba-104">Cursor Ressource</span><span class="sxs-lookup"><span data-stu-id="1ecba-104">CURSOR resource</span></span>

<span data-ttu-id="1ecba-105">Definiert eine Bitmap, die die Form des Cursors auf dem Anzeige Bildschirm oder einen animierten Cursor definiert.</span><span class="sxs-lookup"><span data-stu-id="1ecba-105">Defines a bitmap that defines the shape of the cursor on the display screen or an animated cursor.</span></span>

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a><span data-ttu-id="1ecba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ecba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ecba-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*</span><span class="sxs-lookup"><span data-stu-id="1ecba-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="1ecba-108">Eindeutiger Name oder eine 16-Bit-Ganzzahl ohne Vorzeichen, die die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1ecba-108">Unique name or a 16-bit unsigned integer identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="1ecba-109"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="1ecba-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="1ecba-110">Der Name der Datei, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="1ecba-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="1ecba-111">Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="1ecba-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="1ecba-112">Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.</span><span class="sxs-lookup"><span data-stu-id="1ecba-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="1ecba-113">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1ecba-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="1ecba-114">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1ecba-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ecba-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ecba-115">Remarks</span></span>

<span data-ttu-id="1ecba-116">Symbol-und Cursor Ressourcen können mehr als ein Bild enthalten.</span><span class="sxs-lookup"><span data-stu-id="1ecba-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="1ecba-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ecba-117">Examples</span></span>

<span data-ttu-id="1ecba-118">Im folgenden Beispiel werden zwei Cursor Ressourcen definiert: eine nach Namen (cursor1) und die andere nach Zahl (2):</span><span class="sxs-lookup"><span data-stu-id="1ecba-118">The following example defines two cursor resources; one by name (cursor1) and the other by number (2):</span></span>

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a><span data-ttu-id="1ecba-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ecba-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ecba-120">Verwenden von Cursors</span><span class="sxs-lookup"><span data-stu-id="1ecba-120">Using Cursors</span></span>](./using-cursors.md)
</dt> </dl>

 

 