---
title: Accnamecontainsinvalidstring
description: Accnamecontainsinvalidstring
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338618"
---
# <a name="accnamecontainsinvalidstring"></a><span data-ttu-id="aa1fa-103">Accnamecontainsinvalidstring</span><span class="sxs-lookup"><span data-stu-id="aa1fa-103">AccNameContainsInvalidString</span></span>

## <a name="text"></a><span data-ttu-id="aa1fa-104">Text</span><span class="sxs-lookup"><span data-stu-id="aa1fa-104">Text</span></span>

<span data-ttu-id="aa1fa-105">"accName" darf die Zeichenfolge nicht enthalten. {0}</span><span class="sxs-lookup"><span data-stu-id="aa1fa-105">accName should not contain the string {0}</span></span>

## <a name="type"></a><span data-ttu-id="aa1fa-106">type</span><span class="sxs-lookup"><span data-stu-id="aa1fa-106">Type</span></span>

<span data-ttu-id="aa1fa-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="aa1fa-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="aa1fa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa1fa-108">Description</span></span>

<span data-ttu-id="aa1fa-109">Der Name eines Elements enthält ungültige Zeichen (diese Zeichen werden durch die Zugriffs Prüfung ersetzt).</span><span class="sxs-lookup"><span data-stu-id="aa1fa-109">The name of an element contains invalid characters (these characters are replaced by AccChecker).</span></span> <span data-ttu-id="aa1fa-110">Beispielsweise gibt die [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) -Methode, die zum Abrufen des MSAA-Namens eines Elements verwendet wird, eine Zeichenfolge zurück, die Tabulator-, Zeilen-oder Zeichen-und Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="aa1fa-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string that contains tab, newline, or ampersand characters.</span></span>

<span data-ttu-id="aa1fa-111">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da ein Element möglicherweise einen nicht Aussage fähigen, nicht intuitiven Namen hat.</span><span class="sxs-lookup"><span data-stu-id="aa1fa-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="aa1fa-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="aa1fa-112">Possible causes</span></span>

<span data-ttu-id="aa1fa-113">Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="aa1fa-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa1fa-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa1fa-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa1fa-115">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="aa1fa-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="aa1fa-116">Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="aa1fa-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




