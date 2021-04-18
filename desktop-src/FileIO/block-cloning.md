---
description: Ein Block Klon Vorgang weist das Dateisystem an, einen Bereich von Datei Bytes für eine Anwendung zu kopieren.
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: Klonen blockieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33aa1c1eee693b6ed4b502aedc6da6176ece3e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530008"
---
# <a name="block-cloning"></a>Klonen blockieren

Ein *Block Klon* Vorgang weist das Dateisystem an, einen Bereich von Datei Bytes für eine Anwendung zu kopieren. Die Zieldatei ist möglicherweise mit der Quelldatei identisch oder unterschiedlich.

Ein Dateisystem verwaltet die Zuordnungen von [Clustern und Blöcken](clusters-and-extents.md)und kann möglicherweise die Kopie durchführen, indem die VCN-Zuordnungen (Virtual Cluster Number) zu logischen Cluster Nummern (LCN) als kostengünstiger Metadatenvorgang geändert werden, anstatt die zugrunde liegenden Datei Daten zu lesen und zu schreiben. Dadurch kann die Kopie schneller ausgeführt werden, und es werden weniger e/a-Vorgänge für den zugrunde liegenden Speicher generiert. Darüber hinaus können nach dem Block Klon mehrere Dateien nun logische Cluster gemeinsam nutzen. Dadurch wird die Kapazität eingespart, weil identische Cluster nicht mehrmals auf dem Datenträger gespeichert werden.

Ein Block Klon Vorgang führt nicht zu einer Unterbrechung der von Dateien bereitgestellten Isolation. Wenn ein Block Klon abgeschlossen ist, werden Schreibvorgänge in die Quelldatei nicht im Ziel angezeigt (oder umgekehrt).

Block Klon ist nur für den [Refs-Dateisystemtyp](/windows/desktop/w8cookbook/resilient-file-system--refs-) verfügbar, beginnend mit Windows Server 2016.

## <a name="block-cloning-on-refs"></a>Blockieren des Klonens von refs

Refs unter Windows Server 2016 implementiert das Klonen von Blöcken, indem logische Cluster (also physische Speicherorte auf einem Volume) der Quellregion der Zielregion neu zugeordnet werden. Anschließend wird ein Mechanismus zum Zuweisen bei Schreibzugriff verwendet, um die Isolation zwischen diesen Regionen sicherzustellen. Die Quell-und Zielregionen können sich in derselben oder in unterschiedlichen Dateien befinden.

Diese Implementierung erfordert, dass die Dateioffsets für das Start-und das Ende an den Cluster Grenzen ausgerichtet sind. In Refs unter Windows Server 2016 sind Cluster standardmäßig 4 KB groß, Sie können jedoch optional auf 64 KB festgelegt werden. Bei der Clustergröße handelt es sich um einen volumeweiten Parametersatz zur Formatierungs Zeit.

## <a name="restrictions-and-remarks"></a>Einschränkungen und Hinweise

-   Die Quell-und Zielregionen müssen an einer Cluster Grenze beginnen und enden.
-   Die geklonte Region muss kleiner als 4 GB lang sein.
-   Die Zielregion darf nicht über das Dateiende hinaus erweitert werden. Wenn die Anwendung das Ziel mit geklonten Daten erweitern möchte, muss zuerst [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)aufgerufen werden.
-   Wenn sich die Quell- und Zielregionen in derselben Datei befinden, dürfen diese nicht überlappen. (Die Anwendung kann fortfahren, indem Sie den Block Klon Vorgang in mehrere Block Klone aufteilen, die sich nicht mehr überlappen.)
-   Die Quell- und Zieldateien müssen sich auf demselben Volume ReFS befinden.
-   Die Quell-und Zieldateien müssen dieselbe Einstellung für [**Integritäts Datenströme**](file-attribute-constants.md) aufweisen (d. h., Integritäts Datenströme müssen in beiden Dateien aktiviert oder in beiden Dateien deaktiviert werden).
-   Hat die Quelldatei eine geringe Datendichte, muss die Zieldatei ebenfalls eine geringe Datendichte aufweisen.
-   Durch den Block Klon Vorgang werden freigegebene opportunistische Sperren (auch als [opportunistische Sperren der Ebene 2](types-of-opportunistic-locks.md)bezeichnet) unterbricht.
-   Das Refs-Volume muss mit Windows Server 2016 formatiert sein, und wenn Windows-Failoverclustering verwendet wird, muss die Clustering-Funktionsebene zur Formatierungs Zeit Windows Server 2016 oder höher aufweisen.

## <a name="example"></a>Beispiel

Angenommen, wir haben zwei Dateien: "X" und "Y", wobei jede Datei aus drei unterschiedlichen Regionen besteht. Jeder Datei Bereich wird in einem unterschiedlichen Bereich des Volumes gespeichert. Das Dateisystem speichert die Informationen, auf die in einer Datei Region in den einzelnen volumeregionen verwiesen wird:

![vor dem Klonen](images/before-clone.png)

Angenommen, eine Anwendung gibt einen Block Klon Vorgang aus Datei X, über die Datei Bereiche a und B, um die Datei Y an dem Offset, in dem E aktuell ist, aus. Der folgende Dateisystem Status ergibt sich:

![nach dem Klonen](images/after-clone.png)

Die Daten in den Regionen A und B wurden durch Ändern der VCN-zu-LCN-Zuordnungen im Refs-Volume effektiv von Datei X in Datei Y dupliziert. Die Datenträger Blöcke "A" und "B" wurden nicht gelesen, und die Datenträger Blöcke unterstützten die alten Bereiche, die E und F während des Vorgangs überschrieben haben.

Die Dateien X und Y geben nun logische Cluster auf dem Datenträger frei. Dies spiegelt sich in den Verweis Zählungen wider, die in der Tabelle angezeigt werden. Die Freigabe führt zu einem geringeren Volumen Kapazitäts Verbrauch, als wenn die Regionen A und B auf dem zugrunde liegenden Volume dupliziert wurden.

Angenommen, die Anwendung überschreibt Region a in der Datei x. Refs erstellt eine duplizierte Kopie von, die wir jetzt als "g. Refs" bezeichnen und dann "g" in Datei x zuordnen und die Änderung anwenden. Dadurch wird sichergestellt, dass die Isolation zwischen den Dateien beibehalten wird. Verweis Zähler werden entsprechend aktualisiert:

![nach dem Ändern von Write](images/after-modifying-write.png)

Nach dem Ändern des Schreibzugriffs wird Region B weiterhin auf dem Datenträger freigegeben. Falls Region A größer als ein Cluster wäre, würde nur der geänderte Cluster dupliziert und der verbleibende Teil würde freigegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**doppelte \_ Datenblöcke \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[**Datei Blöcke mit doppelter FSCTL- \_ \_ \_ \_ Datei**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
