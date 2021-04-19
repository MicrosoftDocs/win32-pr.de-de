---
description: Registrieren und Aufheben der Registrierung von Schlüsseln
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrieren und Aufheben der Registrierung von Schlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373191"
---
# <a name="registering-and-deregistering-keys"></a><span data-ttu-id="3adac-103">Registrieren und Aufheben der Registrierung von Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="3adac-103">Registering and Deregistering Keys</span></span>

## <a name="registering-keys"></a><span data-ttu-id="3adac-104">Schlüssel werden registriert</span><span class="sxs-lookup"><span data-stu-id="3adac-104">Registering Keys</span></span>

<span data-ttu-id="3adac-105">Ein Knoten kann jederzeit Schlüssel mit [**drtregisterkey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) registrieren, während er in der **DRT \_ aktiv**, **DRT \_ allein** und **DRT \_ keine \_ Netzwerk** Zustände hat.</span><span class="sxs-lookup"><span data-stu-id="3adac-105">A node can register keys with [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) at anytime while in the **DRT\_ACTIVE**, **DRT\_ALONE**, and **DRT\_NO\_NETWORK** states.</span></span> <span data-ttu-id="3adac-106">Schlüssel, die in **DRT \_ allein** registriert sind, und **DRT \_ keine \_ Netzwerk** Zustände, können nur von anderen DRTs erkannt werden, nachdem der lokale Knoten auf **DRT \_ aktiv** umgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3adac-106">Keys registered in **DRT\_ALONE** and **DRT\_NO\_NETWORK** states can only be recognized by other DRTs after the local node has transitioned to **DRT\_ACTIVE**.</span></span>

<span data-ttu-id="3adac-107">Identische Schlüssel können nicht in derselben DRT-Instanz registriert werden, wenn [**drtkreatederivedkeysecurityprovider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3adac-107">Identical keys cannot be registered within the same DRT instance when using [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span></span> <span data-ttu-id="3adac-108">Wenn die Registrierung identischer Schlüssel versucht wird, tritt ein Fehler bei der Registrierung des zweiten Schlüssels auf.</span><span class="sxs-lookup"><span data-stu-id="3adac-108">If the registration of identical keys is attempted, the registration of the second key will fail.</span></span> <span data-ttu-id="3adac-109">Die Verwendung identischer Schlüssel sollte auch zwischen verschiedenen DRT-Instanzen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="3adac-109">The use of identical keys should also be avoided between different DRT instances.</span></span> <span data-ttu-id="3adac-110">Durchsuchen anhand der eindeutigen Schlüssel Bezeichnung, die diese identische schlüsselfreigabe hat, kann jeder der Schlüssel zurückgegeben werden, unabhängig davon, welche Daten dem Schlüssel zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3adac-110">Searches against the unique key designation these identical keys share could return any one of the keys, regardless of what data is associated to the key.</span></span>

> [!Note]  
> <span data-ttu-id="3adac-111">Wenn für die Implementierung ein anderes Verhalten erforderlich ist, kann ein Sicherheitsanbieter anstelle von [**drtkreatederivedkeysecurityprovider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) erstellt werden, um dies zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3adac-111">If different behavior is required for implementation, a security provider can be created in place of [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) to accommodate.</span></span>

 

## <a name="deregistering-keys"></a><span data-ttu-id="3adac-112">Aufheben der Registrierung von Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="3adac-112">Deregistering Keys</span></span>

<span data-ttu-id="3adac-113">Ein Knoten kann einen Schlüssel jederzeit registrieren, nachdem er registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="3adac-113">A node can deregister a key anytime after it has been registered.</span></span> <span data-ttu-id="3adac-114">Es kann jedoch nur von der Anwendung, die den Schlüssel registriert hat, die Registrierung aufgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="3adac-114">However, only the application that registered the key can deregister it.</span></span> <span data-ttu-id="3adac-115">Eine Anwendung kann einen Schlüssel aus dem lokalen Knoten mithilfe der [**drtunregisterkey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) -Funktion aufheben.</span><span class="sxs-lookup"><span data-stu-id="3adac-115">An application can deregister a key from the local node using the [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) function.</span></span> <span data-ttu-id="3adac-116">Nach Abschluss löst die Funktion ein Ereignis Änderungs Ereignis für das **DRT- \_ Ereignis \_ Blatt \_ \_** aus und informiert die Anwendung sowie andere Knoten, die am DRT-Mesh teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="3adac-116">Upon completion the function triggers a **DRT\_EVENT\_LEAFSET\_KEY\_CHANGE** event; informing the application as well as other nodes participating in the DRT mesh.</span></span>

<span data-ttu-id="3adac-117">Im **DRT- \_ Faulted** -Status führt der erforderliche Aufrufe von [**drtclose**](/windows/desktop/api/drt/nf-drt-drtclose) dazu, dass die DRT-Infrastruktur alle Schlüssel Aufhebung.</span><span class="sxs-lookup"><span data-stu-id="3adac-117">While in the **DRT\_FAULTED** state, the required call of [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) will result in the DRT infrastructure deregistering all keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3adac-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3adac-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3adac-119">Durchsuchen einer verteilten Routing Tabelle</span><span class="sxs-lookup"><span data-stu-id="3adac-119">Searching a Distributed Routing Table</span></span>](searching-a-distributed-routing-table.md)
</dt> <dt>

[<span data-ttu-id="3adac-120">Informationen zu verteilten Routing Tabellen</span><span class="sxs-lookup"><span data-stu-id="3adac-120">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)
</dt> <dt>

[<span data-ttu-id="3adac-121">Tabellen-API Referenz zu verteiltem Routing</span><span class="sxs-lookup"><span data-stu-id="3adac-121">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



