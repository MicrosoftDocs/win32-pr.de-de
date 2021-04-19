---
description: Das Festlegen der Eigenschaft shortfileames bewirkt, dass kurze Dateinamen für die Namen von Zieldateien anstelle von langen Dateinamen verwendet werden. Dies hat keine Auswirkung auf die Dateinamen, nach denen das Installationsprogramm an der Quelle sucht.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: Shortfile Ames (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362174"
---
# <a name="shortfilenames-property"></a><span data-ttu-id="b032a-104">Shortfile Ames (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b032a-104">SHORTFILENAMES property</span></span>

<span data-ttu-id="b032a-105">Das Festlegen der Eigenschaft **shortfileames** bewirkt, dass kurze Dateinamen für die Namen von Zieldateien anstelle von langen Dateinamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b032a-105">Setting the **SHORTFILENAMES** property causes short file names to be used for the names of target files, rather than long file names.</span></span> <span data-ttu-id="b032a-106">Dies hat keine Auswirkung auf die Dateinamen, nach denen das Installationsprogramm an der Quelle sucht.</span><span class="sxs-lookup"><span data-stu-id="b032a-106">It does not affect the file names the installer looks for at the source.</span></span>

## <a name="default-value"></a><span data-ttu-id="b032a-107">Standardwert</span><span class="sxs-lookup"><span data-stu-id="b032a-107">Default Value</span></span>

<span data-ttu-id="b032a-108">Lange Namen werden vom Installationsprogramm verwendet, wenn die **shortfile Ames** -Eigenschaft nicht festgelegt ist und das Ziel Volume lange Namen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b032a-108">Long names are used by the installer if the **SHORTFILENAMES** property is not set and the target volume supports long names.</span></span> <span data-ttu-id="b032a-109">Kurznamen werden vom Installationsprogramm verwendet, wenn das Ziel Volume keine langen Namen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b032a-109">Short names are used by the installer if the target volume does not support long names.</span></span>

## <a name="remarks"></a><span data-ttu-id="b032a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b032a-110">Remarks</span></span>

<span data-ttu-id="b032a-111">Wenn die **shortfileames** -Eigenschaft festgelegt ist, erstellt das Installationsprogramm Ordner und installiert Dateien mit kurzen Dateinamen aus allen kurzen \| langen Paaren, die in der [Dateitabelle](file-table.md) oder der [Verzeichnis Tabelle](directory-table.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b032a-111">When the **SHORTFILENAMES** property is set, the installer creates folders and installs files using short file names from any short\|long pairs listed in the [File table](file-table.md) or [Directory table](directory-table.md).</span></span>

<span data-ttu-id="b032a-112">Anwendungen können die [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) -Funktion verwenden, um die Kurzpfad Form eines angegebenen Dateipfads abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b032a-112">Applications can use the [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) function to retrieve the short path form of a specified file path.</span></span>

## <a name="requirements"></a><span data-ttu-id="b032a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b032a-113">Requirements</span></span>



| <span data-ttu-id="b032a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b032a-114">Requirement</span></span> | <span data-ttu-id="b032a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b032a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b032a-116">Version</span><span class="sxs-lookup"><span data-stu-id="b032a-116">Version</span></span><br/> | <span data-ttu-id="b032a-117">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b032a-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b032a-118">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b032a-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b032a-119">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b032a-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b032a-120">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b032a-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b032a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b032a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b032a-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b032a-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 
