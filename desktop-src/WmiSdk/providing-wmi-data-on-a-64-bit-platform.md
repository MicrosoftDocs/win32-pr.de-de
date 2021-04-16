---
description: Skripts und Anwendungen, die für 32-Bit-Betriebssysteme geschrieben wurden, sollten weiterhin ordnungsgemäß ausgeführt werden.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527746"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="cbd6a-103">Bereitstellen von WMI-Daten auf einer 64-Bit-Plattform</span><span class="sxs-lookup"><span data-stu-id="cbd6a-103">Providing WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="cbd6a-104">Skripts und Anwendungen, die für 32-Bit-Betriebssysteme geschrieben wurden, sollten weiterhin ordnungsgemäß ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-104">Scripts and applications written for 32-bit operating systems should continue to run properly.</span></span> <span data-ttu-id="cbd6a-105">Wenn Sie über einen vorhandenen 32-Bit-Anbieter verfügen, können Sie auswerten, ob Sie für eine parallele Operation eine 64-Bit-Version schreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-105">If you have an existing 32-bit provider, you can evaluate whether you need to write a 64-bit version for side-by-side operation.</span></span> <span data-ttu-id="cbd6a-106">Im Allgemeinen sind beide Versionen nicht erforderlich, und die 64-Bit-Version kann sowohl lokale 32-Bit-als auch 64-Bit-und Remote Clients bedienen.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-106">Generally, both versions are not necessary and the 64-bit version can service both 32-bit and 64-bit local or remote clients.</span></span> <span data-ttu-id="cbd6a-107">Verwenden Sie für den 32-Bit-Anwendungs Kompatibilitätsmodus jedoch Ihren vorhandenen 32-Bit-WMI-Anbieter auf einem 64-Bit-System, das im Modus "32-Bit WOW64" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-107">However, for 32-bit application compatibility mode, use your existing 32-bit WMI provider on a 64-bit system that runs in the 32-bit WOW64 mode.</span></span>

<span data-ttu-id="cbd6a-108">In seltenen Fällen müssen sowohl der 32-Bit-als auch der 64-Bit-Anbieter parallel auf 64-Bit-Systemen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-108">In rare situations, both the 32-bit and 64-bit providers must run side-by-side on 64-bit systems.</span></span> <span data-ttu-id="cbd6a-109">In diesem Fall ist die geeignete Version des Anbieters, die geladen wird, davon abhängig, ob der Aufrufer 32-Bit oder 64-Bit und lokal oder Remote ist.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-109">In this case, the appropriate version of provider that is loaded depends on whether the caller is 32-bit or 64-bit and local or remote.</span></span> <span data-ttu-id="cbd6a-110">Ein Aufrufer, der die verbindungsobjektflags " **\_ \_ providerarchitecture** " und "Requirements **\_ \_ darchitecture**" verwendet, kann anfordern, dass WMI einen nicht standardmäßigen Anbieter lädt.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-110">A caller using the connection object context flags, **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture**, can request that WMI load a nondefault provider.</span></span> <span data-ttu-id="cbd6a-111">Weitere Informationen finden Sie unter " [erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)".</span><span class="sxs-lookup"><span data-stu-id="cbd6a-111">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="cbd6a-112">In dem ungewöhnlichen Fall, dass Sie die 32-Bit-und 64-Bit-Anbieter parallel ausführen müssen, müssen Sie sicherstellen, dass die Installations-und Deinstallations Szenarien sorgfältig verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-112">In the unusual case that you must run both the 32-bit and 64-bit providers side-by-side, then you must ensure that install and uninstall scenarios are handled carefully.</span></span> <span data-ttu-id="cbd6a-113">Dies liegt daran, dass WMI nur über ein [*Repository*](gloss-w.md) verfügt und sowohl die 32-Bit-als auch die 64-Bit-Version von [**mofcomp.exe**](mofcomp.md) die Daten im selben Repository ablegen. Es gibt keinen Unterschied zwischen einer 32-Bit-oder einer 64-Bit. MOF-Datei.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-113">This is because WMI has only one [*repository*](gloss-w.md) and both the 32-bit and 64-bit versions of [**mofcomp.exe**](mofcomp.md) put the data in the same repository; there is no distinction between a 32-bit or a 64-bit .mof file.</span></span> <span data-ttu-id="cbd6a-114">Die Neuinstallation einer Version des Anbieters wird nicht beeinträchtigt: die MOF-Dateien werden kompiliert und die Klassen werden im Repository gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-114">Reinstalling one version of the provider will not hurt: the .mof files will be compiled and the classes stored in the repository.</span></span> <span data-ttu-id="cbd6a-115">Eine zweite Deinstallation, die einen Namespace löscht, kann jedoch den Betrieb des anderen Anbieters beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="cbd6a-115">However, a second uninstall that deletes a namespace can interfere with the operation of the other provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbd6a-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cbd6a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbd6a-117">Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer</span><span class="sxs-lookup"><span data-stu-id="cbd6a-117">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[<span data-ttu-id="cbd6a-118">Anfordern von WMI-Daten auf einer 64-Bit-Plattform</span><span class="sxs-lookup"><span data-stu-id="cbd6a-118">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="cbd6a-119">Bereitstellen von Daten für WMI</span><span class="sxs-lookup"><span data-stu-id="cbd6a-119">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> </dl>

 

 



