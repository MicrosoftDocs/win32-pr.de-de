---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e2673f845d85db88d55cbcd53838f7e682dbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752320"
---
# <a name="d-windows-installer"></a><span data-ttu-id="943fe-103">D (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="943fe-103">D (Windows Installer)</span></span>

<span data-ttu-id="943fe-104">[a](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="943fe-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="943fe-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**Datenbankfunktion**</span><span class="sxs-lookup"><span data-stu-id="943fe-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database function**</span></span>
</dt> <dd>

<span data-ttu-id="943fe-106">Greift auf die Installer-Datenbank zu.</span><span class="sxs-lookup"><span data-stu-id="943fe-106">Accesses the installer database.</span></span> <span data-ttu-id="943fe-107">Diese Funktionen werden in erster Linie für die Verwendung durch [*Installer-Paket*](i-gly.md) Erstellungs Tools bereitgestellt und sind nicht für die Verwendung zum Abrufen von Installations Diensten vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="943fe-107">These functions are provided primarily for use by [*installer package authoring tools*](i-gly.md) and they are not intended to be used to call installer services.</span></span> <span data-ttu-id="943fe-108">Weitere Informationen finden Sie unter [Datenbankfunktionen](database-functions.md) und [installationsfunktions Referenz](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="943fe-108">For more information, see [Database Functions](database-functions.md) and the [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="943fe-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**Daten Bank handle**</span><span class="sxs-lookup"><span data-stu-id="943fe-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**database handle**</span></span>
</dt> <dd>

<span data-ttu-id="943fe-110">Zum Arbeiten mit einer Datenbank erforderlich.</span><span class="sxs-lookup"><span data-stu-id="943fe-110">Required for working with a database.</span></span> <span data-ttu-id="943fe-111">Weitere Informationen finden Sie unter Abrufen [eines Daten Bank Handles](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="943fe-111">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="943fe-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**Delta Patch**</span><span class="sxs-lookup"><span data-stu-id="943fe-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span></span>
</dt> <dd>

<span data-ttu-id="943fe-113">Ein Delta Patch ist ein Delta komprimierter Windows Installer Patch, der mit einem Tool erstellt wird, z. b. Patchwiz.dll, das Delta Komprimierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="943fe-113">A delta patch is a delta-compressed Windows Installer patch created using a tool, such as Patchwiz.dll, that supports delta compression.</span></span> <span data-ttu-id="943fe-114">Patches, die Delta Komprimierung verwenden, können die Größe eines Updates verringern, indem Sie nur die Unterschiede (Delta) zwischen vorhandenen Dateien auf einem Bereitstellungs Zielcomputer und den gewünschten neuen Dateien bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="943fe-114">Patches that use delta compression can reduce the size of an update by providing only the differences (deltas) between existing files on a target computer and the desired new files.</span></span> <span data-ttu-id="943fe-115">Die gewünschten neuen Dateien werden dann aus den vorhandenen Dateien und den heruntergeladenen Delta Dateien synthetisiert.</span><span class="sxs-lookup"><span data-stu-id="943fe-115">The desired new files are then synthesized from the existing files and the downloaded deltas.</span></span> <span data-ttu-id="943fe-116">Weitere Informationen zur Delta Komprimierungs Technologie finden Sie in der [Anwendungsprogrammierschnittstelle für die Delta Komprimierung](https://msdn.microsoft.com/library/ms811406.aspx).</span><span class="sxs-lookup"><span data-stu-id="943fe-116">For more information about delta compression technology, see the [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span></span>

</dd> </dl>

 

 



