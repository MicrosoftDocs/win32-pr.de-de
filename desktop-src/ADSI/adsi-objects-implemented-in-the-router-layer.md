---
title: In der routerschicht implementierte ADSI-Objekte
description: Die folgende Tabelle enthält eine kurze Beschreibung der COM-Objekte, die im ADSI-Router implementiert werden.
ms.assetid: bd446e05-a15d-4354-9204-1df4e360497c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1fad496bbfea220dca0046cac40daf41120675
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387970"
---
# <a name="adsi-objects-implemented-in-the-router-layer"></a>In der routerschicht implementierte ADSI-Objekte

Die folgende Tabelle enthält eine kurze Beschreibung der COM-Objekte, die im ADSI-Router implementiert werden.



| ADSI-Objekt            | BESCHREIBUNG                                                         | Unterstützte Schnittstellen                                                                                                                                                                                                                                                                      |
|------------------------|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **AccessControlEntry** | Ein ADSI-Objekt, das einen Zugriffs Steuerungs Eintrag (ACE) darstellt.       | [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)                                                                                                                                                                                                                                  |
| **AccessControlList**  | Ein ADSI-Objekt, das eine Zugriffs Steuerungs Liste (ACL) darstellt.        | [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                                                                                                                                                                                                                                    |
| **Adsnamespaces**      | Ein ADSI-Objekt, das den Container verschiedener Namespaces darstellt. | <dl> <dt>[**IADs**](/windows/desktop/api/Iads/nn-iads-iads)</dt> <dt>[**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)</dt> <dt>[**iadsnamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)</dt> </dl> |
| **LargeInteger**       | Ein ADSI-Objekt, das eine große ganze Zahl darstellt.                     | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                                                                                                                                                                                                                                              |
| **PropertyEntry**      | Ein ADSI-Objekt, das einen Eigenschafts Eintrag darstellt.                    | [**Iadspropertyentry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                                                                                                                                                                                                                                            |
| **PropertyValue**      | Ein ADSI-Objekt, das einen Eigenschafts Wert darstellt.                    | [**Iadspropertyvalue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                                                                                                                                                                                                                                            |
| **PropertyValue2**     | Ein ADSI-Objekt, das einen Eigenschafts Wert darstellt.                    | [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)                                                                                                                                                                                                                                          |
| **SecurityDescriptor** | Ein ADSI-Objekt, das eine Sicherheits Beschreibung darstellt.               | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                                                                                                                                                                                                                  |



 

 

 




