---
description: Steuert die Art und Weise, wie WMI Klassen abhängig von den angegebenen Flags erstellt oder aktualisiert.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
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
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347262"
---
# <a name="pragma-classflags"></a><span data-ttu-id="4b0b7-103">pragma classflags</span><span class="sxs-lookup"><span data-stu-id="4b0b7-103">pragma classflags</span></span>

<span data-ttu-id="4b0b7-104">Der **pragma classflags** -Präprozessorbefehl steuert die Art und Weise, wie WMI Klassen abhängig von den angegebenen Flags erstellt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-104">The **pragma classflags** preprocessor command controls the way WMI creates or updates classes depending on the flags specified.</span></span>

<span data-ttu-id="4b0b7-105">Im folgenden wird die Syntax für diesen Befehl beschrieben:</span><span class="sxs-lookup"><span data-stu-id="4b0b7-105">The following describes the syntax for this command:</span></span>


```mof
#pragma classflags ("[flag1], [flag2]")
```



<span data-ttu-id="4b0b7-106">Das *\[ Flag \]* muss mindestens eines der folgenden Argumente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-106">*\[Flag\]* must be one or more of the following arguments.</span></span> <span data-ttu-id="4b0b7-107">Sie können alle Flags kombinieren, die einander nicht widersprechen.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-107">You can combine any flags that do not contradict each other.</span></span>



| <span data-ttu-id="4b0b7-108">Flag</span><span class="sxs-lookup"><span data-stu-id="4b0b7-108">Flag</span></span>        | <span data-ttu-id="4b0b7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b0b7-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b0b7-110">createonly</span><span class="sxs-lookup"><span data-stu-id="4b0b7-110">createonly</span></span>  | <span data-ttu-id="4b0b7-111">Weist den Compiler an, keine Änderungen an vorhandenen Klassen vorzunehmen, und beendet eine Kompilierung, wenn eine in der MOF-Datei angegebene Klasse bereits in WMI vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-111">Instructs the compiler not make any changes to existing classes and terminates a compilation if a class specified in the MOF file already exists in WMI.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="4b0b7-112">ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="4b0b7-112">forceupdate</span></span> | <span data-ttu-id="4b0b7-113">Erzwingt das Aktualisieren von Klassen, wenn widersprüchliche untergeordnete Klassen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-113">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="4b0b7-114">Wenn Sie z. b. einen Klassen Qualifizierer in einer untergeordneten Klasse definieren und die Basisklasse versucht, denselben Qualifizierer hinzuzufügen, bewirkt die Verwendung dieses Flags, dass der Compiler diesen Konflikt durch Löschen des in Konflikt stehenden Qualifizierers in der untergeordneten Klasse löst.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-114">For example, if you define a class qualifier in a child class and the base class attempts to add the same qualifier, using this flag causes the compiler to resolve this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="4b0b7-115">Wenn die untergeordnete Klasse über Instanzen verfügt, schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-115">If the child class has instances, the update fails.</span></span> |
| <span data-ttu-id="4b0b7-116">safeupdate</span><span class="sxs-lookup"><span data-stu-id="4b0b7-116">safeupdate</span></span>  | <span data-ttu-id="4b0b7-117">Ermöglicht dem Compiler, Klassen zu aktualisieren, auch wenn untergeordnete Klassen vorhanden sind, wenn die Änderung keine Konflikte mit untergeordneten Klassen verursacht.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-117">Allows the compiler to update classes even if child classes exist, if the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="4b0b7-118">Mithilfe dieses Flags können Sie z. b. einer Basisklasse eine neue Eigenschaft hinzufügen, ohne dass die Eigenschaft auch einer bereits vorhandenen untergeordneten Klasse hinzugefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-118">For example, this flag allows you to add a new property to a base class without also having to add the property to any pre-existing child class.</span></span> <span data-ttu-id="4b0b7-119">Wenn die untergeordneten Klassen Instanzen aufweisen, schlägt die Aktualisierung fehl.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-119">If the child classes have instances, the update fails.</span></span>                           |
| <span data-ttu-id="4b0b7-120">updateonly</span><span class="sxs-lookup"><span data-stu-id="4b0b7-120">updateonly</span></span>  | <span data-ttu-id="4b0b7-121">Weist den Compiler an, keine neuen Klassen zu erstellen, und bewirkt, dass der Compiler die Kompilierung beendet, wenn eine in der MOF-Datei angegebene Klasse nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-121">Instructs the compiler to not create any new classes and causes the compiler to terminate the compilation if a class specified in the MOF file does not exist.</span></span>                                                                                                                                                                                                  |



 

## <a name="examples"></a><span data-ttu-id="4b0b7-122">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b0b7-122">Examples</span></span>

<span data-ttu-id="4b0b7-123">Im folgenden Beispiel wird gezeigt, wie Sie diesen Befehl mit den Flags updateonly und ForceUpdate verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4b0b7-123">The following example shows how to use this command with the updateonly and forceupdate flags.</span></span>


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a><span data-ttu-id="4b0b7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b0b7-124">Requirements</span></span>



| <span data-ttu-id="4b0b7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b0b7-125">Requirement</span></span> | <span data-ttu-id="4b0b7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="4b0b7-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4b0b7-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b0b7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4b0b7-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b0b7-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4b0b7-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b0b7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4b0b7-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b0b7-130">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4b0b7-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b0b7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b0b7-132">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="4b0b7-132">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




