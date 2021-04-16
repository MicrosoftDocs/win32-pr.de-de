---
title: Symbol Ressource
description: Definiert eine Bitmap, die die Form des Symbols definiert, das für eine bestimmte Anwendung oder ein animiertes Symbol verwendet werden soll.
ms.assetid: a8e3205e-e17a-4daf-a599-4dc89cb1e640
keywords:
- Symbol Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f762c4f4b459d51a0243a9cdbd7367deda7b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516733"
---
# <a name="icon-resource"></a><span data-ttu-id="9f977-104">Symbol Ressource</span><span class="sxs-lookup"><span data-stu-id="9f977-104">ICON resource</span></span>

<span data-ttu-id="9f977-105">Definiert eine Bitmap, die die Form des Symbols definiert, das für eine bestimmte Anwendung oder ein animiertes Symbol verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9f977-105">Defines a bitmap that defines the shape of the icon to be used for a given application or an animated icon.</span></span>

``` syntax
nameID ICON filename
```

## <a name="parameters"></a><span data-ttu-id="9f977-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f977-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f977-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*</span><span class="sxs-lookup"><span data-stu-id="9f977-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="9f977-108">Eindeutiger Name oder ein 16-Bit-Ganzzahl-Wert ohne Vorzeichen, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9f977-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9f977-109"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="9f977-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="9f977-110">Der Name der Datei, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="9f977-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="9f977-111">Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="9f977-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="9f977-112">Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.</span><span class="sxs-lookup"><span data-stu-id="9f977-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="9f977-113">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f977-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="9f977-114">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="9f977-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9f977-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f977-115">Remarks</span></span>

<span data-ttu-id="9f977-116">Symbol-und Cursor Ressourcen können mehr als ein Bild enthalten.</span><span class="sxs-lookup"><span data-stu-id="9f977-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="9f977-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9f977-117">Examples</span></span>

<span data-ttu-id="9f977-118">Im folgenden Beispiel werden zwei Symbol Ressourcen definiert:</span><span class="sxs-lookup"><span data-stu-id="9f977-118">The following example defines two icon resources:</span></span>

``` syntax
desk1   ICON "desk.ico"
11      ICON "custom.ico"
```

## <a name="see-also"></a><span data-ttu-id="9f977-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f977-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f977-120">Verwenden von Symbolen</span><span class="sxs-lookup"><span data-stu-id="9f977-120">Using Icons</span></span>](./using-icons.md)
</dt> </dl>

 

 