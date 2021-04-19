---
description: Die msirmshutdown-Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren werden sollen, um die Installation des Updates zu ermöglichen.
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: Msirmshutdown (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372655"
---
# <a name="msirmshutdown-property"></a><span data-ttu-id="6f41f-103">Msirmshutdown (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6f41f-103">MSIRMSHUTDOWN property</span></span>

<span data-ttu-id="6f41f-104">Die **msirmshutdown** -Eigenschaft bestimmt, wie Anwendungen oder Dienste, die derzeit von einem Update betroffene Dateien verwenden, heruntergefahren werden sollen, um die Installation des Updates zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="6f41f-104">The **MSIRMSHUTDOWN** property determines how applications or services that are currently using files affected by an update should be shut down to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="6f41f-105">Wert</span><span class="sxs-lookup"><span data-stu-id="6f41f-105">Value</span></span>



| <span data-ttu-id="6f41f-106">Wert</span><span class="sxs-lookup"><span data-stu-id="6f41f-106">Value</span></span>                                                                        | <span data-ttu-id="6f41f-107">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6f41f-107">Meaning</span></span>                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f41f-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6f41f-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="6f41f-109">Prozesse oder Dienste, die derzeit vom Update betroffene Dateien verwenden, werden heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="6f41f-109">Processes or services that are currently using files affected by the update are shut down.</span></span><br/>                                                                                                                                                                   |
| <dl> <span data-ttu-id="6f41f-110"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6f41f-110"><dt>1</dt></span></span> </dl> | <span data-ttu-id="6f41f-111">Prozesse oder Dienste, die derzeit Dateien verwenden, die vom Update betroffen sind und die nicht auf den [Neustart-Manager](../rstmgr/restart-manager-portal.md)reagieren, müssen heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="6f41f-111">Processes or services that are currently using files affected by the update, and that do not respond to the [Restart Manager](../rstmgr/restart-manager-portal.md), are forced to shut down.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="6f41f-112"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6f41f-112"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6f41f-113">Prozesse oder Dienste, die derzeit vom Update betroffene Dateien verwenden, werden nur heruntergefahren, wenn Sie für einen Neustart registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="6f41f-113">Processes or services that are currently using files affected by the update are shut down only if they have all been registered for a restart.</span></span> <span data-ttu-id="6f41f-114">Wenn ein Prozess oder Dienst nicht für einen Neustart registriert wurde, werden keine Prozesse oder Dienste heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="6f41f-114">If any process or service has not been registered for a restart, then no processes or services are shut down.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6f41f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f41f-115">Remarks</span></span>

<span data-ttu-id="6f41f-116">Die **msirmshutdown** -Eigenschaft wird ignoriert, wenn der [Neustart-Manager](../rstmgr/restart-manager-portal.md) nicht verfügbar oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6f41f-116">The **MSIRMSHUTDOWN** property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f41f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f41f-117">Requirements</span></span>



| <span data-ttu-id="6f41f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f41f-118">Requirement</span></span> | <span data-ttu-id="6f41f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6f41f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f41f-120">Version</span><span class="sxs-lookup"><span data-stu-id="6f41f-120">Version</span></span><br/> | <span data-ttu-id="6f41f-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6f41f-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6f41f-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6f41f-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6f41f-123">Informationen zu den minimalen Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6f41f-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f41f-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f41f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f41f-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6f41f-125">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="6f41f-126">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f41f-126">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
