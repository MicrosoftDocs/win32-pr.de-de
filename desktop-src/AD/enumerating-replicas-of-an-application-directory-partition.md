---
title: Aufzählen von Replikaten einer Anwendungsverzeichnispartition
description: In diesem Thema wird gezeigt, wie die Replikate für eine Anwendungsverzeichnispartition aufzählt werden.
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- Aufzählen von Replikaten einer Anwendungsverzeichnispartitions-AD
- Application Directory Partitions AD , Aufzählen von Replikaten von
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52ff0ea5c2b4737079f4a44997f39dd027299f50c8acd96fe0456b0e5b60d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694887"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>Aufzählen von Replikaten einer Anwendungsverzeichnispartition

Wenn ein Replikat einer Anwendungsverzeichnispartition hinzugefügt wird, wird der Distinguished Name des [**nTDSDSA-Objekts**](/windows/desktop/ADSchema/c-ntdsdsa) für den Domänencontroller, der das Replikat enthalten soll, dem [**msDS-NC-Replica-Locations-Attribut**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) des [**crossRef-Objekts**](/windows/desktop/ADSchema/c-crossref) hinzugefügt. Das **verwendete crossRef-Objekt** stellt die Anwendungsverzeichnispartition dar.

**So enumerieren Sie die Replikate für eine Anwendungsverzeichnispartition**

1.  Suchen Sie im Container Partitionen nach einem [**crossRef-Objekt,**](/windows/desktop/ADSchema/c-crossref) das über einen [**nCName-Attributwert**](/windows/desktop/ADSchema/a-ncname) verfügt, der dem Distinguished Name der Anwendungsverzeichnispartition entspricht.
2.  Verwenden Sie jeden Wert des [**msDS-NC-Replica-Locations-Attributs**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) des [**crossRef-Objekts,**](/windows/desktop/ADSchema/c-crossref) um eine Bindung an das [**nTDSDSA-Objekt**](/windows/desktop/ADSchema/c-ntdsdsa) des Servers herzustellen.
3.  Abrufen des ADsPath für das übergeordnete Element jedes [**nTDSDSA-Objekts.**](/windows/desktop/ADSchema/c-ntdsdsa) Dies ist ein Objekt, das den Domänencontrollerserver darstellt. Verwenden Sie ADsPath, um eine Bindung an das Serverobjekt herzustellen.
4.  Abrufen des [**dNSHostName-Attributwerts**](/windows/desktop/ADSchema/a-dnshostname) des Serverobjekts. Dies ist eine Einzelwerteigenschaft, die den DNS-Namen des Servers enthält.

Aufgrund der Replikationslatenz und geplanten KCC-Ausführungsverzögerungen ist es möglich, dass die tatsächlich aktiven Replikate für eine Anwendungsverzeichnispartition möglicherweise nicht mit der Liste der Domänencontroller übereinstimmen, die durch das [**msDS-NC-Replica-Locations-Attribut**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) des [**crossRef-Objekts**](/windows/desktop/ADSchema/c-crossref) angegeben wird. Eine genauere, aber weniger effiziente Möglichkeit, die tatsächlichen aktiven Replikate einer Anwendungsverzeichnispartition zu ermitteln, besteht in der Suche nach allen [**nTDSDSA-Objekten**](/windows/desktop/ADSchema/c-ntdsdsa) in der Gesamtstruktur, die über ein [**msDS-hasMasterNCs-Attribut**](/windows/desktop/ADSchema/a-msds-hasmasterncs) verfügen, das den Distinguished Name der Anwendungsverzeichnispartition enthält. Das **attribut msDS-hasMasterNCs** enthält die Distinguished Names aller beschreibbaren Verzeichnispartitionen, die der Domänencontroller hostet, einschließlich Anwendungsverzeichnispartitionen.

 

 