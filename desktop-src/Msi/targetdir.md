---
description: Die TARGETDIR-Eigenschaft gibt das Stammverzeichnis für die Installation an.
ms.assetid: 279bb9ad-afb6-406e-b74a-8424da177e6f
title: TARGETDIR-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d5e2650dab798c1f6b9e766fc1dcbb61dcfa77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368626"
---
# <a name="targetdir-property"></a><span data-ttu-id="b2a8a-103">TARGETDIR-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2a8a-103">TARGETDIR property</span></span>

<span data-ttu-id="b2a8a-104">Die **TARGETDIR** -Eigenschaft gibt das Stammverzeichnis für die Installation an.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-104">The **TARGETDIR** property specifies the root destination directory for the installation.</span></span> <span data-ttu-id="b2a8a-105">**TARGETDIR** muss der Name eines Stamms in der [Verzeichnis](directory-table.md) Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-105">**TARGETDIR** must be the name of one root in the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="b2a8a-106">Möglicherweise gibt es nur ein einzelnes Stammverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-106">There may be only a single root destination directory.</span></span> <span data-ttu-id="b2a8a-107">Bei einer [administrativen Installation](administrative-installation.md) gibt diese Eigenschaft den Speicherort für das Kopieren des Installationspakets an.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-107">During an [administrative installation](administrative-installation.md) this property specifies the location to copy the installation package.</span></span> <span data-ttu-id="b2a8a-108">Bei einer nicht administrativen Installation gibt diese Eigenschaft das Stammverzeichnis für das Ziel an.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-108">During a non-administrative installation this property specifies the root destination directory.</span></span>

<span data-ttu-id="b2a8a-109">Zum Angeben des Stammverzeichnis Verzeichnisses legen Sie die Verzeichnis Spalte der Verzeichnis Tabelle auf die **TARGETDIR** -Eigenschaft und die DefaultDir-Spalte auf die [**SourceDir**](sourcedir.md) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-109">To specify the root destination directory, set the Directory column of the Directory table to the **TARGETDIR** property and the DefaultDir column to the [**SourceDir**](sourcedir.md) property.</span></span> <span data-ttu-id="b2a8a-110">Wenn die Eigenschaft **TARGETDIR** definiert ist, wird das Zielverzeichnis in den Wert der Eigenschaft aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-110">If the **TARGETDIR** property is defined, the destination directory is resolved to the property's value.</span></span> <span data-ttu-id="b2a8a-111">Wenn die **TARGETDIR** -Eigenschaft nicht definiert ist, wird der Pfad mithilfe der [**ROOTDRIVE**](rootdrive.md) -Eigenschaft aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-111">If the **TARGETDIR** property is undefined, the [**ROOTDRIVE**](rootdrive.md) property is used to resolve the path.</span></span> <span data-ttu-id="b2a8a-112">Weitere Informationen zur Verwendung der **TARGETDIR** -Eigenschaft finden Sie unter [Verwenden der Verzeichnis Tabelle](using-the-directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="b2a8a-112">For more information about using the **TARGETDIR** property, see [Using the Directory Table](using-the-directory-table.md).</span></span>

<span data-ttu-id="b2a8a-113">Beachten Sie, dass der Wert der **TARGETDIR** -Eigenschaft in der Regel in der Befehlszeile oder über eine Benutzeroberfläche festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-113">Note that the value of the **TARGETDIR** property is typically set at the command line or through a user interface.</span></span> <span data-ttu-id="b2a8a-114">Es wird nicht empfohlen, **TARGETDIR** durch das Erstellen eines Pfads in die [Eigenschaften Tabelle](property-table.md) festzulegen, da die Computer sich in der Einrichtung des lokalen Laufwerks unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-114">Setting **TARGETDIR** by authoring a path into the [Property table](property-table.md) is not recommended because computers differ in the set up of the local drive.</span></span>

<span data-ttu-id="b2a8a-115">Weitere Informationen zum Ändern von TARGETDIR während einer Installation finden Sie unter [Ändern des Zielspeicher Orts für ein Verzeichnis](changing-the-target-location-for-a-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="b2a8a-115">For more information on how to change TARGETDIR during an installation see [Changing the Target Location for a Directory](changing-the-target-location-for-a-directory.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="b2a8a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2a8a-116">Requirements</span></span>



| <span data-ttu-id="b2a8a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2a8a-117">Requirement</span></span> | <span data-ttu-id="b2a8a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b2a8a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a8a-119">Version</span><span class="sxs-lookup"><span data-stu-id="b2a8a-119">Version</span></span><br/> | <span data-ttu-id="b2a8a-120">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b2a8a-121">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b2a8a-122">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2a8a-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b2a8a-123">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b2a8a-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2a8a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2a8a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a8a-125">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2a8a-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




