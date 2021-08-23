---
description: Da der Windows Installer alle Informationen zur Installation in einer relationalen Datenbank speichert, kann die Installation einer Anwendung oder eines Produkts für bestimmte Benutzergruppen angepasst werden, indem Transformationsvorgänge auf das Paket angewendet werden.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Anpassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ece84afd2b9ca5ce547d9ea96aed23786f78c89f01f5b5b5eaa78e2791e86b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947854"
---
# <a name="customization"></a>Anpassung

Da der Windows Installer alle Informationen zur Installation in einer relationalen Datenbank speichert, kann die Installation einer Anwendung oder eines Produkts für bestimmte Benutzergruppen angepasst werden, indem Transformationsvorgänge auf das Paket angewendet werden. Transformationen können verwendet werden, um die verschiedenen Anpassungen eines Basispakets zu kapseln, die von verschiedenen Arbeitsgruppen benötigt werden. Weitere Informationen finden Sie unter [Zusammenführungen und Transformationen.](merges-and-transforms.md)

Während der Installation können mehrere Transformationen eines Basispakets gleichzeitig angewendet werden. Dies bietet einen Mechanismus zum effizienten Zuweisen von benutzerdefinierten Installationen zu verschiedenen Benutzergruppen. Dies wäre beispielsweise in Organisationen nützlich, in denen die Finanz- und Personalsupportabteilungen unterschiedliche Installationen eines bestimmten Produkts erfordern. Das Produkt kann für alle Benutzer in der Organisation durch eine [administrative Installation](administrative-installation.md) des Basispakets auf einem einzelnen Administratorinstallationspunkt zur Verfügung gestellt werden. Jede Arbeitsgruppe kann dann automatisch ihre entsprechende Anpassung durch eine on-the-fly-Transformation erhalten, wenn sie das Produkt installieren.

 

 



