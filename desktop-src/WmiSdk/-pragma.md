---
description: Ähnelt einem Befehls Zeilenschalter. Sie müssen jedoch nicht \# jedes Mal, wenn Sie eine MOF-Datei kompilieren, einen pragma-Befehl erneut eingeben.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353929"
---
# <a name="pragma"></a><span data-ttu-id="8afc5-104">\#pragma</span><span class="sxs-lookup"><span data-stu-id="8afc5-104">\#pragma</span></span>

<span data-ttu-id="8afc5-105">Der **\# pragma** -Präprozessorbefehl ähnelt einem Befehls Zeilenschalter.</span><span class="sxs-lookup"><span data-stu-id="8afc5-105">The **\#pragma** preprocessor command is similar to a command-line switch.</span></span> <span data-ttu-id="8afc5-106">Sie müssen jedoch nicht jedes Mal, wenn Sie eine MOF-Datei kompilieren, einen **\# pragma** -Befehl erneut eingeben.</span><span class="sxs-lookup"><span data-stu-id="8afc5-106">However, you do not need to reenter a **\#pragma** command each time you compile a MOF file.</span></span> <span data-ttu-id="8afc5-107">Im folgenden Beispiel wird die **\# pragma** -Befehlssyntax veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="8afc5-107">The following example illustrates **\#pragma** command syntax:</span></span>


```mof
#pragma [command]
```



<span data-ttu-id="8afc5-108">Normalerweise platzieren Sie einen **\# pragma** -Befehl am Anfang einer MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="8afc5-108">You usually place a **\#pragma** command at the beginning of a MOF file.</span></span> <span data-ttu-id="8afc5-109">Sie können jedoch einige Befehle, z. b. den **\# pragma** -Befehl, im Text Ihres MOF-Codes platzieren.</span><span class="sxs-lookup"><span data-stu-id="8afc5-109">However, you can place some commands, such as the **\#pragma** command, in the body of your MOF code.</span></span> <span data-ttu-id="8afc5-110">Das folgende Beispiel zeigt **\# pragma** -Befehle, die dem MOF-Compiler zeigen, dass Sie Klassen und Instanzen im root \\ CIMV2-Namespace platzieren und die Datei kompilieren müssen, in der die Befehle bei der Wiederherstellung des Repository enthalten sind:</span><span class="sxs-lookup"><span data-stu-id="8afc5-110">The following example shows **\#pragma** commands that indicate to the MOF compiler that it must place classes and instances in the root\\cimv2 namespace and compile the file in which the commands are included during repository recovery:</span></span>


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



<span data-ttu-id="8afc5-111">Im folgenden werden die verfügbaren **\# pragma** -Befehle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8afc5-111">The following lists the available **\#pragma** commands.</span></span>



| <span data-ttu-id="8afc5-112">Get-Help</span><span class="sxs-lookup"><span data-stu-id="8afc5-112">Command</span></span>                                         | <span data-ttu-id="8afc5-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8afc5-113">Description</span></span>                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8afc5-114">**trag**</span><span class="sxs-lookup"><span data-stu-id="8afc5-114">**amendment**</span></span>](pragma-amendment.md)           | <span data-ttu-id="8afc5-115">Weist den MOF-Compiler an, eine MOF-Datei in sprachneutrale und sprachspezifische Versionen aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="8afc5-115">Directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> |
| [<span data-ttu-id="8afc5-116">**Auto Wiederherstellen**</span><span class="sxs-lookup"><span data-stu-id="8afc5-116">**autorecover**</span></span>](pragma-autorecover.md)       | <span data-ttu-id="8afc5-117">Fügt eine MOF-Datei zur Liste der Dateien hinzu, die während der Wiederherstellung des Repository kompiliert wurden.</span><span class="sxs-lookup"><span data-stu-id="8afc5-117">Adds a MOF file to the list of files compiled during repository recovery.</span></span>                             |
| [<span data-ttu-id="8afc5-118">**classflags**</span><span class="sxs-lookup"><span data-stu-id="8afc5-118">**classflags**</span></span>](pragma-classflags.md)         | <span data-ttu-id="8afc5-119">Steuert die Art und Weise, wie Klassen abhängig von den angegebenen Flags erstellt oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8afc5-119">Controls the way classes are created or updated depending on the flags specified.</span></span>                     |
| [<span data-ttu-id="8afc5-120">**deleteclass**</span><span class="sxs-lookup"><span data-stu-id="8afc5-120">**deleteclass**</span></span>](pragma-deleteclass.md)       | <span data-ttu-id="8afc5-121">Löscht eine vorhandene Klasse und deren Instanzen aus dem Repository.</span><span class="sxs-lookup"><span data-stu-id="8afc5-121">Deletes an existing class and its instances from the repository.</span></span>                                      |
| [<span data-ttu-id="8afc5-122">**DeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="8afc5-122">**deleteinstance**</span></span>](pragma-deleteinstance.md) | <span data-ttu-id="8afc5-123">Löscht eine vorhandene Instanz einer Klasse aus dem Repository.</span><span class="sxs-lookup"><span data-stu-id="8afc5-123">Deletes an existing instance of a class from the repository.</span></span>                                          |
| [<span data-ttu-id="8afc5-124">**instanceflags**</span><span class="sxs-lookup"><span data-stu-id="8afc5-124">**instanceflags**</span></span>](pragma-instanceflags.md)   | <span data-ttu-id="8afc5-125">Steuert die Art und Weise, in der Instanzen abhängig von den angegebenen Flags erstellt oder aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8afc5-125">Controls the way instances are created or updated depending on the flags specified.</span></span>                   |
| [<span data-ttu-id="8afc5-126">**namespace**</span><span class="sxs-lookup"><span data-stu-id="8afc5-126">**namespace**</span></span>](pragma-namespace.md)           | <span data-ttu-id="8afc5-127">Fordert an, dass der Compiler die MOF-Datei in den Namespace lädt, der als *Wert von NamespacePath* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="8afc5-127">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="8afc5-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8afc5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8afc5-129">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="8afc5-129">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



