---
description: Die Aktion ankündigen ist eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von angekündigten Komponenten aufgerufen wird.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Aktion ankündigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756246"
---
# <a name="advertise-action"></a><span data-ttu-id="ef121-103">Aktion ankündigen</span><span class="sxs-lookup"><span data-stu-id="ef121-103">ADVERTISE Action</span></span>

<span data-ttu-id="ef121-104">Die Aktion ankündigen ist eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von angekündigten Komponenten aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ef121-104">The ADVERTISE action is a top-level action called to install or remove advertised components.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ef121-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="ef121-105">Sequence Restrictions</span></span>

<span data-ttu-id="ef121-106">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="ef121-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ef121-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="ef121-107">ActionData Messages</span></span>

<span data-ttu-id="ef121-108">Es sind keine Aktions Daten Meldungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ef121-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef121-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef121-109">Remarks</span></span>

<span data-ttu-id="ef121-110">[*Werbung*](a-gly.md) bezieht sich auf die Fähigkeit des Installers, die Lade-und Start Schnittstellen einer Anwendung bereitzustellen, ohne die Anwendung physisch zu installieren.</span><span class="sxs-lookup"><span data-stu-id="ef121-110">[*Advertising*](a-gly.md) refers to the installer's ability to provide the loading and launching interfaces of an application without physically installing the application.</span></span> <span data-ttu-id="ef121-111">Der Installer installiert die erforderlichen Komponenten erst, wenn ein Benutzer oder eine Anwendung eine angekündigte Benutzeroberfläche aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ef121-111">The installer does not install the necessary components until a user or application activates an advertised interface.</span></span> <span data-ttu-id="ef121-112">Dieses Konzept wird als [*install-on-Demand*](i-gly.md)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ef121-112">This concept is called [*install-on-demand*](i-gly.md).</span></span>

<span data-ttu-id="ef121-113">Die Ankündigungs Aktion wird nicht innerhalb der Aktions Tabellen Sequenz aufgerufen. die Windows Installer führt diese Aktion aus, wenn die ausführbare Befehlszeilen Datei Msiexec.exe mit dem Befehls Zeilenschalter '/j ' aufgerufen wird oder wenn ' [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ' aufgerufen wird, wobei der *szcommandline* -Parameter auf Action = Ankündigungs Wert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ef121-113">The ADVERTISE action is not called from within the action table sequence, the Windows Installer executes this action when the command line executable Msiexec.exe is called with the '/j' command line switch or when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to ACTION=ADVERTISE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef121-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef121-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef121-115">AdvtExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="ef121-115">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)
</dt> </dl>

 

 



