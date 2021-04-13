---
title: Anzeigen von Containern als Blattknoten
description: Jedes Objekt in Active Directory Domain Services kann ein Container anderer Objekte sein.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Anzeigen von Containern als Blattknoten
- Container AD, anzeigen als Blattknoten
- Blatt Anzeige, Anzeigen von Containern als Blattknoten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314600"
---
# <a name="viewing-containers-as-leaf-nodes"></a><span data-ttu-id="d8a81-106">Anzeigen von Containern als Blattknoten</span><span class="sxs-lookup"><span data-stu-id="d8a81-106">Viewing Containers as Leaf Nodes</span></span>

<span data-ttu-id="d8a81-107">Jedes Objekt in Active Directory Domain Services kann ein Container anderer Objekte sein.</span><span class="sxs-lookup"><span data-stu-id="d8a81-107">Any object in Active Directory Domain Services can be a container of other objects.</span></span> <span data-ttu-id="d8a81-108">Dadurch kann die Benutzeroberfläche überladen werden. Daher ist es möglich, zu deklarieren, dass ein Objekt einer bestimmten Klasse nur als Blatt in der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d8a81-108">This can clutter the user interface, so it is possible to declare that an object of a specific class be only be displayed as a leaf in the user interface.</span></span> <span data-ttu-id="d8a81-109">Das **treatAsLeaf** -Attribut ist ein einwertiges Anzeige spezifiziererattribut, das bestimmt, ob Objekte dieser Klasse nur als Blattobjekte angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8a81-109">The **treatAsLeaf** attribute is a single-valued display specifier attribute that determines if objects of that class should be only be displayed as leaf objects.</span></span> <span data-ttu-id="d8a81-110">Dieses Attribut ist ein boolescher Wert, der angibt, dass Objekte der Klasse nur als Blatt Elemente angezeigt werden sollen, wenn der Wert **true** ist.</span><span class="sxs-lookup"><span data-stu-id="d8a81-110">This attribute is a Boolean value that, if **TRUE**, indicates that objects of the class should only be displayed as leaf elements.</span></span> <span data-ttu-id="d8a81-111">Wenn der Wert **false** ist, wird angegeben, dass Objekte der Klasse als Container oder als Blatt angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="d8a81-111">If **FALSE**, indicates that objects of the class can be displayed as a container or a leaf.</span></span> <span data-ttu-id="d8a81-112">Wie bei allen bezeichnerspezifiziererattributen wird das **treatAsLeaf** -Attribut pro Gebiets Schema festgelegt, sodass dieses Attribut nach Bedarf lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d8a81-112">Like all display specifier attributes, the **treatAsLeaf** attribute is set on a per-locale basis, so this attribute can be localized as required.</span></span> <span data-ttu-id="d8a81-113">Beispielsweise ist für die **Benutzer Anzeige** für das englische Gebiets Schema (0409) der Anzeige Spezifizierer das Attribut " **treatAsLeaf** " standardmäßig auf " **true** " festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8a81-113">For example, the **User-Display** for the English locale (0409) display specifier has the **treatAsLeaf** attribute set to **TRUE** by default.</span></span> <span data-ttu-id="d8a81-114">Dies bewirkt, dass die Benutzeroberfläche alle **Benutzer** Objekte als Blattobjekte anzeigt.</span><span class="sxs-lookup"><span data-stu-id="d8a81-114">This causes the user interface to display all **User** objects as leaf objects.</span></span>

<span data-ttu-id="d8a81-115">**So legen Sie den Wert des **treatAsLeaf** -Attributs fest**</span><span class="sxs-lookup"><span data-stu-id="d8a81-115">**To set the value of the **treatAsLeaf** attribute**</span></span>

1.  <span data-ttu-id="d8a81-116">Binden Sie an das gewünschte Anzeige Attribut im gewünschten Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="d8a81-116">Bind to the desired display attribute in the desired locale.</span></span> <span data-ttu-id="d8a81-117">Weitere Informationen und ein Codebeispiel finden Sie unter [displayspecifieres Container](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="d8a81-117">For more information and a code example, see [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>
2.  <span data-ttu-id="d8a81-118">Verwenden Sie die [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) -Methode, um das **treatAsLeaf** -Attribut auf " **true** " oder " **false**" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d8a81-118">Use the [**IADs::Put**](/windows/desktop/api/iads/nf-iads-iads-put) method to set the **treatAsLeaf** attribute to either **TRUE** or **FALSE**.</span></span>
3.  <span data-ttu-id="d8a81-119">Um die Änderungen im Verzeichnis zu übertragen, müssen Sie die [**IADs:: abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="d8a81-119">To commit changes to the directory, call the [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method.</span></span>

 

 