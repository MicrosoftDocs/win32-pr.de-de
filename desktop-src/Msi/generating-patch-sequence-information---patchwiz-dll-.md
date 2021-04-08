---
description: Die Version von PATCHWIZ.DLL, die mit Windows Installer&\# 160; 3.0 veröffentlicht wurde, kann automatisch patchsequenzierungs Informationen generieren und der msipatchsequence-Tabelle einen neuen Patch hinzufügen.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Erstellen von Patchsequenzinformationen (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff82166f33266a58cd3ef299b2546b04a94ebb14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960048"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a><span data-ttu-id="1d3a0-103">Erstellen von Patchsequenzinformationen (PATCHWIZ.DLL)</span><span class="sxs-lookup"><span data-stu-id="1d3a0-103">Generating Patch Sequence Information (PATCHWIZ.DLL)</span></span>

<span data-ttu-id="1d3a0-104">Die mit Windows Installer 3,0 veröffentlichte Version von [PATCHWIZ.DLL](patchwiz-dll.md) kann automatisch Informationen zur Patchsequenzierung generieren und der [msipatchsequence-Tabelle](msipatchsequence-table.md) einen neuen Patch hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-104">The version of [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 can automatically generate patch sequencing information and add to the [MsiPatchSequence Table](msipatchsequence-table.md) a new patch.</span></span>

<span data-ttu-id="1d3a0-105">Legen Sie die \_ Eigenschaft sequence data \_ Generation \_ deaktiviert auf 1 (eins) in der [Properties-Tabelle](properties-table-patchwiz-dll-.md) der PCP-Datei fest, um die automatische Generierung von Informationen zur Patchsequenzierung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-105">Set the SEQUENCE\_DATA\_GENERATION\_DISABLED property to 1 (one) in the [Properties Table](properties-table-patchwiz-dll-.md) of the .pcp file to prevent the automatic generation of patch sequencing information.</span></span> <span data-ttu-id="1d3a0-106">Wenn diese Eigenschaft nicht vorhanden ist, werden die Informationen automatisch generiert und hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-106">If this property is absent, the information is automatically generated and added.</span></span>

<span data-ttu-id="1d3a0-107">Wenn die mit Windows Installer 3,0 freigegebene [PATCHWIZ.DLL](patchwiz-dll.md) zum automatischen Generieren der patchsequenzierungs Informationen verwendet wird, geschieht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1d3a0-107">When the [PATCHWIZ.DLL](patchwiz-dll.md) released with Windows Installer 3.0 is used to automatically generate the patch sequencing information, the following occurs:</span></span>

-   <span data-ttu-id="1d3a0-108">Der [msipatchsequence-Tabelle](msipatchsequence-table.md) wird für jeden Produktcode eines zielbilds, das in der [TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md)aufgelistet ist, eine neue Zeile hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-108">A new row is added to the [MsiPatchSequence Table](msipatchsequence-table.md) for each product code of a target image that is listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="1d3a0-109">Die Werte, die der Spalte patchfamily in den neuen Zeilen hinzugefügt werden, entsprechen den Ziel Produktcodes der Ziel Images, die in der [Tabelle TargetImages](targetimages-table-patchwiz-dll-.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-109">The values added to the PatchFamily column in the new rows correspond to the target product codes of the target images that are listed in the [TargetImages Table](targetimages-table-patchwiz-dll-.md).</span></span>
-   <span data-ttu-id="1d3a0-110">Die Werte, die den Sequenz Spalten in den neuen Zeilen hinzugefügt werden, werden mit der höchsten Produktversion, auf die der Patch abzielt, und der UTC-Zeit, zu der der Patch generiert wird, generiert.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-110">The values added to the Sequence columns in the new rows are generated using the highest product version targeted by the patch and the UTC time when the patch is generated.</span></span> <span data-ttu-id="1d3a0-111">Die Sequenznummer ist <Product Minor Version> . <Build Major Number> . <Zeitstempel 1>. <Zeitstempel 2>.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-111">The sequence number is <Product Minor Version>.<Build Major Number>.<Time Stamp 1>.<Time Stamp 2>.</span></span>
    -   <span data-ttu-id="1d3a0-112">Das erste Feld ist die Produktversion der höchsten Version des Produkts, das den Patch als Ziel hat.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-112">The first field is the product version of the highest version of the product that is targeted by the patch.</span></span>
    -   <span data-ttu-id="1d3a0-113">Das zweite Feld ist die buildhauptnummer der höchsten Version des Produkts, das den Patch als Ziel hat.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-113">The second field is the build major number of the highest version of the product that is targeted by the patch.</span></span>

    <span data-ttu-id="1d3a0-114">Die zwei Zeitstempel Felder für den 32-Bit-Zeitstempel, der zum zählen der Sekunden in koordinierter Weltzeit (UTC) benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-114">The two time stamp fields account for the 32 bit time stamp that is needed to count the seconds in Coordinated Universal Time (UTC).</span></span>
    > [!Note]  
    > <span data-ttu-id="1d3a0-115">Produktversionen haben das folgende Format: <Product Major Version> . <Product Minor Version> . <Build Major Number> . <Build Minor Number> und ein Produkt mit der Versionsnummer 2.1.0.0 ist eine höhere Version als ein Produkt mit der Versionsnummer 1.2.0.0</span><span class="sxs-lookup"><span data-stu-id="1d3a0-115">Product versions have the following format: <Product Major Version>.<Product Minor Version>.<Build Major Number>.<Build Minor Number> and a product with a version number 2.1.0.0 is a higher version than a product with version number 1.2.0.0</span></span>

     

-   <span data-ttu-id="1d3a0-116">Das msidbpatchsequencesupersedefrühere-Attribut wird in die Attribut Spalte neuer Zeilen eingegeben, die für Service Packs (SP) oder kleinere Upgradepatches generiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-116">The msidbPatchSequenceSupersedeEarlier attribute is entered into the Attribute column of new rows that are generated for service packs (SP) or minor upgrade patches.</span></span> <span data-ttu-id="1d3a0-117">Das msidbpatchsequencesupersedebug-Attribut wurde keinem QFE-oder Small Update-Patch hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-117">The msidbPatchSequenceSupersedeEarlier attribute is not added to a QFE or small update patch.</span></span>
    > [!Note]  
    > <span data-ttu-id="1d3a0-118">Eine Service Pack (SP) sollte die Korrekturen aller QFEs enthalten, die vor der Veröffentlichung veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-118">A service pack (SP) should contain the fixes of all the QFEs that were released prior to it.</span></span> <span data-ttu-id="1d3a0-119">Wenn ein Patch-Autor jedoch die Eigenschaft Sequenz \_ Daten \_ Ablösung auf 0 (null) oder 1 (eins) in der PCP-Datei festlegt, wird die Spalte Attribute aller Zeilen in der Tabelle msipatchsequence auf den Wert festgelegt, der für die Sequenz \_ Daten Ablösung angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="1d3a0-119">However, if a patch author sets the SEQUENCE\_DATA\_SUPERSEDENCE property to 0 (zero) or 1 (one) in the .pcp file, the Attributes column of all rows in the MsiPatchSequence table is set to the value that is specified for SEQUENCE\_DATA\_SUPERSEDENCE.</span></span> <span data-ttu-id="1d3a0-120">Patchautoren, die mehr Kontrolle benötigen, müssen die Attribut Spalte manuell erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-120">Patch authors who require more control must author the Attributes column manually.</span></span>

     

<span data-ttu-id="1d3a0-121">Wenn Sie in die PCP-Datei eine [patchsequence-Tabelle](patchsequence-table--patchwiz-dll-.md) einschließen, \_ wird die Eigenschaft Sequenzdaten \_ Generierung \_ deaktiviert ignoriert, und die in der Tabelle patchsequence bereitgestellten Informationen können der [msipatchsequence-Tabelle](msipatchsequence-table.md) des Patches hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1d3a0-121">If you include a [PatchSequence Table](patchsequence-table--patchwiz-dll-.md) in the .pcp file, the SEQUENCE\_DATA\_GENERATION\_DISABLED property is ignored and the information provided in the PatchSequence Table can be added to the [MsiPatchSequence Table](msipatchsequence-table.md) of the patch.</span></span>

 

 



