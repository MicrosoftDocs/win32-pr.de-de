---
description: Jede nebenseitige Assembly muss eine Version haben.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Assemblyversionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e555035bf7b43f53d3a68f249005928867f453b78522f70dd45f3b5379c75e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885570"
---
# <a name="assembly-versions"></a>Assemblyversionen

Jede nebenseitige Assembly muss eine Version haben. Jede Assemblyversion ist einer Versionsnummer zugeordnet, die aus vier Teilen besteht, die durch Punkte getrennt sind: *major.minor.build.revision*. Wenn eine Änderung an einer Assembly vorgenommen wird,  die  sie inkompatibel mit vorhandenen Versionen macht, müssen die Haupt- oder Nebenteile der Versionsnummer geändert werden. Eine Versionsnummer, die  sich nur in den Build- oder *Revisionsteilen* ändert, gibt an, dass die Assembly abwärtskompatibel mit früheren Versionen ist.

Die Version muss in **assemblyIdentity-Elementen** von [Manifesten angegeben werden.](manifests.md) Verwenden Sie das vierteilige Versionsformat mmmmm.nnnnn.ooooo.ooooo.oopp. Jeder durch Punkte getrennte Teil kann 0 bis 65535 einschließlich sein.

 

 



