---
title: Menü Ressource
description: Definiert den Inhalt einer Menü Ressource. | Menü Ressource
ms.assetid: fcb420b6-d42e-4044-89ee-028eed1f21ee
keywords:
- Menü Ressourcen Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- MENU
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5cdb564c7bf012255b339a13691d2ecf214a86
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106350644"
---
# <a name="menu-resource"></a><span data-ttu-id="288cf-105">Menü Ressource</span><span class="sxs-lookup"><span data-stu-id="288cf-105">MENU resource</span></span>

<span data-ttu-id="288cf-106">Definiert den Inhalt einer Menü Ressource.</span><span class="sxs-lookup"><span data-stu-id="288cf-106">Defines the contents of a menu resource.</span></span> <span data-ttu-id="288cf-107">Eine Menü Ressource ist eine Auflistung von Informationen, die das Aussehen und die Funktion eines Anwendungs Menüs definiert.</span><span class="sxs-lookup"><span data-stu-id="288cf-107">A menu resource is a collection of information that defines the appearance and function of an application menu.</span></span> <span data-ttu-id="288cf-108">Ein Menü ist ein spezielles Eingabe Tool, mit dem ein Benutzer Befehle auswählen und Untermenüs aus einer Liste von Menü Elementen öffnen kann.</span><span class="sxs-lookup"><span data-stu-id="288cf-108">A menu is a special input tool that lets a user select commands and open submenus from a list of menu items.</span></span>

``` syntax
menuID MENU  [optional-statements]  {item-definitions ... }
```

## <a name="parameters"></a><span data-ttu-id="288cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="288cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="288cf-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*MENUID*</span><span class="sxs-lookup"><span data-stu-id="288cf-110"><span id="menuID"></span><span id="menuid"></span><span id="MENUID"></span>*menuID*</span></span>
</dt> <dd>

<span data-ttu-id="288cf-111">Die Zahl, die das Menü angibt.</span><span class="sxs-lookup"><span data-stu-id="288cf-111">Number that identifies the menu.</span></span> <span data-ttu-id="288cf-112">Dieser Wert ist entweder eine eindeutige Zeichenfolge oder eine eindeutige 16-Bit-Ganzzahl ohne Vorzeichen im Bereich von 1 bis 65.535.</span><span class="sxs-lookup"><span data-stu-id="288cf-112">This value is either a unique string or a unique 16-bit unsigned integer value in the range of 1 to 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="288cf-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="288cf-113"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="288cf-114">Dieser Parameter kann NULL von mehreren der folgenden Anweisungen sein.</span><span class="sxs-lookup"><span data-stu-id="288cf-114">This parameter can be zero of more of the following statements.</span></span>



| <span data-ttu-id="288cf-115">-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="288cf-115">Statement</span></span>                                                        | <span data-ttu-id="288cf-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="288cf-116">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="288cf-117">[**Merkmale**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="288cf-117">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="288cf-118">Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="288cf-118">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="288cf-119">Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="288cf-119">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="288cf-120">[**Sprach**](language-statement.md) *Sprache*, *unter Sprache*</span><span class="sxs-lookup"><span data-stu-id="288cf-120">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="288cf-121">Sprache für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="288cf-121">Language for the resource.</span></span> <span data-ttu-id="288cf-122">Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="288cf-122">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="288cf-123">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="288cf-123">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="288cf-124">Eine benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="288cf-124">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="288cf-125">Weitere Informationen finden Sie unter [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="288cf-125">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> </dl>

<span data-ttu-id="288cf-126">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="288cf-126">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="288cf-127">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="288cf-127">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="288cf-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="288cf-128">Examples</span></span>

<span data-ttu-id="288cf-129">Im folgenden finden Sie ein Beispiel für eine Complete **Menu** -Anweisung:</span><span class="sxs-lookup"><span data-stu-id="288cf-129">The following is an example of a complete **MENU** statement:</span></span>

``` syntax
sample MENU
{
     MENUITEM "&Soup", 100
     MENUITEM "S&alad", 101
     POPUP "&Entree"
     {
          MENUITEM "&Fish", 200
          MENUITEM "&Chicken", 201, CHECKED
          POPUP "&Beef"
          {
               MENUITEM "&Steak", 301
               MENUITEM "&Prime Rib", 302
          }
     }
     MENUITEM "&Dessert", 103
}
```

## <a name="see-also"></a><span data-ttu-id="288cf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="288cf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="288cf-131">Verwenden von Menüs</span><span class="sxs-lookup"><span data-stu-id="288cf-131">Using Menus</span></span>](./using-menus.md)
</dt> <dt>

[<span data-ttu-id="288cf-132">**Accelerators**</span><span class="sxs-lookup"><span data-stu-id="288cf-132">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="288cf-133">**Charakteristik**</span><span class="sxs-lookup"><span data-stu-id="288cf-133">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="288cf-134">**Kurse**</span><span class="sxs-lookup"><span data-stu-id="288cf-134">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="288cf-135">**Menuex**</span><span class="sxs-lookup"><span data-stu-id="288cf-135">**MENUEX**</span></span>](menuex-resource.md)
</dt> <dt>

[<span data-ttu-id="288cf-136">**MENUITEM**</span><span class="sxs-lookup"><span data-stu-id="288cf-136">**MENUITEM**</span></span>](menuitem-statement.md)
</dt> <dt>

[<span data-ttu-id="288cf-137">**Up**</span><span class="sxs-lookup"><span data-stu-id="288cf-137">**POPUP**</span></span>](popup-resource.md)
</dt> <dt>

[<span data-ttu-id="288cf-138">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="288cf-138">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="288cf-139">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="288cf-139">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="288cf-140">**Version**</span><span class="sxs-lookup"><span data-stu-id="288cf-140">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
