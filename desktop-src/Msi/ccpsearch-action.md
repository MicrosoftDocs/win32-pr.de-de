---
description: Die ccpsearch-Aktion verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: Ccpsearch-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b1f01462ac0ba9dcf8838b9a043d95aef8cefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356679"
---
# <a name="ccpsearch-action"></a><span data-ttu-id="99cae-103">Ccpsearch-Aktion</span><span class="sxs-lookup"><span data-stu-id="99cae-103">CCPSearch Action</span></span>

<span data-ttu-id="99cae-104">Die ccpsearch-Aktion verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99cae-104">The CCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="99cae-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="99cae-105">Sequence Restrictions</span></span>

<span data-ttu-id="99cae-106">Die ccpsearch-Aktion sollte in der Tabelle " [InstallUISequence](installuisequence-table.md) " und der [Tabelle "InstallExecuteSequence](installexecutesequence-table.md)" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="99cae-106">CCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="99cae-107">Das Installationsprogramm verhindert, dass die ccpsearch-Aktion in der InstallExecuteSequence-Sequenz ausgeführt wird, wenn die Aktion bereits in der InstallUISequence-Sequenz ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="99cae-107">The installer prevents the CCPSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span> <span data-ttu-id="99cae-108">Die ccpsearch-Aktion muss vor der [RMCCPSEARCH](rmccpsearch-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="99cae-108">The CCPSearch action must come before the [RMCCPSearch](rmccpsearch-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="99cae-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="99cae-109">ActionData Messages</span></span>

<span data-ttu-id="99cae-110">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="99cae-110">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="99cae-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99cae-111">Remarks</span></span>

<span data-ttu-id="99cae-112">Die ccpsearch-Aktion sucht in der folgenden Tabelle nach Datei Signaturen, die in der Tabelle ccpsearch auf dem System aufgeführt sind: Signature, complocator, reglocator, inilocator und drlocator.</span><span class="sxs-lookup"><span data-stu-id="99cae-112">The CCPSearch action searches for file signatures listed in the CCPSearch table on the system using the following tables in order: Signature, CompLocator, RegLocator, IniLocator, and DrLocator.</span></span>

<span data-ttu-id="99cae-113">Wenn eine Signatur als vorhanden festgelegt wird, wird die Eigenschaft **CCP \_ Success** auf 1 festgelegt, und die ccpsearch-Aktion wird beendet.</span><span class="sxs-lookup"><span data-stu-id="99cae-113">If any signature is determined to exist, the **CCP\_Success** property is set to 1 and the CCPSearch action terminates.</span></span>

<span data-ttu-id="99cae-114">Das Fehlen der Signatur aus der Signatur Tabelle deutet auf ein Verzeichnis hin.</span><span class="sxs-lookup"><span data-stu-id="99cae-114">The absence of the signature from the Signature table denotes a directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99cae-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99cae-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99cae-116">Ccpsearch</span><span class="sxs-lookup"><span data-stu-id="99cae-116">CCPSearch</span></span>](ccpsearch-table.md)
</dt> <dt>

[<span data-ttu-id="99cae-117">Signature</span><span class="sxs-lookup"><span data-stu-id="99cae-117">Signature</span></span>](signature-table.md)
</dt> <dt>

[<span data-ttu-id="99cae-118">Complocator</span><span class="sxs-lookup"><span data-stu-id="99cae-118">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="99cae-119">Reglocator</span><span class="sxs-lookup"><span data-stu-id="99cae-119">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="99cae-120">Inilocator</span><span class="sxs-lookup"><span data-stu-id="99cae-120">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="99cae-121">Drlocator</span><span class="sxs-lookup"><span data-stu-id="99cae-121">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



