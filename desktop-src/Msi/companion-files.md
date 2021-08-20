---
description: Der Installationsstatus einer Begleitdatei hängt nicht von ihren eigenen Versionsinformationen zur Dateiversion ab, sondern von der Versionierung des übergeordneten Begleitdatei.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Begleitdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d35aa89e216df4e17c84fb15c9c1f19908a74e9c1d14113da4df2128cdfb87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145099"
---
# <a name="companion-files"></a>Begleitdateien

Der Installationsstatus einer Begleitdatei hängt nicht von ihren eigenen Versionsinformationen zur Dateiversion ab, sondern von der Versionierung des übergeordneten Begleitdatei. Weitere Informationen finden [Sie unter Regeln für die Dateiversionsversion.](file-versioning-rules.md) Um eine Begleitdatei anzugeben, muss der Primärschlüssel des übergeordneten Begleitschlüssels in der Tabelle Datei in der Spalte Version des Datensatzes für den Begleitdatensatz verfasst werden. [](file-table.md)

Im folgenden Beispiel ist FileA das übergeordnete Element und FileB die Begleitdatei.

[Dateitabelle](file-table.md) (partiell)



| Datei  | Version |
|-------|---------|
| Filea | 1.0.0.0 |
| Fileb | Filea   |



 

In diesem Beispiel hängt der Installationsstatus [](file-versioning-rules.md) von FileB von den Dateiversionsregeln und den Versionsinformationen für FileA ab. Wenn das Installationsprogramm feststellt, dass die Version von FileA im Paket über eine ältere Version von FileA installiert werden soll, die bereits auf dem Computer des Benutzers vorhanden ist, installiert es auch FileB aus dem Paket, unabhängig von der Version der installierten FileB.

Beachten Sie, dass eine Datei, die der Schlüsselpfad für die Komponente ist, keine Begleitdatei sein darf. Dies würde dazu führen, dass die Versionslogik der Schlüsselpfaddatei von der übergeordneten Begleitdatei bestimmt wird.

 

 



