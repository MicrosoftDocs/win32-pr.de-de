---
description: Es gibt mehrere Funktionen, die eine Anwendung aufrufen muss, um Features an fordern zu können.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Anfordern eines Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7288804168f6adf936550fee0ac0c542bd68f4d468d6aedd6372071744b9fec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990559"
---
# <a name="requesting-a-feature"></a>Anfordern eines Features

Es gibt mehrere Funktionen, die eine Anwendung aufrufen muss, um Features an fordern zu können. Vor dem Anfordern eines Features muss die Anwendung sicherstellen, dass das Feature installiert ist. Wenn die Anwendung [**MsiUseFeature aufruft,**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) bevor die Anwendung auf ein Feature zutritt, kann die Anwendung die zurückgegebenen Informationen verwenden, um Nutzungsmetriken zu verwalten.

**So fordern Sie ein Feature an**

1.  Rufen Sie [**die MsiEnumFeatures-**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) oder [**MsiQueryFeatureState-Funktion**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) auf, wenn Sie die Verfügbarkeit eines Features bestimmen möchten, ohne die Nutzungsanzahl zu erhöhen.
2.  Geben Sie die Absicht Ihrer Anwendung an, ein Feature zu verwenden, indem Sie die [**MsiUseFeature-Funktion**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) aufrufen.
3.  Ermitteln Sie Dateipfade, indem Sie die [**MsiGetComponentPath-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) aufrufen.
4.  Konfigurieren Sie das Feature, indem Sie die [**MsiConfigureFeature-Funktion**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) aufrufen.
5.  Rufen Sie Nutzungsmetriken ab, die Ihre Anwendung verwenden kann, indem Sie die [**MsiGetFeatureUsage-Funktion**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) aufrufen.

Das folgende Diagramm veranschaulicht das Featureanforderungsmodell.

![Featureanforderungsmodell. ](images/over2.png)

 

 



