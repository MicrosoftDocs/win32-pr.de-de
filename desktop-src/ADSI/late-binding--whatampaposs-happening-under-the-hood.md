---
title: Späte Bindung, was im Hintergrund passiert
description: In diesem Thema wird beschrieben, wie die späte Bindung in ADSI funktioniert.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- Erweiterungen ADSI, späte Bindung, was geschieht im Hintergrund
- Binden von AD, späte Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474228"
---
# <a name="late-binding-whats-happening-under-the-hood"></a><span data-ttu-id="9eb2f-105">Späte Bindung: Was geschieht im Hintergrund?</span><span class="sxs-lookup"><span data-stu-id="9eb2f-105">Late Binding: What's Happening Under the Hood?</span></span>

<span data-ttu-id="9eb2f-106">In der folgenden Liste wird der allgemeine Prozess zum Durchführen einer späten Bindung beschrieben:</span><span class="sxs-lookup"><span data-stu-id="9eb2f-106">The following list outlines the general process for performing a late bind:</span></span>

-   <span data-ttu-id="9eb2f-107">Etwas wird an ein ADSI-Verzeichnis Objekt gebunden.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="9eb2f-108">Beispielsweise wird "LDAP://CN = JeffSmith, OU = Sales, DC = fabrikam, DC = com" mithilfe der com-späten Bindung gebunden.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-108">For example, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" binds using COM late binding.</span></span> <span data-ttu-id="9eb2f-109">Dies bewirkt, dass ADSI die [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Methode für die **IDispatch** -Schnittstelle aufruft.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-109">This causes ADSI to call the [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) method on the **IDispatch** interface.</span></span>
-   <span data-ttu-id="9eb2f-110">ADSI findet ein Objekt in der Benutzerklasse und erstellt ein Objekt, das die entsprechenden Schnittstellen unterstützt, z. b. [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span><span class="sxs-lookup"><span data-stu-id="9eb2f-110">ADSI finds an object in the user class and creates an object that supports the appropriate interfaces, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span></span>
-   <span data-ttu-id="9eb2f-111">ADSI führt eine Suche in der Registrierung durch und findet Erweiterungs-CLSIDs für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-111">ADSI performs a lookup in the registry and finds extension CLSIDs for user.</span></span> <span data-ttu-id="9eb2f-112">Beachten Sie, dass ADSI diese Daten zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-112">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="9eb2f-113">Ein Vorgang ruft die **mynewmethod** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-113">Something makes a call to the **MyNewMethod** method.</span></span> <span data-ttu-id="9eb2f-114">ADSI sucht nach der Dispatch-ID und den dispatchids für andere ADSI-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-114">ADSI looks up its dispatch ID and the dispatch IDs for other ADSI extensions.</span></span> <span data-ttu-id="9eb2f-115">ADSI findet dann die Erweiterung, die diesen Aufruf verarbeitet, und ruft die [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) -Schnittstelle für diese Erweiterung auf.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-115">ADSI then finds the extension that serves this call, and calls the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>
-   <span data-ttu-id="9eb2f-116">Die-Erweiterung führt die-Funktion aus.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-116">The extension executes the function.</span></span>
-   <span data-ttu-id="9eb2f-117">Nun ruft der Client-Writer die **yournewmethod** -Methode mithilfe der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle für die aktuelle Erweiterung auf.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-117">Now, the client writer invokes the **YourNewMethod** method using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the current extension.</span></span> <span data-ttu-id="9eb2f-118">Die **IDispatch** -Implementierung der Erweiterung delegiert zurück an den **IDispatch** für ADSI.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-118">The extension's **IDispatch** implementation delegates back to the **IDispatch** for ADSI.</span></span>
-   <span data-ttu-id="9eb2f-119">Der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) für ADSI sucht erneut nach der entsprechenden Erweiterung oder selbst und ruft dann die entsprechende Erweiterung mithilfe der [**iadsextension**](/windows/desktop/api/Iads/nn-iads-iadsextension) -Schnittstelle für diese Erweiterung auf.</span><span class="sxs-lookup"><span data-stu-id="9eb2f-119">The [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) for ADSI again searches for the appropriate extension, or itself, then it calls the appropriate extension using the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>

 

 