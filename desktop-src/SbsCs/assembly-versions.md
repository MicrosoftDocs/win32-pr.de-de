---
description: Jede parallele Assembly muss eine Version aufweisen.
ms.assetid: 0b78ecf6-fbff-4172-9b0d-09f993666db1
title: Assemblyversionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c9e32ecc0990572f17264edd2ff51c205a01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757315"
---
# <a name="assembly-versions"></a>Assemblyversionen

Jede parallele Assembly muss eine Version aufweisen. Jede Assemblyversion ist einer Versionsnummer zugeordnet, die vier Teile durch Punkte trennt: *Major. Minor. Build. Revision*. Wenn eine Assembly geändert wird, sodass Sie mit den vorhandenen Versionen nicht kompatibel ist, müssen die *Haupt* -oder *nebenteile* der Versionsnummer geändert werden. Eine Versionsnummer, die nur in den *Build* -oder *Revisions* Teilen geändert wird, gibt an, dass die Assembly abwärts kompatibel mit früheren Versionen ist.

Die Version muss in **assemblyIdentity** -Elementen der [Manifeste](manifests.md)angegeben werden. Verwenden Sie das vierteilige Versions Format: mmmmm. nnnnn. Ooooo. ppppp. Alle durch Zeiträume getrennten Teile können 0-65535 einschließlich sein.

 

 



