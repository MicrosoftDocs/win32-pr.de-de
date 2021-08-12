---
title: Zuordnen von ADSI Visual Basic Code zu C++-Code
description: ADSI besteht aus mehr als 50 Schnittstellen.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a924f403dcbdbe89b1b0bbf846c95223b401a04d1925ce9362a5300faf828fe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179207"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>Zuordnen von ADSI Visual Basic Code zu C++-Code

ADSI besteht aus mehr als 50 Schnittstellen. Die meisten Verzeichnisvorgänge können mit nur fünf Schnittstellen abgeschlossen werden. Sie lauten wie folgt:

-   [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**Iads**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

In der folgenden Tabelle sind Zuordnungen von ADSI-VB/VBS-Code zu C++-Code aufgeführt. Beachten Sie, dass dies keine vollständige Liste ist.



| VBS-Code                           | VC-Code                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject()              | hr = AdsGetObject()                                                   |
| Obj. Put obj. Get obj. Elternteil         | IADs oder IDirectoryObject                                              |
| Obj. Erstellen Sie obj. Löschen Sie obj. MoveHere | IADsContainer                                                         |
| For each... In...                      | AdsBuildEnumerator() ADsEnumerateNext()                               |
| Verbindung, Befehl, RecordSet     | Idirectorysearch                                                      |
| Sicherheitsdeskriptor, ACL, ACE      | IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry |



 

 

 




