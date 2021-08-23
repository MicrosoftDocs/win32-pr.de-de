---
description: Sie können den Windows Installer verwenden, um fehlende Komponenten oder Dateien zu erkennen und dann Features neu zu installieren, die die fehlenden Komponenten enthalten.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Installieren einer fehlenden Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e788cad738d46d35a7ac0948be2e2e2d6ede4347eec424fb24cf17571e3a59f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828790"
---
# <a name="installing-a-missing-component"></a>Installieren einer fehlenden Komponente

Sie können den Windows Installer verwenden, um fehlende Komponenten oder Dateien zu erkennen und dann Features neu zu installieren, die die fehlenden Komponenten enthalten. Da das Installationsprogramm Funktionen und keine Komponenten installiert, muss es zuerst auflösen, zu welcher Komponente eine fehlende Datei gehört, und dann das Feature installieren, das die Komponente enthält. Wenn mehr als ein Feature mit der Komponente verknüpft ist, installiert das Installationsprogramm das Feature, das den geringsten Speicherplatz erfordert.

Wenn Sie [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)aufrufen, können Sie überprüfen, ob die Schlüsseldatei einer Komponente vorhanden ist. Es ist jedoch weiterhin möglich, dass andere Dateien, die zur Komponente gehören, fehlen. Rufen Sie in diesem Szenario [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)auf. Der Installer löst dann auf, zu welcher Komponente die Datei gehört, und installiert das Feature, das mit der Komponente verknüpft ist, für die der geringste Speicherplatz erforderlich ist.

Wenn die [**MsiGetComponentPath-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) unerwartet ausfällt, müssen Sie alle fehlenden Komponenten installieren.

Im folgenden Verfahren wird gezeigt, wie Sie fehlende Komponenten installieren.

**So erkennen und installieren Sie eine fehlende Komponente**

1.  Rufen Sie [**MsiGetComponentPath auf,**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) um zu überprüfen, ob die Schlüsseldatei einer Komponente vorhanden ist. Selbst wenn die Schlüsseldatei der Komponente vorhanden ist, ist es jedoch möglich, dass andere Dateien, die zur Komponente gehören, fehlen.
2.  Rufen Sie die [**MsiInstallMissingComponent-Funktion auf,**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) wenn das der Komponente zugeordnete Feature unbekannt ist.
3.  Rufen Sie die [**MsiConfigureFeature-**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) oder [**MsiProvideComponent-Funktion auf,**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) wenn das der Komponente zugeordnete Feature bekannt ist.
4.  Rufen Sie [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) auf, wenn eine Anwendung keine Datei öffnen kann.

 

 



