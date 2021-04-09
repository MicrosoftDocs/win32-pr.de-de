---
description: Die Administrator Aktion ist eine Aktion der obersten Ebene, mit der administrative Installationen durchgeführt werden.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Administrator Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864508"
---
# <a name="admin-action"></a><span data-ttu-id="940dd-103">Administrator Aktion</span><span class="sxs-lookup"><span data-stu-id="940dd-103">ADMIN Action</span></span>

<span data-ttu-id="940dd-104">Die Administrator Aktion ist eine Aktion der obersten Ebene, mit der [administrative Installationen](administrative-installation.md)durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="940dd-104">The ADMIN action is a top-level action used to perform [administrative installations](administrative-installation.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="940dd-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="940dd-105">Sequence Restrictions</span></span>

<span data-ttu-id="940dd-106">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="940dd-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="940dd-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="940dd-107">ActionData Messages</span></span>

<span data-ttu-id="940dd-108">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="940dd-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="940dd-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="940dd-109">Remarks</span></span>

<span data-ttu-id="940dd-110">Die admin-Aktion wird nicht innerhalb der Aktions Tabellen Sequenz aufgerufen, Windows Installer diese Aktion ausführt, wenn [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) mit dem Parameter " *szcommandline* " aufgerufen wird, der auf "action = admin" festgelegt ist, oder die ausführbare Befehlszeilen Datei Msiexec.exe mit dem Befehls Zeilenschalter "/a" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="940dd-110">The ADMIN action is not called from within the action table sequence, Windows Installer executes this action when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to "ACTION=ADMIN" or the command line executable Msiexec.exe is called with the '/a' command line switch.</span></span>

## <a name="related-topics"></a><span data-ttu-id="940dd-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="940dd-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="940dd-112">AdminUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="940dd-112">AdminUISequence Table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="940dd-113">AdminExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="940dd-113">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)
</dt> </dl>

 

 



