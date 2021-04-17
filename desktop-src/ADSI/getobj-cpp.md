---
title: Getobj. CPP
description: In der Beispiel Anbieter Komponente wird ein Codebeispiel angezeigt, das zum Suchen und Binden von Objekten in getobj. cpp verwendet wird. In der folgenden Tabelle sind die unterstützten Routinen aufgeführt.
ms.assetid: d202e5ec-27b5-4809-a7fa-4a2e39c65295
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d58647208c68437c068d58cd9908bc08989141
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316461"
---
# <a name="getobjcpp"></a>Getobj. CPP

In der Beispiel Anbieter Komponente wird ein Codebeispiel angezeigt, das zum Suchen und Binden von Objekten in getobj. cpp verwendet wird. In der folgenden Tabelle sind die unterstützten Routinen aufgeführt.



| Element                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Relativegetobject**               | Ruft ein Objekt relativ zu einem angegebenen ADsPath ab.                                                                                                                                                                                                                                                       |
| **GetObject**                       | Ruft **AdsObject** ("Analyse. cpp") auf, um die Pfad Syntax zu überprüfen. dabei wird überprüft, ob der Pfad das richtige Anbieter Token hat, und den Objekttyp überprüfen. Wenn keine Fehler vorhanden sind, erstellen Sie eine Instanz des richtigen Objekt Typs, und rufen Sie einen Zeiger auf die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des Objekts ab. |
| **Buildadspathfromdspath**          | Es wurde eine ADsPath-Zeichenfolge aus dem nativen Verzeichnispfad erstellt.                                                                                                                                                                                                                                           |
| **Builddstreenamefromadspath**      | Verwenden Sie den ADsPath, um einen möglichen Struktur Verzeichnispfad für den nativen Verzeichnispfad zu erstellen.                                                                                                                                                                                                           |
| **Builddspathfromadspath**          | Verwendet ADsPath und dspathname.                                                                                                                                                                                                                                                                      |
| **Buildadsparentpath**              | Erstellt den ADsPath für das übergeordnete Element für dieses Objekt.                                                                                                                                                                                                                                                  |
| **Getnamespaceobject**              | Validate und [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ein BeispielNamespace-Objekt.                                                                                                                                                                                                           |
| **Validatenamespaceobject**         | Überprüfen Sie, ob das Namespace-Objekt mit dem aktuellen Anbieter Namen übereinstimmt.                                                                                                                                                                                                                               |
| **Validateprovider**                | Anbieter Namen überprüfen (Groß-/Kleinschreibung beachten).                                                                                                                                                                                                                                                          |
| **GetSchemaObject**                 | Überprüfen und öffnen Sie den entsprechenden Schema Objekttyp. Erstellen Sie dann die richtige, und rufen Sie den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Zeiger darauf ab.                                                                                                                                        |
| **Validateschemaobject**            | Überprüfen Sie, ob es ein gültiger Schema Objekttyp ist.                                                                                                                                                                                                                                                     |
| **Validateobjecttype**              | Vergewissern Sie sich, dass der Objekttyp im Schema vorhanden ist.                                                                                                                                                                                                                                                 |
| **Buildsampledsrootrdnfromadspath** | Erstellen Sie den ADsPath zum Stamm Knoten für die Beispiel Anbieter Komponente.                                                                                                                                                                                                                            |
| **Builddspathfromadspath**          | Verwendet ADsPath, dsrootrdn und dspathname.                                                                                                                                                                                                                                                          |



 

 

 