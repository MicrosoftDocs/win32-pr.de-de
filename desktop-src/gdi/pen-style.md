---
description: Das Style-Attribut gibt das Linien Muster an, das angezeigt wird, wenn ein bestimmter kosmetischer oder geometrischer Stift verwendet wird. Es gibt acht vordefinierte Stift Stile. Die folgende Abbildung zeigt die sieben dieser Stile, die vom System definiert werden.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Stift Stil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959304"
---
# <a name="pen-style"></a><span data-ttu-id="c82e2-105">Stift Stil</span><span class="sxs-lookup"><span data-stu-id="c82e2-105">Pen Style</span></span>

<span data-ttu-id="c82e2-106">Das Style-Attribut gibt das Linien Muster an, das angezeigt wird, wenn ein bestimmter kosmetischer oder geometrischer Stift verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c82e2-106">The style attribute specifies the line pattern that appears when a particular cosmetic or geometric pen is used.</span></span> <span data-ttu-id="c82e2-107">Es gibt acht vordefinierte Stift Stile.</span><span class="sxs-lookup"><span data-stu-id="c82e2-107">There are eight predefined pen styles.</span></span> <span data-ttu-id="c82e2-108">Die folgende Abbildung zeigt die sieben dieser Stile, die vom System definiert werden.</span><span class="sxs-lookup"><span data-stu-id="c82e2-108">The following illustration shows the seven of these styles that are defined by the system.</span></span>

![Abbildung, die sieben Zeilen anzeigt, die jeweils mit einem anderen vordefinierten Stil gezeichnet werden](images/cspen-01.png)

<span data-ttu-id="c82e2-110">Die innere Frame-Formatvorlage ist mit dem Stil für optische Stifte identisch.</span><span class="sxs-lookup"><span data-stu-id="c82e2-110">The inside-frame style is identical to the solid style for cosmetic pens.</span></span> <span data-ttu-id="c82e2-111">Sie funktioniert jedoch anders, wenn Sie mit einem geometrischen Stift verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c82e2-111">However, it operates differently when used with a geometric pen.</span></span> <span data-ttu-id="c82e2-112">Wenn der geometrische Stift breiter als ein einzelnes Pixel ist und eine Zeichnungs Funktion den Stift verwendet, um einen Rahmen um ein ausgefülltes Objekt zu zeichnen, zeichnet das System den Rahmen im Frame des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c82e2-112">If the geometric pen is wider than a single pixel and a drawing function uses the pen to draw a border around a filled object, the system draws the border inside the object's frame.</span></span> <span data-ttu-id="c82e2-113">Mithilfe der inneren Frame-Stil kann eine Anwendung sicherstellen, dass ein Objekt vollständig innerhalb der angegebenen Dimensionen angezeigt wird, unabhängig von der geometrischen Stift Breite.</span><span class="sxs-lookup"><span data-stu-id="c82e2-113">By using the inside-frame style, an application can ensure that an object appears entirely within the specified dimensions, regardless of the geometric pen width.</span></span>

<span data-ttu-id="c82e2-114">Zusätzlich zu den sieben vom System definierten Stilen gibt es einen achten Stil, bei dem es sich um einen definierten Benutzer (oder eine Anwendung) handelt.</span><span class="sxs-lookup"><span data-stu-id="c82e2-114">In addition to the seven styles defined by the system, there is an eighth style that is user (or application) defined.</span></span> <span data-ttu-id="c82e2-115">Ein benutzerdefinierter Stil generiert Zeilen mit einer angepassten Reihe von Bindestrichen und Punkten.</span><span class="sxs-lookup"><span data-stu-id="c82e2-115">A user-defined style generates lines with a customized series of dashes and dots.</span></span>

<span data-ttu-id="c82e2-116">Verwenden Sie die Funktion " [**kreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen)", " [**kreatepenindirekte**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)" oder " [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) ", um einen Stift zu erstellen, der über die System definierten Stile verfügt.</span><span class="sxs-lookup"><span data-stu-id="c82e2-116">Use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function to create a pen that has the system-defined styles.</span></span> <span data-ttu-id="c82e2-117">Verwenden Sie die **extkreatepen** -Funktion, um einen Stift mit einem benutzerdefinierten Stil zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c82e2-117">Use the **ExtCreatePen** function to create a pen that has a user-defined style.</span></span>

 

 



