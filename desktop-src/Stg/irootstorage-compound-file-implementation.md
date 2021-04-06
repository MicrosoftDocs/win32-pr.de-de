---
title: Implementierung von irootstorage-Verbund Dateien
description: Die Implementierung der Verbund Datei von com in irootstorage ermöglicht Ihnen das Speichern von Dateien in Situationen mit geringem Arbeitsspeicher oder geringem Speicherplatz. Informationen dazu, wie sich diese Schnittstelle verhält, finden Sie unter irootstorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- Irootstorage-Erweiterung "STG", Implementierung von Verbund Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714568"
---
# <a name="irootstorage---compound-file-implementation"></a><span data-ttu-id="44422-105">Implementierung von irootstorage-Verbund Dateien</span><span class="sxs-lookup"><span data-stu-id="44422-105">IRootStorage - Compound File Implementation</span></span>

<span data-ttu-id="44422-106">Die Implementierung der Verbund Datei von com in [**irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) ermöglicht Ihnen das Speichern von Dateien in Situationen mit geringem Arbeitsspeicher oder geringem Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="44422-106">COM's compound file implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) allows you to support saving files in low-memory or low disk-space situations.</span></span> <span data-ttu-id="44422-107">Informationen dazu, wie sich diese Schnittstelle verhält, finden Sie unter **irootstorage**.</span><span class="sxs-lookup"><span data-stu-id="44422-107">For information on how this interface behaves, see **IRootStorage**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="44422-108">Verwendungs Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="44422-108">When to Use</span></span>

<span data-ttu-id="44422-109">Verwenden Sie die vom System bereitgestellte Implementierung von [**irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) nur, um das Speichern von Dateien unter einem Mangel an Arbeitsspeicher zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="44422-109">Use the system-supplied implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) only to support saving files under low-memory conditions.</span></span>

## <a name="remarks"></a><span data-ttu-id="44422-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44422-110">Remarks</span></span>

<span data-ttu-id="44422-111">Es ist möglich, die com-Implementierung von [**irootstorage:: switchdefile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) aufzurufen, um einen normalen Speicherungs Vorgang in einer anderen Datei durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="44422-111">It is possible to call COM's implementation of [**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) to do a normal save-as operation to another file.</span></span> <span data-ttu-id="44422-112">Anwendungen, die dies tun, sind jedoch möglicherweise nicht mit zukünftigen Generations Generationen des com-Speichers kompatibel.</span><span class="sxs-lookup"><span data-stu-id="44422-112">However, applications that do this might not be compatible with future generations of COM storage.</span></span> <span data-ttu-id="44422-113">Um diese Möglichkeit zu vermeiden, sollten Anwendungen, die einen Save-as-Vorgang ausführen, die zweite Verbund Datei manuell erstellen und [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="44422-113">To avoid this possibility, applications performing a save-as operation should manually create the second compound file and invoke [**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span></span> <span data-ttu-id="44422-114">Die **irootstorage:: switchdefile** -Methode sollte nur in Notfällen (wenig Arbeitsspeicher oder Speicherplatz) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="44422-114">The **IRootStorage::SwitchToFile** method should be used only in emergency (low-memory or disk-space) situations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44422-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44422-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44422-116">**Irootstorage**</span><span class="sxs-lookup"><span data-stu-id="44422-116">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="44422-117">**Irootstorage:: SwitchTo-Datei**</span><span class="sxs-lookup"><span data-stu-id="44422-117">**IRootStorage::SwitchToFile**</span></span>](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




