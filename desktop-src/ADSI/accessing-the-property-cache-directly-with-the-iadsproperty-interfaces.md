---
title: Zugreifen auf den Eigenschaftencache mit IADsEigenschaftenschnittstellen
description: Die IADsProperty-Schnittstellen bestehen aus IADsPropertyList, IADsPropertyEntry und IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Direkter Zugriff auf den Eigenschaftencache mit den IADsProperty Interfaces ADSI
- Eigenschaftencache ADSI
- Eigenschaftencache ADSI mithilfe von IADsProperty-Schnittstellen für den Zugriff auf den Eigenschaftencache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a68cd77a10d6631b52e48ed19650dd5cd18dff0ee59ba2332db73b7fce1a8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024118"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>Zugreifen auf den Eigenschaftencache mit IADsEigenschaftenschnittstellen

Die [**IADsProperty-Schnittstellen**](/windows/desktop/api/Iads/nn-iads-iadsproperty) bestehen aus [**IADsPropertyList,**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)und [**IADsPropertyValue.**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) Diese Schnittstellen stellen Methoden bereit, um direkt auf die Eigenschaften eines Objektcaches zu zugreifen und sie zu bearbeiten. Eine Eigenschaft wird als Eigenschafteneintrag bezeichnet und entspricht einem im Schema definierten Attribut. Ein Eigenschafteneintrag kann einen oder mehrere Eigenschaftswerte enthalten. Ein Satz von Eigenschafteneinträgen ist als Eigenschaftenliste organisiert.

Die [**IADsPropertyList-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) verwaltet die Eigenschaftenliste eines ADSI-Objekts. Die [**IADsPropertyEntry-Schnittstelle führt**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) diesen Vorgang für einen Eigenschafteneintrag aus. Auf ähnliche Weise stellt die [**IADsPropertyValue-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) einen oder mehrere Eigenschaftswerte dar. Zusammen bieten sie benutzern einen Mechanismus für:

-   Arbeiten Sie direkt mit dem Eigenschaftencache.
-   Arbeiten Sie mit Verzeichnissen, die keine Schemas enthalten, z. B. einen LDAP-Server der Version 2.

Die [**IADsProperty-Schnittstellen**](/windows/desktop/api/Iads/nn-iads-iadsproperty) arbeiten ausschließlich mit dem Eigenschaftencache und versuchen nicht, mit dem Server zusammenzuarbeiten, um die Daten im persistenten Speicher abzurufen oder \* zu ändern. Daher werden diese Schnittstellen nur verwendet, um Eigenschaften im Clientcache zu untersuchen und zu bearbeiten. Bevor Sie diese Schnittstellen verwenden, müssen Sie die [**IADs::GetInfo-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) oder die [**IADs::GetInfoEx-Methode**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) explizit aufrufen, um die Objekteigenschaften in den Cache zu laden, wenn der Cache nicht initialisiert wurde. Nach dem Aufrufen der Methoden dieser Schnittstellen müssen Sie [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) aufrufen, um die Änderungen im zugrunde liegenden Verzeichnisspeicher persistent zu speichern.

Weitere Informationen und ein Codebeispiel, das zum Implementieren dieser Schnittstellen verwendet werden kann, finden Sie unter Beispielcode für die Verwendung [von IADsProperty-Schnittstellen](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md)für den Zugriff auf den Eigenschaftencache.

 

 




