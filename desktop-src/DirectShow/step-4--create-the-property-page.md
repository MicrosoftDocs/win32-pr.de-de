---
description: Implementieren Sie eine Eigenschaftenseite als Teil der Erstellung einer Filtereigenschaftenseite für einen benutzerdefinierten DirectShow-Filter.
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: Schritt 4. Erstellen der Eigenschaftenseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32cd9eacc98af5f273897a3837390ab5cc75f7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406853"
---
# <a name="step-4-create-the-property-page"></a><span data-ttu-id="ad011-104">Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="ad011-104">Step 4.</span></span> <span data-ttu-id="ad011-105">Erstellen der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="ad011-105">Create the Property Page</span></span>

<span data-ttu-id="ad011-106">An diesem Punkt unterstützt der Filter alles, was er für eine Eigenschaftenseite benötigt.</span><span class="sxs-lookup"><span data-stu-id="ad011-106">At this point the filter supports everything that it needs for a property page.</span></span> <span data-ttu-id="ad011-107">Im nächsten Schritt wird die Eigenschaftenseite selbst implementiert.</span><span class="sxs-lookup"><span data-stu-id="ad011-107">The next step is implementing the property page itself.</span></span> <span data-ttu-id="ad011-108">Beginnen Sie, indem Sie eine neue Klasse von **CBasePropertyPage** ableiten.</span><span class="sxs-lookup"><span data-stu-id="ad011-108">Start by deriving a new class from **CBasePropertyPage**.</span></span> <span data-ttu-id="ad011-109">Das folgende Beispiel zeigt einen Teil der Deklaration, einschließlich einiger privater Membervariablen, die später im Beispiel verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ad011-109">The following example shows part of the declaration, including some private member variables that will be used later in the example:</span></span>


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



<span data-ttu-id="ad011-110">Erstellen Sie als Nächstes eine Dialogressource im Ressourcen-Editor zusammen mit einer Zeichenfolgenressource für den Dialogtitel.</span><span class="sxs-lookup"><span data-stu-id="ad011-110">Next, create a dialog resource in the resource editor, along with a string resource for the dialog title.</span></span> <span data-ttu-id="ad011-111">Die Zeichenfolge wird auf der Registerkarte für die Eigenschaftenseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad011-111">The string will appear in the tab for the property page.</span></span> <span data-ttu-id="ad011-112">Die beiden Ressourcen-IDs sind Argumente für den **CBasePropertyPage-Konstruktor:**</span><span class="sxs-lookup"><span data-stu-id="ad011-112">The two resource IDs are arguments to the **CBasePropertyPage** constructor:</span></span>


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



<span data-ttu-id="ad011-113">Die folgende Abbildung zeigt die Dialogressource für die Beispieleigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="ad011-113">The following illustration shows the dialog resource for the example property page.</span></span>

![Dialogfeld "Eigenschaftenseite"](images/proppage.png)

<span data-ttu-id="ad011-115">Nun können Sie die Eigenschaftenseite implementieren.</span><span class="sxs-lookup"><span data-stu-id="ad011-115">Now you are ready to implement the property page.</span></span> <span data-ttu-id="ad011-116">Hier sind die Methoden in **CBasePropertyPage,** die überschrieben werden sollen:</span><span class="sxs-lookup"><span data-stu-id="ad011-116">Here are the methods in **CBasePropertyPage** to override:</span></span>

-   <span data-ttu-id="ad011-117">**OnConnect** wird aufgerufen, wenn der Client die Eigenschaftenseite erstellt.</span><span class="sxs-lookup"><span data-stu-id="ad011-117">**OnConnect** is called when the client creates the property page.</span></span> <span data-ttu-id="ad011-118">Er legt den **IUnknown-Zeiger** auf den Filter fest.</span><span class="sxs-lookup"><span data-stu-id="ad011-118">It sets the **IUnknown** pointer to the filter.</span></span>
-   <span data-ttu-id="ad011-119">**OnActivate** wird aufgerufen, wenn das Dialogfeld erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ad011-119">**OnActivate** is called when the dialog is created.</span></span>
-   <span data-ttu-id="ad011-120">**OnReceiveMessage** wird aufgerufen, wenn das Dialogfeld eine Fenstermeldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="ad011-120">**OnReceiveMessage** is called when the dialog receives a window message.</span></span>
-   <span data-ttu-id="ad011-121">**OnApplyChanges** wird aufgerufen, wenn der Benutzer die Eigenschaftenänderungen committet, indem er auf die Schaltfläche **OK** oder **Übernehmen** klickt.</span><span class="sxs-lookup"><span data-stu-id="ad011-121">**OnApplyChanges** is called when the user commits the property changes by clicking the **OK** or **Apply** button.</span></span>
-   <span data-ttu-id="ad011-122">**OnDisconnect** wird aufgerufen, wenn der Benutzer das Eigenschaftenblatt verwarf.</span><span class="sxs-lookup"><span data-stu-id="ad011-122">**OnDisconnect** is called when the user dismisses the property sheet.</span></span>

<span data-ttu-id="ad011-123">Im weiteren Verlauf dieses Tutorials werden die einzelnen Methoden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ad011-123">The remainder of this tutorial describes each of these methods.</span></span>

<span data-ttu-id="ad011-124">Weiter: [Schritt 5. Speichern Sie einen Zeiger auf den Filter](step-5--store-a-pointer-to-the-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ad011-124">Next: [Step 5. Store a Pointer to the Filter](step-5--store-a-pointer-to-the-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad011-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad011-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad011-126">Erstellen einer Filtereigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="ad011-126">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



