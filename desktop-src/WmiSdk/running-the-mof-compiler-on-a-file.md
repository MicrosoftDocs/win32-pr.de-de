---
description: 'Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: das Befehlszeilenprogramm oder eine programmgesteuerte Schnittstelle.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Ausführen des MOF-Compilers für eine Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230244"
---
# <a name="running-the-mof-compiler-on-a-file"></a><span data-ttu-id="19cf9-103">Ausführen des MOF-Compilers für eine Datei</span><span class="sxs-lookup"><span data-stu-id="19cf9-103">Running the MOF Compiler on a File</span></span>

<span data-ttu-id="19cf9-104">Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: das Befehlszeilenprogramm oder eine programmgesteuerte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="19cf9-104">You have two choices when compiling a MOF file: using the command-line utility or using a programmatic interface.</span></span>

<span data-ttu-id="19cf9-105">Bis Sie den MOF-Compiler [**Mofcomp.exe**](mofcomp.md)ausführen, ist ein Anbieter nicht bei WMI registriert, und die klassen, die er in der MOF-Datei erstellt hat, sind im [*WMI-Repository*](gloss-w.md)nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19cf9-105">Until you run the MOF compiler, [**Mofcomp.exe**](mofcomp.md), a provider is not registered with WMI and the classes it created in the MOF file are not available in the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="19cf9-106">Im folgenden Verfahren wird beschrieben, wie Sie eine MOF-Datei kompilieren.</span><span class="sxs-lookup"><span data-stu-id="19cf9-106">The following procedure describes how to compile a MOF file.</span></span>

<span data-ttu-id="19cf9-107">**So führen Sie den MOF-Compiler in einer Datei über die Befehlszeile aus**</span><span class="sxs-lookup"><span data-stu-id="19cf9-107">**To run the MOF compiler on a file from the command line**</span></span>

1.  <span data-ttu-id="19cf9-108">Rufen Sie den MOF-Compiler über die Befehlszeile mit der folgenden Syntax auf.</span><span class="sxs-lookup"><span data-stu-id="19cf9-108">Call the MOF compiler from the command line, using the following syntax.</span></span>

    <span data-ttu-id="19cf9-109">**mofcomp** _MOFfile_**.mof**</span><span class="sxs-lookup"><span data-stu-id="19cf9-109">**mofcomp** _MOFfile_**.mof**</span></span>

    <span data-ttu-id="19cf9-110">Der MOF-Compiler unterstützt eine Vielzahl von Schaltern, um spezielle Verarbeitungssituationen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="19cf9-110">The MOF compiler supports a variety of switches to control special processing situations.</span></span> <span data-ttu-id="19cf9-111">Alle Switches sind optional, und jede Kombination von Schaltern ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="19cf9-111">All of the switches are optional, and any combination of switches is allowed.</span></span> <span data-ttu-id="19cf9-112">Es ist jedoch nicht sinnvoll, einige der Schalter in Kombination mit anderen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="19cf9-112">However, it does not make sense to use some of the switches in combination with others.</span></span> <span data-ttu-id="19cf9-113">Wenn sie beispielsweise die Schalter **-class:updateonly** und **-class:createonly kombinieren,** führt dies dazu, dass der Compiler keine Aktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="19cf9-113">For example, to combine the **-class:updateonly** and **-class:createonly** switches results in the compiler not performing any action.</span></span>

    <span data-ttu-id="19cf9-114">Standardmäßig speichert Mofcomp.exe die kompilierten Klassen im \\ WMI-Stammnamespace.</span><span class="sxs-lookup"><span data-stu-id="19cf9-114">By default, Mofcomp.exe stores the compiled classes in the root\\default WMI namespace.</span></span> <span data-ttu-id="19cf9-115">Beachten Sie, dass der Standardnamespace für Mofcomp.exe nicht mit dem Standardnamespace für die Skripterstellung identisch ist.</span><span class="sxs-lookup"><span data-stu-id="19cf9-115">Note that the default namespace for Mofcomp.exe is not the same as the default namespace for scripting.</span></span> <span data-ttu-id="19cf9-116">Der Standardnamespace für die Skripterstellung wird im WMI-Steuerelement auf der Registerkarte Erweitert angegeben. Weitere Informationen finden Sie unter [Festlegen der Namespacesicherheit mit dem WMI-Steuerelement](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="19cf9-116">The default namespace for scripting is specified in the WMI Control on the Advanced tab. For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

    <span data-ttu-id="19cf9-117">Sie können den Namespace, der die Klassen empfängt, auf zwei Arten ändern.</span><span class="sxs-lookup"><span data-stu-id="19cf9-117">You can change the namespace that receives the classes in two ways.</span></span>

    1.  <span data-ttu-id="19cf9-118">Verwenden Sie den Schalter **-N** für den **mofcomp-Befehl.**</span><span class="sxs-lookup"><span data-stu-id="19cf9-118">Use the **-N** switch for the **mofcomp** command.</span></span>
    2.  <span data-ttu-id="19cf9-119">Fügen Sie den \# [**Präprozessorbefehls-Pragmanamespace**](pragma-namespace.md) in die MOF-Datei ein.</span><span class="sxs-lookup"><span data-stu-id="19cf9-119">Insert the preprocessor command \#[**pragma namespace**](pragma-namespace.md) in the MOF file.</span></span>

2.  <span data-ttu-id="19cf9-120">Optional können Sie eine MOF-Datei programmgesteuert kompilieren.</span><span class="sxs-lookup"><span data-stu-id="19cf9-120">Optionally, you can compile a MOF file programmatically.</span></span> <span data-ttu-id="19cf9-121">Weitere Informationen finden Sie unter [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span><span class="sxs-lookup"><span data-stu-id="19cf9-121">For more information, see [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19cf9-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19cf9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19cf9-123">Kompilieren von MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="19cf9-123">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="19cf9-124">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="19cf9-124">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="19cf9-125">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="19cf9-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



