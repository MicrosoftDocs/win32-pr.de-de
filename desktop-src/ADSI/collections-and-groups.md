---
title: Sammlungen und Gruppen
description: ADSI verwendet Sammlungsobjekte, um beliebige beliebige Elemente in einem Verzeichnisdienst darzustellen, die mit demselben Datentyp dargestellt werden können.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, using, Collections und Groups
- Sammlungen ADSI
- Gruppen-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949101"
---
# <a name="collections-and-groups"></a>Sammlungen und Gruppen

ADSI verwendet Sammlungsobjekte, um beliebige beliebige Elemente in einem Verzeichnisdienst darzustellen, die mit demselben Datentyp dargestellt werden können. Sammlungsobjekte werden als eine Reihe von **Variant** -Werten definiert, die einen der gültigen Automatisierungs Datentypen darstellen. Auflistungs Objekte können permanente Informationen darstellen, z. b. Zugriffs Steuerungs Listen und flüchtige Informationen, wie z. b. Druckaufträge in einer Druck Warteschlange.

Die com-Standard Konvention zum Auflisten des Inhalts eines Auflistungs Objekts (oder eines Container Objekts) besteht darin, ein Enumeratorobjekt zu erstellen, das [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)unterstützt, das über Methoden zum Durchlaufen der Liste der Auflistungs Objekte verfügt. Die Schnittstellen in ADSI, die die **get \_ \_ NewEnum** -Methode bereitstellen (Beachten Sie die zwei Unterstriche), sind [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) und [**iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection). ADSI stellt außerdem die Hilfsfunktionen [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) und [**adsenumeratenext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) für C-und C++-Programme bereit, um die Enumeration zu vereinfachen. Automatisierungs Clients verwenden implizit eine Enumeration, wenn **Sie in** einer **for** -Schleife aufgerufen werden.

Gruppen sind einfach Sammlungen von Objekten, die die [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) -Schnittstelle unterstützen.

 

 