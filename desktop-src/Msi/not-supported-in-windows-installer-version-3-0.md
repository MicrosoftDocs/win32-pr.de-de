---
description: Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer&\# 160; 3.0 und früheren Versionen nicht unterstützt.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Wird in Windows Installer 3,0 nicht unterstützt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355644"
---
# <a name="not-supported-in-windows-installer-30"></a><span data-ttu-id="43ad2-103">Wird in Windows Installer 3,0 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43ad2-103">Not Supported in Windows Installer 3.0</span></span>

<span data-ttu-id="43ad2-104">Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer 3,0 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43ad2-104">The Windows Installer functions, tables, and properties listed on this page are not supported by Windows Installer 3.0 and earlier versions.</span></span> <span data-ttu-id="43ad2-105">Das Fehlen eines Features aus dieser Liste garantiert nicht, dass das Feature unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="43ad2-105">The absence of a feature from this list does not guarantee that the feature is supported.</span></span> <span data-ttu-id="43ad2-106">In der Haupt Dokumentation finden Sie Informationen dazu, welche Windows Installer Version für eine bestimmte Funktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="43ad2-106">See the main documentation to determine which Windows Installer version is required for a particular feature.</span></span> <span data-ttu-id="43ad2-107">Weitere Informationen zu anderen Windows Installer Versionen finden Sie [unter What es New in Windows Installer](what-s-new-in-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="43ad2-107">For information about other Windows Installer versions see [What's New in Windows Installer](what-s-new-in-windows-installer.md).</span></span>

<span data-ttu-id="43ad2-108">Windows Installer 3,0 ist für Windows Server 2003, Windows XP oder Windows 2000 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43ad2-108">Windows Installer 3.0 is available for Windows Server 2003, Windows XP, or Windows 2000.</span></span> <span data-ttu-id="43ad2-109">Eine Liste aller Windows Installer Versionen und verteilbaren Komponenten finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="43ad2-109">For a list of all Windows Installer versions and redistributables, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

<span data-ttu-id="43ad2-110">Die folgenden Funktionen werden in Windows Installer 3,0 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="43ad2-110">The following features are not supported in Windows Installer 3.0 and earlier versions.</span></span>

[<span data-ttu-id="43ad2-111">Installer-Funktionen</span><span class="sxs-lookup"><span data-stu-id="43ad2-111">Installer Functions</span></span>](installer-functions.md)

-   [<span data-ttu-id="43ad2-112">**Msiseeltexternaluirecord**</span><span class="sxs-lookup"><span data-stu-id="43ad2-112">**MsiSetExternalUIRecord**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [<span data-ttu-id="43ad2-113">**Msinotif ysidchange**</span><span class="sxs-lookup"><span data-stu-id="43ad2-113">**MsiNotifySidChange**</span></span>](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

<span data-ttu-id="43ad2-114">Rückruf Funktionsprototyp</span><span class="sxs-lookup"><span data-stu-id="43ad2-114">Callback Function Prototype</span></span>

-   [<span data-ttu-id="43ad2-115">**installui \_ - \_ handlerdatensatz**</span><span class="sxs-lookup"><span data-stu-id="43ad2-115">**INSTALLUI\_HANDLER\_RECORD**</span></span>](/windows/win32/api/msi/nc-msi-installui_handler_record)

[<span data-ttu-id="43ad2-116">Datenbanktabellen</span><span class="sxs-lookup"><span data-stu-id="43ad2-116">Database Tables</span></span>](database-tables.md)

-   <span data-ttu-id="43ad2-117">In der Value-Spalte der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) werden **OptimizedInstallMode** und **minorupdatetargetrtm** akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="43ad2-117">The Value column of the [MsiPatchMetadata Table](msipatchmetadata-table.md) accepts **OptimizedInstallMode** and **MinorUpdateTargetRTM**.</span></span>

[<span data-ttu-id="43ad2-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43ad2-118">Properties</span></span>](properties.md)

-   [<span data-ttu-id="43ad2-119">**Msix64-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="43ad2-119">**Msix64 Property**</span></span>](msix64.md)

[<span data-ttu-id="43ad2-120">Windows Installer auf 64-Bit-Betriebssystemen</span><span class="sxs-lookup"><span data-stu-id="43ad2-120">Windows Installer on 64-bit Operating Systems</span></span>](windows-installer-on-64-bit-operating-systems.md)

-   <span data-ttu-id="43ad2-121">Die [**Vorlagen Zusammenfassungs Eigenschaft**](template-summary.md) akzeptiert den Wert x64.</span><span class="sxs-lookup"><span data-stu-id="43ad2-121">The [**Template Summary Property**](template-summary.md) accepts the value x64.</span></span>

[<span data-ttu-id="43ad2-122">Interne Konsistenz Auswertung-ICES</span><span class="sxs-lookup"><span data-stu-id="43ad2-122">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

-   [<span data-ttu-id="43ad2-123">ICE99</span><span class="sxs-lookup"><span data-stu-id="43ad2-123">ICE99</span></span>](ice99.md)

 

 
