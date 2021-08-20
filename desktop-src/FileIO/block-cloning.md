---
description: Ein Blockklonvorgang weist das Dateisystem an, einen Bereich von Dateibytes im Auftrag einer Anwendung zu kopieren.
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: Klonen blockieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7d94afdb9b630f501de4baee0b690715f42d057a157f31b142c231e0a03f9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582662"
---
# <a name="block-cloning"></a>Klonen blockieren

Ein *Blockklonvorgang* weist das Dateisystem an, einen Bereich von Dateibytes im Auftrag einer Anwendung zu kopieren. Die Zieldatei kann mit der Quelldatei identisch sein oder sich von dieser unterscheiden.

Ein Dateisystem verwaltet die Zuordnungen von Clustern und [Extents](clusters-and-extents.md)und kann die Kopie ausführen, indem die Zuordnungen der virtuellen Clusternummer (VIRTUAL Cluster Number, VCN) in LCN-Zuordnungen (Logical Cluster Number) als kostengünstiger Metadatenvorgang geändert werden, anstatt die zugrunde liegenden Dateidaten zu lesen und zu schreiben. Dadurch kann die Kopie schneller abgeschlossen werden und weniger E/A-Vorgänge für den zugrunde liegenden Speicher generiert werden. Darüber hinaus können mehrere Dateien nach dem Blockklon logische Cluster gemeinsam verwenden, um Kapazität zu sparen, indem identische Cluster nicht mehrmals auf dem Datenträger gespeichert werden.

Ein Blockklonvorgang unterbricht nicht die Isolation, die zwischen Dateien bereitgestellt wird. Nach Abschluss eines Blockklons werden Schreibvorgänge in die Quelldatei nicht im Ziel angezeigt (oder umgekehrt).

Blockklonen ist nur für den [ReFS-Dateisystemtyp](/windows/desktop/w8cookbook/resilient-file-system--refs-) verfügbar, der mit Windows Server 2016.

## <a name="block-cloning-on-refs"></a>Klonen auf ReFS blockieren

ReFS auf Windows Server 2016 implementiert Blockklonen, indem logische Cluster (d. h. physische Speicherorte auf einem Volume) aus der Quellregion in die Zielregion neu verteilt werden. Anschließend wird ein Mechanismus zum Zuordnen bei Schreibzugriff verwendet, um die Isolation zwischen diesen Regionen sicherzustellen. Die Quell- und Zielregionen können sich in denselben oder unterschiedlichen Dateien enthalten.

Diese Implementierung erfordert, dass die Anfangs- und Enddateioffsets an Den Clustergrenzen ausgerichtet sind. In ReFS auf Windows Server 2016 haben Cluster standardmäßig eine Größe von 4 KB, können aber optional auf 64 KB festgelegt werden. Bei der Clustergröße handelt es sich um einen volumeweiten Parameter, der zur Formatzeit festgelegt wird.

## <a name="restrictions-and-remarks"></a>Einschränkungen und Hinweise

-   Die Quell- und Zielregionen müssen an einer Clustergrenze beginnen und enden.
-   Die geklonte Region muss kleiner als 4 GB lang sein.
-   Die Zielregion darf sich nicht über das Ende der Datei erstrecken. Wenn die Anwendung das Ziel mit geklonten Daten erweitern möchte, muss sie zuerst [**SetEndOfFile aufrufen.**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)
-   Wenn sich die Quell- und Zielregionen in derselben Datei befinden, dürfen diese nicht überlappen. (Die Anwendung kann möglicherweise fortfahren, indem sie den Blockklonvorgang in mehrere Blockklone aufteilt, die sich nicht mehr überschneiden.)
-   Die Quell- und Zieldateien müssen sich auf demselben Volume ReFS befinden.
-   Die Quell- und Zieldateien [](file-attribute-constants.md) müssen über die gleiche Integritätseinstellung Streams verfügen (d. h. Integritäts-Streams muss in beiden Dateien aktiviert oder in beiden Dateien deaktiviert sein).
-   Hat die Quelldatei eine geringe Datendichte, muss die Zieldatei ebenfalls eine geringe Datendichte aufweisen.
-   Der Blockklonvorgang unterbricht freigegebene, nicht bare Sperren (auch bekannt als [level 2-bare Sperren).](types-of-opportunistic-locks.md)
-   Das ReFS-Volume muss mit Windows Server 2016 formatiert worden sein, und wenn Windows-Failoverclustering verwendet wird, muss die Clusteringfunktionsebene zur Formatzeit Windows Server 2016 oder höher sein.

## <a name="example"></a>Beispiel

Angenommen, wir haben zwei Dateien, X und Y, wobei jede Datei aus drei unterschiedlichen Regionen besteht. Jeder Dateibereich wird in einem bestimmten Bereich des Volumes gespeichert. Das Dateisystem speichert das Wissen, dass auf jede dieser Volumeregionen in einer Dateiregion verwiesen wird:

![vor dem Klonen](images/before-clone.png)

Angenommen, eine Anwendung gibt einen Blockklonvorgang von Datei X über die Dateiregionen A und B in Datei Y an dem Offset aus, in dem sich E derzeit befindet. Der folgende Dateisystemstatus würde zu folgendem Ergebnis führen:

![nach dem Klonen](images/after-clone.png)

Die Daten in den Regionen A und B wurden effektiv von Datei X in Datei Y dupliziert, indem der VCN in LCN-Zuordnungen innerhalb des ReFS-Volumes geändert wurde. Die Datenträgerblocks, die die Regionen A und B unterstützen, wurden während des Vorgangs nicht gelesen, und die Datenträgerdädungen, die die alten Regionen E und F unterstützen, wurden nicht überschrieben.

Die Dateien X und Y teilen sich jetzt logische Cluster auf dem Datenträger. Dies spiegelt sich in den in der Tabelle angezeigten Verweiszählern wider. Die Freigabe führt zu einem geringeren Volumenkapazitätsverbrauch, als wenn die Regionen A und B auf dem zugrunde liegenden Volume dupliziert wurden.

Angenommen, die Anwendung überschreibt Region A in Datei X. ReFS macht eine doppelte Kopie von A, die wir nun G nennen. ReFS ordnet G dann Datei X zu und wendet die Änderung an. Dadurch wird sichergestellt, dass die Isolation zwischen den Dateien beibehalten wird. Die Verweisanzahl wird entsprechend aktualisiert:

![nach dem Ändern des Schreibzugriffs](images/after-modifying-write.png)

Nach dem Ändern des Schreibzugriffs wird Region B weiterhin auf dem Datenträger freigegeben. Falls Region A größer als ein Cluster wäre, würde nur der geänderte Cluster dupliziert und der verbleibende Teil würde freigegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**\_DUPLIZIERTE WERTE FÜR \_ WERTE**](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[**FSCTL \_ DUPLICATE \_ EXTENTS \_ TO \_ FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
