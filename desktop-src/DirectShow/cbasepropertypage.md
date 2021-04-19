---
description: Die cbasepropertypage-Klasse ist eine abstrakte Klasse zum Implementieren einer Eigenschaften Seite. Verwenden Sie diese Klasse, wenn Sie einen Filter (oder ein anderes Objekt) schreiben, der Eigenschaften Seiten unterstützt.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: Cbasepropertypage-Klasse (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365685"
---
# <a name="cbasepropertypage-class"></a><span data-ttu-id="824f9-104">Cbasepropertypage-Klasse</span><span class="sxs-lookup"><span data-stu-id="824f9-104">CBasePropertyPage class</span></span>

![cbasepropertypage-Klassenhierarchie](images/cprop01.png)

<span data-ttu-id="824f9-106">Die- `CBasePropertyPage` Klasse ist eine abstrakte Klasse zum Implementieren einer Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="824f9-106">The `CBasePropertyPage` class is an abstract class for implementing a property page.</span></span> <span data-ttu-id="824f9-107">Verwenden Sie diese Klasse, wenn Sie einen Filter (oder ein anderes Objekt) schreiben, der Eigenschaften Seiten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="824f9-107">Use this class if you are writing a filter (or other object) that supports property pages.</span></span>



| <span data-ttu-id="824f9-108">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="824f9-108">Protected Member Variables</span></span>                                             | <span data-ttu-id="824f9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="824f9-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="824f9-110">**m \_ bdirty**</span><span class="sxs-lookup"><span data-stu-id="824f9-110">**m\_bDirty**</span></span>](cbasepropertypage-m-bdirty.md)                        | <span data-ttu-id="824f9-111">Gibt an, ob eine der Eigenschaften geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="824f9-111">Indicates whether any of the properties have changed.</span></span>                                                                             |
| [<span data-ttu-id="824f9-112">**m- \_ dialogID**</span><span class="sxs-lookup"><span data-stu-id="824f9-112">**m\_DialogId**</span></span>](cbasepropertypage-m-dialogid.md)                    | <span data-ttu-id="824f9-113">Ressourcen Bezeichner für den Dialog.</span><span class="sxs-lookup"><span data-stu-id="824f9-113">Resource identifier for the dialog.</span></span>                                                                                               |
| [<span data-ttu-id="824f9-114">**m \_ Dlg**</span><span class="sxs-lookup"><span data-stu-id="824f9-114">**m\_Dlg**</span></span>](cbasepropertypage-m-dlg.md)                              | <span data-ttu-id="824f9-115">Handle für das Dialogfeld Fenster.</span><span class="sxs-lookup"><span data-stu-id="824f9-115">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="824f9-116">**m- \_ HWND**</span><span class="sxs-lookup"><span data-stu-id="824f9-116">**m\_hwnd**</span></span>](cbasepropertypage-m-hwnd.md)                            | <span data-ttu-id="824f9-117">Handle für das Dialogfeld Fenster.</span><span class="sxs-lookup"><span data-stu-id="824f9-117">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="824f9-118">**m \_ ppagesite**</span><span class="sxs-lookup"><span data-stu-id="824f9-118">**m\_pPageSite**</span></span>](cbasepropertypage-m-ppagesite.md)                  | <span data-ttu-id="824f9-119">Zeiger auf die **ipropertypagesite** -Schnittstelle der Eigenschaften Seiten Website.</span><span class="sxs-lookup"><span data-stu-id="824f9-119">Pointer to the **IPropertyPageSite** interface of the property page site.</span></span>                                                         |
| [<span data-ttu-id="824f9-120">**m \_ TitleId**</span><span class="sxs-lookup"><span data-stu-id="824f9-120">**m\_TitleId**</span></span>](cbasepropertypage-m-titleid.md)                      | <span data-ttu-id="824f9-121">Ressourcen Bezeichner für eine Zeichenfolge, die den Dialog Titel enthält.</span><span class="sxs-lookup"><span data-stu-id="824f9-121">Resource identifier for a string that contains the dialog title.</span></span>                                                                  |
| <span data-ttu-id="824f9-122">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="824f9-122">Public Methods</span></span>                                                         | <span data-ttu-id="824f9-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="824f9-123">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="824f9-124">**Cbasepropertypage**</span><span class="sxs-lookup"><span data-stu-id="824f9-124">**CBasePropertyPage**</span></span>](cbasepropertypage-cbasepropertypage.md)       | <span data-ttu-id="824f9-125">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="824f9-125">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="824f9-126">**~ Cbasepropertypage**</span><span class="sxs-lookup"><span data-stu-id="824f9-126">**~CBasePropertyPage**</span></span>](cbasepropertypage--cbasepropertypage.md)     | <span data-ttu-id="824f9-127">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="824f9-127">Destructor method.</span></span> <span data-ttu-id="824f9-128">Virtu.</span><span class="sxs-lookup"><span data-stu-id="824f9-128">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="824f9-129">**Onaktivierung**</span><span class="sxs-lookup"><span data-stu-id="824f9-129">**OnActivate**</span></span>](cbasepropertypage-onactivate.md)                     | <span data-ttu-id="824f9-130">Wird aufgerufen, wenn die Eigenschaften Seite aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="824f9-130">Called when the property page is activated.</span></span> <span data-ttu-id="824f9-131">Virtu.</span><span class="sxs-lookup"><span data-stu-id="824f9-131">Virtual.</span></span>                                                                              |
| [<span data-ttu-id="824f9-132">**Onapplychanges**</span><span class="sxs-lookup"><span data-stu-id="824f9-132">**OnApplyChanges**</span></span>](cbasepropertypage-onapplychanges.md)             | <span data-ttu-id="824f9-133">Wird aufgerufen, wenn der Benutzer Änderungen auf der Eigenschaften Seite anwendet.</span><span class="sxs-lookup"><span data-stu-id="824f9-133">Called when the user applies changes to the property page.</span></span> <span data-ttu-id="824f9-134">Virtu.</span><span class="sxs-lookup"><span data-stu-id="824f9-134">Virtual.</span></span>                                                               |
| [<span data-ttu-id="824f9-135">**OnConnect**</span><span class="sxs-lookup"><span data-stu-id="824f9-135">**OnConnect**</span></span>](cbasepropertypage-onconnect.md)                       | <span data-ttu-id="824f9-136">Stellt einen **IUnknown** -Zeiger auf das-Objekt bereit, das der Eigenschaften Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="824f9-136">Provides an **IUnknown** pointer to the object associated with the property page.</span></span> <span data-ttu-id="824f9-137">Virtu.</span><span class="sxs-lookup"><span data-stu-id="824f9-137">Virtual.</span></span>                                        |
| [<span data-ttu-id="824f9-138">**Ondeaktivieren**</span><span class="sxs-lookup"><span data-stu-id="824f9-138">**OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)                 | <span data-ttu-id="824f9-139">Wird aufgerufen, wenn das Dialogfeld Fenster zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="824f9-139">Called when the dialog box window is destroyed.</span></span> <span data-ttu-id="824f9-140">Virtu.</span><span class="sxs-lookup"><span data-stu-id="824f9-140">Virtual.</span></span>                                                                          |
| [<span data-ttu-id="824f9-141">**OnDisconnect**</span><span class="sxs-lookup"><span data-stu-id="824f9-141">**OnDisconnect**</span></span>](cbasepropertypage-ondisconnect.md)                 | <span data-ttu-id="824f9-142">Wird aufgerufen, wenn die Eigenschaften Seite das zugeordnete-Objekt freigeben soll.</span><span class="sxs-lookup"><span data-stu-id="824f9-142">Called when the property page should release the associated object.</span></span> <span data-ttu-id="824f9-143">Virtu.</span><span class="sxs-lookup"><span data-stu-id="824f9-143">Virtual.</span></span>                                                      |
| [<span data-ttu-id="824f9-144">**Onreceivemess**</span><span class="sxs-lookup"><span data-stu-id="824f9-144">**OnReceiveMessage**</span></span>](cbasepropertypage-onreceivemessage.md)         | <span data-ttu-id="824f9-145">Wird aufgerufen, wenn das Dialogfeld eine Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="824f9-145">Called when the dialog box receives a message.</span></span> <span data-ttu-id="824f9-146">Virtu.</span><span class="sxs-lookup"><span data-stu-id="824f9-146">Virtual.</span></span>                                                                           |
| <span data-ttu-id="824f9-147">IPropertyPage-Methoden</span><span class="sxs-lookup"><span data-stu-id="824f9-147">IPropertyPage Methods</span></span>                                                  | <span data-ttu-id="824f9-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="824f9-148">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="824f9-149">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="824f9-149">**Activate**</span></span>](cbasepropertypage-activate.md)                         | <span data-ttu-id="824f9-150">Erstellt das Fenster des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="824f9-150">Creates the dialog box window.</span></span>                                                                                                    |
| [<span data-ttu-id="824f9-151">**Anwenden**</span><span class="sxs-lookup"><span data-stu-id="824f9-151">**Apply**</span></span>](cbasepropertypage-apply.md)                               | <span data-ttu-id="824f9-152">Wendet die aktuellen Eigenschaften Seiten Werte auf das-Objekt an, das der Eigenschaften Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="824f9-152">Applies the current property page values to the object associated with the property page</span></span>                                          |
| [<span data-ttu-id="824f9-153">**Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="824f9-153">**Deactivate**</span></span>](cbasepropertypage-deactivate.md)                     | <span data-ttu-id="824f9-154">Zerstört das Dialogfenster.</span><span class="sxs-lookup"><span data-stu-id="824f9-154">Destroys the dialog window.</span></span>                                                                                                       |
| [<span data-ttu-id="824f9-155">**Getpageingefo**</span><span class="sxs-lookup"><span data-stu-id="824f9-155">**GetPageInfo**</span></span>](cbasepropertypage-getpageinfo.md)                   | <span data-ttu-id="824f9-156">Ruft Informationen zur Eigenschaften Seite ab.</span><span class="sxs-lookup"><span data-stu-id="824f9-156">Retrieves information about the property page.</span></span>                                                                                    |
| [<span data-ttu-id="824f9-157">**Hilfe**</span><span class="sxs-lookup"><span data-stu-id="824f9-157">**Help**</span></span>](cbasepropertypage-help.md)                                 | <span data-ttu-id="824f9-158">Ruft die Hilfe der Eigenschaften Seite auf.</span><span class="sxs-lookup"><span data-stu-id="824f9-158">Invokes the property page help.</span></span>                                                                                                   |
| [<span data-ttu-id="824f9-159">**Ispagedirty**</span><span class="sxs-lookup"><span data-stu-id="824f9-159">**IsPageDirty**</span></span>](cbasepropertypage-ispagedirty.md)                   | <span data-ttu-id="824f9-160">Gibt an, ob die Eigenschaften Seite seit der Aktivierung oder seit dem letzten Aufrufen von **IPropertyPage:: apply** geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="824f9-160">Indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> |
| [<span data-ttu-id="824f9-161">**Move**</span><span class="sxs-lookup"><span data-stu-id="824f9-161">**Move**</span></span>](cbasepropertypage-move.md)                                 | <span data-ttu-id="824f9-162">Positioniert und ändert die Größe des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="824f9-162">Positions and resizes the dialog box.</span></span>                                                                                             |
| [<span data-ttu-id="824f9-163">**"Eintobjects"**</span><span class="sxs-lookup"><span data-stu-id="824f9-163">**SetObjects**</span></span>](cbasepropertypage-setobjects.md)                     | <span data-ttu-id="824f9-164">Stellt **IUnknown** -Zeiger für die Objekte bereit, die der Eigenschaften Seite zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="824f9-164">Provides **IUnknown** pointers for the objects associated with the property page.</span></span>                                                 |
| [<span data-ttu-id="824f9-165">**Setpagesite**</span><span class="sxs-lookup"><span data-stu-id="824f9-165">**SetPageSite**</span></span>](cbasepropertypage-setpagesite.md)                   | <span data-ttu-id="824f9-166">Initialisiert die Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="824f9-166">Initializes the property page.</span></span>                                                                                                    |
| [<span data-ttu-id="824f9-167">**Auftritt**</span><span class="sxs-lookup"><span data-stu-id="824f9-167">**Show**</span></span>](cbasepropertypage-show.md)                                 | <span data-ttu-id="824f9-168">Zeigt das Dialogfeld an oder blendet es aus.</span><span class="sxs-lookup"><span data-stu-id="824f9-168">Shows or hides the dialog box.</span></span>                                                                                                    |
| [<span data-ttu-id="824f9-169">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="824f9-169">**TranslateAccelerator**</span></span>](cbasepropertypage-translateaccelerator.md) | <span data-ttu-id="824f9-170">Weist die Eigenschaften Seite an, eine Tastatureingabe zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="824f9-170">Instructs the property page to process a keystroke.</span></span>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="824f9-171">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="824f9-171">Remarks</span></span>

<span data-ttu-id="824f9-172">Eine Eigenschaften Seite ist ein COM-Objekt, daher müssen Sie eine GUID für den Klassen Bezeichner (CLSID) generieren und einen Eintrag im [**cfactorytemplate**](cfactorytemplate.md) -Array bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="824f9-172">A property page is a COM object, so you must generate a GUID for the class identifier (CLSID) and provide an entry in the [**CFactoryTemplate**](cfactorytemplate.md) array.</span></span> <span data-ttu-id="824f9-173">Weitere Informationen finden Sie unter [DirectShow und com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="824f9-173">For more information, see [DirectShow and COM](directshow-and-com.md).</span></span> <span data-ttu-id="824f9-174">Das folgende Beispiel zeigt einen typischen klassenfactoryeintrag:</span><span class="sxs-lookup"><span data-stu-id="824f9-174">The following example shows a typical class factory entry:</span></span>


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



<span data-ttu-id="824f9-175">Der Filter muss die **ISpecifyPropertyPages** -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="824f9-175">Your filter must expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="824f9-176">Diese Schnittstelle enthält eine einzelne Methode, **GetPages**, die die CLSID der Eigenschaften Seite zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="824f9-176">This interface contains a single method, **GetPages**, which returns the CLSID of the property page.</span></span> <span data-ttu-id="824f9-177">Im folgenden Beispiel wird gezeigt, wie diese Methode implementiert wird:</span><span class="sxs-lookup"><span data-stu-id="824f9-177">The following example shows how to implement this method:</span></span>


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



<span data-ttu-id="824f9-178">Denken Sie daran, die **nondelegatingqueryinterface** -Methode des Filters ebenfalls zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="824f9-178">Remember to override the filter's **NonDelegatingQueryInterface** method as well.</span></span> <span data-ttu-id="824f9-179">Weitere Informationen finden Sie unter [DirectShow und com](directshow-and-com.md) und [**inondelegatingunknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="824f9-179">For more information, see [DirectShow and COM](directshow-and-com.md) and [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>

<span data-ttu-id="824f9-180">Erstellen Sie als nächstes das Dialogfeld als Ressource in Ihrem Projekt, und erstellen Sie eine Zeichen folgen Ressource, die den Dialog Titel enthält.</span><span class="sxs-lookup"><span data-stu-id="824f9-180">Next, create the dialog as a resource in your project, and create a string resource that holds the dialog title.</span></span> <span data-ttu-id="824f9-181">Beide Ressourcen-IDs sind Parameter des **cbasepropertypage** -Konstruktors.</span><span class="sxs-lookup"><span data-stu-id="824f9-181">Both of these resource IDs are parameters to the **CBasePropertyPage** constructor.</span></span> <span data-ttu-id="824f9-182">Wenn Sie die Titel Zeichenfolge in einer Ressource aufbewahren, ist es einfacher, die Eigenschaften Seite zu lokalisieren.</span><span class="sxs-lookup"><span data-stu-id="824f9-182">Keeping the title string in a resource makes it easier to localize your property page.</span></span>

<span data-ttu-id="824f9-183">Die **cbasepropertypage** -Klasse stellt ein Framework für die **IPropertyPage** -Schnittstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="824f9-183">The **CBasePropertyPage** class provides a framework for the **IPropertyPage** interface.</span></span> <span data-ttu-id="824f9-184">Dieses Framework ruft eine Reihe von virtuellen Methoden auf, einschließlich [**cbasepropertypage:: onaktivierung**](cbasepropertypage-onactivate.md), [**cbasepropertypage:: onapplychanges**](cbasepropertypage-onapplychanges.md)usw.</span><span class="sxs-lookup"><span data-stu-id="824f9-184">This framework calls a number of virtual methods, including [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md), and so on.</span></span> <span data-ttu-id="824f9-185">In der Basisklasse geben diese Methoden einfach S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="824f9-185">In the base class, these methods simply return S\_OK.</span></span> <span data-ttu-id="824f9-186">Ihre abgeleitete Klasse muss einige oder alle dieser virtuellen Methoden überschreiben.</span><span class="sxs-lookup"><span data-stu-id="824f9-186">Your derived class will need to override some or all of these virtual methods.</span></span> <span data-ttu-id="824f9-187">Weitere Informationen finden Sie in den Hinweisen für die einzelnen Methoden.</span><span class="sxs-lookup"><span data-stu-id="824f9-187">For details, see the remarks for the individual methods.</span></span>

<span data-ttu-id="824f9-188">Ein erweitertes Beispiel für die Verwendung dieser Klasse zum Erstellen einer Eigenschaften Seite finden Sie unter [Erstellen einer Filter Eigenschaften Seite](creating-a-filter-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="824f9-188">For an extended example of how to use this class to create a property page, see [Creating a Filter Property Page](creating-a-filter-property-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="824f9-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="824f9-189">Requirements</span></span>



| <span data-ttu-id="824f9-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="824f9-190">Requirement</span></span> | <span data-ttu-id="824f9-191">Wert</span><span class="sxs-lookup"><span data-stu-id="824f9-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="824f9-192">Header</span><span class="sxs-lookup"><span data-stu-id="824f9-192">Header</span></span><br/>  | <dl> <span data-ttu-id="824f9-193"><dt>Cprop. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="824f9-193"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="824f9-194">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="824f9-194">Library</span></span><br/> | <dl> <span data-ttu-id="824f9-195">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="824f9-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




