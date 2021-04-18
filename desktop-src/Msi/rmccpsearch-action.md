---
description: Die RMCCPSEARCH-Aktion verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: RMCCPSEARCH-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343773"
---
# <a name="rmccpsearch-action"></a><span data-ttu-id="eaa76-103">RMCCPSEARCH-Aktion</span><span class="sxs-lookup"><span data-stu-id="eaa76-103">RMCCPSearch Action</span></span>

<span data-ttu-id="eaa76-104">Die RMCCPSEARCH-Aktion verwendet Datei Signaturen, um zu überprüfen, ob qualifizierte Produkte auf einem System installiert sind, bevor eine Upgrade-Installation durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eaa76-104">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="eaa76-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="eaa76-105">Sequence Restrictions</span></span>

<span data-ttu-id="eaa76-106">Die RMCCPSEARCH-Aktion sollte in der Tabelle " [InstallUISequence](installuisequence-table.md) " und der [Tabelle "InstallExecuteSequence](installexecutesequence-table.md)" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eaa76-106">RMCCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="eaa76-107">Das Installationsprogramm verhindert, dass RMCCPSEARCH in der InstallExecuteSequence-Sequenz ausgeführt wird, wenn die Aktion bereits in der InstallUISequence-Sequenz ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="eaa76-107">The installer prevents RMCCPSearch from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="eaa76-108">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="eaa76-108">ActionData Messages</span></span>

<span data-ttu-id="eaa76-109">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="eaa76-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaa76-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eaa76-110">Remarks</span></span>

<span data-ttu-id="eaa76-111">Die RMCCPSEARCH-Aktion erfordert [*, dass die*](v-gly.md) Eigenschaft des [**CCP- \_ Laufwerks**](ccp-drive.md) auf den Stammpfad auf dem Wechsel Datenträger festgelegt wird, der über die Installation der qualifizierenden Produkte verfügt.</span><span class="sxs-lookup"><span data-stu-id="eaa76-111">The RMCCPSearch action requires the [**CCP\_DRIVE**](ccp-drive.md) property to be set to the root path on the removable [*volume*](v-gly.md) that has the installation for any of the qualifying products.</span></span>

<span data-ttu-id="eaa76-112">Jede Datei Signatur in der ccpsearch-Tabelle wird unter dem Pfad gesucht, auf den die Eigenschaft des [**CCP- \_ Laufwerks**](ccp-drive.md) mithilfe der [drlocator](drlocator-table.md) -Tabelle verweist.</span><span class="sxs-lookup"><span data-stu-id="eaa76-112">Each file signature in the CCPSearch table is searched for under the path referred to by the [**CCP\_DRIVE**](ccp-drive.md) property using the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="eaa76-113">Das Fehlen der Signatur aus der [Signatur](signature-table.md) Tabelle deutet auf ein Verzeichnis hin.</span><span class="sxs-lookup"><span data-stu-id="eaa76-113">The absence of the signature from the [Signature](signature-table.md) table denotes a directory.</span></span> <span data-ttu-id="eaa76-114">Wenn eine Signatur so bestimmt ist, dass Sie vorhanden ist, wird die RMCCPSEARCH-Aktion beendet.</span><span class="sxs-lookup"><span data-stu-id="eaa76-114">If any signature is determined to exist, the RMCCPSearch action terminates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaa76-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eaa76-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaa76-116">Ccpsearch-Tabelle</span><span class="sxs-lookup"><span data-stu-id="eaa76-116">CCPSearch table</span></span>](ccpsearch-table.md)
</dt> </dl>

 

 



