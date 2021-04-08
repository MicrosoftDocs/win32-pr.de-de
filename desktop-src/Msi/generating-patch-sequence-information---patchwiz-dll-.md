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
# <a name="generating-patch-sequence-information-patchwizdll"></a>Erstellen von Patchsequenzinformationen (PATCHWIZ.DLL)

Die mit Windows Installer 3,0 veröffentlichte Version von [PATCHWIZ.DLL](patchwiz-dll.md) kann automatisch Informationen zur Patchsequenzierung generieren und der [msipatchsequence-Tabelle](msipatchsequence-table.md) einen neuen Patch hinzufügen.

Legen Sie die \_ Eigenschaft sequence data \_ Generation \_ deaktiviert auf 1 (eins) in der [Properties-Tabelle](properties-table-patchwiz-dll-.md) der PCP-Datei fest, um die automatische Generierung von Informationen zur Patchsequenzierung zu verhindern. Wenn diese Eigenschaft nicht vorhanden ist, werden die Informationen automatisch generiert und hinzugefügt.

Wenn die mit Windows Installer 3,0 freigegebene [PATCHWIZ.DLL](patchwiz-dll.md) zum automatischen Generieren der patchsequenzierungs Informationen verwendet wird, geschieht Folgendes:

-   Der [msipatchsequence-Tabelle](msipatchsequence-table.md) wird für jeden Produktcode eines zielbilds, das in der [TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md)aufgelistet ist, eine neue Zeile hinzugefügt.
-   Die Werte, die der Spalte patchfamily in den neuen Zeilen hinzugefügt werden, entsprechen den Ziel Produktcodes der Ziel Images, die in der [Tabelle TargetImages](targetimages-table-patchwiz-dll-.md)aufgeführt sind.
-   Die Werte, die den Sequenz Spalten in den neuen Zeilen hinzugefügt werden, werden mit der höchsten Produktversion, auf die der Patch abzielt, und der UTC-Zeit, zu der der Patch generiert wird, generiert. Die Sequenznummer ist <Product Minor Version> . <Build Major Number> . <Zeitstempel 1>. <Zeitstempel 2>.
    -   Das erste Feld ist die Produktversion der höchsten Version des Produkts, das den Patch als Ziel hat.
    -   Das zweite Feld ist die buildhauptnummer der höchsten Version des Produkts, das den Patch als Ziel hat.

    Die zwei Zeitstempel Felder für den 32-Bit-Zeitstempel, der zum zählen der Sekunden in koordinierter Weltzeit (UTC) benötigt wird.
    > [!Note]  
    > Produktversionen haben das folgende Format: <Product Major Version> . <Product Minor Version> . <Build Major Number> . <Build Minor Number> und ein Produkt mit der Versionsnummer 2.1.0.0 ist eine höhere Version als ein Produkt mit der Versionsnummer 1.2.0.0

     

-   Das msidbpatchsequencesupersedefrühere-Attribut wird in die Attribut Spalte neuer Zeilen eingegeben, die für Service Packs (SP) oder kleinere Upgradepatches generiert werden. Das msidbpatchsequencesupersedebug-Attribut wurde keinem QFE-oder Small Update-Patch hinzugefügt.
    > [!Note]  
    > Eine Service Pack (SP) sollte die Korrekturen aller QFEs enthalten, die vor der Veröffentlichung veröffentlicht wurden. Wenn ein Patch-Autor jedoch die Eigenschaft Sequenz \_ Daten \_ Ablösung auf 0 (null) oder 1 (eins) in der PCP-Datei festlegt, wird die Spalte Attribute aller Zeilen in der Tabelle msipatchsequence auf den Wert festgelegt, der für die Sequenz \_ Daten Ablösung angegeben wird \_ . Patchautoren, die mehr Kontrolle benötigen, müssen die Attribut Spalte manuell erstellen.

     

Wenn Sie in die PCP-Datei eine [patchsequence-Tabelle](patchsequence-table--patchwiz-dll-.md) einschließen, \_ wird die Eigenschaft Sequenzdaten \_ Generierung \_ deaktiviert ignoriert, und die in der Tabelle patchsequence bereitgestellten Informationen können der [msipatchsequence-Tabelle](msipatchsequence-table.md) des Patches hinzugefügt werden.

 

 



