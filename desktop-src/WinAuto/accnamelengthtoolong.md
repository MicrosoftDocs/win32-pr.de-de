---
title: Accnamelengthtoolong
description: Accnamelengthtoolong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337184"
---
# <a name="accnamelengthtoolong"></a><span data-ttu-id="89688-103">Accnamelengthtoolong</span><span class="sxs-lookup"><span data-stu-id="89688-103">AccNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="89688-104">Text</span><span class="sxs-lookup"><span data-stu-id="89688-104">Text</span></span>

<span data-ttu-id="89688-105">Der Element Name darf keine Zeichenfolge zurückgeben, die länger als Zeichen ist. {0}</span><span class="sxs-lookup"><span data-stu-id="89688-105">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="89688-106">type</span><span class="sxs-lookup"><span data-stu-id="89688-106">Type</span></span>

<span data-ttu-id="89688-107">Fehler</span><span class="sxs-lookup"><span data-stu-id="89688-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="89688-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="89688-108">Description</span></span>

<span data-ttu-id="89688-109">Der Name eines Elements enthält zu viele Zeichen.</span><span class="sxs-lookup"><span data-stu-id="89688-109">The name of an element contains too many characters.</span></span> <span data-ttu-id="89688-110">Beispielsweise gibt die [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) -Methode, die zum Abrufen des MSAA-Namens eines Elements verwendet wird, eine Zeichenfolge zurück, die größer ist als das Limit von 32000 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="89688-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string greater than the limit of 32000 characters.</span></span>

<span data-ttu-id="89688-111">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da ein Element möglicherweise einen nicht Aussage fähigen, nicht intuitiven Namen hat.</span><span class="sxs-lookup"><span data-stu-id="89688-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="89688-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="89688-112">Possible causes</span></span>

<span data-ttu-id="89688-113">Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="89688-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89688-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89688-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89688-115">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="89688-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="89688-116">Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="89688-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




