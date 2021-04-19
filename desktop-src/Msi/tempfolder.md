---
description: Der Installer legt die TempFolder-Eigenschaft auf den vollständigen Pfad zum temporären Ordner fest. Autoren sollten die TempFolder-Eigenschaft nicht festlegen müssen.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: TempFolder (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359230"
---
# <a name="tempfolder-property"></a><span data-ttu-id="f3db7-103">TempFolder (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f3db7-103">TempFolder property</span></span>

<span data-ttu-id="f3db7-104">Der Installer legt die **TempFolder** -Eigenschaft auf den vollständigen Pfad zum temporären Ordner fest.</span><span class="sxs-lookup"><span data-stu-id="f3db7-104">The installer sets the **TempFolder** property to the full path to the Temp folder.</span></span>

<span data-ttu-id="f3db7-105">Autoren sollten die **TempFolder** -Eigenschaft nicht festlegen müssen.</span><span class="sxs-lookup"><span data-stu-id="f3db7-105">Authors should not need to set the **TempFolder** property.</span></span> <span data-ttu-id="f3db7-106">Windows Installer verwendet die [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) -Funktion, um den Pfad des für temporäre Dateien vorgesehenen Verzeichnisses abzurufen und diese Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f3db7-106">Windows Installer uses the [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files and to set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3db7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3db7-107">Remarks</span></span>

<span data-ttu-id="f3db7-108">Ein allgemeiner Wert für diese Eigenschaft ist C: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="f3db7-108">A common value for this property is C:\\Temp.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3db7-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3db7-109">Requirements</span></span>



| <span data-ttu-id="f3db7-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3db7-110">Requirement</span></span> | <span data-ttu-id="f3db7-111">Wert</span><span class="sxs-lookup"><span data-stu-id="f3db7-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3db7-112">Version</span><span class="sxs-lookup"><span data-stu-id="f3db7-112">Version</span></span><br/> | <span data-ttu-id="f3db7-113">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f3db7-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f3db7-114">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f3db7-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f3db7-115">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f3db7-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f3db7-116">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f3db7-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3db7-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3db7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3db7-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3db7-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 
