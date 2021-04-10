---
title: Veröffentlichen unter einem Computer Objekt
description: In der Regel erstellen Host basierte Dienste SCPs unter dem Computer Objekt für den Host Computer. Host basierte Dienste sind Dienste, die eng an einen einzelnen Host Computer gebunden sind.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858127"
---
# <a name="publishing-under-a-computer-object"></a><span data-ttu-id="ff949-104">Veröffentlichen unter einem Computer Objekt</span><span class="sxs-lookup"><span data-stu-id="ff949-104">Publishing Under a Computer Object</span></span>

<span data-ttu-id="ff949-105">In der Regel erstellen Host basierte Dienste SCPs unter dem Computer Objekt für den Host Computer.</span><span class="sxs-lookup"><span data-stu-id="ff949-105">Typically, host-based services create SCPs under the computer object for the host computer.</span></span> <span data-ttu-id="ff949-106">Host basierte Dienste sind Dienste, die eng an einen einzelnen Host Computer gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="ff949-106">Host-based services are services closely tied to a single host computer.</span></span>

<span data-ttu-id="ff949-107">**So erstellen Sie SCPs unter einem Computer Objekt**</span><span class="sxs-lookup"><span data-stu-id="ff949-107">**To create SCPs under a computer object**</span></span>

1.  <span data-ttu-id="ff949-108">Aufrufen der Funktion [**getcomputerobjectname**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) , um den Distinguished Name (DN) im Verzeichnis des Computer Objekts für den lokalen Computer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff949-108">Call the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to get the distinguished name (DN) in the directory of the computer object for the local computer.</span></span>
2.  <span data-ttu-id="ff949-109">Verwenden Sie diesen DN zum Binden an das Computer Objekt und zum Erstellen des Dienst Verbindungs Punkts.</span><span class="sxs-lookup"><span data-stu-id="ff949-109">Use that DN to bind to the computer object and create the SCP.</span></span>

<span data-ttu-id="ff949-110">Weitere Informationen und ein Codebeispiel finden Sie unter Gewusst wie: Suchen [und Verwenden eines Dienst Verbindungs Punkts durch Clients](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="ff949-110">For more information and a code example, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="ff949-111">Beachten Sie, dass nur Domänen Mitglieds Computer über gültige Computer Objekte im Verzeichnis verfügen.</span><span class="sxs-lookup"><span data-stu-id="ff949-111">Be aware that only domain-member computers have valid computer objects in the directory.</span></span>

<span data-ttu-id="ff949-112">Um den DNS-oder NetBIOS-Namen des lokalen Computers abzurufen, müssen Sie die Funktion [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ff949-112">To get the DNS or NetBIOS name of the local computer, call the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function.</span></span>

 

 