---
title: Verwenden von objectGUID für die Bindung an ein Objekt
description: Ein definierter Name eines Objekts ändert sich, wenn das Objekt umbenannt oder verschoben wird. der Distinguished Name ist daher kein zuverlässiger Objekt Bezeichner.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Verwenden von objectGUID für die Bindung an ein Objekt AD
- objectGUID AD
- objectGUID AD, verwenden von zum Binden an ein Objekt
- Active Directory mithilfe von, Bindung und Verwendung von objectGUID für die Bindung an das Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038723"
---
# <a name="using-objectguid-to-bind-to-an-object"></a>Verwenden von objectGUID für die Bindung an ein Objekt

Ein definierter Name eines Objekts ändert sich, wenn das Objekt umbenannt oder verschoben wird. der Distinguished Name ist daher kein zuverlässiger Objekt Bezeichner. In Active Directory Domain Services ändert sich die **objectGUID** -Eigenschaft eines Objekts nie, auch wenn das Objekt umbenannt oder verschoben wird. Weitere Informationen zu **objectGUID** und Bezeichnerinformationen finden Sie unter [Objektnamen und-Identitäten](object-names-and-identities.md).

Der Active Directory LDAP-Anbieter stellt eine Methode bereit, mit der die Objekt-GUID an ein Objekt gebunden wird. Das Format der Bindungs Zeichenfolge lautet wie folgt:


```C++
LDAP://servername/<GUID=XXXXX>
```



In diesem Beispiel ist "Servername" der Name des Verzeichnis Servers und "xxxxx" die Zeichen folgen Darstellung des hexadezimal Werts der GUID. Der Servername ist optional. Die GUID-Zeichenfolge wird im Formular "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" angegeben. Die GUID-Zeichenfolge kann auch das Format "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" aufweisen. Dies ist die gleiche Form wie die Zeichenfolge, die von der [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) -Funktion erstellt wurde, ohne die umgebenden geschweiften Klammern " {} ". Weitere Informationen und ein Codebeispiel, das zeigt, wie eine bindbare Zeichenfolge aus einer GUID erstellt wird, finden Sie unter [Beispielcode zum Erstellen einer typfähigen Zeichen folgen Darstellung einer GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md). Die [**IADs. GUID**](/windows/desktop/ADSI/iads-property-methods) -Eigenschaft kann verwendet werden, um die richtige Zeichen folgen Form der GUID abzurufen.

Bei der Bindung mit der Objekt-GUID werden einige [**IADs**](/windows/desktop/api/iads/nn-iads-iads) und [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Methoden und-Eigenschaften nicht unterstützt. Die folgenden **IADs** -Eigenschaften werden von Objekten, die über die Objekt-GUID abgerufen werden, nicht unterstützt:

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Name**](/windows/desktop/ADSI/iads-property-methods)
-   [**Parent**](/windows/desktop/ADSI/iads-property-methods)

Die folgenden **IADsContainer** -Methoden werden von Objekten, die über die Objekt-GUID abgerufen werden, nicht unterstützt:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**Stelle**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Lösch**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**Copyhere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**Muvehere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Wenn Sie diese Methoden und Eigenschaften nach dem Binden an ein Objekt mithilfe der Objekt-GUID verwenden möchten, verwenden Sie die [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) -Methode, um den Distinguished Name des Objekts abzurufen, und verwenden Sie dann den Distinguished Name, um die Bindung an das Objekt wiederherzustellen.

Wenn eine Anwendung Bezeichner oder Verweise auf Objekte speichert oder speichert, die in Active Directory Domain Services gespeichert sind, ist die Objekt-GUID der beste Bezeichner, der aus verschiedenen Gründen verwendet werden kann:

-   Die **objectGUID** -Eigenschaft von für Objekt ändert sich nie, auch wenn das Objekt umbenannt oder verschoben wird.
-   Es ist einfach, mithilfe der Objekt-GUID eine Bindung an das Objekt herzustellen.
-   Wenn das Objekt umbenannt oder verschoben wird, stellt die **objectGUID** -Eigenschaft einen einzelnen Bezeichner bereit, der verwendet werden kann, um das Objekt schnell zu finden und zu identifizieren, anstatt eine Abfrage zu erstellen, die Bedingungen für alle Eigenschaften hat, die das Objekt identifizieren würden.

 

 