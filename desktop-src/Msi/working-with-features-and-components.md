---
description: Es gibt mehrere Funktionen, die die Installation von Produktkomponenten und -features ändern. Im Folgenden wird beschrieben, wie Sie Features und Komponenten ändern.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Arbeiten mit Features und Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b77fd93a9f2ee8181020f6c436d7e61e09a0f6d7858f0159fb70a7c7d8eeef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145173"
---
# <a name="working-with-features-and-components"></a>Arbeiten mit Features und Komponenten

Es gibt mehrere Funktionen, die die Installation von [Produktkomponenten und -features](components-and-features.md)ändern. Im Folgenden wird beschrieben, wie Sie Features und Komponenten ändern.

**So ändern Sie die Installation von Features und Komponenten**

1.  Legen Sie die Installationsebene für eine Komponente oder ein Feature fest, indem Sie die [**MsiSetInstallLevel-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) aufrufen.

    Jedem Feature in einem Paket wird in der [Tabelle Feature](feature-table.md)eine Installationsebene zugewiesen. Wenn die Installationsebene eines Features niedriger als die von [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)festgelegte Ebene ist, wird das Feature für die Installation ausgewählt. Nachdem **MsiSetInstallLevel** aufgerufen wurde, können Sie explizit ändern, ob ein Feature installiert ist.

2.  Bestimmen Sie, welche Zustände für ein angegebenes Feature verfügbar sind, indem Sie die [**MsiGetFeatureValidStates-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) aufrufen.
3.  Rufen Sie die [**MsiGetFeatureCost-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) auf, um die Speicherplatzanforderungen für ein angegebenes Feature und die zugehörigen untergeordneten Features abzurufen.
4.  Rufen Sie den aktuellen Zustand eines Features oder einer Komponente ab, indem Sie die [**MsiGetFeatureState-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) oder die [**MsiGetComponentState-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) aufrufen.
5.  Ändern Sie den Status des Features oder der Komponente mit der [**MsiSetFeatureState-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) oder der [**MsiSetComponentState-Funktion.**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)

 

 



