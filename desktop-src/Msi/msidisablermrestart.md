---
description: Die msidisablermrestart-Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren und neu gestartet werden müssen, um die Installation des Updates zu ermöglichen.
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: Msidisablermrestart (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368483"
---
# <a name="msidisablermrestart-property"></a><span data-ttu-id="ece44-103">Msidisablermrestart (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ece44-103">MSIDISABLERMRESTART property</span></span>

<span data-ttu-id="ece44-104">Die **msidisablermrestart** -Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren und neu gestartet werden müssen, um die Installation des Updates zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ece44-104">The **MSIDISABLERMRESTART** property determines how applications or services that are currently using files affected by an update should be shut down and restarted to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="ece44-105">Wert</span><span class="sxs-lookup"><span data-stu-id="ece44-105">Value</span></span>



| <span data-ttu-id="ece44-106">Wert</span><span class="sxs-lookup"><span data-stu-id="ece44-106">Value</span></span>                                                                        | <span data-ttu-id="ece44-107">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ece44-107">Meaning</span></span>                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ece44-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ece44-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="ece44-109">Alle Systemdienste, die zur Installation des Updates heruntergefahren wurden, werden neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="ece44-109">All system services that were shut down to install the update are restarted.</span></span> <span data-ttu-id="ece44-110">Alle Anwendungen, die sich mit dem [Neustart-Manager](../rstmgr/restart-manager-portal.md) registriert haben, werden neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="ece44-110">All applications that registered themselves with the [Restart Manager](../rstmgr/restart-manager-portal.md) are restarted.</span></span><br/> |
| <dl> <span data-ttu-id="ece44-111"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ece44-111"><dt>1</dt></span></span> </dl> | <span data-ttu-id="ece44-112">Prozesse, die mit dem Neustart- [Manager](../rstmgr/restart-manager-portal.md) während der Installation des Updates heruntergefahren wurden, werden nach dem Anwenden des Updates nicht neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="ece44-112">Processes that were shut down using the [Restart Manager](../rstmgr/restart-manager-portal.md) while installing the update will not be restarted after the update is applied.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="ece44-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ece44-113">Remarks</span></span>

<span data-ttu-id="ece44-114">Die **msidisablermrestart** -Eigenschaft wird ignoriert, wenn der [Neustart-Manager](../rstmgr/restart-manager-portal.md) nicht verfügbar oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ece44-114">The **MSIDISABLERMRESTART** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="ece44-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ece44-115">Requirements</span></span>



| <span data-ttu-id="ece44-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ece44-116">Requirement</span></span> | <span data-ttu-id="ece44-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ece44-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ece44-118">Version</span><span class="sxs-lookup"><span data-stu-id="ece44-118">Version</span></span><br/> | <span data-ttu-id="ece44-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ece44-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ece44-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ece44-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ece44-121">Informationen zu den minimalen Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ece44-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ece44-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ece44-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece44-123">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ece44-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ece44-124">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ece44-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
