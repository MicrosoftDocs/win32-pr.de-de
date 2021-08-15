---
title: CGENOBJ. Cpp
description: In der Beispielanbieterkomponente sind generische Active Directory-Objektmethoden, die in cgenobj.cpp unterstützt werden, in der folgenden Tabelle aufgeführt.
ms.assetid: 72ccdc6e-1f3e-4633-92b3-500309433337
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0667d44bfb3861989a58ac3764a113b4eb23a87ce3722709a5ca959a0fe4da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962099"
---
# <a name="cgenobjcpp"></a>CGENOBJ. Cpp

In der Beispielanbieterkomponente sind generische Active Directory-Objektmethoden, die in cgenobj.cpp unterstützt werden, in der folgenden Tabelle aufgeführt.



| Methode                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObject::CSampleDSGenObject**                                              | Standardkonstruktor.                                                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::~CSampleDSGenObject**                                             | Standard-Destruktor.                                                                                                                                                                                                                                                                                                        |
| **CSampleDSGenObject::CreateGenericObject**                                             | Erstellen Sie ein generisches ADS-Objekt. Initialisieren Sie nach Bedarf.                                                                                                                                                                                                                                                                    |
| **CSampleDSGenObject::SampleDSCreateObject**                                            | Erstellen Sie dieses Objekt im übergeordneten Container.                                                                                                                                                                                                                                                                                 |
| **CSampleDSGenObject::SampleDSSetObject**                                               | Speichern Sie die Eigenschaften dieses Objekts (löschen Sie den Cache).                                                                                                                                                                                                                                                                       |
| **CSampleDSGenObject::AllocateGenObject**                                               | Erstellen Sie ein generisches -Objekt, und laden Sie dessen Typdaten.                                                                                                                                                                                                                                                                             |
| **CSampleDSGenObject::QueryInterface**                                                  | Gibt ggf. den angeforderten Schnittstellenzeiger zurück.                                                                                                                                                                                                                                                                       |
| [**Standard-IADs-Methoden,**](/windows/desktop/api/Iads/nn-iads-iads) einschließlich Implementierungen für:                   | [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get) (einschließlich Zuordnung vom nativen Datentyp zum VARIANT-Typ) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) (einschließlich Zuordnung vom VARIANT-Typ zum nativen Datentyp)<br/> [**GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) (Aktualisieren des Eigenschaftencaches)<br/> [**SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) (Speichern des Eigenschaftencaches)<br/> |
| [**IADsContainer-Standardmethoden,**](/windows/desktop/api/Iads/nn-iads-iadscontainer) einschließlich Implementierungen für: | [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)[**get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)<br/> [**filter \_ abrufen**](iadscontainer-property-methods.md)<br/> [**Erstellen**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)<br/> [**Löschen**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)<br/>                                            |
| **ConvertSafeArrayToVariantArray**                                                      | Hilfsprogrammroutine.                                                                                                                                                                                                                                                                                                            |



 

 

 





