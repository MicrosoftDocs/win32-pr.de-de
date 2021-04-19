---
description: Der Ordner "PRIMARYFOLDER" ist eine globale Eigenschaft, die dem Autor das Festlegen eines primären Ordners für die Installation ermöglicht.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: PRIMARYFOLDER (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359290"
---
# <a name="primaryfolder-property"></a><span data-ttu-id="5af89-103">PRIMARYFOLDER (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5af89-103">PRIMARYFOLDER property</span></span>

<span data-ttu-id="5af89-104">Der **Ordner "PRIMARYFOLDER** " ist eine globale Eigenschaft, die dem Autor das Festlegen eines primären Ordners für die Installation ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5af89-104">The **PRIMARYFOLDER** is a global property that allows the author to designate a primary folder for the installation.</span></span> <span data-ttu-id="5af89-105">Der Wert für diese Eigenschaft muss der Schlüssel Name eines Verzeichnisses sein, das in der [Verzeichnis Tabelle](directory-table.md)vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5af89-105">The value for this property must be the key name of a directory that exists in the [Directory table](directory-table.md).</span></span>

<span data-ttu-id="5af89-106">Das Installationsprogramm verwendet den aufgelösten Pfad des primären Ordners, um zu bestimmen, welches Volume beim Festlegen der Werte der Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) , der Eigenschaft [**primaryvolumespaceavailable**](primaryvolumespaceavailable.md) , der Eigenschaft [**primaryvolumespacerequired**](primaryvolumespacerequired.md) und der Eigenschaft [**primaryvolumespaceremainte**](primaryvolumespaceremaining.md) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5af89-106">The installer uses the resolved path of the primary folder to determine which volume to use when setting the values of the [**PrimaryVolumePath**](primaryvolumepath.md) property, [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) property, and [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) property.</span></span> <span data-ttu-id="5af89-107">Das Installationsprogramm stellt den Benutzern in der Benutzeroberfläche die Werte dieser letzteren Eigenschaften zur Verfügung, um Sie bei der Verwaltung des Speicherplatzes zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5af89-107">The installer provides the values of these latter properties to users in the user interface to help them manage disk space.</span></span> <span data-ttu-id="5af89-108">Häufig können Paket Autoren den größten Ordner als primären Ordner auswählen.</span><span class="sxs-lookup"><span data-stu-id="5af89-108">Commonly package authors can select the largest folder as the primary folder.</span></span>

<span data-ttu-id="5af89-109">Der Wert für diese Eigenschaft muss der Schlüssel Name eines Verzeichnis Datensatzes sein, der in der [Verzeichnis Tabelle](directory-table.md)gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="5af89-109">The value for this property must be the key name of a directory record found in the [Directory table](directory-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5af89-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5af89-110">Requirements</span></span>



| <span data-ttu-id="5af89-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5af89-111">Requirement</span></span> | <span data-ttu-id="5af89-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5af89-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af89-113">Version</span><span class="sxs-lookup"><span data-stu-id="5af89-113">Version</span></span><br/> | <span data-ttu-id="5af89-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5af89-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5af89-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5af89-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5af89-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5af89-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5af89-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5af89-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5af89-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5af89-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af89-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5af89-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




