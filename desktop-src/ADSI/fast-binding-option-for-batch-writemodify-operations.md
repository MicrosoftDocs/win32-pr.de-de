---
title: Fast Binding-Option für Batch Schreib-/Änderungsvorgänge
description: Wenn ein Verzeichnisdienst Objekt an gebunden ist, erstellt ADSI ein COM-Objekt, das das angegebene Verzeichnis Objekt darstellt.
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- Fast Binding-Option für Batch Schreib-/Änderungsvorgänge (ADSI)
- ADSI ADSI, using, fast Binding-Option für Batch Schreib-/Änderungsvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322cf3c8b5f40dc43304f95d08ff53a7c5c14217
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517114"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Fast Binding-Option für Batch Schreib-/Änderungsvorgänge

Wenn ein Verzeichnisdienst Objekt an gebunden ist, erstellt ADSI ein COM-Objekt, das das angegebene Verzeichnis Objekt darstellt. Beim Binden ruft ADSI in der Regel das **objectClass** -Attribut ab, sodass ADSI die für diese Objektklasse geeigneten com-Schnittstellen verfügbar machen kann. Beispielsweise würde ein Benutzerobjekt zusätzlich zu den Basis-ADSI-Schnittstellen, die für alle Objekte unterstützt werden, die [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) -Schnittstelle verfügbar machen. Für einen einzelnen Vorgang sollte dies keine Auswirkung auf die Leistung haben. Wenn jedoch Batch Vorgänge ausgeführt werden, die Hunderte oder Tausende von Bindungen über eine langsame Verbindung benötigen, und diese Vorgänge Daten in den Verzeichnisdienst schreiben, ist es möglicherweise wünschenswert, die vollständige Objekt Unterstützung für schnellere Bindungen auszutauschen. Dies wird als schnelle Bindung bezeichnet und erfolgt durch Angabe des **Ads " \_ schnelles \_ binden** "-Flag, wenn " [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) " oder " [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) " aufgerufen wird.

Für die schnelle Bindung gelten die folgenden Einschränkungen:

-   Der Bindungs Vorgang muss mit der [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) -Funktion oder der [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) -Methode ausgeführt werden. Der Bindungs Vorgang wird einmal statt zweimal an den Verzeichnisserver geleitet. ADSI Ruft das **objectClass** -Attribut nicht ab und macht daher nur die Basis-ADSI-Schnittstellen für das Objekt verfügbar.
-   Die folgenden Schnittstellen werden für das COM-Objekt unterstützt:

    -   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**Iadsdeleteops**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   Wenn die [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) -Methode zum Binden an untergeordnete Objekte verwendet wird, weist das untergeordnete Objekt dieselben fast-BIND-Merkmale wie das übergeordnete Objekt auf.
-   Das vorhanden sein des Objekts, an das gebunden wird, wird während des Bindungs Vorgangs nicht überprüft, sodass nachfolgende Methodenaufrufe fehlschlagen, wenn das Objekt nicht vorhanden ist. Daher sollte die schnelle Bindung nur für Objekte verwendet werden, die bekanntermaßen vorhanden sind, z. b. direkt nach dem Ausführen einer Abfrage, die die Distinguished Names der an gebundenen Objekte zurückgegeben hat.
-   ADSI-Erweiterungen werden für Objekte der Klasse **Top** verfügbar gemacht. Daher werden nur die Erweiterungen für die oben aufgeführten Basis-ADSI-Schnittstellen verfügbar gemacht.

 

 