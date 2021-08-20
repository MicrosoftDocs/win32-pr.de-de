---
description: Der Systemadministrator kann Kontingente für bestimmte Benutzer auf einem Volume festlegen. Der Administrator kann auch Standardkontingente für das Volume festlegen.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Verwaltung von Datenträgerkontingenten auf Systemebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2465d082ff93ee6a4ef02351e17e6b1214d005dc1d13be27f83db89e78c6bcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996417"
---
# <a name="system-level-administration-of-disk-quotas"></a>Verwaltung von Datenträgerkontingenten auf Systemebene

Der Systemadministrator kann Kontingente für bestimmte Benutzer auf einem Volume festlegen. Der Administrator kann auch Standardkontingente für das Volume festlegen. Ein neuer Benutzer auf dem Volume erhält das Standardkontingent, es sei denn, der Administrator hat ein Kontingent speziell für diesen Benutzer eingerichtet.

Der Administrator kann die Ebene der Kontingentnachverfolgung und -erzwingung (oder Kontingentzustände), die Standardkontingentgrenzen und die Benutzerkontingentinformationen abfragen. Die Kontingentinformationen pro Benutzer enthalten die harte Kontingentgrenze des Benutzers, den Warnungsschwellenwert und die Kontingentnutzung. Der Administrator kann auch die Kontingenterzwingung aktivieren oder deaktivieren.

Es gibt drei Kontingentzustände, wie in der folgenden Tabelle gezeigt.



| State          | Beschreibung                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kontingent deaktiviert | Änderungen der Kontingentnutzung werden nicht nachverfolgt, aber die Kontingentgrenzen werden nicht entfernt. In diesem Zustand wird die Leistung durch Datenträgerkontingente nicht beeinträchtigt. Dies ist die Standardeinstellung.                         |
| Nachverfolgte Kontingente  | Änderungen der Kontingentnutzung werden nachverfolgt, aber Kontingentgrenzen werden nicht erzwungen. In diesem Zustand werden keine Kontingentverletzungsereignisse generiert, und dateivorgänge können aufgrund von Datenträgerkontingentverletzungen nicht fehlschlagen. |
| Erzwungenes Kontingent | Änderungen der Kontingentnutzung werden nachverfolgt, und Kontingentgrenzen werden erzwungen.                                                                                                                           |



 

 

 



