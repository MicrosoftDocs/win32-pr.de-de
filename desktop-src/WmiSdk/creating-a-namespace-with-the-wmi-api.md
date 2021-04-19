---
description: Eine weitere Möglichkeit zum Erstellen eines Namespace besteht darin, die WMI-API zu verwenden, um den Namespace Programm gesteuert zu erstellen.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Erstellen eines Namespace mit der WMI-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348548"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a><span data-ttu-id="b2b99-103">Erstellen eines Namespace mit der WMI-API</span><span class="sxs-lookup"><span data-stu-id="b2b99-103">Creating a Namespace with the WMI API</span></span>

<span data-ttu-id="b2b99-104">Eine weitere Möglichkeit zum Erstellen eines Namespace besteht darin, die WMI-API zu verwenden, um den Namespace Programm gesteuert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2b99-104">Another way of creating a namespace is to use the WMI API to create the namespace programmatically.</span></span> <span data-ttu-id="b2b99-105">Der Vorteil der programmgesteuerten Erstellung eines Namespace besteht darin, dass Sie den Namespace in einer Anwendung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="b2b99-105">The advantage to creating a namespace programmatically is that you can create the namespace from within an application.</span></span> <span data-ttu-id="b2b99-106">Allerdings ist die Verwendung der WMI-API komplexer als die Verwendung von MOF-Code (Managed Object Format), und Sie können Ihre Namespaces nicht so einfach für andere Entwickler freigeben.</span><span class="sxs-lookup"><span data-stu-id="b2b99-106">However, using the WMI API is more complex than using Managed Object Format (MOF) code, and you cannot as easily share your namespaces with other developers.</span></span>

<span data-ttu-id="b2b99-107">Im folgenden Verfahren wird beschrieben, wie Sie einen Namespace mithilfe der WMI-API erstellen.</span><span class="sxs-lookup"><span data-stu-id="b2b99-107">The following procedure describes how to create a namespace using the WMI API.</span></span>

<span data-ttu-id="b2b99-108">**So erstellen Sie einen Namespace mithilfe der WMI-API**</span><span class="sxs-lookup"><span data-stu-id="b2b99-108">**To create a namespace using the WMI API**</span></span>

1.  <span data-ttu-id="b2b99-109">Verwenden Sie [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) zum Abrufen eines Zeigers auf ein [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) -Objekt, das auf die Klasse [**\_ \_ Namespace**](--namespace.md) System verweist.</span><span class="sxs-lookup"><span data-stu-id="b2b99-109">Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a pointer to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) object that points to the [**\_\_Namespace**](--namespace.md) system class.</span></span>
2.  <span data-ttu-id="b2b99-110">Definieren Sie eine Instanz der [**\_ \_ Namespace**](--namespace.md) -System Klasse mit einem-Befehl, der [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)aufruft.</span><span class="sxs-lookup"><span data-stu-id="b2b99-110">Define an instance of the [**\_\_Namespace**](--namespace.md) system class with a call to [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span></span>
3.  <span data-ttu-id="b2b99-111">Legen Sie die **Name** -Eigenschaft der [**\_ \_ Namespace**](--namespace.md) Instanz mit einem Befehl [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)fest.</span><span class="sxs-lookup"><span data-stu-id="b2b99-111">Set the **Name** property of the [**\_\_Namespace**](--namespace.md) instance with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>
4.  <span data-ttu-id="b2b99-112">Erstellen Sie den Namespace mit einem [**callbemservices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="b2b99-112">Create the namespace with a call to [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span></span>

    <span data-ttu-id="b2b99-113">Der *pinst* -Parameter von [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) sollte auf die neue Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="b2b99-113">The *pInst* parameter of [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) should point to the new instance.</span></span>

 

 



