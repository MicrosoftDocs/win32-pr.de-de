---
title: Verwenden von Value Map-Anmerkungen
description: Beispielcode finden Sie unter Beispiel für Value Map Annotation.
ms.assetid: 29be74c7-a7c2-41f4-8b94-5771988b74ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a3e8d003d863372e21a413fad56bc93b977ee3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390372"
---
# <a name="using-value-map-annotation"></a><span data-ttu-id="21b22-103">Verwenden von Value Map-Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="21b22-103">Using Value Map Annotation</span></span>

<span data-ttu-id="21b22-104">**So erstellen Sie eine Werte Zuordnung**</span><span class="sxs-lookup"><span data-stu-id="21b22-104">**To create a value map**</span></span>

1.  <span data-ttu-id="21b22-105">**Erstellen Sie eine Mapping-Zeichenfolge.**</span><span class="sxs-lookup"><span data-stu-id="21b22-105">**Create a mapping string.**</span></span>

    <span data-ttu-id="21b22-106">Eine Mapping-Zeichenfolge ist eine Liste der numerischen Werte eines Steuer Elements, die einer lesbaren Zeichenfolge in Unicode entsprechen.</span><span class="sxs-lookup"><span data-stu-id="21b22-106">A mapping string is a list of a control's numeric values corresponding to a human-readable string in Unicode.</span></span> <span data-ttu-id="21b22-107">Er beginnt mit "a:" gefolgt von einer Zahl, die den Typ des verwendeten Indexes angibt.</span><span class="sxs-lookup"><span data-stu-id="21b22-107">It starts with "A:" followed by a number that indicates the type of index used.</span></span> <span data-ttu-id="21b22-108">Nur Bild Indizes werden unterstützt. Daher ist der Indextyp immer 0.</span><span class="sxs-lookup"><span data-stu-id="21b22-108">Only image indexes are supported; therefore the index type is always 0.</span></span>

    <span data-ttu-id="21b22-109">Auf die Zeichenfolge folgt: Index: result-Paare.</span><span class="sxs-lookup"><span data-stu-id="21b22-109">The string is followed by :index:result pairs.</span></span> <span data-ttu-id="21b22-110">Der Index ist eine Zahl, die einen Bildindex für einen List-View oder eine Strukturansicht darstellt, oder den Wert für ein Schieberegler-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="21b22-110">The "index" is a number representing an image index for a List-View or Tree-View, or the value for a slider control.</span></span>

    <span data-ttu-id="21b22-111">Der resultierende Wert ist eine Zahl, die abgerufen wird, wenn Sie die Role-oder State-Eigenschaft für eine Listenansicht oder ein Strukturansicht-Steuerelement zuordnen.</span><span class="sxs-lookup"><span data-stu-id="21b22-111">The resulting value is a number obtained when you map the Role or State property for a list view or tree view control.</span></span> <span data-ttu-id="21b22-112">Diese Zahlen werden im Dezimal-oder Hexadezimal Format mit dem Präfix "0x" ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="21b22-112">Such numbers are expressed in decimal or hexadecimal with an "0x" prefix.</span></span>

    <span data-ttu-id="21b22-113">Die Mapping-Zeichenfolge wird immer mit einem abschließenden Doppelpunkt (":") beendet.</span><span class="sxs-lookup"><span data-stu-id="21b22-113">The mapping string is always terminated with a final colon (":").</span></span>

    <span data-ttu-id="21b22-114">Im folgenden finden Sie ein Beispiel für eine Anmerkung-Zuordnung für die Zustands-und Rollen Eigenschaften eines Kontrollkästchens in einer Listenansicht oder einem Strukturansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="21b22-114">The following is an example of an annotation map for the State and Role properties of a check box in a list view or tree view control.</span></span> <span data-ttu-id="21b22-115">Die Ansicht enthält zwei Elemente, die Kontrollkästchen darstellen, und jede enthält Bilder, die dem aktivierten und deaktivierten Zustand entsprechen.</span><span class="sxs-lookup"><span data-stu-id="21b22-115">There are two items in the view that represent check boxes, and each has images corresponding to the checked and unchecked state.</span></span>

    ```C++
    LPCWSTR g_ListOrTreeStateMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x00" // Image 0 is normal !
    L":1:0x10" // Image 1 is checked - STATE_SYSTEM_CHECKED (0x10) !
    L":";

    LPCWSTR g_ListOrTreeRoleMap = 
    L"A:0"     // Index type; always 0. !
    L":0:0x2C" // Image 0 is a check box - ROLE_SYSTEM_CHECKBUTTON
    (0x2c) !
    L":1:0x2C" // image 1 is also a check box !
    L":";
    ```

    

    <span data-ttu-id="21b22-116">Gültige Rollen-und Zustands Werte finden Sie unter [Objekt Rollen](object-roles.md) und [Objekt Zustands Konstanten](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="21b22-116">For valid Role and State values, see [Object Roles](object-roles.md) and [Object State Constants](object-state-constants.md).</span></span>

    <span data-ttu-id="21b22-117">Der Indexwert kann negativ sein, wenn Sie Eigenschaften für ein Schieberegler-Steuerelement zuordnen.</span><span class="sxs-lookup"><span data-stu-id="21b22-117">The index value may be negative when you map properties for a slider control.</span></span>

    <span data-ttu-id="21b22-118">Wenn Sie einen Wert oder eine Beschreibungs Eigenschaft zuordnen, ist das Ergebnis eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="21b22-118">When you map a Value or Description property, the result is a string.</span></span> <span data-ttu-id="21b22-119">Zeichen folgen werden nicht in Anführungszeichen eingeschlossen, und die Doppelpunkte fungieren als Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="21b22-119">Strings are not quoted and the colons act as delimiters.</span></span>

    <span data-ttu-id="21b22-120">Weitere Informationen finden Sie unter [Annotation](value-map-annotation.md)-Zuordnungs Format.</span><span class="sxs-lookup"><span data-stu-id="21b22-120">For more information, see [Annotation Map Format](value-map-annotation.md).</span></span>

2.  <span data-ttu-id="21b22-121">**Erstellen Sie den Anmerkung-Manager, und rufen Sie einen Zeiger auf seine**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)-**Schnittstelle ab.**</span><span class="sxs-lookup"><span data-stu-id="21b22-121">**Create the annotation manager and obtain a pointer to its**[**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)**interface.**</span></span>

    <span data-ttu-id="21b22-122">Im folgenden finden Sie ein Beispiel für die Erstellung des Anmerkung-Managers.</span><span class="sxs-lookup"><span data-stu-id="21b22-122">The following is an example of how to create the annotation manager.</span></span>

    ```C++
    IAccPropServices * pAccPropSvc = NULL;
    HRESULT hr = CoCreateInstance(CLSID_AccPropServices, NULL,
    CLSCTX_SERVER, IID_IAccPropServices, (void**) & pAccPropSvc));
    
    ```

    

3.  <span data-ttu-id="21b22-123">**Fügen Sie die Mapping-Zeichenfolge an das Steuerelement an**</span><span class="sxs-lookup"><span data-stu-id="21b22-123">**Attach the mapping string to the control.**</span></span>

    <span data-ttu-id="21b22-124">Wenden Sie [**IAccPropServices:: "abwndpropstr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)" an, indem Sie das **HWND** des Steuer Elements und einen Zeiger auf die Mapping-Zeichenfolge übergeben.</span><span class="sxs-lookup"><span data-stu-id="21b22-124">Call [**IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr), passing the **HWND** of the control and a pointer to the mapping string.</span></span>

    <span data-ttu-id="21b22-125">Der *idProp* -Parameter ist einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="21b22-125">The *IdProp* parameter will be one of the following.</span></span>

    

    | <span data-ttu-id="21b22-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="21b22-126">Parameter</span></span>                   | <span data-ttu-id="21b22-127">Verwendung</span><span class="sxs-lookup"><span data-stu-id="21b22-127">Used for</span></span>                                                |
    |-----------------------------|---------------------------------------------------------|
    | <span data-ttu-id="21b22-128">msaapropid- \_ rolemap</span><span class="sxs-lookup"><span data-stu-id="21b22-128">MSAAPROPID\_ROLEMAP</span></span>         | <span data-ttu-id="21b22-129">So legen Sie eine Rollen Zuordnung für Listenansicht-oder Strukturansicht-Steuerelemente fest</span><span class="sxs-lookup"><span data-stu-id="21b22-129">To set a role map for list view or tree view controls.</span></span>  |
    | <span data-ttu-id="21b22-130">msaapropid \_ statemap</span><span class="sxs-lookup"><span data-stu-id="21b22-130">MSAAPROPID\_STATEMAP</span></span>        | <span data-ttu-id="21b22-131">Zum Festlegen einer Zustands Zuordnung für Listenansicht-oder Strukturansicht-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="21b22-131">To set a state map for list view or tree view controls.</span></span> |
    | <span data-ttu-id="21b22-132">PROPID- \_ ACC- \_ deskriptionmap</span><span class="sxs-lookup"><span data-stu-id="21b22-132">PROPID\_ACC\_DESCRIPTIONMAP</span></span> | <span data-ttu-id="21b22-133">Um eine Beschreibungs Zuordnung für Listenansicht-oder Struktur Ansichten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="21b22-133">To set a description map for list view or tree views.</span></span>   |
    | <span data-ttu-id="21b22-134">msaapropid \_ ValueMap</span><span class="sxs-lookup"><span data-stu-id="21b22-134">MSAAPROPID\_VALUEMAP</span></span>        | <span data-ttu-id="21b22-135">Um eine Werte Zuordnung für Schieberegler-Steuerelemente festzulegen.</span><span class="sxs-lookup"><span data-stu-id="21b22-135">To set a value map on slider controls.</span></span>                  |

    

     

4.  <span data-ttu-id="21b22-136">**Bereinigen.**</span><span class="sxs-lookup"><span data-stu-id="21b22-136">**Clean up.**</span></span>

    <span data-ttu-id="21b22-137">Vor dem Zerstören von Werten, die mit Anmerkungen versehen sind (z. b. bei der Behandlung von [WM- \_ Zerstörung](../winmsg/wm-destroy.md)), müssen Sie zuvor registrierte Eigenschaften löschen und den Anmerkung-Manager freigeben.</span><span class="sxs-lookup"><span data-stu-id="21b22-137">Before you destroy any value map annotated controls (for example, when handling [WM\_DESTROY](../winmsg/wm-destroy.md)), you must clear previously registered properties and release the annotation manager.</span></span>

    <span data-ttu-id="21b22-138">Dazu müssen Sie [**IAccPropServices:: clearhwnd-**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) Eigenschaften entsprechend aufrufen und den Zeiger auf [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)freigeben.</span><span class="sxs-lookup"><span data-stu-id="21b22-138">To do this, call [**IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) as appropriate and release your pointer to [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices).</span></span>

<span data-ttu-id="21b22-139">Beispielcode finden Sie unter [Beispiel für Value Map Annotation](value-map-annotation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="21b22-139">For sample code, see [Value Map Annotation Sample](value-map-annotation-sample.md).</span></span>

 

 