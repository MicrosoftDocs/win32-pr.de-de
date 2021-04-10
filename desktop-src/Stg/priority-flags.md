---
title: Prioritätsflags
description: Das Prioritäts Kennzeichen öffnet ein Speicher Objekt im Prioritäts Modus.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Prioritätsflags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037645"
---
# <a name="priority-flags"></a>Prioritätsflags

Das Prioritäts Kennzeichen öffnet ein Speicher Objekt im Prioritäts Modus. Wenn ein Objekt geöffnet wird, kann eine Anwendung in der Regel mit einer Momentaufnahme Kopie verwendet werden, da andere Anwendungen möglicherweise auch das Objekt gleichzeitig verwenden. Wenn Sie ein Speicher Objekt im Prioritäts Modus öffnen, verfügt die Anwendung jedoch über exklusive Rechte, um Änderungen am Objekt zu übertragen.

Der Prioritäts Modus ermöglicht einer Anwendung, einige Datenströme aus dem Speicher zu lesen, bevor das Objekt in einem Modus geöffnet wird, in dem das System eine Momentaufnahme Kopie erstellen muss. Da die Anwendung exklusiven Zugriff hat, muss Sie keine Momentaufnahme Kopie des-Objekts erstellen. Wenn die Anwendung das Objekt anschließend in einem Modus öffnet, in dem eine Momentaufnahme Kopie erforderlich ist, kann die Anwendung die Datenströme ausschließen, die Sie bereits aus der Momentaufnahme gelesen hat, wodurch der Aufwand für das Öffnen des Objekts reduziert wird.

Da andere Anwendungen keine Änderungen an einem Objekt ausführen können, während es im Prioritäts Modus geöffnet ist, sollten Anwendungen das Objekt so kurz wie möglich in diesem Modus belassen.

 

 




