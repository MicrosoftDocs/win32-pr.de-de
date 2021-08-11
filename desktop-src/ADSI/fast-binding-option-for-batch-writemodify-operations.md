---
title: Schnelle Bindungsoption für Batchschreib-/Änderungsvorgänge
description: Wenn ein Verzeichnisdienstobjekt an gebunden ist, erstellt ADSI ein COM-Objekt, das das angegebene Verzeichnisobjekt darstellt.
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- Schnelle Bindungsoption für Batchschreib-/Änderungsvorgänge ADSI
- ADSI ADSI , Using, Fast Binding Option for Batch Write/Modify Operations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f27cbbe9ea76089ca1fd460f76c56d10e60664ae39ad28945440c6006acb9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179899"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Schnelle Bindungsoption für Batchschreib-/Änderungsvorgänge

Wenn ein Verzeichnisdienstobjekt an gebunden ist, erstellt ADSI ein COM-Objekt, das das angegebene Verzeichnisobjekt darstellt. Bei der Bindung ruft ADSI in der Regel das **objectClass-Attribut** ab, sodass ADSI die COM-Schnittstellen verfügbar machen kann, die für diese Objektklasse geeignet sind. Beispielsweise würde ein Benutzerobjekt die [**IADsUser-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsuser) zusätzlich zu den adsi-Basisschnittstellen verfügbar machen, die für alle Objekte unterstützt werden. Bei einem einzelnen Vorgang sollte dies keine Auswirkungen auf die Leistung haben. Wenn jedoch Batchvorgänge ausgeführt werden, die Hunderte oder Tausende von Bindungen über eine langsame Verbindung erfordern, und diese Vorgänge Daten in den Verzeichnisdienst schreiben, kann es wünschenswert sein, vollständige Objektunterstützung für eine schnellere Bindung auszutauschen. Dies wird als schnelle Bindung bezeichnet und wird durch Angabe des **ADS \_ FAST \_ BIND-Flags** erreicht, wenn [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) aufgerufen wird.

Für die schnelle Bindung gelten die folgenden Einschränkungen:

-   Der Bindungsvorgang muss mit der [**ADsOpenObject-Funktion**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) oder der [**IADsOpenDSObject::OpenDSObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ausgeführt werden. Der Bindungsvorgang wird einmal statt zweimal an den Verzeichnisserver gesendet. ADSI ruft das **objectClass-Attribut** nicht ab und macht daher nur die ADSI-Basisschnittstellen für das Objekt verfügbar.
-   Die folgenden Schnittstellen werden für das COM-Objekt unterstützt:

    -   [**Iads**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   Wenn die [**IADsContainer::GetObject-Methode**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) zum Binden an untergeordnete Objekte verwendet wird, weist das untergeordnete Objekt die gleichen Eigenschaften für die schnelle Bindung auf wie das übergeordnete Objekt.
-   Das Vorhandensein des Objekts, an das gebunden wird, wird während des Bindungsvorgangs nicht überprüft, sodass nachfolgende Methodenaufrufe fehlschlagen, wenn das Objekt nicht vorhanden ist. Aus diesem Grund sollte die schnelle Bindung nur für Objekte verwendet werden, die bekanntermaßen vorhanden sind, z. B. direkt nach dem Ausführen einer Abfrage, die die Distinguished Names der Objekte zurückgegeben hat, an die gebunden wird.
-   ADSI-Erweiterungen werden für Objekte der **obersten** Klasse verfügbar gemacht. Daher werden nur die Erweiterungen für die oben aufgeführten ADSI-Basisschnittstellen verfügbar gemacht.

 

 