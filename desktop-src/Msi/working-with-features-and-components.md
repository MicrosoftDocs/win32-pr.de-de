---
description: Es gibt mehrere Funktionen, die die Installation von Produktkomponenten und Features ändern. Im folgenden wird beschrieben, wie Features und Komponenten geändert werden.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Arbeiten mit Features und Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363539"
---
# <a name="working-with-features-and-components"></a>Arbeiten mit Features und Komponenten

Es gibt mehrere Funktionen, die die Installation von Produkt [Komponenten und Features](components-and-features.md)ändern. Im folgenden wird beschrieben, wie Features und Komponenten geändert werden.

**So ändern Sie die Installation von Features und Komponenten**

1.  Legen Sie die Installations Ebene für eine Komponente oder ein Feature fest, indem Sie die [**msisetinstalllevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) -Funktion aufrufen.

    Jeder Funktion in einem Paket wird eine Installations Ebene in der [Featuretabelle](feature-table.md)zugewiesen. Wenn die Installations Ebene eines Features niedriger ist als die von [**msisetinstalllevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)festgelegte Ebene, wird das Feature für die Installation ausgewählt. Nachdem **msisetinstalllevel** aufgerufen wurde, können Sie explizit ändern, ob eine Funktion installiert ist.

2.  Bestimmen Sie, welche Zustände für eine bestimmte Funktion verfügbar sind, indem Sie die [**msigetfeaturevalidstates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) -Funktion aufrufen.
3.  Abrufen der Speicherplatzanforderungen für eine angegebene Funktion und deren untergeordneter Funktionen durch Aufrufen der Funktion " [**msigetfeaturecost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) ".
4.  Rufen Sie den aktuellen Status eines Features oder einer Komponente ab, indem Sie die [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) -Funktion oder die [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) -Funktion aufrufen.
5.  Ändern Sie den Status des Features oder der Komponente mit der [**msisetfeaturestate**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) -Funktion oder der [**msisetcomponentstate**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) -Funktion.

 

 



