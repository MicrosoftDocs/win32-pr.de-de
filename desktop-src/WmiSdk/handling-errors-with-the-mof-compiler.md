---
description: Wenn der MOF-Compiler die Kompilierung einer MOF-Datei nicht abschließen kann, bleibt das WMI-Repository möglicherweise in einem nicht definierten Zustand.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Behandeln von Fehlern mit dem MOF-Compiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485819"
---
# <a name="handling-errors-with-the-mof-compiler"></a><span data-ttu-id="cea5e-103">Behandeln von Fehlern mit dem MOF-Compiler</span><span class="sxs-lookup"><span data-stu-id="cea5e-103">Handling Errors with the MOF Compiler</span></span>

<span data-ttu-id="cea5e-104">Wenn der MOF-Compiler die Kompilierung einer MOF-Datei nicht abschließen kann, bleibt das WMI-Repository möglicherweise in einem nicht definierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="cea5e-104">If the MOF compiler cannot finish compiling a MOF file, the WMI repository may be left in an undefined state.</span></span> <span data-ttu-id="cea5e-105">Wenn Sie z. b. eine MOF-Datei kompilieren und den Befehls Zeilenschalter **-Class: comateonly** verwenden, wird die Kompilierung beendet, wenn bereits eine in der MOF-Datei angegebene Klasse vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cea5e-105">For example, if you are compiling a MOF file and you use the **-class:createonly** command-line switch, the compilation terminates if a class specified in the MOF file already exists.</span></span> <span data-ttu-id="cea5e-106">Der MOF-Compiler speichert alle Klassen oder Instanzen, die bis zu dem Punkt definiert wurden, an dem der Compiler anhält, im Repository.</span><span class="sxs-lookup"><span data-stu-id="cea5e-106">The MOF compiler stores in the repository any classes or instances that were defined up to the point where the compiler stops.</span></span> <span data-ttu-id="cea5e-107">In einigen Fällen kann dies das WMI-Repository in einem nicht definierten Zustand belassen.</span><span class="sxs-lookup"><span data-stu-id="cea5e-107">In some cases, this can leave the WMI repository in an undefined condition.</span></span>

<span data-ttu-id="cea5e-108">In diesem Fall müssen Sie möglicherweise WMI abbrechen, das WMI-Repository löschen und die WMI-Datei neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cea5e-108">In this situation, you may need to stop WMI, delete the WMI repository, and have WMI rebuild it.</span></span> <span data-ttu-id="cea5e-109">Alle MOF-Dateien, die den [**pragma Auto Wiederherstellen**](pragma-autorecover.md) - [Präprozessorbefehl](preprocessor-commands.md) enthalten, werden neu erstellt, wenn WMI neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="cea5e-109">All MOF files that contain the [**pragma autorecover**](pragma-autorecover.md) [preprocessor command](preprocessor-commands.md) are rebuilt when WMI is restarted.</span></span> <span data-ttu-id="cea5e-110">Sie müssen alle MOF-Dateien, die keine-Anweisung enthalten, manuell neu kompilieren `#pragma autorecover` .</span><span class="sxs-lookup"><span data-stu-id="cea5e-110">You must manually recompile any MOF files that do not include a `#pragma autorecover` statement.</span></span>

<span data-ttu-id="cea5e-111">Weitere Informationen zum Deklarieren von Klassen und Instanzen mithilfe der MOF-Syntax finden Sie unter [Entwerfen von Managed Object Format Klassen (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="cea5e-111">For more information about how to declare classes and instances using the MOF syntax, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cea5e-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cea5e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cea5e-113">Kompilieren von MOF-Dateien</span><span class="sxs-lookup"><span data-stu-id="cea5e-113">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="cea5e-114">**Mofcomp**</span><span class="sxs-lookup"><span data-stu-id="cea5e-114">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="cea5e-115">Präprozessorbefehle</span><span class="sxs-lookup"><span data-stu-id="cea5e-115">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



