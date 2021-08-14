---
title: Active Directory-Dienstschnittstellenobjekte
description: Das ADSI-Objektmodell besteht aus COM-Objekten. Clients bearbeiten Objekte mit Schnittstellen. ADSI-Anbieter implementieren die Objekte und ihre Schnittstellen.
ms.assetid: 3c9fd08e-47d6-4b71-8259-7c831d7d95c9
ms.tgt_platform: multiple
keywords:
- Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20d75454b840597e1fd2ac0599d72d04acb1ee674f84aff40da64f9886879cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181185"
---
# <a name="active-directory-service-interfaces-objects"></a>Active Directory-Dienstschnittstellenobjekte

Das ADSI-Objektmodell besteht aus COM-Objekten. Clients bearbeiten Objekte mit Schnittstellen. ADSI-Anbieter implementieren die Objekte und ihre Schnittstellen.

ADSI-Objekte sind COM-Objekte, die ein Element innerhalb eines Verzeichnisdiensts darstellen: Computer, Benutzer, Dateien, Server, Drucker, Druckwarteschlangen usw. Das heißt, Elemente, mit denen Netzwerkadministratoren täglich arbeiten. ADSI definiert verschiedene Arten von Objekten, um verschiedene Arten von Elementen darzustellen. Jedes Objekt unterstützt, wie in der folgenden Abbildung dargestellt, eine oder mehrere COM-Schnittstellen, die den Zugriff auf Objektdaten ermöglichen, die häufig als Metadaten bezeichnet werden.

![Active Directory-Dienstschnittstellenobjekte](images/ds2objex.png)

Da COM-Schnittstellen logisch verbundene Sätze von Eigenschaften und Methoden sind, können Sie sich jede Schnittstelle als Handle für das -Objekt vorstellen, das jeweils nur zugriff auf einen Satz logischer Funktionen bereitstellt. In der folgenden Tabelle sind die grundlegenden ADSI-Elemente aufgeführt.



| Schnittstelle            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Iads**             | Wird für die Objektidentifikation verwendet. Als grundlegende Schnittstelle, die für alle ADSI-Objekte erforderlich ist, ermöglichen [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) den Zugriff auf Objektmetadaten, einschließlich ihrer Definition im ADSI-Schema. IADs bieten auch Zugriff auf die Eigenschaften und Methoden, die Objektdaten im Eigenschaftencache verwalten.                                                                                   |
| **IADsContainer**    | Wird für die Objektverwaltung und -erkennung verwendet. Alle ADSI-Containerobjekte erfordern die [**IADsContainer-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadscontainer) zum Verwalten der Objekterstellung, des Löschens, Kopierens und Verschiebens, der Bindung und der Enumeration.                                                                                                                                                                      |
| **IADsPropertyList** | Wird für die Objekteigenschaftenverwaltung verwendet. Die [**IADsPropertyList-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) optimiert die Verwaltung von Objektdaten im Eigenschaftencache.                                                                                                                                                                                                                                |
| **IDirectoryObject** | Wird für den direkten Objektzugriff verwendet. Die [**IDirectoryObject-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) bietet Objektzugriff auf niedriger Ebene für Clients, die automation nicht verwenden. Diese Schnittstelle umgeht den Objekteigenschaftencache und bietet direkten Zugriff auf Objekteigenschaften. Weitere Informationen finden Sie unter [Die IADs und IDirectoryObject-Schnittstellen.](the-iads-and-idirectoryobject-interfaces.md) |
| **IUnknown**         | Wird für die COM-Objektverwaltung verwendet. Die [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ist für alle COM-Objekte erforderlich.                                                                                                                                                                                                                                                                              |
| **IDispatch**        | Wird für Typbibliotheksdaten und Methodenaufrufe verwendet. Die [**IDispatch-Schnittstelle**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ist für alle Automation-Objekte erforderlich.                                                                                                                                                                                                                             |



 

Komplexere ADSI-Objekte können zusätzliche Schnittstellen verfügbar machen. [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) unterstützt beispielsweise Methoden, die Sammlungen von Verzeichniselementen desselben Datentyps verwalten. [**IADsGroup-Methoden**](/windows/desktop/api/Iads/nn-iads-iadsgroup) verwalten die Sonderfallauflistungen von Objekten, die die [**IADsMembers-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsmembers) unterstützen. Für Anbieter, die dies unterstützen, unterstützt die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Methoden zum Abfragen von Verzeichnisdiensten. Darüber hinaus stellt ADSI Schnittstellen bereit, die bekannte logische und physische Elemente darstellen. ADSI-Objekte, die Benutzer darstellen, unterstützen beispielsweise [**IADsUser,**](/windows/desktop/api/Iads/nn-iads-iadsuser)solche, die Computer darstellen, unterstützen [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)usw. Weitere Informationen zu ADSI-Objekten finden Sie unter [The IADs and IDirectoryObject Interfaces](the-iads-and-idirectoryobject-interfaces.md). Nicht alle Anbieter implementieren alle Schnittstellen oder alle Methoden und Eigenschaften für alle Schnittstellen. Weitere Informationen finden Sie in der [ADSI-Referenz.](adsi-reference.md)

 

 