---
description: Sie können das kleine Update auf ein administratives Quell Abbild von MNP2000.msi anwenden, indem Sie das Beispiel Patch MNP2000. msp installieren, das beim Erstellen eines Patchpakets erstellt wurde.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Anwenden eines Patchpakets auf eine administrative Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959536"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a><span data-ttu-id="8ee0a-103">Anwenden eines Patchpakets auf eine administrative Installation</span><span class="sxs-lookup"><span data-stu-id="8ee0a-103">Applying a Patch Package to an Administrative Installation</span></span>

<span data-ttu-id="8ee0a-104">Sie können das kleine Update auf ein administratives Quell Abbild von MNP2000.msi anwenden, indem Sie das Beispiel Patch MNP2000. msp installieren, das beim [Erstellen eines Patchpakets](generating-a-patch-package.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8ee0a-104">You may apply the small update to an administrative source image of MNP2000.msi by installing the sample patch MNP2000.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="8ee0a-105">Das Update kann dann an Benutzer weitergegeben werden, indem angefordert wird, dass die Anwendung erneut aus dem neuen administrativen Quell Image installiert wird.</span><span class="sxs-lookup"><span data-stu-id="8ee0a-105">The update can then be propagated to users by requesting that they reinstall the application from the new administrative source image.</span></span>

<span data-ttu-id="8ee0a-106">Ein Administrator kann die folgende Befehlszeile verwenden, um das administrative Quell Image unter MNP2000.msi//Server/auf ein neues Quell Image zu aktualisieren, das von einer administrativen Installation von einer vollständig aktualisierten CD-ROM erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8ee0a-106">An administrator can use the following command line to update the administrative source image located at //server/MNP2000.msi to a new source image that is the same as would be produced by an administrative installation from a fully updated CD-ROM.</span></span>

<span data-ttu-id="8ee0a-107">**msiexec/a//Server/MNP2000.msi/p MNP2000. msp**</span><span class="sxs-lookup"><span data-stu-id="8ee0a-107">**msiexec /a //server/MNP2000.msi /p MNP2000.msp**</span></span>

<span data-ttu-id="8ee0a-108">Mitglieder der Arbeitsgruppe, die MNP2000 verwendet, müssen dann die Anwendung erneut aus dem neuen administrativen Quell Image installieren, um das Update zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ee0a-108">Members of the workgroup using MNP2000 then must reinstall the application from the new administrative source image to receive the update.</span></span>

<span data-ttu-id="8ee0a-109">Um die Anwendungen vollständig neu zu installieren und die aktualisierte MSI-Datei auf dem Computer des Benutzers zwischenzuspeichern, können Benutzer einen der folgenden Befehle eingeben.</span><span class="sxs-lookup"><span data-stu-id="8ee0a-109">To completely reinstall the applications and cache the updated .msi file on the user's computer, users may enter either of the following commands.</span></span>

<span data-ttu-id="8ee0a-110">**msiexec/fvomus//Server/MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="8ee0a-110">**msiexec /fvomus //server/MNP2000.msi**</span></span>

<span data-ttu-id="8ee0a-111">**msiexec/I//Server/MNP2000.msi REINSTALL = ALL REINSTALLMODE = vomus**</span><span class="sxs-lookup"><span data-stu-id="8ee0a-111">**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**</span></span>

<span data-ttu-id="8ee0a-112">Wenn Sie nur das aktualisierte Konzert Feature neu installieren und die aktualisierte MSI-Datei auf dem Computer des Benutzers zwischenspeichern möchten, können Benutzer den folgenden Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="8ee0a-112">To reinstall only the updated Concert feature and cache the updated .msi file on the user's computer, users may enter the following command.</span></span>

<span data-ttu-id="8ee0a-113">**msiexec/I//Server/MNP2000.msi REINSTALL = Concert REINSTALLMODE = vomus**</span><span class="sxs-lookup"><span data-stu-id="8ee0a-113">**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**</span></span>

## <a name="next-example"></a><span data-ttu-id="8ee0a-114">Nächstes Beispiel</span><span class="sxs-lookup"><span data-stu-id="8ee0a-114">Next example</span></span>

[<span data-ttu-id="8ee0a-115">Beispiel für eine Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="8ee0a-115">A Localization Example</span></span>](a-localization-example.md)

 

 



