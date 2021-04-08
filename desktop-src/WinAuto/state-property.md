---
title: State-Eigenschaft
description: Die State-Eigenschaft beschreibt den Status eines Objekts zu einem bestimmten Zeitpunkt. Alle-Objekte unterstützen die State-Eigenschaft.
ms.assetid: 6a56070f-7913-45b2-b693-3c0a8b7fa2f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151f09fca6c31abaaa98a19139d3e22eb28ec90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856860"
---
# <a name="state-property"></a><span data-ttu-id="c37f7-104">State-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c37f7-104">State Property</span></span>

<span data-ttu-id="c37f7-105">Die **State** -Eigenschaft beschreibt den Status eines Objekts zu einem bestimmten Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="c37f7-105">The **State** property describes an object's status at a moment in time.</span></span> <span data-ttu-id="c37f7-106">Alle-Objekte unterstützen die **State** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c37f7-106">All objects support the **State** property.</span></span>

<span data-ttu-id="c37f7-107">Die **State** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c37f7-107">The **State** property is retrieved by calling [**IAccessible::get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate).</span></span>

<span data-ttu-id="c37f7-108">Microsoft Active Accessibility bietet in Oleacc. h definierte [Objekt Zustands Konstanten](object-state-constants.md), die zum Identifizieren des Zustands eines Objekts kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="c37f7-108">Microsoft Active Accessibility provides [object state constants](object-state-constants.md), defined in oleacc.h, that are combined to identify an object's state.</span></span> <span data-ttu-id="c37f7-109">Es wird empfohlen, dass Server Entwickler diese vordefinierten Zustands Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="c37f7-109">It is recommended that server developers use these predefined state values.</span></span> <span data-ttu-id="c37f7-110">Wenn vordefinierte Zustands Werte zurückgegeben werden, wird [**getstatetext**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) von Clients verwendet, um eine lokalisierte Zeichenfolge abzurufen, die den Zustand beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c37f7-110">If predefined state values are returned, clients use [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) to retrieve a localized string that describes the state.</span></span>

<span data-ttu-id="c37f7-111">Für Grafiken, die gelegentlich animiert werden, sollte die Eigenschaft **State** auf [**State \_ System \_ animiert**](object-state-constants.md) und die [**Role**](role-property.md) -Eigenschaft auf [**Role System- \_ \_ Grafik**](object-roles.md)festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="c37f7-111">Graphics that are occasionally animated should have the **State** property set to [**STATE\_SYSTEM\_ANIMATED**](object-state-constants.md) and the [**Role**](role-property.md) property set to [**ROLE\_SYSTEM\_GRAPHIC**](object-roles.md).</span></span>

 

 




