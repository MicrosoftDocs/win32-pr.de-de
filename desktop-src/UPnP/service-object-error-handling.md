---
title: Fehlerbehandlung bei Dienst Objekten
description: Wenn ein Fehler in einem Dienst Objekt auftritt, sollte der Rückgabewert für den Aufruf-IDispatch-Aufruf DISP \_ E \_ Exception lauten, und der pexceptinfo-Parameter Zeiger auf eine exceptinfo-Struktur in sollte ausgefüllt werden.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd39d08dc7ca5152ca412df1a6fb67d6df524f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101799"
---
# <a name="service-object-error-handling"></a><span data-ttu-id="d872e-103">Fehlerbehandlung bei Dienst Objekten</span><span class="sxs-lookup"><span data-stu-id="d872e-103">Service Object Error Handling</span></span>

<span data-ttu-id="d872e-104">Wenn ein Fehler in einem Dienst Objekt auftritt, sollte der Rückgabewert für den Aufruf [**IDispatch:: Aufrufen**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) DISP \_ E Exception lauten \_ , und der *pexceptinfo* -Parameter Zeiger auf eine [**exceptinfo**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) -Struktur in muss ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="d872e-104">When an error occurs in a service object, the return value for the call [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) should be DISP\_E\_EXCEPTION, and the *pExceptInfo* parameter pointer to an [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure in the should be filled in.</span></span>

<span data-ttu-id="d872e-105">Insbesondere die Elemente **bstrausource** und **bstraudescription** der [**exceptinfo**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) -Struktur werden vom Geräte Host mit der UPnP-Technologie verwendet, um eine UPnP-Fehler Antwort zu erstellen. **bstrausource** ist der Fehlercode, und **bstraudescription** ist die Fehlerbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="d872e-105">Specifically, the **bstrSource**, and **bstrDescription** members of the [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) structure are used by the Device Host with UPnP technology to create a UPnP Fault response; **bstrSource** is the error code and **bstrDescription** is the error description.</span></span>

 

 