---
description: Befolgen Sie die allgemeinen Richtlinien zum Anwenden von Mergemodulen, die unter Anwenden von Mergemodulen
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: Anwenden eines konfigurierbaren Mergemoduls mit Anpassungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360220"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a><span data-ttu-id="065fa-103">Anwenden eines konfigurierbaren Mergemoduls mit Anpassungen</span><span class="sxs-lookup"><span data-stu-id="065fa-103">Applying a Configurable Merge Module with Customizations</span></span>

<span data-ttu-id="065fa-104">Befolgen Sie die allgemeinen Richtlinien zum Anwenden von Mergemodulen, die unter [Anwenden von Mergemodulen](applying-merge-modules.md)</span><span class="sxs-lookup"><span data-stu-id="065fa-104">Follow the general guidelines for applying merge modules described in [Applying Merge Modules](applying-merge-modules.md).</span></span> <span data-ttu-id="065fa-105">Außerdem müssen mergemodulconsumer folgende Schritte ausführen, um ein Mergemodul zum Zeitpunkt der Installation zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="065fa-105">In addition, merge module consumers must do the following to configure a merge module at the time of installation:</span></span>

-   <span data-ttu-id="065fa-106">Verwenden Sie ein Mergemodul, das erstellt wurde, um konfigurierbare Einstellungen zu haben.</span><span class="sxs-lookup"><span data-stu-id="065fa-106">Use a merge module that is authored to have configurable settings.</span></span> <span data-ttu-id="065fa-107">Weitere Informationen finden Sie unter [Erstellen eines Mergemoduls, das vom Endbenutzer konfiguriert werden kann](creating-a-merge-module-that-can-be-configured-by-the-end-user.md) .</span><span class="sxs-lookup"><span data-stu-id="065fa-107">For more information, see [Creating a Merge Module that Can Be Configured by the End-User](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)</span></span>
-   <span data-ttu-id="065fa-108">Verwenden Sie ein Merge-und Konfigurationstool, das Mergemod.dll-Version 2,0 oder höher aufruft.</span><span class="sxs-lookup"><span data-stu-id="065fa-108">Use a merge and configuration tool that calls Mergemod.dll version 2.0 or later.</span></span> <span data-ttu-id="065fa-109">In früheren Versionen von Mergmod.dll können die mergemoduleinstellungen nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="065fa-109">Earlier versions of Mergmod.dll cannot configure merge module settings.</span></span> <span data-ttu-id="065fa-110">Autoren sollten Mergemodule erstellen, die Standardwerte bereitstellen und mit früheren Versionen von Mergmod.dll kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="065fa-110">Authors should create merge modules that provide default values and are compatible with earlier versions of Mergmod.dll.</span></span>
-   <span data-ttu-id="065fa-111">Geben Sie Anpassungs Informationen an, wenn Sie vom Konfigurations Client Tool dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="065fa-111">Provide customization information when prompted by the configuration client tool.</span></span> <span data-ttu-id="065fa-112">Autoren sollten Mergemodule erstellen, die Standardwerte verwenden, wenn ein Benutzer die Angabe von Informationen ablehnt.</span><span class="sxs-lookup"><span data-stu-id="065fa-112">Authors should create merge modules that use default values when a user declines to provide information.</span></span>

 

 



