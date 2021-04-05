---
description: Fordert an, dass der Compiler die MOF-Datei in den Namespace lädt, der als NamespacePath angegeben ist. Wenn sowohl der MOF-Compiler-n-Namespace-Schalter als auch der \# pragma-Namespace&\# 32; NamespacePath-Befehl verwendet werden, hat der Befehl Vorrang vor dem Switch.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: pragma-Namespace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753688"
---
# <a name="pragma-namespace"></a><span data-ttu-id="ee4f3-104">pragma-Namespace</span><span class="sxs-lookup"><span data-stu-id="ee4f3-104">pragma namespace</span></span>

<span data-ttu-id="ee4f3-105">Der Präprozessorbefehl " **pragma Namespace** " fordert an, dass der Compiler die MOF-Datei in den als " *Wert von NamespacePath*" angegebenen Namespace lädt.</span><span class="sxs-lookup"><span data-stu-id="ee4f3-105">The **pragma namespace** preprocessor command requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="ee4f3-106">Wenn sowohl der MOF **-Compiler-n-** Namespace-Schalter als auch der **\# pragma Namespace Namespace Namespace** -Befehl verwendet werden, hat der Befehl Vorrang vor dem Switch. </span><span class="sxs-lookup"><span data-stu-id="ee4f3-106">If both the MOF compiler **-n** namespace switch and the **\#pragma namespace** *namespacepath* command are used, the command takes priority over the switch.</span></span>

<span data-ttu-id="ee4f3-107">Im folgenden wird die Syntax beschrieben:</span><span class="sxs-lookup"><span data-stu-id="ee4f3-107">The following describes the syntax:</span></span>


```mof
#pragma namespace ("[Namespace]")
```



<span data-ttu-id="ee4f3-108">*\[ Namespace \]* ist der angegebene Namespace.</span><span class="sxs-lookup"><span data-stu-id="ee4f3-108">*\[Namespace\]* is the specified namespace.</span></span>

<span data-ttu-id="ee4f3-109">Wenn Sie diesen Befehl oder den entsprechenden Befehls Zeilenschalter nicht angeben, verwendet der MOF-Compiler \\ standardmäßig den Standard Namespace.</span><span class="sxs-lookup"><span data-stu-id="ee4f3-109">If you do not specify this command or the equivalent command-line switch, the MOF compiler uses the root\\default namespace by default.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee4f3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee4f3-110">Remarks</span></span>

<span data-ttu-id="ee4f3-111">Sie können festlegen, dass Client Skripts und-Anwendungen eine verschlüsselte Verbindung für die Authentifizierung verwenden, indem Sie der MOF-Datei, die den Namespace erstellt, den Wert "Requirements **sencryption** " hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ee4f3-111">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="ee4f3-112">Sie können auch einen vorhandenen Namespace ändern, indem Sie dieses Attribut hinzufügen und die MOF-Datei erneut kompilieren.</span><span class="sxs-lookup"><span data-stu-id="ee4f3-112">You can also modify an existing namespace by adding this attribute and compile the MOF file again.</span></span> <span data-ttu-id="ee4f3-113">Weitere Informationen **zur Verwendung von**"Requirements" finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="ee4f3-113">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ee4f3-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee4f3-114">Examples</span></span>

<span data-ttu-id="ee4f3-115">Im folgenden Beispiel wird gezeigt, wie Klassen oder Instanzen im \\ Namespace "root Test" platziert werden.</span><span class="sxs-lookup"><span data-stu-id="ee4f3-115">The following example shows how place classes or instances in the "Root\\Test" namespace.</span></span>


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a><span data-ttu-id="ee4f3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee4f3-116">Requirements</span></span>



| <span data-ttu-id="ee4f3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee4f3-117">Requirement</span></span> | <span data-ttu-id="ee4f3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ee4f3-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ee4f3-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee4f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee4f3-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee4f3-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ee4f3-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee4f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee4f3-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee4f3-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee4f3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee4f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee4f3-124">Festlegen von namepace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="ee4f3-124">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="ee4f3-125">**WMI-Standard Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="ee4f3-125">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="ee4f3-126">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="ee4f3-126">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




