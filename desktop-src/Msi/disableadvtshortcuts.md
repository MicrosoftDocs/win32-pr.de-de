---
description: Das Festlegen der disableadvtverknüpfungs-Eigenschaft deaktiviert die Generierung von Verknüpfungen, die Installation bei Bedarf und Ankündigung unterstützen. Durch Festlegen dieser Eigenschaft wird angegeben, dass diese Tastenkombinationen stattdessen durch reguläre Verknüpfungen ersetzt werden sollen.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Disableadvtverknüpfungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360261"
---
# <a name="disableadvtshortcuts-property"></a><span data-ttu-id="b29f3-104">Disableadvtverknüpfungs Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b29f3-104">DISABLEADVTSHORTCUTS property</span></span>

<span data-ttu-id="b29f3-105">Das Festlegen der **disableadvtverknüpfungs** [-Eigenschaft](advertisement.md)deaktiviert die Generierung von Verknüpfungen, die [Installation bei Bedarf](installation-on-demand.md) und Ankündigung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b29f3-105">Setting the **DISABLEADVTSHORTCUTS** property disables the generation of shortcuts supporting [installation-on-demand](installation-on-demand.md) and [advertisement](advertisement.md).</span></span> <span data-ttu-id="b29f3-106">Durch Festlegen dieser Eigenschaft wird angegeben, dass diese Tastenkombinationen stattdessen durch reguläre Verknüpfungen ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b29f3-106">Setting this property specifies that these shortcuts should instead be replaced by regular shortcuts.</span></span>

## <a name="default-value"></a><span data-ttu-id="b29f3-107">Standardwert</span><span class="sxs-lookup"><span data-stu-id="b29f3-107">Default Value</span></span>

<span data-ttu-id="b29f3-108">Standardmäßig ist die Option für die Bedarfs gesteuerte Verknüpfung bei Bedarf aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b29f3-108">By default, installation-on-demand shortcut generation is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="b29f3-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b29f3-109">Remarks</span></span>

<span data-ttu-id="b29f3-110">Die Verknüpfungen, die Ankündigungen unterstützen, haben den Namen eines Features und keinen formatierten Dateipfad der Form " \[ \# filekey" \] , der in der Ziel Spalte der Verknüpfungs [Tabelle](shortcut-table.md)eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b29f3-110">The shortcuts that support advertisement have the name of a feature, rather than a formatted file path of the form \[\#filekey\], entered in the Target column of the [Shortcut table](shortcut-table.md).</span></span> <span data-ttu-id="b29f3-111">Wenn diese Eigenschaft festgelegt ist und die Funktion installiert ist, generiert das Installationsprogramm eine reguläre Verknüpfung mit der Funktion.</span><span class="sxs-lookup"><span data-stu-id="b29f3-111">If this property is set and the feature is installed, the installer generates a regular shortcut to the feature.</span></span>

<span data-ttu-id="b29f3-112">Diese Eigenschaft wird häufig von Administratoren für Benutzer verwendet, die sich zwischen Umgebungen bewegen, von denen keine Werbung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b29f3-112">This property is commonly used by administrators for users who roam between environments that do and do not support advertising.</span></span> <span data-ttu-id="b29f3-113">Diese Eigenschaft kann durch eine Transformation, den administrativen Stream oder in der [Eigenschaften Tabelle](property-table.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b29f3-113">This property can be set by a transform, in the administrative stream, or in the [Property table](property-table.md).</span></span> <span data-ttu-id="b29f3-114">Wenn Sie über die Befehlszeile oder einen [**msisetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)-aufrufstyp festgelegt wird, muss Sie bei jeder nachfolgenden Installation erneut zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="b29f3-114">If it is set using the command line or by a call to [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya), then it must be reset again during each subsequent installation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b29f3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b29f3-115">Requirements</span></span>



| <span data-ttu-id="b29f3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b29f3-116">Requirement</span></span> | <span data-ttu-id="b29f3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="b29f3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b29f3-118">Version</span><span class="sxs-lookup"><span data-stu-id="b29f3-118">Version</span></span><br/> | <span data-ttu-id="b29f3-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b29f3-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b29f3-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b29f3-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b29f3-121">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b29f3-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b29f3-122">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b29f3-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b29f3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b29f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b29f3-124">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b29f3-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




