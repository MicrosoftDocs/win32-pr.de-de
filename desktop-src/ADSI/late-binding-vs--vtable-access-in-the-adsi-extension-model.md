---
title: Späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell
description: Eine duale Schnittstelle ermöglicht den direkten Vtable-Zugriff auf alle Funktionen, während eine Dispatchschnittstelle dies nicht tut.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell ADSI
- Erweiterungen ADSI, späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell
- ADSI ADSI, Beispielcode Visual Basic mit iadsdualinf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339097"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a><span data-ttu-id="8add0-106">Späte Bindung im Vergleich zu Vtable-Zugriff im ADSI-Erweiterungs Modell</span><span class="sxs-lookup"><span data-stu-id="8add0-106">Late Binding vs. Vtable Access in the ADSI Extension Model</span></span>

<span data-ttu-id="8add0-107">Eine duale Schnittstelle ermöglicht den direkten Vtable-Zugriff auf alle Funktionen, während eine Dispatchschnittstelle dies nicht tut.</span><span class="sxs-lookup"><span data-stu-id="8add0-107">A dual interface enables direct vtable access to all its functions while a dispatch interface does not.</span></span> <span data-ttu-id="8add0-108">Ein C/C++-Client kann einen doppelten Schnittstellen Zeiger Abfragen und den direkten Vtable-Zugriff verwenden, um seine Funktionen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="8add0-108">A C/C++ client can query for a dual interface pointer and use direct vtable access to invoke its functions.</span></span> <span data-ttu-id="8add0-109">Dies ermöglicht einen schnelleren Zugriff als das Aufrufen der Funktion mithilfe der Funktionen [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) und [**IDispatch:: Aufrufen**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .</span><span class="sxs-lookup"><span data-stu-id="8add0-109">This provides faster access than invoking the function using the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions.</span></span> <span data-ttu-id="8add0-110">Dies gilt insbesondere für das Erweiterungs Modell, da alle Dual Schnittstellen in einem Erweiterungs Objekt ihre **GetIDsOfNames** -und **Aufruf** Funktionen zunächst an den Aggregator (ADSI) zurück delegieren müssen.</span><span class="sxs-lookup"><span data-stu-id="8add0-110">This is especially true in the extension model, because all dual interfaces in an extension object must delegate their **GetIDsOfNames** and **Invoke** functions back to the aggregator (ADSI) first.</span></span> <span data-ttu-id="8add0-111">Der Aggregator muss dann zusätzliche interne Schritte durchführen, um zu ermitteln, welches Erweiterungs Objekt, möglicherweise auch den Aggregator selbst, Unterstützung für die aufgerufene Funktion und den Aufruf an das entsprechende-Objekt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8add0-111">The aggregator then must perform extra internal steps to identify which extension object, possibly including the aggregator itself, provides support for the function called and redirect the call to the appropriate object.</span></span>

<span data-ttu-id="8add0-112">Visual Basic ruft auch eine Dual-Interface-Funktion mit direktem Zugriff auf eine Vtable auf, wenn Sie über einen Zeiger auf die-Schnittstelle und Zugriff auf Typdaten aus der Typbibliothek verfügt.</span><span class="sxs-lookup"><span data-stu-id="8add0-112">Visual Basic also invokes a dual-interface function using direct access to a vtable, if it has a pointer to the interface and access to type data from the type library.</span></span> <span data-ttu-id="8add0-113">In Visual Basic geschriebene ADSI-Clients können einen Zeiger auf eine duale Schnittstelle, z. b. [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explizit angeben und somit den vtable-Zugriff auf Funktionen in der Schnittstelle ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="8add0-113">ADSI clients written in Visual Basic can specify a pointer to a dual interface, for example, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitly, and thus enable vtable access to functions in the interface.</span></span>


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



<span data-ttu-id="8add0-114">Da eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle keinen Vtable-Zugriff unterstützt, gilt dieses Beispiel nicht.</span><span class="sxs-lookup"><span data-stu-id="8add0-114">Because an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface does not support vtable access, this example does not apply.</span></span> <span data-ttu-id="8add0-115">Das heißt, eine dispatchfunktion wird immer durch die [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) -und [**IDispatch:: Aufrufen**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) -Funktionen aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8add0-115">That is, a dispatch function is always invoked through the [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) and [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) functions only.</span></span>

<span data-ttu-id="8add0-116">Die aktuellen Releases von VBScript und JScript unterstützen auch keinen Vtable-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="8add0-116">Current releases of VBScript and JScript also do not support vtable access.</span></span> <span data-ttu-id="8add0-117">Daher wird eine duale Schnittstelle in einer VBScript-oder JScript-Umgebung wie eine Dispatch-Schnittstelle ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8add0-117">Therefore, a dual interface in a VBScript or JScript environment performs like a dispatch interface.</span></span>

 

 