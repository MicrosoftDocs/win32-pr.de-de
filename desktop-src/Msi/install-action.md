---
description: Die Installations Aktion ist eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von Komponenten aufgerufen wird.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Installations Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042096"
---
# <a name="install-action"></a><span data-ttu-id="617fd-103">Installations Aktion</span><span class="sxs-lookup"><span data-stu-id="617fd-103">INSTALL Action</span></span>

<span data-ttu-id="617fd-104">Die Installations Aktion ist eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von Komponenten aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="617fd-104">The INSTALL action is a top-level action called to install or remove components.</span></span> <span data-ttu-id="617fd-105">Mit dieser Aktion werden die Tabelle " [InstallUISequence](installuisequence-table.md) " und die [Tabelle "InstallExecuteSequence](installexecutesequence-table.md) " für die auszuführende Aktion, die Bedingung für die Ausführung der Aktion und die Position der Aktion in der Sequenz abgefragt:</span><span class="sxs-lookup"><span data-stu-id="617fd-105">This action queries the [InstallUISequence Table](installuisequence-table.md) and [InstallExecuteSequence Table](installexecutesequence-table.md) for the action to execute, the condition for action execution, and the place of the action in the sequence:</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="617fd-106">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="617fd-106">Sequence Restrictions</span></span>

<span data-ttu-id="617fd-107">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="617fd-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="617fd-108">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="617fd-108">ActionData Messages</span></span>

<span data-ttu-id="617fd-109">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="617fd-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="617fd-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="617fd-110">Remarks</span></span>

<span data-ttu-id="617fd-111">Die Installations Aktion wird nicht innerhalb der Aktions Tabellen Sequenz aufgerufen, Sie wird an Windows Installer weitergegeben, wenn [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) aufgerufen wird, oder die ausführbare Befehlszeilen Datei Msiexec.exe mit dem Befehls Zeilenschalter '**/i**' aufgerufen wird, oder wenn eine beliebige Installer-Funktion aufgerufen wird, die möglicherweise eine Installationsaufgabe ausführt, z. b. [**msikonfigurirefeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)oder [**msiinstallmissingfile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="617fd-111">The INSTALL action is not called from within the action table sequence, it is passed to Windows Installer when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called, or the command line executable Msiexec.exe is called with the '**/i**' command line switch, or when any installer function is called that may perform an installation task, such as [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta), or [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span>

 

 



