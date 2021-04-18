---
title: Zuordnung von ADSI-Visual Basic Code zu C++-Code
description: ADSI besteht aus mehr als 50 Schnittstellen.
ms.assetid: 6316f504-265e-44d4-ba24-e6289065981b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c64a022569a95f38ec1da7a1cb7acf533eb04ca6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340193"
---
# <a name="mapping-adsi-visual-basic-code-to-c-code"></a>Zuordnung von ADSI-Visual Basic Code zu C++-Code

ADSI besteht aus mehr als 50 Schnittstellen. Die meisten Verzeichnis Vorgänge können nur mit fünf Schnittstellen abgeschlossen werden. Sie lauten wie folgt:

-   [**Iadsopendsobject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)
-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

In der folgenden Tabelle sind die Zuordnungen von ADSI VB/VSB-Code zu C++-Code aufgeführt. Beachten Sie, dass es sich hierbei nicht um eine komplette Liste handelt.



| VSB-Code                           | VC-Code                                                               |
|------------------------------------|-----------------------------------------------------------------------|
| Set obj = GetObject ()              | HR = ADsGetObject ()                                                   |
| obj. Legen Sie obj ab. "Obj" erhalten. Übergeordneten         | IADs oder IDirectoryObject                                              |
| obj. Erstellen Sie obj. Löschen Sie obj. Muvehere | IADsContainer                                                         |
| For each... in...                      | Adsbuildenvererator () adseneneratenext ()                               |
| Verbindung, Befehl, Recordset     | IDirectorySearch                                                      |
| Sicherheits Beschreibung, ACL, ACE      | IADsSecurityDescriptor, IADsAccessControlList, IADsAccessControlEntry |



 

 

 




