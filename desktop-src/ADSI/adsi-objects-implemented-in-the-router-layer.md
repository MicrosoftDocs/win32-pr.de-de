---
title: ADSI-Objekte, die in der Routerebene implementiert sind
description: Die folgende Tabelle enthält eine kurze Beschreibung der COM-Objekte, die im ADSI-Router implementiert sind.
ms.assetid: bd446e05-a15d-4354-9204-1df4e360497c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99cc96eac8a2d680cb83622e01d94f8ef7a1d236726ab6b6fef9b2e6c5c40f50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692817"
---
# <a name="adsi-objects-implemented-in-the-router-layer"></a>ADSI-Objekte, die in der Routerebene implementiert sind

Die folgende Tabelle enthält eine kurze Beschreibung der COM-Objekte, die im ADSI-Router implementiert sind.



| ADSI-Objekt            | Beschreibung                                                         | Unterstützte Schnittstellen                                                                                                                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Accesscontrolentry** | Ein ADSI-Objekt, das einen Zugriffssteuerungseintrag (ACE) darstellt.       | [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)                                                                                                                                                                                                                                  |
| **AccessControlList**  | Ein ADSI-Objekt, das eine Zugriffssteuerungsliste (Access Control List, ACL) darstellt.        | [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                                                                                                                                                                                                                                    |
| **ADsNamespaces**      | Ein ADSI-Objekt, das den Container verschiedener Namespaces darstellt. | <dl> <dt>[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)</dt> <dt>[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)</dt> <dt>[**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)</dt> </dl> |
| **LargeInteger**       | Ein ADSI-Objekt, das eine große ganze Zahl darstellt.                     | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                                                                                                                                                                                                                                              |
| **Propertyentry**      | Ein ADSI-Objekt, das einen Eigenschafteneintrag darstellt.                    | [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                                                                                                                                                                                                                                            |
| **PropertyValue**      | Ein ADSI-Objekt, das einen Eigenschaftswert darstellt.                    | [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                                                                                                                                                                                                                                            |
| **PropertyValue2**     | Ein ADSI-Objekt, das einen Eigenschaftswert darstellt.                    | [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)                                                                                                                                                                                                                                          |
| **SecurityDescriptor** | Ein ADSI-Objekt, das einen Sicherheitsdeskriptor darstellt.               | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                                                                                                                                                                                                                  |



 

 

 




