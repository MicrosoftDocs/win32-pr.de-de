---
description: Schritt 4.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Schritt 4. Erstellen der Eigenschaften Seite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e8ea1a22e30c57c66b263a62afc1e0cf801903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218863"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="f2e37-104">Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="f2e37-104">Step 4.</span></span> <span data-ttu-id="f2e37-105">Erstellen der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="f2e37-105">Create the Property Page</span></span>

<span data-ttu-id="f2e37-106">An diesem Punkt unterstützt der Filter alle Elemente, die für eine Eigenschaften Seite benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="f2e37-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="f2e37-107">Der nächste Schritt besteht darin, die Eigenschaften Seite zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="f2e37-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="f2e37-108">Beginnen Sie, indem Sie eine neue Klasse von **cbasepropertypage** ableiten.</span><span class="sxs-lookup"><span data-stu-id="f2e37-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="f2e37-109">Das folgende Beispiel zeigt einen Teil der Deklaration, einschließlich einiger private Member-Variablen, die später im Beispiel verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="f2e37-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



<span data-ttu-id="f2e37-110">Erstellen Sie als nächstes eine Dialogfeld Ressource zusammen mit einer Zeichen folgen Ressource für den Dialog Titel im Ressourcen-Editor.</span><span class="sxs-lookup"><span data-stu-id="f2e37-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="f2e37-111">Die Zeichenfolge wird auf der Registerkarte für die Eigenschaften Seite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2e37-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="f2e37-112">Die beiden Ressourcen-IDs sind Argumente für den **cbasepropertypage** -Konstruktor:</span><span class="sxs-lookup"><span data-stu-id="f2e37-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="f2e37-113">Die folgende Abbildung zeigt die Dialog Ressource für die Beispiel Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="f2e37-113">The following illustration shows the dialog resource for the example property page.</span></span>

![Eigenschaften Seiten Dialogfeld](images/proppage.png)

<span data-ttu-id="f2e37-115">Nun sind Sie bereit, die Eigenschaften Seite zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="f2e37-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="f2e37-116">Die folgenden Methoden werden in **cbasepropertypage** zum Überschreiben angezeigt:</span><span class="sxs-lookup"><span data-stu-id="f2e37-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="f2e37-117">" **OnConnect** " wird aufgerufen, wenn der Client die Eigenschaften Seite erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2e37-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="f2e37-118">Der **IUnknown** -Zeiger wird auf den Filter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f2e37-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="f2e37-119">**Onaktivierungs** wird aufgerufen, wenn das Dialogfeld erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f2e37-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="f2e37-120">" **Onreceivemess Age** " wird aufgerufen, wenn das Dialogfeld eine Fenster Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="f2e37-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="f2e37-121">" **Onapplychanges** " wird aufgerufen, wenn der Benutzer einen Commit für die Eigenschafts Änderungen durchführt, indem er auf **die Schaltfläche** **OK**</span><span class="sxs-lookup"><span data-stu-id="f2e37-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="f2e37-122">" **OnDisconnect** " wird aufgerufen, wenn der Benutzer das Eigenschaften Blatt schließt.</span><span class="sxs-lookup"><span data-stu-id="f2e37-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="f2e37-123">Im restlichen Teil dieses Tutorials wird jede dieser Methoden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2e37-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="f2e37-124">Weiter: [Schritt 5. Speichert einen Zeiger auf den Filter](step-5--store-a-pointer-to-the-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f2e37-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2e37-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2e37-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2e37-126">Erstellen einer Filter Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="f2e37-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



