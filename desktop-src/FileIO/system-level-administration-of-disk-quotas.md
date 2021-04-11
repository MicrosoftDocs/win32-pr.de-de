---
description: Der Systemadministrator kann Kontingente für bestimmte Benutzer auf einem Volume festlegen. Der Administrator kann auch Standard Kontingente für das Volume festlegen.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Verwaltung von Datenträger Kontingenten auf System Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214766"
---
# <a name="system-level-administration-of-disk-quotas"></a>Verwaltung von Datenträger Kontingenten auf System Ebene

Der Systemadministrator kann Kontingente für bestimmte Benutzer auf einem Volume festlegen. Der Administrator kann auch Standard Kontingente für das Volume festlegen. Ein neuer Benutzer auf dem Volume erhält das Standard Kontingent, es sei denn, der Administrator hat ein speziell für diesen Benutzerspezifisches Kontingent festgelegt.

Der Administrator kann die Ebene der Kontingent Nachverfolgung und Erzwingung (oder Kontingent Status), die Standard Kontingent Limits und die Kontingent Informationen pro Benutzer Abfragen. Die Kontingent Informationen pro Benutzer enthalten die feste Kontingent Grenze, den Warnungs Schwellenwert und die Kontingent Nutzung des Benutzers. Der Administrator kann die Kontingent Erzwingung auch aktivieren oder deaktivieren.

Es gibt drei Kontingent Zustände, wie in der folgenden Tabelle dargestellt.



| State          | BESCHREIBUNG                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kontingent deaktiviert | Kontingent Nutzungsänderungen werden nicht nachverfolgt, die Kontingent Limits werden jedoch nicht entfernt. In diesem Zustand wird die Leistung von Datenträger Kontingenten nicht beeinträchtigt. Dies ist die Standardeinstellung.                         |
| Kontingent nachverfolgt  | Kontingent Nutzungsänderungen werden nachverfolgt, aber Kontingent Limits werden nicht erzwungen. In diesem Zustand werden keine Kontingent Verletzungs Ereignisse generiert, und es sind keine Datei Vorgänge aufgrund von Datenträger Kontingent Verstößen fehlgeschlagen. |
| Kontingent erzwungen | Kontingent Nutzungsänderungen werden nachverfolgt, und Kontingent Limits werden erzwungen.                                                                                                                           |



 

 

 



