---
description: 'Wenn sich das Installationspaket, das mit einer Anwendung ausgeliefert wird, nicht im Stammverzeichnis der CD-ROM befindet, die Kunden empfängt, muss die mediapackagepath-Eigenschaft in der Befehlszeile auf den relativen Pfad der Anwendung auf der CD-Rom festgelegt werden. Wenn z. b. der Pfad zum Paket auf dem Medium "E: \\ myPath \\My.msi lautet, verwenden Sie mediapackagepath =&\# 0034; \\ MyPath \\ & \# 0034;. Administratoren können CD-ROMs von einem administrativen Installations Punkt aus erstellen. Wenn der Speicherort des Stamm Verzeichnisses der Installation auf den neuen CD-ROMs geändert wird, muss die mediapackagepath-Eigenschaft auf den neuen Pfad festgelegt werden, der von diesem Medium aus installiert werden soll. Eine Quelle mit einem anderen Speicherort auf der CD-Rom ist nicht verwendbar. Es ist jedoch nicht erforderlich, diese Eigenschaft zu verwenden, wenn Sie einen administrativen Installations Punkt von einem Versand Medium erstellen.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Mediapackagepath (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360896"
---
# <a name="mediapackagepath-property"></a><span data-ttu-id="6a344-106">Mediapackagepath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6a344-106">MEDIAPACKAGEPATH property</span></span>

<span data-ttu-id="6a344-107">Wenn sich das Installationspaket, das mit einer Anwendung ausgeliefert wird, nicht im Stammverzeichnis der CD-ROM befindet, die Kunden empfängt, muss die **mediapackagepath** -Eigenschaft in der Befehlszeile auf den relativen Pfad der Anwendung auf der CD-Rom festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6a344-107">If the installation package shipping with an application is not at the root of the CD-ROM that customers receive, the **MEDIAPACKAGEPATH** property must be set on the command line to the relative path of the application on the CD-ROM.</span></span>

<span data-ttu-id="6a344-108">Wenn z. b. der Pfad zum Paket auf dem Medium "E: \\ myPath \\My.msi lautet, verwenden Sie mediapackagepath =" \\ myPath \\ ".</span><span class="sxs-lookup"><span data-stu-id="6a344-108">For example, if the path to the package on the media is E:\\MyPath\\My.msi, then use MEDIAPACKAGEPATH="\\MyPath\\".</span></span>

<span data-ttu-id="6a344-109">Administratoren können CD-ROMs von einem administrativen Installations Punkt aus erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a344-109">Administrators may create CD-ROMs from an administrative installation point.</span></span> <span data-ttu-id="6a344-110">Wenn der Speicherort des Stamm Verzeichnisses der Installation auf den neuen CD-ROMs geändert wird, muss die **mediapackagepath** -Eigenschaft auf den neuen Pfad festgelegt werden, der von diesem Medium aus installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a344-110">If the location of the root of the installation is changed on the new CD-ROMs, the **MEDIAPACKAGEPATH** property must be set to the new path to install from this media.</span></span> <span data-ttu-id="6a344-111">Eine Quelle mit einem anderen Speicherort auf der CD-Rom ist nicht verwendbar.</span><span class="sxs-lookup"><span data-stu-id="6a344-111">A source with a location on the CD-ROM different than what is specified in the package is unusable.</span></span> <span data-ttu-id="6a344-112">Es ist jedoch nicht erforderlich, diese Eigenschaft zu verwenden, wenn Sie einen administrativen Installations Punkt von einem Versand Medium erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a344-112">It is not necessary, however, to use this property when creating an administrative installation point from shipping media.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a344-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a344-113">Requirements</span></span>



| <span data-ttu-id="6a344-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a344-114">Requirement</span></span> | <span data-ttu-id="6a344-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6a344-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a344-116">Version</span><span class="sxs-lookup"><span data-stu-id="6a344-116">Version</span></span><br/> | <span data-ttu-id="6a344-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6a344-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6a344-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6a344-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6a344-119">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6a344-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6a344-120">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6a344-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a344-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a344-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a344-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6a344-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




