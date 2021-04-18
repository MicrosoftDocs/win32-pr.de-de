---
description: Definieren von benutzerdefinierten Eigenschaften.
ms.assetid: 6adcf414-2c5a-451c-b30a-d1c161886c9a
title: Definieren von benutzerdefinierten Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd91ee4d4e657ce0d6c01330d85e8df4ef57a36d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347598"
---
# <a name="defining-custom-properties"></a><span data-ttu-id="85c5d-103">Definieren von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="85c5d-103">Defining Custom Properties</span></span>

<span data-ttu-id="85c5d-104">**Definieren von benutzerdefinierten Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="85c5d-104">**Defining Custom Properties**.</span></span>

<span data-ttu-id="85c5d-105">Wenn es erforderlich ist, dass der Windows-Abbild Erfassungs Dienst (WIA) benutzerdefinierte Eigenschaften definiert, sollte die WIA \_ private \_ devprop-Eigenschaft für benutzerdefinierte Stamm Element Eigenschaften verwendet werden, und die WIA \_ private \_ ItemProp-Eigenschaft sollte für andere Element Eigenschaften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85c5d-105">If it is necessary for the Windows Image Acquisition (WIA) minidriver to define custom properties, the WIA\_PRIVATE\_DEVPROP property should be used for custom root item properties, and the WIA\_PRIVATE\_ITEMPROP" property should be used for other item properties.</span></span> <span data-ttu-id="85c5d-106">Diese Konstanten werden in *wiadef. h* definiert.</span><span class="sxs-lookup"><span data-stu-id="85c5d-106">These constants are defined in *wiadef.h*.</span></span>

<span data-ttu-id="85c5d-107">Der folgende Beispielcode zeigt Definitionen für drei Stamm Element Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85c5d-107">The following example code shows definitions for three root item properties.</span></span> <span data-ttu-id="85c5d-108">Die Eigenschaften-ID für die erste benutzerdefinierte root-Element Eigenschaft, die benutzerdefinierte Stamm-Prop-Eigenschaft \_ \_ \_ 1, wird in Form von WIA \_ private \_ devprop definiert.</span><span class="sxs-lookup"><span data-stu-id="85c5d-108">The property ID for the first custom root item property, CUSTOM\_ROOT\_PROP\_1, is defined in terms of WIA\_PRIVATE\_DEVPROP.</span></span> <span data-ttu-id="85c5d-109">Eigenschaften-IDs für zusätzliche Stamm Element Eigenschaften werden in Form von WIA \_ private \_ devprop + 1, WIA \_ private \_ devprop + 2 usw. definiert.</span><span class="sxs-lookup"><span data-stu-id="85c5d-109">Property IDs for additional root item properties are defined in terms of WIA\_PRIVATE\_DEVPROP + 1, WIA\_PRIVATE\_DEVPROP + 2, and so on.</span></span> <span data-ttu-id="85c5d-110">Das Muster kann fortgesetzt werden, wenn zusätzliche benutzerdefinierte Stamm Element Eigenschaften benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="85c5d-110">The pattern can be continued if additional custom root item properties are needed.</span></span>


```
#define CUSTOM_ROOT_PROP_1 WIA_PRIVATE_DEVPROP
#define CUSTOM_ROOT_PROP_2 (WIA_PRIVATE_DEVPROP + 1) 
#define CUSTOM_ROOT_PROP_3 (WIA_PRIVATE_DEVPROP + 2)
```



<span data-ttu-id="85c5d-111">Das nächste Beispiel zeigt Definitionen für drei benutzerdefinierte untergeordnete Element Eigenschaften und Eigenschaften-IDs.</span><span class="sxs-lookup"><span data-stu-id="85c5d-111">The next example shows definitions for three custom child item properties and property IDs.</span></span> <span data-ttu-id="85c5d-112">Die Eigenschaften-ID für die erste benutzerdefinierte untergeordnete Element Eigenschaft, benutzerdefinierte untergeordnete \_ \_ Prop \_ 1, wird in Form von WIA \_ private \_ ItemProp definiert.</span><span class="sxs-lookup"><span data-stu-id="85c5d-112">The property ID for the first custom child item property, CUSTOM\_CHILD\_PROP\_1, is defined in terms of WIA\_PRIVATE\_ITEMPROP.</span></span> <span data-ttu-id="85c5d-113">Eigenschaften-IDs für zusätzliche untergeordnete Element Eigenschaften werden in Form von WIA \_ private \_ ItemProp + 1 usw. definiert.</span><span class="sxs-lookup"><span data-stu-id="85c5d-113">Property IDs for additional child item properties are defined in terms of WIA\_PRIVATE\_ITEMPROP + 1, and so on.</span></span> <span data-ttu-id="85c5d-114">Wie zuvor kann das Muster fortgesetzt werden, wenn mehr dieser Eigenschaften für ein benutzerdefiniertes untergeordnetes Element benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="85c5d-114">As before, the pattern can be continued if more of these custom child item properties are needed.</span></span>


```
#define CUSTOM_CHILD_PROP_1 WIA_PRIVATE_ITEMPROP
#define CUSTOM_CHILD_PROP_2 (WIA_PRIVATE_ITEMPROP + 1)
#define CUSTOM_CHILD_PROP_3 (WIA_PRIVATE_ITEMPROP + 2)
```



<span data-ttu-id="85c5d-115">Benutzerdefinierte WIA-Eigenschaften müssen benutzerdefinierte Eigenschaftsnamen aufweisen, die den benutzerdefinierten Eigenschaften-IDs zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="85c5d-115">Custom WIA properties must have custom property names that are associated with the custom property IDs.</span></span> <span data-ttu-id="85c5d-116">Der folgende Beispielcode zeigt Definitionen für drei benutzerdefinierte Stamm Element-Eigenschaften Namen.</span><span class="sxs-lookup"><span data-stu-id="85c5d-116">The following example code shows definitions for three custom root item property names.</span></span> <span data-ttu-id="85c5d-117">(Diese Eigenschaftsnamen werden mit den benutzerdefinierten Eigenschaften-IDs verwendet, die in einem vorherigen Beispiel erstellt wurden, wobei der Name der benutzerdefinierten Eigenschaft in Custom \_ Root \_ Prop \_ 1 \_ str ist der benutzerdefinierten Stamm-ID des Stamm Elements \_ root \_ Prop \_ 1 zugeordnet.)</span><span class="sxs-lookup"><span data-stu-id="85c5d-117">(These property names are used with the custom property IDs that were created in a previous example, where the custom property name contained in CUSTOM\_ROOT\_PROP\_1\_STR is associated with the custom root item property ID CUSTOM\_ROOT\_PROP\_1.)</span></span>


```
#define CUSTOM_ROOT_PROP_1_STR L"My First Custom Root Item Property"
#define CUSTOM_ROOT_PROP_2_STR L"My Second Custom Root Item Property"
#define CUSTOM_ROOT_PROP_3_STR L"My Third Custom Root Item Property"
```



> [!Note]  
> <span data-ttu-id="85c5d-118">WIA-Eigenschaften Namen sind in mehreren Sprachen *nicht* lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="85c5d-118">WIA property names are *not* localized in multiple languages.</span></span> <span data-ttu-id="85c5d-119">Dies liegt daran, dass WIA-Eigenschaften von Anwendungen gelesen werden können, die die Eigenschaften-ID oder den Eigenschaften Namen verwenden.</span><span class="sxs-lookup"><span data-stu-id="85c5d-119">This is because WIA properties can be read by applications using the property ID or the property name.</span></span> <span data-ttu-id="85c5d-120">Wenn der Name verwendet wird, muss er eine Konstante sein, ebenso wie die eigen schafts-ID.</span><span class="sxs-lookup"><span data-stu-id="85c5d-120">If the name is used, it must be a constant, just as the property ID is.</span></span>

 

 

 



