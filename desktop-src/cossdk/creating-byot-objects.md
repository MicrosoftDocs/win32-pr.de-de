---
description: Erstellen von BYOT-Objekten
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Erstellen von BYOT-Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343172"
---
# <a name="creating-byot-objects"></a><span data-ttu-id="0c5f8-103">Erstellen von BYOT-Objekten</span><span class="sxs-lookup"><span data-stu-id="0c5f8-103">Creating BYOT Objects</span></span>

<span data-ttu-id="0c5f8-104">Ein neues BYOT-Objekt erstellt Objekte mit manuellen Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="0c5f8-104">A new BYOT object creates objects with manual transactions.</span></span> <span data-ttu-id="0c5f8-105">Die beiden Schnittstellen [**ikreatewithtransaktionex**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) und [**ikreatewithtiptransaktionex**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex)verfügen über eine einzige Methode, " **kreateinstance**", die einen **ITransaction** -Schnittstellen Zeiger bzw. eine Tip-URL annimmt.</span><span class="sxs-lookup"><span data-stu-id="0c5f8-105">The two interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) and [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), have a single method, **CreateInstance**, which take an **ITransaction** interface pointer and TIP URL, respectively.</span></span> <span data-ttu-id="0c5f8-106">" [**Kreateinstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) " gibt einen Schnittstellen Zeiger auf das neu erstellte Objekt zurück, das in der angegebenen Transaktion eingetragen ist.</span><span class="sxs-lookup"><span data-stu-id="0c5f8-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) returns an interface pointer to the newly created object, which is enlisted within the specified transaction.</span></span>

<span data-ttu-id="0c5f8-107">Wenn ein Objekt mit einer manuellen Transaktion freigegeben wird, versucht com+ nicht, einen Commit für die Transaktion durchführen.</span><span class="sxs-lookup"><span data-stu-id="0c5f8-107">When an object with a manual transaction is released, COM+ does not attempt to commit the transaction.</span></span> <span data-ttu-id="0c5f8-108">Die Transaktion wird explizit vom externen Transaktions-Manager gesteuert, der die Transaktion ausgegeben hat, in der dieses Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0c5f8-108">The transaction is controlled explicitly by the external transaction manager that dispensed the transaction under which this object had been created.</span></span>

> [!Note]  
> <span data-ttu-id="0c5f8-109">Das BYOT. ByotServerEx-Objekt muss in eine COM+-Anwendung importiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c5f8-109">The Byot.ByotServerEx object needs to be imported into a COM+ application.</span></span>

 

 

 



