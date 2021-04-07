---
description: Der Schlüssel Qualifizierer gibt an, ob die Eigenschaft Teil des Namespace Handles ist.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Schlüssel Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758323"
---
# <a name="key-qualifier"></a><span data-ttu-id="acb3c-103">Schlüssel Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="acb3c-103">Key Qualifier</span></span>

<span data-ttu-id="acb3c-104">Der **Schlüssel** Qualifizierer gibt an, ob die Eigenschaft Teil des Namespace Handles ist.</span><span class="sxs-lookup"><span data-stu-id="acb3c-104">The **Key** qualifier indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="acb3c-105">Wenn mehr als eine Eigenschaft den **Schlüssel** Qualifizierer aufweist, bilden alle diese Eigenschaften zusammen den Schlüssel (einen Verbund Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="acb3c-105">If more than one property has the **Key** qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="acb3c-106">Bei gemeinsamer Erstellung müssen die Schlüsseleigenschaften einen eindeutigen Verweis für jede Klasseninstanz angeben.</span><span class="sxs-lookup"><span data-stu-id="acb3c-106">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="acb3c-107">Wenn dieser Qualifizierer für eine Eigenschaft platziert wird, ist nur der Wert **true** zulässig.</span><span class="sxs-lookup"><span data-stu-id="acb3c-107">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

<span data-ttu-id="acb3c-108">Sie können einen beliebigen Eigenschaftentyp verwenden, mit Ausnahme der folgenden:</span><span class="sxs-lookup"><span data-stu-id="acb3c-108">You can use any property type except for the following:</span></span>

-   <span data-ttu-id="acb3c-109">Arrays</span><span class="sxs-lookup"><span data-stu-id="acb3c-109">Arrays</span></span>
-   <span data-ttu-id="acb3c-110">Real-und Gleit Komma Zahlen</span><span class="sxs-lookup"><span data-stu-id="acb3c-110">Real and floating-point numbers</span></span>
-   <span data-ttu-id="acb3c-111">Eingebettete Objekte</span><span class="sxs-lookup"><span data-stu-id="acb3c-111">Embedded objects</span></span>
-   <span data-ttu-id="acb3c-112">Zeichen niedriger als ASCII 32 (d. h. Leerzeichen)</span><span class="sxs-lookup"><span data-stu-id="acb3c-112">Characters lower than ASCII 32 (that is, white space characters)</span></span>
-   <span data-ttu-id="acb3c-113">Zeichen folgen vom Typ **char16** oder Zeichen folgen, die als Schlüssel definiert sind, müssen Werte größer als U + 0020 enthalten.</span><span class="sxs-lookup"><span data-stu-id="acb3c-113">Character strings of type **char16** or character strings that are defined as keys must contain values greater than U+0020.</span></span> <span data-ttu-id="acb3c-114">Dies liegt daran, dass WMI Schlüsselwerte in Objekt Pfaden verwendet und Sie keine nicht druckbaren Zeichen in einem Objekt Pfad verwenden können.</span><span class="sxs-lookup"><span data-stu-id="acb3c-114">This is because WMI uses key values in object paths, and you cannot use nonprinting characters in an object path.</span></span>

<span data-ttu-id="acb3c-115">Wenn eine übergeordnete Klasse einen Schlüssel angibt, erben alle Klassen, die von der übergeordneten Klasse abgeleitet sind, diesen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="acb3c-115">When a parent class specifies a key, all classes derived from the parent class inherit that key.</span></span> <span data-ttu-id="acb3c-116">Die abgeleiteten Klassen können den geerbten Schlüssel nicht ändern oder eine neue Schlüsseleigenschaft definieren.</span><span class="sxs-lookup"><span data-stu-id="acb3c-116">The derived classes cannot alter the inherited key or define any new key property.</span></span> <span data-ttu-id="acb3c-117">Wenn Sie jedoch eine Unterklasse von einer abstrakten Klasse ohne einen Schlüssel ableiten, können Sie einen Schlüssel in der Unterklasse einfügen.</span><span class="sxs-lookup"><span data-stu-id="acb3c-117">However, when you derive a subclass from an abstract class without a key, you can introduce a key in the subclass.</span></span>

<span data-ttu-id="acb3c-118">Alle Klassen, die mehr als eine Instanz definieren, müssen einen Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="acb3c-118">All classes that define more than one instance must specify a key.</span></span> <span data-ttu-id="acb3c-119">Da abstrakte Klassen keine-Instanzen definieren, müssen Sie keine Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="acb3c-119">Because abstract classes do not define any instances, they do not need to specify keys.</span></span> <span data-ttu-id="acb3c-120">Da Singleton-Klassen nur eine Instanz definieren, können Sie keine Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="acb3c-120">Because singleton classes define only one instance, they cannot specify keys.</span></span>

<span data-ttu-id="acb3c-121">Schlüssel werden bei der Objekt Instanziierung einmal geschrieben und dürfen nicht später geändert werden.</span><span class="sxs-lookup"><span data-stu-id="acb3c-121">Keys are written one time at object instantiation and must not be modified later.</span></span> <span data-ttu-id="acb3c-122">Es ist nicht sinnvoll, einen Standardwert auf eine Schlüssel qualifizierte Eigenschaft anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="acb3c-122">It does not make sense to apply a default value to a key-qualified property.</span></span>

## <a name="requirements"></a><span data-ttu-id="acb3c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acb3c-123">Requirements</span></span>



| <span data-ttu-id="acb3c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acb3c-124">Requirement</span></span> | <span data-ttu-id="acb3c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="acb3c-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="acb3c-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="acb3c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="acb3c-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acb3c-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="acb3c-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="acb3c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="acb3c-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acb3c-129">Windows Server 2008</span></span><br/> |



 

 




