---
description: Die einfachste Möglichkeit, einen Namespace zu erstellen, ist die Verwendung von Managed Object Format (MOF)-Code, um den Namespace im aktuellen Verzeichnis zu erstellen. Das aktuelle Verzeichnis wird definiert, wenn Sie sich anmelden.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Erstellen eines untergeordneten Namespace mit MOF-Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104050724"
---
# <a name="creating-a-child-namespace-with-mof-code"></a><span data-ttu-id="7b7a2-104">Erstellen eines untergeordneten Namespace mit MOF-Code</span><span class="sxs-lookup"><span data-stu-id="7b7a2-104">Creating a Child Namespace with MOF Code</span></span>

<span data-ttu-id="7b7a2-105">Die einfachste Möglichkeit, einen Namespace zu erstellen, ist die Verwendung von Managed Object Format (MOF)-Code, um den Namespace im aktuellen Verzeichnis zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-105">The simplest way of creating a namespace is to use Managed Object Format (MOF) code to create the namespace inside the current directory.</span></span> <span data-ttu-id="7b7a2-106">Das aktuelle Verzeichnis wird definiert, wenn Sie sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-106">The current directory is defined when you log on.</span></span>

<span data-ttu-id="7b7a2-107">Im folgenden Verfahren wird beschrieben, wie ein untergeordneter Namespace mithilfe von MOF-Code erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-107">The following procedure describes how to create a child namespace using MOF code.</span></span>

<span data-ttu-id="7b7a2-108">**So erstellen Sie einen untergeordneten Namespace mithilfe von MOF-Code**</span><span class="sxs-lookup"><span data-stu-id="7b7a2-108">**To create a child namespace using MOF code**</span></span>

1.  <span data-ttu-id="7b7a2-109">Erstellen Sie eine Instanz der [**\_ \_ Namespace**](--namespace.md) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-109">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>

    <span data-ttu-id="7b7a2-110">Im folgenden Codebeispiel wird gezeigt, wie ein untergeordneter Namespace erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-110">The following code example shows how to create a child namespace.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  <span data-ttu-id="7b7a2-111">Wenn Sie festlegen möchten, dass der Benutzer eine verschlüsselte Verbindung mit dem-Namespace herstellen muss, verwenden Sie den-Qualifizierer "Requirements **sencryption** ".</span><span class="sxs-lookup"><span data-stu-id="7b7a2-111">If you want to require the user to make an encrypted connection to the namespace, use the **RequiresEncryption** qualifier.</span></span> <span data-ttu-id="7b7a2-112">Weitere Informationen finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="7b7a2-112">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

    <span data-ttu-id="7b7a2-113">Im folgenden Codebeispiel wird gezeigt, wie eine verschlüsselte Verbindung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-113">The following code example shows how to require an encrypted connection.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  <span data-ttu-id="7b7a2-114">Wenn Sie anstelle der standardmäßigen Namespace Sicherheit eine Sicherheits Beschreibung für den Namespace festlegen möchten, verwenden Sie den **namespacesecuritysddl** -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-114">If you want to set a security descriptor on the namespace rather than using the default namespace security, use the **NamespaceSecuritySDDL** qualifier.</span></span> <span data-ttu-id="7b7a2-115">Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit, wenn der Namespace erstellt wird](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="7b7a2-115">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

    <span data-ttu-id="7b7a2-116">Im folgenden Codebeispiel wird gezeigt, wie eine Sicherheits Beschreibung für den-Namespace festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-116">The following code example shows how to set a security descriptor on the namespace.</span></span>

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  <span data-ttu-id="7b7a2-117">Kompilieren und laden Sie die [**\_ \_ Namespace**](--namespace.md) Instanz mithilfe des [Mofcomp](mofcomp.md) -Hilfsprogramms oder der [**imofcompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-117">Compile and load the [**\_\_Namespace**](--namespace.md) instance using the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span> <span data-ttu-id="7b7a2-118">Sowohl der-Namespace als auch die **imuscompiler** -Schnittstelle laden den Namespace automatisch in das aktuelle Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7b7a2-118">Both mofcomp and the **IMofCompiler** interface automatically load the namespace into the current directory.</span></span> <span data-ttu-id="7b7a2-119">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="7b7a2-119">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b7a2-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b7a2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b7a2-121">**WMI-Standard Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="7b7a2-121">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



