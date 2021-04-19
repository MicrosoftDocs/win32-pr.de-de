---
title: Name-Eigenschaft
description: Die Name-Eigenschaft ist eine Zeichenfolge, die von Clients verwendet wird, um ein Objekt für den Benutzer zu identifizieren, zu suchen oder zu ankündigen. Alle-Objekte unterstützen die Name-Eigenschaft.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339205"
---
# <a name="name-property"></a><span data-ttu-id="ef9b2-104">Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ef9b2-104">Name Property</span></span>

<span data-ttu-id="ef9b2-105">Die **Name** -Eigenschaft ist eine Zeichenfolge, die von Clients verwendet wird, um ein Objekt für den Benutzer zu identifizieren, zu suchen oder zu ankündigen.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-105">The **Name** property is a string used by clients to identify, find, or announce an object for the user.</span></span> <span data-ttu-id="ef9b2-106">Alle-Objekte unterstützen die **Name** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-106">All objects support the **Name** property.</span></span>

<span data-ttu-id="ef9b2-107">Der Text auf einem Schaltflächen-Steuerelement ist beispielsweise der Name, während der Name für ein Listenfeld oder Bearbeitungs Steuerelement der statische Text ist, der unmittelbar vor dem Steuerelement in der Tabstopp Reihenfolge steht.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-107">For example, the text on a button control is its name, while the name for a list box or edit control is the static text that immediately precedes the control in the tabbing order.</span></span> <span data-ttu-id="ef9b2-108">Auch Grafik Objekte, die keinen Namen anzeigen, stellen Text bereit, wenn die **Name** -Eigenschaft abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-108">Even graphic objects that do not display a name provide text when queried for the **Name** property.</span></span>

<span data-ttu-id="ef9b2-109">Die **Name** -Eigenschaft wird durch Aufrufen von " [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-109">The **Name** property is retrieved by calling [**IAccessible::get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).</span></span>

## <a name="selecting-names"></a><span data-ttu-id="ef9b2-110">Auswählen von Namen</span><span class="sxs-lookup"><span data-stu-id="ef9b2-110">Selecting Names</span></span>

<span data-ttu-id="ef9b2-111">Der Name eines Objekts sollte intuitiv sein, damit die Benutzer die Bedeutung oder den Zweck des Objekts verstehen.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-111">An object's name should be intuitive so that users understand the object's meaning or purpose.</span></span> <span data-ttu-id="ef9b2-112">Außerdem sollte die **Name** -Eigenschaft in Bezug auf alle gleich geordneten Objekte im übergeordneten Element eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-112">Also, the **Name** property should be unique relative to any sibling objects in the parent.</span></span>

<span data-ttu-id="ef9b2-113">Die Navigation innerhalb von Tabellen stellt für einige Benutzer besonders schwierige Probleme dar.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-113">Navigation within tables presents especially difficult problems for some users.</span></span> <span data-ttu-id="ef9b2-114">Daher sollten Server Entwickler Tabellen Zell Namen so beschreibend wie möglich machen.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-114">Therefore, server developers should make table cell names as descriptive as possible.</span></span> <span data-ttu-id="ef9b2-115">Beispielsweise können Sie einen Zellnamen erstellen, indem Sie die Namen der Zeile und der Spalte, die Sie einnimmt, kombinieren, z. b. "a1".</span><span class="sxs-lookup"><span data-stu-id="ef9b2-115">For example, you could create a cell name by combining the names of the row and column it occupies, such as "A1."</span></span> <span data-ttu-id="ef9b2-116">Es ist jedoch in der Regel besser, aussagekräftigeren Namen zu verwenden, wie z. b. "Nancy, Februar", wobei "Nancy" die aktuelle Zeile und "Februar" die aktuelle Spalte ist.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-116">However, it is generally better to use more descriptive names, such as "Nancy, February" where "Nancy" is the current row and "February" is the current column.</span></span>

## <a name="delegating-requests"></a><span data-ttu-id="ef9b2-117">Delegieren von Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef9b2-117">Delegating Requests</span></span>

<span data-ttu-id="ef9b2-118">Wenn ein Objekt keinen Zugriff auf die **Name** -Eigenschaft hat, delegiert es Anforderungen an das übergeordnete Objekt und identifiziert sich selbst durch seine untergeordnete ID.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-118">If an object does not have access to its **Name** property, it delegates requests to its parent, identifying itself by its child ID.</span></span> <span data-ttu-id="ef9b2-119">Wenn ein Client z. b. die **Name** -Eigenschaft eines Bearbeitungs Steuer Elements aufruft, delegiert das Bearbeitungs Steuerelement die Abfrage an das übergeordnete Element, das den Wert des statischen Text Steuer Elements zurückgibt, das das Bearbeitungs Steuerelement bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ef9b2-119">For example, if a client calls an edit control's **Name** property, the edit control delegates the query to its parent, which returns the value of the static text control that labels the edit control.</span></span>

 

 




