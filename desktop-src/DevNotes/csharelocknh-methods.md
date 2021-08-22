---
description: Eine Gruppe von Methoden, die zum Bearbeiten von Sperren verwendet wird.
ms.assetid: ba4cc37c-bd2f-446f-8b3d-bc2a2e2e4de4
title: CShareLockNH-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97234d65a3be75ffc1eb679db31360aa6ce6c416d879c67c0ffc5385e10bdb49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654650"
---
# <a name="csharelocknh-methods"></a>CShareLockNH-Methoden

Eine Gruppe von Methoden, die zum Bearbeiten von Sperren verwendet wird.

## <a name="methods"></a>Methoden

Die folgenden Methoden werden von Rwnh.dll exportiert.



| Methode                                                                   | Beschreibung                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**ExclusiveLock**](csharelocknh--exclusivelock.md)                     | Er erhält eine Reader-/Writersperre.                                  |
| [**ExclusiveToPartial**](csharelocknh--exclusivetopartial.md)           | Ändert den Zustand.                                              |
| [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)                 | Gibt eine Sperre frei.                                                |
| [**FirstPartialToExclusive**](csharelocknh--firstpartialtoexclusive.md) | Wird beim Konvertieren einer partiellen Sperre in eine exklusive Sperre verwendet.         |
| [**PartialLock**](csharelocknh--partiallock.md)                         | Verhindert, dass mehrere Threads das Abrufen einer Sperre abschließen. |
| [**PartialUnlock**](csharelocknh--partialunlock.md)                     | Gibt eine Teilsperre frei.                                        |
| [**ShareLock**](csharelocknh--sharelock.md)                             | Ruft eine Sperre für den freigegebenen Modus ab.                                 |
| [**ShareUnlock**](csharelocknh--shareunlock.md)                         | Gibt eine Sperre aus dem freigegebenen Modus frei.                               |
| [**SharedToPartial**](csharelocknh--sharedtopartial.md)                 | Ruft eine partielle Sperre ab.                                         |
| [**TryExclusiveLock**](csharelocknh--tryexclusivelock.md)               | Ruft ausschließlich eine Sperre ab.                                     |



 

 

 



