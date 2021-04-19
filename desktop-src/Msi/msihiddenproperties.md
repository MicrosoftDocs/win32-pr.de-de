---
description: Die msihiddenproperties-Eigenschaft kann verwendet werden, um zu verhindern, dass das Installationsprogramm Kenn Wörter oder andere vertrauliche Informationen in der Protokolldatei anzeigt.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Msihiddenproperties (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355933"
---
# <a name="msihiddenproperties-property"></a><span data-ttu-id="3fd9b-103">Msihiddenproperties (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3fd9b-103">MsiHiddenProperties property</span></span>

<span data-ttu-id="3fd9b-104">Die **msihiddenproperties** -Eigenschaft kann verwendet werden, um zu verhindern, dass das Installationsprogramm Kenn Wörter oder andere vertrauliche Informationen in der Protokolldatei anzeigt.</span><span class="sxs-lookup"><span data-stu-id="3fd9b-104">The **MsiHiddenProperties** property may be used to prevent the installer from displaying passwords or other confidential information in the log file.</span></span> <span data-ttu-id="3fd9b-105">Um zu verhindern, dass eine Eigenschaft in die Protokolldatei geschrieben wird, legen Sie den Wert der Eigenschaft **msihiddenproperties** auf den Namen der Eigenschaft fest, die Sie ausblenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3fd9b-105">To prevent a property from being written into the log file, set the value of the **MsiHiddenProperties** property to the name of the property you wish to hide.</span></span> <span data-ttu-id="3fd9b-106">Sie können mehrere Eigenschaften ausblenden, indem Sie eine Zeichenfolge von Eigenschaften Namen angeben, die durch Semikolons (;) getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="3fd9b-106">You can hide multiple properties by specifying a string of property names delimited by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="3fd9b-107">Wenn die [debugrichtlinie](debug.md) auf den Wert 7 festgelegt ist, schreibt das Installationsprogramm Informationen, die in der Befehlszeile eingegeben werden, in das Protokoll.</span><span class="sxs-lookup"><span data-stu-id="3fd9b-107">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="3fd9b-108">Dadurch werden öffentliche Eigenschaften in einer Befehlszeile sichtbar, auch wenn die Eigenschaft in der **msihiddenproperties** -Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3fd9b-108">This makes public properties entered on a command line visible even if the property is included in the **MsiHiddenProperties** property.</span></span> <span data-ttu-id="3fd9b-109">Dadurch können vertrauliche Informationen in eine Befehlszeile eingegeben werden, die im Protokoll sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="3fd9b-109">This can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="3fd9b-110">Weitere Informationen finden Sie unter [verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="3fd9b-110">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3fd9b-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3fd9b-111">Requirements</span></span>



| <span data-ttu-id="3fd9b-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3fd9b-112">Requirement</span></span> | <span data-ttu-id="3fd9b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3fd9b-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd9b-114">Version</span><span class="sxs-lookup"><span data-stu-id="3fd9b-114">Version</span></span><br/> | <span data-ttu-id="3fd9b-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3fd9b-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3fd9b-116">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3fd9b-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3fd9b-117">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3fd9b-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3fd9b-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd9b-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3fd9b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3fd9b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd9b-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3fd9b-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




