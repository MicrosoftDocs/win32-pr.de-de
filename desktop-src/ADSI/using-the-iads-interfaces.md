---
title: Verwenden der IADs-Schnittstellen
description: ADSI, jedes Element eines Verzeichnis Dienstanbieter wird durch ein ADSI-Objekt dargestellt, bei dem es sich um ein COM-Objekt (Component Object Model) handelt, das die standardmäßige com-IUnknown-Schnittstelle sowie die Schnittstellen IDispatch und IADs unterstützt.
ms.assetid: bdbf2012-6863-4611-8173-6a3cd9c4960f
ms.tgt_platform: multiple
keywords:
- IADs ADSI, using
- ADSI ADSI, using, using the IADs Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878afa9350a45f18238bebb69df1a96eba52715e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391021"
---
# <a name="using-the-iads-interfaces"></a>Verwenden der IADs-Schnittstellen

ADSI, jedes Element eines Verzeichnis Dienstanbieter wird durch ein ADSI-Objekt dargestellt, bei dem es sich um ein COM-Objekt (Component Object Model) handelt, das die standardmäßige com- [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle sowie die Schnittstellen [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) und [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) unterstützt. **IADs** stellt die grundlegenden Wartungsfunktionen für ADSI-Objekte bereit.

Jedes ADSI-Objekt muss diese Schnittstelle unterstützen, die Folgendes bietet:

-   Stellen Sie die Objekt Identifizierung nach Name, Klasse oder ADsPath bereit.
-   Identifizieren Sie den Objekt Container, der das Erstellen und Löschen von Objekten verwaltet.
-   Abrufen der Objekt Schema Definition
-   Laden Sie die Objekt Attribute in den Eigenschafts Cache, und übertragen Sie die Änderungen im permanenten Verzeichnis Speicher.
-   Greifen Sie auf die Objekt Attributwerte im Eigenschaften Cache zu, und ändern Sie Sie.

Die [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle soll sicherstellen, dass ADSI-Objekte Netzwerkadministratoren und Verzeichnis Dienstanbietern eine effiziente und konsistente Darstellung verschiedener zugrunde liegender Verzeichnisdienste bereitstellen.

![ADSI-Objekt Unterstützung der IADs-Schnittstelle](images/ds2iads.png)

Die vorherige Abbildung zeigt ein generisches ADSI-Objekt, das die grundlegenden Schnittstellen [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)und [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)unterstützt. Ein ADSI-Objekt, wie z. b., verwaltet Daten aus dem Datenspeicher des zugrunde liegenden Verzeichnis Dienstanbieter über die unterstützten Schnittstellen. Diese Daten werden als Eigenschaften des-Objekts bezeichnet, und die Routinen, die diese Eigenschaften abrufen und festlegen, werden als Eigenschafts Methoden bezeichnet. Schreibgeschützte Eigenschaften verfügen über eine Eigenschaften Methode, die den Eigenschafts Wert abruft. Lese-/Schreibeigenschaften verfügen über zwei Methoden: eine Methode, die den Wert und einen Wert festlegt, der den Wert erhält. Eigenschaften werden in jedem ADSI-Objekt mit einem [Eigenschafts Cache](the-adsi-attribute-cache.md)implementiert. [**IADs:: get \_ ADsPath**](iads-property-methods.md) und **IADs::p UT- \_ ADsPath** sind Beispiele für Eigenschafts Methoden. Eigenschaften Methoden sind nicht offensichtlich für Visual Basic und andere Automatisierungs Clients, die direkte Verweise auf die Eigenschaft ermöglichen. Visual Basic bezieht sich z. b. auf **IADs:: ADsPath** direkt mithilfe der **Object. ADsPath** -Syntax. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

Außerdem interagiert ein ADSI-Objekt mithilfe von Methoden mit anderen ADSI-Objekten und direkt mit einem Namespace. -Methoden werden sofort ausgeführt. Beispiele für Methoden sind " [**IADs:: abtinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) " und " [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)".

Auf Eigenschaften, Eigenschaften Methoden und Methoden wird über Standard-COM-Schnittstellen zugegriffen.

Ein ADSI-Objekt wird durch seinen ADsPath eindeutig identifiziert. Ein ADsPath für den LDAP-Namespace ist beispielsweise "LDAP://MyServer/DC=fabrikam,DC=com". Weitere Informationen zu AD-then finden Sie unter [ADSI Binding (ADSI-Bindung](binding-to-an-adsi-object.md)). Für Programmierer, die mit com-Monikern vertraut sind, ist dies konzeptionell vergleichbar mit dem anzeigen amen des com-Monikers.

Jedes ADSI-Objekt, das weitere ADSI-Objekte enthält, die als ADSI-Container Objekt bezeichnet werden, unterstützt auch die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle, die Methoden und Eigenschaften bereitstellt, die die Erstellung, Löschung und Enumeration der im-Objekt enthaltenen ADSI-Objekte verwalten. Die folgende Abbildung zeigt ein ADSI-Container Objekt.

![ADSI-Container Objekt](images/dsiadsc.png)

Die meisten ADSI-Objekte sind in anderen Objekten enthalten. Das einzige ADSI-Objekt ohne übergeordneten Container ist das ADSI- **Namespaces** -Objekt der obersten Ebene ("ADS:").

Die [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode in einem Container Objekt speichert permanent die zwischengespeicherten Eigenschaften des ADSI-Container Objekts im Speicher, zusätzlich zu den Objekten, die mit der [**IADsContainer:: Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) -Methode erstellt wurden. [**IADsContainer::D Elete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) wirkt sich nicht auf den Eigenschaften Cache aus, löscht jedoch das zugrunde liegende Namespace-Verzeichnis Element, das durch dieses Objekt dargestellt wird.

 

 