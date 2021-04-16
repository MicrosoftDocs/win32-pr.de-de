---
title: Verfügbar machen von Steuerelementen basierend auf System Steuerelementen
description: Verfügbar machen von Steuerelementen basierend auf System Steuerelementen
ms.assetid: 9291b79e-3ed0-4f3c-a610-38215d84f5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2fe31eae8c2283c020de93b0c1f3350bd0f417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390779"
---
# <a name="exposing-controls-based-on-system-controls"></a><span data-ttu-id="b8c5b-103">Verfügbar machen von Steuerelementen basierend auf System Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="b8c5b-103">Exposing Controls Based on System Controls</span></span>

<span data-ttu-id="b8c5b-104">Sie sollten die Verwendung einer Form dynamischer Anmerkung – Direct, Value Map oder Server – in Erwägung gezogen, bevor Sie das in diesem Abschnitt beschriebene Verfahren ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-104">You should consider using some form of Dynamic Annotation—Direct, Value Map, or Server—before attempting the technique described in this section.</span></span> <span data-ttu-id="b8c5b-105">Weitere Informationen finden Sie unter [Dynamic Annotation-API](dynamic-annotation-api.md).</span><span class="sxs-lookup"><span data-stu-id="b8c5b-105">For more information, see [Dynamic Annotation API](dynamic-annotation-api.md).</span></span>

<span data-ttu-id="b8c5b-106">In den meisten Fällen stellt Microsoft Active Accessibility Informationen zu übergeordneten oder untergeordneten Steuerelementen bereit.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-106">In most cases, Microsoft Active Accessibility exposes information about superclassed or subclassed controls.</span></span> <span data-ttu-id="b8c5b-107">Mithilfe von übergeordneten Klassen und Unterklassen können Anwendungsentwickler ein benutzerdefiniertes Steuerelement mit den grundlegenden Funktionen eines System Steuer Elements erstellen und Erweiterungen einschließen, die von der Anwendung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-107">Superclassing and subclassing allow an application developer to create a custom control with the basic functionality of a system control and include enhancements provided by the application.</span></span> <span data-ttu-id="b8c5b-108">Ein übergeordnetes Steuerelement hat einen anderen Fenster Klassennamen als das System Steuerelement, auf dem es basiert.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-108">A superclassed control has a different window class name than the system control on which it is based.</span></span> <span data-ttu-id="b8c5b-109">Ein Unterklassen-Steuerelement hat denselben Fenster Klassennamen.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-109">A subclassed control has the same window class name.</span></span> <span data-ttu-id="b8c5b-110">Weitere Informationen zu übergeordneten Klassen und Unterklassen finden Sie in der Dokumentation zum Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b8c5b-110">For more information about superclassing and subclassing, see the Windows Software Development Kit (SDK) documentation.</span></span>

<span data-ttu-id="b8c5b-111">Da Microsoft Active Accessibility Informationen zu vom System bereitgestellten Steuerelementen verfügbar macht, macht Microsoft Active Accessibility das geänderte Steuerelement verfügbar, es sei denn, ein übergeordnetes oder untergeordnetes Steuerelement unterscheidet sich deutlich vom Basis Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-111">Because Microsoft Active Accessibility exposes information about system-provided controls, Microsoft Active Accessibility exposes the modified control unless a superclassed or subclassed control is significantly different from the base control.</span></span> <span data-ttu-id="b8c5b-112">Um zu ermitteln, ob auf das geänderte Steuerelement zugegriffen werden kann, sollten Anwendungsentwickler Dienstprogramme wie z. b. über [prüfen](inspect-objects.md) und [barrierefreie Ereignis](accessible-event-watcher.md) Überwachung verwenden, um das Verhalten des geänderten Steuer Elements mit dem Basis Steuerelement zu vergleichen</span><span class="sxs-lookup"><span data-stu-id="b8c5b-112">To determine if the modified control is accessible, application developers should use utilities such as [Inspect](inspect-objects.md) and [Accessible Event Watcher](accessible-event-watcher.md) to compare the behavior of the modified control with the base control.</span></span>

<span data-ttu-id="b8c5b-113">Wenn Sie nach der Verwendung dieser Hilfsprogramme feststellen, dass auf das geänderte Steuerelement nicht zugegriffen werden kann, müssen Sie das Steuerelement wie jedes andere benutzerdefinierte Steuerelement behandeln.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-113">If after using these utilities you determine that the modified control is not accessible, you must treat the control as any other custom control.</span></span> <span data-ttu-id="b8c5b-114">Das Steuerelement muss Ereignisse auslöst, und die Fenster Prozedur der Anwendung muss auf die [**WM- \_ GetObject**](wm-getobject.md)-Nachricht reagieren, indem eine [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle bereitgestellt wird, die Client Anwendungen zum Abrufen von Informationen über das Steuerelement verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-114">The control must trigger events, and the application's window procedure must respond to the [**WM\_GETOBJECT**](wm-getobject.md)message by supplying an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface that client applications use to obtain information about the control.</span></span>

## <a name="createstdaccessibleproxy-and-createstdaccessibleobject"></a><span data-ttu-id="b8c5b-115">"Kreatestdaccessibleproxy" und "kreatestdaccessibleobject"</span><span class="sxs-lookup"><span data-stu-id="b8c5b-115">CreateStdAccessibleProxy and CreateStdAccessibleObject</span></span>

<span data-ttu-id="b8c5b-116">Wenn alle oder die meisten der [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften für das geänderte Steuerelement mit dem Basis Steuerelement identisch sind [**, verwenden Sie**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) "" [**, um die**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) Implementierung der **IAccessible** -Schnittstelle des Steuer Elements zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-116">If all or most of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for the modified control are the same as the base control, use [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) or [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) to simplify the implementation of the control's **IAccessible** interface.</span></span>

> [!Note]  
> <span data-ttu-id="b8c5b-117">Beachten Sie beim überlagern oder Unterklassen für ein barrierefreies Steuerelement, dass das Objekt, das von der Funktion "Funktion" von "| [**atestdaccessibleobject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) " abgerufen wurde, möglicherweise mehr als nur die Schnittstelle [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementiert</span><span class="sxs-lookup"><span data-stu-id="b8c5b-117">When superclassing or subclassing an accessible control, be aware that the object retrieved by the [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) function may implement more than just the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="b8c5b-118">Sie kann andere Schnittstellen wie [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)enthalten.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-118">It may include other interfaces such as [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant).</span></span> <span data-ttu-id="b8c5b-119">Möglicherweise müssen Sie diese zusätzlichen Schnittstellen umschließen, um die von der ursprünglichen Implementierung des Steuer Elements bereitgestellte Barrierefreiheits Unterstützung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-119">You might need to wrap these additional interfaces to retain the accessibility support provided by the original implemenation of the control.</span></span>

 

<span data-ttu-id="b8c5b-120">Die Funktionen " [**foratestdaccessibleproxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) " und " [**foratestdaccessibleobject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) " rufen einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger für das angegebene System Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-120">The [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya) and [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) functions retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer for the specified system control.</span></span> <span data-ttu-id="b8c5b-121">Der Unterschied in diesen Funktionen besteht darin, dass von " **kreatestdaccessibleobject** " der Fenster Klassenname verwendet wird, der aus seinem *HWND* -Parameter abgerufen wird, während " **kreatestdaccessibleproxy** " den Fenster Klassennamen verwendet, der in seinem *szclassname*</span><span class="sxs-lookup"><span data-stu-id="b8c5b-121">The difference in these functions is that **CreateStdAccessibleObject** uses the window class name obtained from its *hwnd* parameter whereas **CreateStdAccessibleProxy** uses the window class name specified in its *szClassName* parameter.</span></span> <span data-ttu-id="b8c5b-122">Wenn Sie sich entscheiden, diese Funktionen zu verwenden, verwenden Sie daher " **foratestdaccessibleproxy** ", um Informationen über übergeordnete Steuerelemente verfügbar zu machen, und jede Funktion mit untergeordneten Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-122">Therefore, if you decide to use these functions, use **CreateStdAccessibleProxy** to expose information about superclassed controls, and either function with subclassed controls.</span></span>

<span data-ttu-id="b8c5b-123">Nachdem Sie einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger auf das System Steuerelement erhalten haben, verwenden Sie den-Zeiger in der Implementierung der **IAccessible** -Schnittstelle für das geänderte-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-123">After obtaining an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to the system control, use the pointer in your implementation of the **IAccessible** interface for the modified control.</span></span> <span data-ttu-id="b8c5b-124">Wenn eine Eigenschaft oder Methode für das geänderte Steuerelement mit dem Basis Steuerelement identisch ist, verwenden Sie den **IAccessible** -Zeiger, um die vom Basis Steuerelement bereitgestellten Informationen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-124">If a property or method for the modified control is the same as the base control, use the **IAccessible** pointer to return the information provided by the base control.</span></span> <span data-ttu-id="b8c5b-125">Wenn sich eine Eigenschaft für das geänderte Steuerelement vom Basis Steuerelement unterscheidet, überschreiben Sie die-Eigenschaft des Basis Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-125">If a property for the modified control is different from the base control, override the base control's property.</span></span>

<span data-ttu-id="b8c5b-126">Im folgenden Beispiel ist **cacccustombutton** die Anwendungs definierte Klasse, die von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-126">In the following example, **CAccCustomButton** is the application-defined class derived from [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="b8c5b-127">Die Member-Variable **m \_ paccdefaultbutton** ist ein Zeiger auf eine **IAccessible** -Schnittstelle, die während der Initialisierungs Prozedur für das-Steuerelement von " [**foratestdaccessibleobject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) " abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-127">The member variable **m\_pAccDefaultButton** is a pointer to an **IAccessible** interface that was retrieved from [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject) during the initialization procedure for the control.</span></span> <span data-ttu-id="b8c5b-128">In diesem Beispiel ist die **Role** -Eigenschaft für das benutzerdefinierte Steuerelement identisch mit der **Role** -Eigenschaft des System Steuer Elements, sodass die **Role** -Eigenschaft des Basis Steuer Elements zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-128">In this example, the **Role** property for the custom control is the same as the **Role** property of the system control, so the **Role** property of the base control is returned.</span></span> <span data-ttu-id="b8c5b-129">Allerdings unterscheidet sich die **Description** -Eigenschaft von der des Basis Steuer Elements, sodass diese Eigenschaft überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b8c5b-129">However, the **Description** property is different from that of the base control, so this property is overridden.</span></span>


```C++
HRESULT CAccCustomButton::Initialize( HWND hWnd, HINSTANCE hInst )
{
.
.
.
    hr = CreateStdAccessibleObject( m_hWnd, 
                                    OBJID_CLIENT, 
                                    IID_IAccessible, 
                                    (void **) &m__pAccDefaultButton );
.
.
.
}

STDMETHODIMP CAccCustomButton::get_accRole( VARIANT varID )
{
    return m_pAccDefaultButton->get_accRole(varID);
}


STDMETHODIMP CAccCustomButton::get_accDescription( VARIANT varChild,
                                                   BSTR* pszDesc )
{
    TCHAR   szString[256];
    OLECHAR wszString[256];

    LoadString( m_hInst, ID_DESCRIPTION, szString, 256 );
    MultiByteToWideChar( CP_ACP, 0, szString, -1, wszString, 256 );
   *pszDesc = SysAllocString( wszString );
   if ( !pszDesc )
       return S_OK;
   else
       return E_OUTOFMEMORY;
}
```



<span data-ttu-id="b8c5b-130">Weitere Informationen zu den Eigenschaften und Methoden von System Steuerelementen in [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) finden Sie [unter Anhang A: Unterstützte Elemente der Benutzeroberflächen Elemente](appendix-a--supported-user-interface-elements-reference.md).</span><span class="sxs-lookup"><span data-stu-id="b8c5b-130">For more information about the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of system controls, see [Appendix A: Supported User Interface Elements Reference](appendix-a--supported-user-interface-elements-reference.md).</span></span>

 

 