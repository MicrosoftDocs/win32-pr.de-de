---
title: Was wird von einem Client angezeigt?
description: Dieses Thema listet Möglichkeiten auf, wie ein Client ADSI-Daten anzeigt.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, was wird von einem Client angezeigt?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517108"
---
# <a name="what-does-a-client-see"></a><span data-ttu-id="519a8-104">Was wird von einem Client angezeigt?</span><span class="sxs-lookup"><span data-stu-id="519a8-104">What Does a Client See?</span></span>

-   <span data-ttu-id="519a8-105">Ein Client sieht ADSI und alle seine Erweiterungs Objekte als ein Objekt.</span><span class="sxs-lookup"><span data-stu-id="519a8-105">A client sees ADSI and all of its extension objects as one object.</span></span>
-   <span data-ttu-id="519a8-106">Ein ADSI-Client sieht eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle, die alle Dual-und Dispatch-Schnittstellen im-Objekt verarbeitet, unabhängig davon, ob die Dual-oder Dispatch-Schnittstelle vom Aggregator im Anbieter oder durch eine Erweiterung implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="519a8-106">An ADSI client sees one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface that handles all the dual and dispatch interfaces in the object, whether the dual or dispatch interface is implemented by the aggregator in the provider or by an extension.</span></span> <span data-ttu-id="519a8-107">Weitere Informationen finden Sie unter [Auflösung von Konflikten bei Funktions-/Eigenschaftennamen in Automation](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="519a8-107">Please see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>
-   <span data-ttu-id="519a8-108">ADSI macht keine Typinformationen über die [**IDispatch:: GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) -Methode oder die [**IDispatch:: GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) -Methode verfügbar.</span><span class="sxs-lookup"><span data-stu-id="519a8-108">ADSI does not expose any type information through the [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) or [**IDispatch::GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) methods.</span></span> <span data-ttu-id="519a8-109">ADSI stellt Typinformationen über die Typbibliothek bereit.</span><span class="sxs-lookup"><span data-stu-id="519a8-109">ADSI provides type information through the type library.</span></span>

 

 