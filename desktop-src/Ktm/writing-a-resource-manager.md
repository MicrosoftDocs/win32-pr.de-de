---
description: Wenn Sie einen Dienst oder eine Komponente schreiben und transaktionale Dienste verwenden müssen, oder wenn Sie den Status einer Kernel Transaktion überwachen müssen, müssen Sie einen Ressourcen-Manager (RM) erstellen.
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Schreiben einer Ressourcen-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347966"
---
# <a name="writing-a-resource-manager"></a><span data-ttu-id="10b14-103">Schreiben einer Ressourcen-Manager</span><span class="sxs-lookup"><span data-stu-id="10b14-103">Writing a Resource Manager</span></span>

<span data-ttu-id="10b14-104">Wenn Sie einen Dienst oder eine Komponente schreiben und transaktionale Dienste verwenden müssen, oder wenn Sie den Status einer Kernel Transaktion überwachen müssen, müssen Sie einen Ressourcen-Manager (RM) erstellen.</span><span class="sxs-lookup"><span data-stu-id="10b14-104">If you are writing a service or component and need to use transactional services or if you need to monitor the state of a kernel transaction, you need to create a resource manager (RM).</span></span>

<span data-ttu-id="10b14-105">Zum Schreiben eines Ressourcen-Managers müssen Sie mehrere Kernel Objekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="10b14-105">To write a resource manager, you must create multiple kernel objects.</span></span> <span data-ttu-id="10b14-106">Die von einem RM verwendeten Objekte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="10b14-106">The objects that an RM uses are:</span></span>

-   <span data-ttu-id="10b14-107">Transaktions-Manager-Objekte (TM)</span><span class="sxs-lookup"><span data-stu-id="10b14-107">Transaction Manager (TM) objects</span></span>
-   <span data-ttu-id="10b14-108">Ressourcen-Manager Objekte</span><span class="sxs-lookup"><span data-stu-id="10b14-108">Resource Manager objects</span></span>
-   <span data-ttu-id="10b14-109">Eintragung von Objekten</span><span class="sxs-lookup"><span data-stu-id="10b14-109">Enlistment objects</span></span>

<span data-ttu-id="10b14-110">Erstellen Sie zunächst ein TM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="10b14-110">First, create a TM object.</span></span> <span data-ttu-id="10b14-111">Es gibt zwei Arten von TMS:</span><span class="sxs-lookup"><span data-stu-id="10b14-111">There are two types of TMs:</span></span>

-   <span data-ttu-id="10b14-112">Flüchtig – diese TMS verfügen nicht über ein Protokoll und können Ihren Zustand nicht wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="10b14-112">Volatile – these TMs do not have a log and cannot recover their state</span></span>
-   <span data-ttu-id="10b14-113">Permanent – diese TMS verfügen über ein Protokoll.</span><span class="sxs-lookup"><span data-stu-id="10b14-113">Durable – these TMs have a log</span></span>

<span data-ttu-id="10b14-114">Um ein dauerhaftes TM zu erstellen, müssen Sie entweder ein CLFS-Protokoll erstellen und den Befehl " [**kreatetransaktionsmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) " aufrufen, oder Sie müssen von KTM für Sie erstellen.</span><span class="sxs-lookup"><span data-stu-id="10b14-114">To create a durable TM, you must either create a CLFS log and call [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) or have KTM create it for you.</span></span> <span data-ttu-id="10b14-115">Nachdem ein dauerhaftes TM erstellt wurde, müssen Sie das TM zuerst wiederherstellen, indem Sie den [**wiederherstellbaren Transaktions-Manager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="10b14-115">After a durable TM is created, you must first recover the TM by calling [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager).</span></span> <span data-ttu-id="10b14-116">Nachdem die TM-Datei wieder hergestellt wurde, kann Sie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10b14-116">After the TM is recovered, it is available for use.</span></span>

<span data-ttu-id="10b14-117">Wenn Sie ein vorhandenes TM wieder hergestellt haben, empfangen alle diesem TM zugeordneten RMS Wiederherstellungs Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="10b14-117">If you recovered an existing TM, all RMs associated with this TM will start receiving recovery messages.</span></span> <span data-ttu-id="10b14-118">Weitere Informationen finden Sie unter [Wiederherstellungs Verarbeitung](recovery-processing.md).</span><span class="sxs-lookup"><span data-stu-id="10b14-118">For more information, see [Recovery Processing](recovery-processing.md).</span></span>

<span data-ttu-id="10b14-119">Als Nächstes erstellen Sie einen Ressourcen-Manager, indem Sie [**createresourcemanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) mit dem TM-handle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="10b14-119">Next, you create a resource manager by calling [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) with the TM handle.</span></span> <span data-ttu-id="10b14-120">Der RM kann flüchtig oder dauerhaft sein.</span><span class="sxs-lookup"><span data-stu-id="10b14-120">The RM can be volatile or durable.</span></span> <span data-ttu-id="10b14-121">Nur dauerhafte TMS können mit Durable RMS verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10b14-121">Only durable TMs can be used with durable RMs.</span></span>

<span data-ttu-id="10b14-122">Wenn Sie transaktional arbeiten, tragen Sie in die Transaktion ein, indem Sie [**createenlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)aufrufen und angeben, welche Benachrichtigungen empfangen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="10b14-122">When working transactionally, you enlist in the transaction by calling [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)and specifying which notifications to receive.</span></span>

<span data-ttu-id="10b14-123">**Hinweis**  Sie können Benachrichtigungen empfangen, bevor der aufzurufende [**Auflistungs**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="10b14-123">**Note**  You can start receiving notifications before the call to [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) is completed.</span></span>

<span data-ttu-id="10b14-124">Wenn Sie eine Benachrichtigung erhalten, wenden Sie die entsprechende "Complete \* "-Funktion an, wenn die Arbeit, die mit der Verarbeitung der Benachrichtigung verknüpft ist, abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="10b14-124">When you receive a notification, call the appropriate "Complete\*" function when any work associated with processing the notification is completed.</span></span> <span data-ttu-id="10b14-125">Die kompletten Funktionen sind:</span><span class="sxs-lookup"><span data-stu-id="10b14-125">The complete functions are:</span></span>

-   [<span data-ttu-id="10b14-126">**Commitcomplete**</span><span class="sxs-lookup"><span data-stu-id="10b14-126">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="10b14-127">**Preparecomplete**</span><span class="sxs-lookup"><span data-stu-id="10b14-127">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="10b14-128">**Prepreparecomplete**</span><span class="sxs-lookup"><span data-stu-id="10b14-128">**PreprepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

<span data-ttu-id="10b14-129">Wenn ein Ressourcen-Manager zu einem beliebigen Zeitpunkt nicht in der Lage ist, die Transaktion abzuschließen, oder wenn die Anwendung fortgesetzt wird, kann die in der Transaktion ausgeführte Aufgabe nicht rückgängig gemacht werden, müssen Sie die Transaktion durch Aufrufen von [**rollbackenlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="10b14-129">If at any time a resource manager is unable to complete the work of the transaction, or if continuing would render your application unable to undo the work done within the transaction, you must roll back the transaction by calling [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).</span></span>

 

 



