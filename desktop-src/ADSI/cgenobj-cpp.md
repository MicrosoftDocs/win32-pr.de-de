---
title: Cgenobj. CPP
description: In der Beispiel Anbieter Komponente sind generische Active Directory-Objektmethoden, die in "cgenobj. cpp" unterstützt werden, in der folgenden Tabelle aufgeführt.
ms.assetid: 72ccdc6e-1f3e-4633-92b3-500309433337
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe769dcfa6e4ab607188728115bcba16e40c0e56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707469"
---
# <a name="cgenobjcpp"></a>Cgenobj. CPP

In der Beispiel Anbieter Komponente sind generische Active Directory-Objektmethoden, die in "cgenobj. cpp" unterstützt werden, in der folgenden Tabelle aufgeführt.



| Methode                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Csampledsgenobject:: csampledsgenobject**                                              | Standardkonstruktor.                                                                                                                                                                                                                                                                                                       |
| **Csampledsgenobject:: ~ csampledsgenobject**                                             | Standardedekonstruktor.                                                                                                                                                                                                                                                                                                        |
| **Csampledsgenobject:: kreategenericobject**                                             | Erstellen Sie ein generisches ADS-Objekt. Initialisieren Sie nach Bedarf.                                                                                                                                                                                                                                                                    |
| **Csampledsgenobject:: sampledscreateobject**                                            | Erstellen Sie dieses Objekt in seinem übergeordneten Container.                                                                                                                                                                                                                                                                                 |
| **Csampledsgenobject:: sampledssetobject**                                               | Speichern Sie die Eigenschaften dieses Objekts (Löschen Sie den Cache).                                                                                                                                                                                                                                                                       |
| **Csampledsgenobject:: Zuordnungs Objekt**                                               | Erstellen Sie ein generisches Objekt, und laden Sie dessen Typdaten.                                                                                                                                                                                                                                                                             |
| **Csampledsgenobject:: QueryInterface**                                                  | Gibt den angeforderten Schnittstellen Zeiger zurück, falls verfügbar.                                                                                                                                                                                                                                                                       |
| Standard mäßige [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Methoden, einschließlich Implementierungen für:                   | [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get) (einschließlich Zuordnung vom systemeigenen Datentyp zum Variant-Typ) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) (einschließlich der Zuordnung vom Variant-Typ zum systemeigenen Datentyp)<br/> [**GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) (Aktualisieren des Eigenschaften Caches)<br/> " [**Ttinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) " (Speichern des Eigenschafts Caches)<br/> |
| Standard mäßige [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Methoden, einschließlich Implementierungen für: | [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)[**get \_ \_ netwenum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum)<br/> [**\_Filter erhalten**](iadscontainer-property-methods.md)<br/> [**Stelle**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create)<br/> [**Lösch**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)<br/>                                            |
| **Convertafearraytvariantarray**                                                      | Hilfsprogrammroutine                                                                                                                                                                                                                                                                                                            |



 

 

 





