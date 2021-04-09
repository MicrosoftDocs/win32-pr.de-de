---
title: Active Directory von Dienst Schnittstellen Objekten
description: Das ADSI-Objektmodell besteht aus COM-Objekten. -Clients bearbeiten-Objekte mit-Schnittstellen. ADSI-Anbieter implementieren die Objekte und ihre Schnittstellen.
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- Objekte ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e356d9b1212b448d16bb6bba081f6141a877b0b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858469"
---
# <a name="active-directory-service-interfaces-objects"></a>Active Directory von Dienst Schnittstellen Objekten

Das ADSI-Objektmodell besteht aus COM-Objekten. -Clients bearbeiten-Objekte mit-Schnittstellen. ADSI-Anbieter implementieren die Objekte und ihre Schnittstellen.

Bei ADSI-Objekten handelt es sich um COM-Objekte, die ein Element innerhalb eines Verzeichnis Diensts darstellen: Computer, Benutzer, Dateien, Server, Drucker, Druck Warteschlangen usw. Das heißt, Elemente, die von Netzwerkadministratoren täglich verwendet werden. ADSI definiert verschiedene Arten von Objekten, um unterschiedliche Arten von Elementen darzustellen. Jedes-Objekt, wie in der folgenden Abbildung gezeigt, unterstützt eine oder mehrere COM-Schnittstellen, die den Zugriff auf Objektdaten ermöglichen, die häufig als Metadaten bezeichnet werden.

![Active Directory-Dienst Schnittstellen Objekte](images/ds2objex.png)

Da com-Schnittstellen logisch verbundene Sätze von Eigenschaften und Methoden sind, können Sie sich jede Schnittstelle als Handle für das Objekt vorstellen, das gleichzeitig Zugriff auf jeweils nur einen Satz logischer Funktionen bietet. In der folgenden Tabelle sind die grundlegenden ADSI-Elemente aufgelistet.



| Schnittstelle            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IADs**             | Wird für die Objektidentifikation verwendet. Da die grundlegende Schnittstelle für alle ADSI-Objekte erforderlich ist, bietet [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) Zugriff auf Objekt Metadaten, einschließlich ihrer Definition im ADSI-Schema. IADs bietet auch Zugriff auf die Eigenschaften und Methoden, die Objektdaten im Eigenschaften Cache verwalten.                                                                                   |
| **IADsContainer**    | Wird für die Objekt Verwaltung und-Erkennung verwendet. Für alle ADSI-Containerobjekte ist die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle erforderlich, um das Erstellen, löschen, kopieren und Verschieben von Objekten, die Bindung und die Enumeration zu verwalten.                                                                                                                                                                      |
| **IADsPropertyList** | Wird für die Objekteigenschaften Verwaltung verwendet. Die [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) -Schnittstelle optimiert die Verwaltung von Objektdaten im Eigenschaften Cache.                                                                                                                                                                                                                                |
| **IDirectoryObject** | Wird für direkten Objektzugriff verwendet. Die [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle bietet Zugriff auf Low-Level-Objekten für Clients, die keine Automatisierung verwenden. Diese Schnittstelle umgeht den Objekt Eigenschafts Cache und ermöglicht den direkten Zugriff auf Objekteigenschaften. Weitere Informationen finden Sie [unter IADs und IDirectoryObject-Schnittstellen](the-iads-and-idirectoryobject-interfaces.md). |
| **IUnknown**         | Wird für die Verwaltung von COM-Objekten verwendet. Die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle ist für alle COM-Objekte erforderlich.                                                                                                                                                                                                                                                                              |
| **IDispatch**        | Wird für Typbibliotheks Daten und Methodenaufrufe verwendet. Die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle ist für alle Automatisierungs Objekte erforderlich.                                                                                                                                                                                                                             |



 

Komplexere ADSI-Objekte können zusätzliche Schnittstellen verfügbar machen. [**Iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) unterstützt z. b. Methoden, die Sammlungen von Verzeichnis Elementen desselben Datentyps verwalten. [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) -Methoden verwalten die speziellen Case-Auflistungen von Objekten, die die [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) -Schnittstelle unterstützen. Für Anbieter, die dies unterstützen, unterstützt die [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle Methoden zum Abfragen von Verzeichnisdiensten. Außerdem bietet ADSI Schnittstellen, die bekannte logische und physische Elemente darstellen. Beispielsweise unterstützen ADSI-Objekte, die Benutzer darstellen, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), die Computer, die [**iadscomputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)darstellen, usw. Weitere Informationen zu ADSI-Objekten finden Sie [unter IADs und IDirectoryObject-Schnittstellen](the-iads-and-idirectoryobject-interfaces.md). Nicht alle Anbieter implementieren alle Schnittstellen oder alle Methoden und Eigenschaften für alle Schnittstellen. Weitere Informationen finden Sie unter [ADSI Reference](adsi-reference.md).

 

 