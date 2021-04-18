---
description: Sie können den Windows Installer verwenden, um fehlende Komponenten oder Dateien zu erkennen, und dann Features neu installieren, die die fehlenden Komponenten enthalten.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Installieren einer fehlenden Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357514"
---
# <a name="installing-a-missing-component"></a>Installieren einer fehlenden Komponente

Sie können den Windows Installer verwenden, um fehlende Komponenten oder Dateien zu erkennen, und dann Features neu installieren, die die fehlenden Komponenten enthalten. Da das Installationsprogramm Features und keine Komponenten installiert, muss es zuerst aufgelöst werden, zu welcher Komponente eine fehlende Datei gehört, und dann die Funktion installieren, die die Komponente enthält. Wenn mehr als eine Funktion mit der Komponente verknüpft ist, installiert das Installationsprogramm die Funktion, die den geringsten Speicherplatz benötigt.

Wenn Sie [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)aufrufen, können Sie überprüfen, ob die Schlüsseldatei einer Komponente vorhanden ist. Es ist jedoch weiterhin möglich, dass andere Dateien, die der Komponente angehören, fehlen. In diesem Szenario wird [**msiinstallmissingfile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea)aufgerufen. Der Installer löst dann eine Auflösung zu der Komponente aus, zu der die Datei gehört, und installiert das Feature, das mit der Komponente verknüpft ist, für die der geringste Speicherplatz erforderlich ist.

Wenn die [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) -Funktion unerwartet ausfällt, müssen Sie fehlende Komponenten installieren.

Im folgenden Verfahren wird gezeigt, wie Sie fehlende Komponenten installieren.

**So erkennen und installieren Sie eine fehlende Komponente**

1.  [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) aufrufen, um zu überprüfen, ob die Schlüsseldatei einer Komponente vorhanden ist. Auch wenn die Schlüsseldatei der Komponente vorhanden ist, ist es weiterhin möglich, dass andere Dateien, die der Komponente angehören, fehlen.
2.  Wenn die Funktion, die der Komponente zugeordnet ist, unbekannt ist, wird die Funktion [**msiinstallmissingcomponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) aufgerufen.
3.  Wenn die Funktion bekannt ist, die der Komponente zugeordnet ist, wird die Funktion [**msikonfigurirefeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) oder [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) aufgerufen.
4.  [**Msiinstallmissingfile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) wird aufgerufen, wenn eine Anwendung nicht in der Lage ist, eine Datei zu öffnen.

 

 



