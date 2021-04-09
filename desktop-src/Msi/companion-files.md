---
description: Der Installationsstatus einer Begleit Datei hängt nicht von den eigenen Datei Versionsinformationen, sondern von der Versionsverwaltung des zugehörigen übergeordneten Elements ab.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Begleit Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960269"
---
# <a name="companion-files"></a>Begleit Dateien

Der Installationsstatus einer Begleit Datei hängt nicht von den eigenen Datei Versionsinformationen, sondern von der Versionsverwaltung des zugehörigen übergeordneten Elements ab. Sehen Sie sich die Regeln für die [Datei Versions](file-versioning-rules.md)Verwaltung an. Um eine Begleit Datei anzugeben, muss der Primärschlüssel des übergeordneten Elements in der [Dateitabelle](file-table.md) in der Versions Spalte des Datensatzes für den begleitenden erstellt werden.

Im folgenden Beispiel ist fileA das übergeordnete Element, und fileB ist die Begleit Datei.

[Dateitabelle](file-table.md) (partiell)



| File  | Version |
|-------|---------|
| Mit der | 1.0.0.0 |
| FileB | Mit der   |



 

In diesem Beispiel hängt der Installationsstatus von fileB von den Regeln für die [Datei Versions](file-versioning-rules.md) Verwaltung und den Versionsinformationen für fileA ab. Wenn das Installationsprogramm feststellt, dass die Version von fileA im Paket über eine ältere Version von fileA installiert werden soll, die bereits auf dem Computer des Benutzers vorhanden ist, wird fileB unabhängig von der Version der installierten fileB aus dem Paket installiert.

Beachten Sie, dass es sich bei einer Datei, die den Schlüssel Pfad für Ihre Komponente ist, nicht um eine Begleit Datei handeln darf. Dies würde dazu führen, dass die versionierungslogik der Schlüssel Pfad Datei von der begleitenden übergeordneten Datei bestimmt wird.

 

 



