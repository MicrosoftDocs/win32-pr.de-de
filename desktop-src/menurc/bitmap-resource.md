---
title: Bitmap-Ressource
description: Definiert eine Bitmap, die von einer Anwendung in der Bildschirm Anzeige oder als Element in einem Menü oder Steuerelement verwendet wird.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Bitmap-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390211"
---
# <a name="bitmap-resource"></a><span data-ttu-id="d4065-104">Bitmap-Ressource</span><span class="sxs-lookup"><span data-stu-id="d4065-104">BITMAP resource</span></span>

<span data-ttu-id="d4065-105">Definiert eine Bitmap, die von einer Anwendung in der Bildschirm Anzeige oder als Element in einem Menü oder Steuerelement verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4065-105">Defines a bitmap that an application uses in its screen display or as an item in a menu or control.</span></span>

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a><span data-ttu-id="d4065-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4065-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4065-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*</span><span class="sxs-lookup"><span data-stu-id="d4065-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="d4065-108">Eindeutiger Name oder ein 16-Bit-Ganzzahl-Wert ohne Vorzeichen, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d4065-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="d4065-109"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="d4065-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="d4065-110">Der Name der Datei, die die Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d4065-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="d4065-111">Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet.</span><span class="sxs-lookup"><span data-stu-id="d4065-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="d4065-112">Der Pfad muss eine Zeichenfolge in Anführungszeichen sein.</span><span class="sxs-lookup"><span data-stu-id="d4065-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="d4065-113">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4065-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="d4065-114">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d4065-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d4065-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4065-115">Examples</span></span>

<span data-ttu-id="d4065-116">Im folgenden Beispiel werden zwei Bitmapressourcen definiert:</span><span class="sxs-lookup"><span data-stu-id="d4065-116">The following example defines two bitmap resources:</span></span>

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a><span data-ttu-id="d4065-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4065-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4065-118">Verwenden von Bitmaps</span><span class="sxs-lookup"><span data-stu-id="d4065-118">Using Bitmaps</span></span>](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[<span data-ttu-id="d4065-119">**LoadBitmap**</span><span class="sxs-lookup"><span data-stu-id="d4065-119">**LoadBitmap**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[<span data-ttu-id="d4065-120">**LoadImage**</span><span class="sxs-lookup"><span data-stu-id="d4065-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 