---
title: Unterstützung späterer Bindungen
description: Wenn eine späte Bindungs Unterstützung vorhanden ist, muss jeder Funktions Aufrufer die ADSI IDispatch-Schnittstelle durchlaufen, bevor er an die entsprechende Erweiterung umgeleitet wird.
ms.assetid: fbdc6234-9381-4d64-bf02-05e393b3e0bd
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, späte Bindungs Unterstützung
- ADSI ADSI, Beispielcode Visual Basic, späte Bindungs Unterstützung
- Binden von AD, späterer Bindungs Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e4dd1de0000d9edbe3e73cbc47b81d094d48c2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730312"
---
# <a name="late-binding-support"></a><span data-ttu-id="6662b-106">Unterstützung späterer Bindungen</span><span class="sxs-lookup"><span data-stu-id="6662b-106">Late Binding Support</span></span>

<span data-ttu-id="6662b-107">Wenn eine späte Bindungs Unterstützung vorhanden ist, muss jeder Funktions Aufrufer die ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle durchlaufen, bevor er an die entsprechende Erweiterung umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="6662b-107">When late binding support is in place, each function call must go through the ADSI [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface, before it is rerouted to the appropriate extension.</span></span>

<span data-ttu-id="6662b-108">Betrachten Sie das folgende Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="6662b-108">Consider the following code example.</span></span>


```C++
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
 
x.MyNewMethod( "\\srv\public")
x.MyProperty = "Hello World"
 
x.OtherMethod()
x.OtherProperty = 4362
 
Debug.Print x.LastName
```



<span data-ttu-id="6662b-109">Es gibt keine expliziten Aufrufe der **QueryInterface** -Methode, um die Erweiterungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6662b-109">There are no explicit calls to the **QueryInterface** method to get to the extensions.</span></span> <span data-ttu-id="6662b-110">Die Erweiterungen müssen Ihre [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Aufrufe an die ADSI **IDispatch** -Schnittstelle umleiten.</span><span class="sxs-lookup"><span data-stu-id="6662b-110">The extensions must reroute their [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) calls to the ADSI **IDispatch** interface.</span></span> <span data-ttu-id="6662b-111">ADSI trifft die Entscheidung und löst alle auftretenden Konflikte auf und leitet dann mithilfe einer Schnittstelle namens [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension)wieder an die entsprechende Erweiterung weiter.</span><span class="sxs-lookup"><span data-stu-id="6662b-111">ADSI makes the decision and resolves any conflicts that occur, then it re-routes back to the appropriate extension using an interface called [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span> <span data-ttu-id="6662b-112">Daher muss jede Erweiterung, die spätes Binden unterstützt, **iadsextension** implementieren.</span><span class="sxs-lookup"><span data-stu-id="6662b-112">Therefore, any extension that supports late binding must implement **IADsExtension**.</span></span>

 

 