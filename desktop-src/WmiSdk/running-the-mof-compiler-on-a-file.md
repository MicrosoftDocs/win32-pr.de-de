---
description: 'Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: mithilfe des Befehlszeilen-Hilfsprogramms oder mithilfe einer programmgesteuerten Schnittstelle.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Ausführen des MOF-Compilers für eine Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1605544e05f59670f9e6fd73fcd8c01862b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215336"
---
# <a name="running-the-mof-compiler-on-a-file"></a><span data-ttu-id="64264-103">Ausführen des MOF-Compilers für eine Datei</span><span class="sxs-lookup"><span data-stu-id="64264-103">Running the MOF Compiler on a File</span></span>

<span data-ttu-id="64264-104">Beim Kompilieren einer MOF-Datei haben Sie zwei Möglichkeiten: mithilfe des Befehlszeilen-Hilfsprogramms oder mithilfe einer programmgesteuerten Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="64264-104">You have two choices when compiling a MOF file: using the command-line utility or using a programmatic interface.</span></span>

<span data-ttu-id="64264-105">Wenn Sie den MOF-Compiler [**Mofcomp.exe**](mofcomp.md)ausführen, ist ein Anbieter nicht bei WMI registriert, und die in der MOF-Datei erstellten Klassen sind im [*WMI-Repository*](gloss-w.md)nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="64264-105">Until you run the MOF compiler, [**Mofcomp.exe**](mofcomp.md), a provider is not registered with WMI and the classes it created in the MOF file are not available in the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="64264-106">Im folgenden Verfahren wird beschrieben, wie eine MOF-Datei kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="64264-106">The following procedure describes how to compile a MOF file.</span></span>

<span data-ttu-id="64264-107">**So führen Sie den MOF-Compiler für eine Datei in der Befehlszeile aus**</span><span class="sxs-lookup"><span data-stu-id="64264-107">**To run the MOF compiler on a file from the command line**</span></span>

1.  <span data-ttu-id="64264-108">Verwenden Sie die folgende Syntax, um den MOF-Compiler von der Befehlszeile aus aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="64264-108">Call the MOF compiler from the command line, using the following syntax.</span></span>

    <span data-ttu-id="64264-109">**MAF Comp** -Datei \*\* \* *. MOF*\*</span><span class="sxs-lookup"><span data-stu-id="64264-109">**mofcomp** *MOFfile\*\*\*.mof*\*</span></span>

    <span data-ttu-id="64264-110">Der MOF-Compiler unterstützt eine Vielzahl von Schaltern, um besondere Verarbeitungs Situationen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="64264-110">The MOF compiler supports a variety of switches to control special processing situations.</span></span> <span data-ttu-id="64264-111">Alle Schalter sind optional, und eine beliebige Kombination von Switches ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="64264-111">All of the switches are optional, and any combination of switches is allowed.</span></span> <span data-ttu-id="64264-112">Es ist jedoch nicht sinnvoll, einige Switches in Kombination mit anderen Switches zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="64264-112">However, it does not make sense to use some of the switches in combination with others.</span></span> <span data-ttu-id="64264-113">Wenn Sie z. b. die Schalter **-Class: updateonly** und **-Class:** |.</span><span class="sxs-lookup"><span data-stu-id="64264-113">For example, to combine the **-class:updateonly** and **-class:createonly** switches results in the compiler not performing any action.</span></span>

    <span data-ttu-id="64264-114">Standardmäßig speichert Mofcomp.exe die kompilierten Klassen im standardmäßigen \\ WMI-Standard Namespace.</span><span class="sxs-lookup"><span data-stu-id="64264-114">By default, Mofcomp.exe stores the compiled classes in the root\\default WMI namespace.</span></span> <span data-ttu-id="64264-115">Beachten Sie, dass der Standard Namespace für Mofcomp.exe nicht mit dem Standard Namespace für die Skripterstellung identisch ist.</span><span class="sxs-lookup"><span data-stu-id="64264-115">Note that the default namespace for Mofcomp.exe is not the same as the default namespace for scripting.</span></span> <span data-ttu-id="64264-116">Der Standard Namespace für die Skripterstellung wird im WMI-Steuerelement auf der Registerkarte Erweitert angegeben. Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="64264-116">The default namespace for scripting is specified in the WMI Control on the Advanced tab. For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

    <span data-ttu-id="64264-117">Sie können den Namespace, der die Klassen empfängt, auf zwei Arten ändern.</span><span class="sxs-lookup"><span data-stu-id="64264-117">You can change the namespace that receives the classes in two ways.</span></span>

    1.  <span data-ttu-id="64264-118">Verwenden Sie den Schalter **-N** für den Befehl " **MUF Comp** ".</span><span class="sxs-lookup"><span data-stu-id="64264-118">Use the **-N** switch for the **mofcomp** command.</span></span>
    2.  <span data-ttu-id="64264-119">Fügen Sie den \# [**pragma-Namespace**](pragma-namespace.md) des Präprozessorbefehls in die MOF-Datei ein.</span><span class="sxs-lookup"><span data-stu-id="64264-119">Insert the preprocessor command \#[**pragma namespace**](pragma-namespace.md) in the MOF file.</span></span>

2.  <span data-ttu-id="64264-120">Optional können Sie eine MOF-Datei Programm gesteuert kompilieren.</span><span class="sxs-lookup"><span data-stu-id="64264-120">Optionally, you can compile a MOF file programmatically.</span></span> <span data-ttu-id="64264-121">Weitere Informationen finden Sie unter [**imuf Compiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span><span class="sxs-lookup"><span data-stu-id="64264-121">For more information, see [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span></span>

## <a name="related-topics"></a><span data-ttu-id="64264-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64264-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64264-123">Kompilieren von MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="64264-123">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="64264-124">**Mofcomp**</span><span class="sxs-lookup"><span data-stu-id="64264-124">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="64264-125">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="64264-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



