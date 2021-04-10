---
title: Abrufen von Fehlerinformationen
description: Abrufen von Fehlerinformationen
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039637"
---
# <a name="retrieving-error-information"></a><span data-ttu-id="f77b6-103">Abrufen von Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="f77b6-103">Retrieving Error Information</span></span>

<span data-ttu-id="f77b6-104">Mithilfe der Schnittstellen und Funktionen für die com-Fehlerbehandlung können Sie Fehlerinformationen wie folgt abrufen:</span><span class="sxs-lookup"><span data-stu-id="f77b6-104">Using the COM error-handling interfaces and functions, you can retrieve error information as follows:</span></span>

1.  <span data-ttu-id="f77b6-105">Überprüfen Sie, ob der zurückgegebene Wert einen Fehler darstellt, der vom-Objekt verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f77b6-105">Check whether the returned value represents an error that the object is prepared to handle.</span></span>
2.  <span data-ttu-id="f77b6-106">Ruft [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) auf, um einen Zeiger auf die [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f77b6-106">Call [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span> <span data-ttu-id="f77b6-107">Anschließend wird [**ISupportErrorInfo:: interfakesupportserrorinfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) aufgerufen, um zu überprüfen, ob der Fehler von dem zurückgegebenen Objekt ausgelöst wurde und dass sich das Fehler Objekt auf den aktuellen Fehler und nicht auf einen vorherigen-Befehl bezieht.</span><span class="sxs-lookup"><span data-stu-id="f77b6-107">Then call [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) to verify that the error was raised by the object that returned it and that the error object pertains to the current error and not to a previous call.</span></span>
3.  <span data-ttu-id="f77b6-108">Um einen Zeiger auf das Fehler Objekt zu erhalten, müssen Sie die [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f77b6-108">To get a pointer to the error object, call the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function.</span></span>
4.  <span data-ttu-id="f77b6-109">Verwenden Sie zum Abrufen von Informationen aus dem Fehler Objekt die [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="f77b6-109">To retrieve information from the error object, use the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) methods.</span></span>

<span data-ttu-id="f77b6-110">Wenn das Objekt nicht für die Behandlung des Fehlers vorbereitet ist, aber die Fehlerinformationen weiter unten in der Aufruf Kette weitergeben muss, sollte der Rückgabewert einfach an seinen Aufrufer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f77b6-110">If the object is not prepared to handle the error but needs to propagate the error information further down the call chain, it should simply pass the return value to its caller.</span></span> <span data-ttu-id="f77b6-111">Da die [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) -Funktion die Fehlerinformationen löscht und den Besitz des Error-Objekts an den Aufrufer übergibt, sollte die Funktion nur von dem Objekt aufgerufen werden, das den Fehler behandelt.</span><span class="sxs-lookup"><span data-stu-id="f77b6-111">Because the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function clears the error information and passes ownership of the error object to the caller, the function should be called only by the object that handles the error.</span></span>

 

 