---
description: Eine weitere Möglichkeit zum Erstellen eines Namespace ist die Verwendung von Managed Object Format (MOF)-Code zum Erstellen eines gleich geordneten Namespace. Ein gleich geordneter Namespace ist ein Namespace, der nicht als untergeordnetes Element des aktuellen Namespace vorhanden ist.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Erstellen eines gleich geordneten Namespace mit MOF-Code
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352694"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a><span data-ttu-id="64122-104">Erstellen eines gleich geordneten Namespace mit MOF-Code</span><span class="sxs-lookup"><span data-stu-id="64122-104">Creating a Sibling Namespace with MOF Code</span></span>

<span data-ttu-id="64122-105">Eine weitere Möglichkeit zum Erstellen eines Namespace ist die Verwendung von Managed Object Format (MOF)-Code zum Erstellen eines gleich geordneten Namespace.</span><span class="sxs-lookup"><span data-stu-id="64122-105">Another way of creating a namespace is to use Managed Object Format (MOF) code to create a sibling namespace.</span></span> <span data-ttu-id="64122-106">Ein gleich geordneter Namespace ist ein Namespace, der nicht als untergeordnetes Element des aktuellen Namespace vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="64122-106">A sibling namespace is a namespace that does not exist as a child of the current namespace.</span></span>

<span data-ttu-id="64122-107">Im folgenden Verfahren wird beschrieben, wie ein gleich geordneter Namespace mit MOF-Code erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="64122-107">The following procedure describes how to create a sibling namespace with MOF code.</span></span>

<span data-ttu-id="64122-108">**So erstellen Sie einen gleich geordneten Namespace mit MOF-Code**</span><span class="sxs-lookup"><span data-stu-id="64122-108">**To create a sibling namespace with MOF code**</span></span>

1.  <span data-ttu-id="64122-109">Fügen Sie den [**\# pragma-Namespace**](pragma-namespace.md) -Befehl in den MOF-Code vor der Namespace Deklaration ein.</span><span class="sxs-lookup"><span data-stu-id="64122-109">Insert the [**\#pragma namespace**](pragma-namespace.md) command into your MOF code prior to the namespace declaration.</span></span>

    <span data-ttu-id="64122-110">Der [**\# pragma-Namespace**](pragma-namespace.md) Befehl weist WMI an, wo die Instanzen nach der-Direktive erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="64122-110">The [**\#pragma namespace**](pragma-namespace.md) command instructs WMI where to create the instances following the directive.</span></span>

2.  <span data-ttu-id="64122-111">Erstellen Sie eine Instanz der [**\_ \_ Namespace**](--namespace.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="64122-111">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>
3.  <span data-ttu-id="64122-112">Kompilieren Sie den Code mit dem Hilfsprogramm [Mofcomp](mofcomp.md) oder der [**imofcompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="64122-112">Compile your code with the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="64122-113">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="64122-113">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="64122-114">Im folgenden MOF-Codebeispiel wird beschrieben, wie ein Namespace als gleich geordnetes Element des \\ Namespace "root CIMv2" erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="64122-114">The following MOF code example describes how to create a namespace as a sibling to the "Root\\CIMv2" namespace.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



