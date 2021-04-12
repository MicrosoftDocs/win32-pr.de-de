---
description: Zusätzlich zu Klassen und Instanzen können Sie mithilfe von WMI eine Methode ändern. Der Hauptgrund, warum Sie eine Methode ändern möchten, ist, wenn Sie die Implementierung einer Methode in einem Anbieter geändert haben. Weitere Informationen finden Sie unterschreiben eines Methoden Anbieters.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Ändern einer Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393329"
---
# <a name="modifying-a-method"></a><span data-ttu-id="737a0-105">Ändern einer Methode</span><span class="sxs-lookup"><span data-stu-id="737a0-105">Modifying a Method</span></span>

<span data-ttu-id="737a0-106">Zusätzlich zu Klassen und Instanzen können Sie mithilfe von WMI eine Methode ändern.</span><span class="sxs-lookup"><span data-stu-id="737a0-106">In addition to classes and instances, WMI allows you to modify a method.</span></span> <span data-ttu-id="737a0-107">Der Hauptgrund, warum Sie eine Methode ändern möchten, ist, wenn Sie die Implementierung einer Methode in einem Anbieter geändert haben.</span><span class="sxs-lookup"><span data-stu-id="737a0-107">The main reason you would want to modify a method is if you changed the implementation of a method in a provider.</span></span> <span data-ttu-id="737a0-108">Weitere Informationen finden Sie unter [Schreiben eines Methoden Anbieters](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="737a0-108">For more information, see [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="737a0-109">Das Ändern einer Methode ist kein Vorgang, der im Skript ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="737a0-109">Modifying a method is not an operation that can be done in script.</span></span>

<span data-ttu-id="737a0-110">Im folgenden Verfahren wird beschrieben, wie eine Methode Programm gesteuert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="737a0-110">The following procedure describes how to modify a method programmatically.</span></span>

<span data-ttu-id="737a0-111">**So ändern Sie eine Methode Programm gesteuert**</span><span class="sxs-lookup"><span data-stu-id="737a0-111">**To modify a method programmatically**</span></span>

1.  <span data-ttu-id="737a0-112">Rufen Sie die Klassendefinition mit einem-Befehl von [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod)ab.</span><span class="sxs-lookup"><span data-stu-id="737a0-112">Retrieve the class definition with a call to [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span></span>

    <span data-ttu-id="737a0-113">Die zwei out-Parameter *ppinsignature* und *ppoutsignature* enthalten die in-Parameter-Klasse bzw. die Out-Parameter-Klasse.</span><span class="sxs-lookup"><span data-stu-id="737a0-113">The two out parameters, *ppInSignature* and *ppOutSignature*, contain the in-parameter class and the out-parameter class, respectively.</span></span> <span data-ttu-id="737a0-114">Der Rückgabewert wird in der Out-Parameter-Klasse als Eigenschaft gebündelt und sollte als " **ReturnValue**" benannt werden.</span><span class="sxs-lookup"><span data-stu-id="737a0-114">The return value is bundled into the out-parameter class as a property, and should be named **ReturnValue**.</span></span>

2.  <span data-ttu-id="737a0-115">Rufen Sie die Parameter mit den Aufrufen von [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)oder [**IWbemClassObject::D Elete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete)ab, und ändern Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="737a0-115">Retrieve and modify the parameters with calls to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put), or [**IWbemClassObject::Delete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span></span>
3.  <span data-ttu-id="737a0-116">Platzieren Sie die neue Version der Methode mithilfe eines Aufrufens von [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod)wieder in der übergeordneten Klasse.</span><span class="sxs-lookup"><span data-stu-id="737a0-116">Place your new version of the method back into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="737a0-117">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="737a0-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



