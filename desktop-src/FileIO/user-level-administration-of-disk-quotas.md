---
description: Erfahren Sie, wie Sie nach überschreiten des Kontingentkontingents mehr freien Speicherplatz erhalten.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Verwaltung von Datenträgerkontingenten auf Benutzerebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214f1fb915d199ff6db3a6b3084c5c0f6f2df5c9737290fbdaa0e977a1163f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914360"
---
# <a name="user-level-administration-of-disk-quotas"></a>Verwaltung von Datenträgerkontingenten auf Benutzerebene

Datenträgerkontingente sind für den Benutzer transparent. Wenn ein Benutzer fragt, wie viel Speicherplatz auf einem Datenträger frei ist, meldet das System nur das verfügbare Kontingent, das dem Benutzer zur Verfügung steht. Wenn der Benutzer diese Überschreitung überschreitet, gibt das System den Fehler **ERROR \_ DISK \_ FULL** zurück, so wie er angibt, dass der Datenträger voll ist.

Um nach überschreiten des Kontingentkontingents mehr freien Speicherplatz zu erhalten, muss der Benutzer einen der folgenden Schritte unternehmen:

-   Löschen Sie einige Dateien.
-   Besitz einiger Dateien durch einen anderen Benutzer beanspruchen.
-   Der Administrator muss das Kontingent erhöhen.

Programme, die die tatsächliche Menge an freiem Speicherplatz abrufen müssen, können die [**GetDiskFreeSpaceEx-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) aufrufen und den *TotalNumberOfFreeBytes-Parameter* betrachten.

 

 



