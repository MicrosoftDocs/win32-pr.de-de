---
description: So erhalten Sie mehr freien Speicherplatz, nachdem Sie das Kontingent Kontingent überschritten haben.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Verwaltung von Datenträger Kontingenten auf Benutzerebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356978"
---
# <a name="user-level-administration-of-disk-quotas"></a>Verwaltung von Datenträger Kontingenten auf Benutzerebene

Datenträger Kontingente sind für den Benutzer transparent. Wenn ein Benutzer fragt, wie viel Speicherplatz auf einem Datenträger frei ist, meldet das System nur die verfügbare Kontingent Menge, die dem Benutzer zur Verfügung steht. Wenn der Benutzer dieses Kontingent überschreitet, gibt das System den Fehler Datenträger " **\_ \_ vollständig** " zurück, so wie er darauf hindeuten würde, dass der Datenträger voll ist.

Der Benutzer muss einen der folgenden Schritte ausführen, um mehr freien Speicherplatz zu erhalten, nachdem das Kontingent Kontingent überschritten wurde:

-   Löschen Sie einige Dateien.
-   Einen anderen Benutzer beanspruchen den Besitz einiger Dateien.
-   Lassen Sie den Administrator das Kontingent Kontingent erhöhen.

Programme, die den tatsächlichen Umfang des freien Speicherplatzes abrufen müssen, können die [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) -Funktion aufrufen und den *totalnumoffreebytes* -Parameter überprüfen.

 

 



