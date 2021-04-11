---
title: Auflisten von Replikaten einer Anwendungsverzeichnis Partition
description: In diesem Thema wird gezeigt, wie die Replikate für eine Anwendungsverzeichnis Partition aufgelistet werden.
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- Auflisten von Replikaten einer Anwendungsverzeichnis-Partitions Anzeige
- Anwendungsverzeichnis Partitionen AD, Enumerieren von Replikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1415c147fe4320e5f8169487a656db4f365f03a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948579"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>Auflisten von Replikaten einer Anwendungsverzeichnis Partition

Wenn ein Replikat einer Anwendungsverzeichnis Partition hinzugefügt wird, wird der Distinguished Name des [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) -Objekts für den Domänen Controller, der das Replikat enthalten wird, dem [**msDS-NC-Replikat-Locations-**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) Attribut des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts hinzugefügt. Das verwendete **CrossRef** -Objekt stellt die Anwendungsverzeichnis Partition dar.

**So zählen Sie die Replikate für eine Anwendungsverzeichnis Partition auf**

1.  Durchsuchen Sie den Container Partitionen nach einem [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekt, das einen [**NCName**](/windows/desktop/ADSchema/a-ncname) -Attribut Wert aufweist, der gleich dem Distinguished Name der Anwendungsverzeichnis Partition ist.
2.  Verwenden Sie jeden Wert des [**msDS-NC-Replica-Locations-**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) Attributs des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts, um eine Bindung mit dem [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) -Objekt des Servers herzustellen.
3.  Rufen Sie den ADsPath für das übergeordnete Element jedes [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) -Objekts ab. Dabei handelt es sich um ein Objekt, das den Domänen Controller Server darstellt. Verwenden Sie den ADsPath zum Binden an das Server Objekt.
4.  Rufen Sie den [**dNSHostName**](/windows/desktop/ADSchema/a-dnshostname) -Attribut Wert des Server Objekts ab. Dabei handelt es sich um eine Einzelwert Eigenschaft, die den DNS-Namen des Servers enthält.

Aufgrund der Replikations Latenz und geplanter KCC-laufzeitverzögerungen ist es möglich, dass die tatsächlichen aktiven Replikate für eine Anwendungsverzeichnis Partition nicht mit der Liste der Domänen Controller identisch sind, die durch das [**msDS-NC-Replica-Locations-**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) Attribut des [**CrossRef**](/windows/desktop/ADSchema/c-crossref) -Objekts angegeben werden. Eine genauere, aber weniger effiziente Methode zum Ermitteln der tatsächlichen aktiven Replikate einer Anwendungsverzeichnis Partition ist die Suche nach allen [**NTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) -Objekten in der Gesamtstruktur, die über ein [**msDS-hasmasterncs-**](/windows/desktop/ADSchema/a-msds-hasmasterncs) Attribut verfügen, das den Distinguished Name der Anwendungsverzeichnis Partition enthält. Das **msDS-hasmasterncs-** Attribut enthält die Distinguished Names aller beschreibbaren Verzeichnis Partitionen, die der Domänen Controller hostet, einschließlich der Anwendungsverzeichnis Partitionen.

 

 