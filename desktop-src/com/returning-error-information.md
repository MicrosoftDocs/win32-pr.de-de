---
title: Zurückgeben von Fehlerinformationen
description: Zurückgeben von Fehlerinformationen
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391042"
---
# <a name="returning-error-information"></a><span data-ttu-id="b4fb0-103">Zurückgeben von Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="b4fb0-103">Returning Error Information</span></span>

<span data-ttu-id="b4fb0-104">Mithilfe der com-Fehler Behandlungs Schnittstellen und-Funktionen können Sie Fehlerinformationen zurückgeben, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="b4fb0-104">Using the COM error-handling interfaces and functions, you can return error information by performing the following the steps:</span></span>

1.  <span data-ttu-id="b4fb0-105">Implementieren Sie die [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-105">Implement the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span>
2.  <span data-ttu-id="b4fb0-106">Um eine Instanz des generischen Fehler Objekts zu erstellen, rufen Sie [**die Funktion "**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) -Funktion" auf.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-106">To create an instance of the generic error object, call the [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) function.</span></span>
3.  <span data-ttu-id="b4fb0-107">Um den Inhalt festzulegen, verwenden Sie die [**ikreateerrorinfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-107">To set its contents, use the [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) methods.</span></span>
4.  <span data-ttu-id="b4fb0-108">Um das Fehler Objekt dem aktuellen logischen Thread zuzuordnen, wenden Sie die [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-108">To associate the error object with the current logical thread, call the [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) function.</span></span>

<span data-ttu-id="b4fb0-109">Die Fehler Behandlungs Schnittstellen erstellen und verwalten ein Fehler Objekt, das Informationen über den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-109">The error handling interfaces create and manage an error object, which provides information about the error.</span></span> <span data-ttu-id="b4fb0-110">Das Fehler Objekt ist nicht mit dem Objekt identisch, bei dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-110">The error object is not the same as the object that encountered the error.</span></span> <span data-ttu-id="b4fb0-111">Dabei handelt es sich um ein separates-Objekt, das dem aktuellen Ausführungs Thread zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b4fb0-111">It is a separate object associated with the current thread of execution.</span></span>

 

 