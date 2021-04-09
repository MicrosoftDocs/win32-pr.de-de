---
description: Es gibt mehrere Funktionen, die von einer Anwendung aufgerufen werden müssen, um Features anzufordern.
ms.assetid: 5253c6f0-316f-4f24-b0c0-951db8d16745
title: Anfordern einer Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5261aac69ad2dd604a072e4b02e3bcde76a2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042496"
---
# <a name="requesting-a-feature"></a>Anfordern einer Funktion

Es gibt mehrere Funktionen, die von einer Anwendung aufgerufen werden müssen, um Features anzufordern. Bevor eine Funktion angefordert wird, muss die Anwendung sicherstellen, dass die Funktion installiert ist. Wenn die Anwendung [**msiusefeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) aufruft, bevor die Anwendung auf eine Funktion zugreift, kann die Anwendung die zurückgegebenen Informationen verwenden, um nutzungsmetriken beizubehalten.

**So fordern Sie eine Funktion an**

1.  Wenn Sie die Verfügbarkeit eines Features ohne Erhöhung der Verwendungs Anzahl ermitteln möchten, können Sie die [**msienüberfeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) -oder [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) -Funktion aufzurufen.
2.  Geben Sie an, dass die Anwendung eine Funktion verwenden soll, indem Sie die [**msiusefeature**](/windows/desktop/api/Msi/nf-msi-msiusefeaturea) -Funktion aufrufen.
3.  Bestimmen Sie die Speicherorte durch Aufrufen der [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) -Funktion.
4.  Konfigurieren Sie die Funktion, indem Sie die Funktion [**msikonfigurirefeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) aufrufen.
5.  Rufen Sie nutzungsmetriken ab, die Ihre Anwendung verwenden kann, indem Sie die [**msigetfeatureusage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea) -Funktion aufrufen.

Das folgende Diagramm veranschaulicht das Funktions Anforderungsmodell.

![Funktions Anforderungsmodell. ](images/over2.png)

 

 



