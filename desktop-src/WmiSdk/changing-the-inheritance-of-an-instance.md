---
description: Es kann vorkommen, dass eine Instanz, die als untergeordnetes Element einer übergeordneten Klasse erstellt wurde, übergeordnete Klassen ändern muss und das untergeordnete Element einer anderen übergeordneten Klasse werden muss.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Ändern der Vererbung einer Instanz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865676"
---
# <a name="changing-the-inheritance-of-an-instance"></a><span data-ttu-id="7da83-103">Ändern der Vererbung einer Instanz</span><span class="sxs-lookup"><span data-stu-id="7da83-103">Changing the Inheritance of an Instance</span></span>

<span data-ttu-id="7da83-104">Es kann vorkommen, dass eine Instanz, die als untergeordnetes Element einer übergeordneten Klasse erstellt wurde, übergeordnete Klassen ändern muss und das untergeordnete Element einer anderen übergeordneten Klasse werden muss.</span><span class="sxs-lookup"><span data-stu-id="7da83-104">You may find a situation where an instance that was created as a child of one parent class must change parent classes and become the child of a different parent class.</span></span> <span data-ttu-id="7da83-105">Angenommen, Sie verfügen über eine abgeleitete Klasse, **manualservice**, die einen manuellen Dienst beschreibt, und eine abgeleitete Klasse, **Autoservice**, die einen automatischen Dienst beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7da83-105">For example, you may have a derived class, **ManualService**, describing a manual service, and a derived class, **AutoService**, describing an automatic service.</span></span> <span data-ttu-id="7da83-106">Beide Klassen verfügen über eine große Anzahl von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7da83-106">Both classes have a large number of properties.</span></span> <span data-ttu-id="7da83-107">Nicht alle Eigenschaften sind identisch.</span><span class="sxs-lookup"><span data-stu-id="7da83-107">Not all properties are identical.</span></span> <span data-ttu-id="7da83-108">Um einen Dienst von manuell in automatisch zu ändern, müssen Sie auch die Instanz, die den Dienst darstellt, von **manualservice** zu **Autoservice** ändern.</span><span class="sxs-lookup"><span data-stu-id="7da83-108">To change a service from manual to automatic, you must also change the instance representing the service from **ManualService** to **AutoService**.</span></span> <span data-ttu-id="7da83-109">In der aktuellen Version von WMI können Sie die [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) -Methode nicht mit dem *pinst* -Parameter aufrufen, der auf eine Instanz von **Autoservice** verweist, und die Schlüsseleigenschaften, die die **manualservice** -Instanz beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7da83-109">In the current version of WMI, you cannot call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) method with the *pInst* parameter pointing to an instance of **AutoService** and the key properties describing the **ManualService** instance.</span></span> <span data-ttu-id="7da83-110">Wenn Sie dies tun, löschen Sie implizit die ursprüngliche **manualservice** -Instanz.</span><span class="sxs-lookup"><span data-stu-id="7da83-110">If you do, you implicitly delete the original **ManualService** instance.</span></span> <span data-ttu-id="7da83-111">Im Wesentlichen können Sie nach dem Einrichten der Klasse einer Instanz nur die übergeordnete Klasse einer Instanz ändern, indem Sie die Instanz löschen und die Instanz als Instanz der neuen übergeordneten Klasse neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7da83-111">In essence, after you establish the class of an instance, you can only change the parent class of an instance by deleting the instance and recreating the instance as an instance of the new parent class.</span></span>

<span data-ttu-id="7da83-112">Im folgenden Verfahren wird beschrieben, wie Sie eine-Instanz von einer Klasse in eine andere Klasse verschieben.</span><span class="sxs-lookup"><span data-stu-id="7da83-112">The following procedure describes how to move an instance from one class to another class.</span></span>

<span data-ttu-id="7da83-113">**So verschieben Sie eine Instanz von einer Klasse in eine andere Klasse**</span><span class="sxs-lookup"><span data-stu-id="7da83-113">**To move an instance from one class to another class**</span></span>

1.  <span data-ttu-id="7da83-114">Löschen Sie die Instanz aus der ursprünglichen Klasse.</span><span class="sxs-lookup"><span data-stu-id="7da83-114">Delete the instance from the original class.</span></span>
2.  <span data-ttu-id="7da83-115">Erstellen Sie die-Instanz unter der neuen-Klasse.</span><span class="sxs-lookup"><span data-stu-id="7da83-115">Create the instance under the new class.</span></span>

    <span data-ttu-id="7da83-116">In WMI ist es nicht zulässig, dass Anwendungen eine Instanz verschieben, indem Sie Sie in der neuen Klasse erstellen und anschließend mit dem Schlüssel der ursprünglichen Instanz aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7da83-116">WMI does not allow applications to move an instance by creating it in the new class and then updating it with the key of the original instance.</span></span>

<span data-ttu-id="7da83-117">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="7da83-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



