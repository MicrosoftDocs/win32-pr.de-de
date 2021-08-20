---
description: Die Version von PATCHWIZ.DLL, die mit Windows Installer&\# 160;3.0 veröffentlicht wurde, kann automatisch Patchsequenzierungsinformationen generieren und der MsiPatchSequence-Tabelle einen neuen Patch hinzufügen.
ms.assetid: 03e7eea6-1a37-4c86-a9da-109fbaf20728
title: Generieren von Patchsequenzinformationen (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03094d9df26f4565db5b3a31c9a27c58a0bb45dac8aac93b2fefce34104d58c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947021"
---
# <a name="generating-patch-sequence-information-patchwizdll"></a>Generieren von Patchsequenzinformationen (PATCHWIZ.DLL)

Die mit Windows Installer 3.0 veröffentlichte Version von [PATCHWIZ.DLL](patchwiz-dll.md) kann automatisch Patchsequenzierungsinformationen generieren und der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) einen neuen Patch hinzufügen.

Legen Sie die \_ SEQUENCE DATA \_ GENERATION \_ DISABLED-Eigenschaft in der [Eigenschaftentabelle](properties-table-patchwiz-dll-.md) der PCP-Datei auf 1 (eins) fest, um die automatische Generierung von Patchsequenzierungsinformationen zu verhindern. Wenn diese Eigenschaft nicht vorhanden ist, werden die Informationen automatisch generiert und hinzugefügt.

Wenn die mit Windows Installer 3.0 freigegebene [PATCHWIZ.DLL](patchwiz-dll.md) verwendet wird, um die Patchsequenzierungsinformationen automatisch zu generieren, geschieht Folgendes:

-   Der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) wird für jeden Produktcode eines Zielimages, das in der [Tabelle TargetImages](targetimages-table-patchwiz-dll-.md)aufgeführt ist, eine neue Zeile hinzugefügt.
-   Die Werte, die der Spalte PatchFamily in den neuen Zeilen hinzugefügt werden, entsprechen den Zielproduktcodes der Zielimages, die in der [Tabelle TargetImages](targetimages-table-patchwiz-dll-.md)aufgeführt sind.
-   Die Werte, die den Sequenzspalten in den neuen Zeilen hinzugefügt werden, werden mit der höchsten Produktversion generiert, auf die der Patch abzielt, und der UTC-Zeit, zu der der Patch generiert wird. Die Sequenznummer ist <Product Minor Version> <Build Major Number> . <Zeitstempel 1>.<Zeitstempel 2>.
    -   Das erste Feld ist die Produktversion der höchsten Version des Produkts, für das der Patch gilt.
    -   Das zweite Feld ist die Build-Hauptnummer der höchsten Version des Produkts, für das der Patch gilt.

    Die beiden Zeitstempelfelder berücksichtigen den 32-Bit-Zeitstempel, der zum Zählen der Sekunden in koordinierte Weltzeit (UTC) benötigt wird.
    > [!Note]  
    > Produktversionen weisen das folgende Format auf: <Product Major Version> . . Und ein Produkt mit der <Product Minor Version> <Build Major Number> <Build Minor Number> Versionsnummer 2.1.0.0 ist eine höhere Version als ein Produkt mit der Versionsnummer 1.2.0.0.

     

-   Das msidbPatchSequenceSupersedeEarlier-Attribut wird in die Spalte Attribute der neuen Zeilen eingegeben, die für Service Packs (SP) oder kleinere Upgradepatches generiert werden. Das msidbPatchSequenceSupersedeEarlier-Attribut wird keinem QFE- oder kleinen Updatepatch hinzugefügt.
    > [!Note]  
    > Ein Service Pack (SP) sollte die Fixes aller EQEs enthalten, die zuvor veröffentlicht wurden. Wenn jedoch ein Patchautor die SEQUENCE \_ DATA \_ SUPERSEDENCE-Eigenschaft in der PCP-Datei auf 0 (null) oder 1 (eins) festlegt, wird die Attributes-Spalte aller Zeilen in der MsiPatchSequence-Tabelle auf den Wert festgelegt, der für SEQUENCE \_ DATA \_ SUPERSEDENCE angegeben ist. Patchautoren, die mehr Kontrolle benötigen, müssen die Spalte Attribute manuell erstellen.

     

Wenn Sie eine [PatchSequence-Tabelle](patchsequence-table--patchwiz-dll-.md) in die PCP-Datei einschließen, wird die \_ SEQUENCE DATA GENERATION \_ \_ DISABLED-Eigenschaft ignoriert, und die in der PatchSequence-Tabelle bereitgestellten Informationen können der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) des Patches hinzugefügt werden.

 

 



