---
description: Der Kern jedes Installationsprogramms ist die eigentliche Installation von Dateien.
ms.assetid: e6f6d6a5-bdb0-4866-8d2c-56313d92c94c
title: Regeln für die Dateiversionsierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8dfda6a909450ba45cc213016a159bbbc8f9a54b958c7d4e37d051fd86935ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828980"
---
# <a name="file-versioning-rules"></a>Regeln für die Dateiversionsierung

Der Kern jedes Installationsprogramms ist die eigentliche Installation von Dateien. Das Bestimmen, ob eine Datei installiert werden soll, ist ein komplexer Prozess. Auf der höchsten Ebene hängt diese Bestimmung davon ab, ob die Komponente, zu der eine Datei gehört, für die Installation markiert ist. Nachdem festgestellt wurde, dass eine Datei kopiert werden soll, ist der Prozess kompliziert, wenn eine andere Datei mit dem gleichen Namen im Zielordner vorhanden ist. In solchen Situationen erfordert die Bestimmung einen Satz von Regeln mit den folgenden Eigenschaften:

-   Version
-   Date
-   Sprache

Das Installationsprogramm verwendet diese Regeln nur, wenn versucht wird, eine Datei an einem Speicherort zu installieren, der bereits eine Datei mit dem gleichen Namen enthält. In diesem Fall verwendet der Windows Installer die folgenden Regeln, wobei alle anderen Dinge gleich sind, um zu bestimmen, ob installiert werden soll.

Höchste Version gewinnt– Alle anderen Punkte, die gleich sind, gewinnt die Datei mit der höchsten Version, auch wenn die Datei auf dem Computer die höchste Version aufwies.

Versionsierte Dateien Win: Eine Datei mit Versionsversion wird über eine Nichtversionsdatei installiert.

Produktsprache bevorzugen: Wenn die zu installierende Datei eine andere Sprache als die Datei auf dem Computer hat, bevorzugen Sie die Datei mit der Sprache, die dem installierten Produkt entspricht. Sprachneutrale Dateien werden als eine andere Sprache behandelt, sodass das zu installierende Produkt wieder bevorzugt wird.

Nicht übereinstimmende mehrere Sprachen: Nachdem alle gängigen Sprachen zwischen der installierten Datei und der Datei auf dem Computer herausgegrenzt wurden, werden alle verbleibenden Sprachen entsprechend dem bevorzugt, was für das zu installierende Produkt erforderlich ist.

Übergeordnete Sprachen beibehalten: Behalten Sie die Datei bei, die mehrere Sprachen unterstützt, unabhängig davon, ob sie sich bereits auf dem Computer befindet oder installiert wird.

Nichtversionierte Dateien sind Benutzerdaten: Wenn das Geänderte Datum nach dem Erstellungsdatum für die Datei auf dem Computer liegt, installieren Sie die Datei nicht, da Benutzeranpassungen gelöscht würden. Wenn die Datumsangaben Geändert und Erstellen identisch sind, installieren Sie die Datei. Wenn das Erstellungsdatum nach dem Änderungsdatum liegt, wird die Datei als unverändert betrachtet. Installieren Sie die Datei.

Die Installation einer [Begleitdatei](companion-files.md) hängt nicht von eigenen Informationen zur Dateiversionsversionsierung ab, sondern von der Versionsangabe des zugehörigen übergeordneten Elements. Im Fall von Begleitdateien wird die Installation nur übersprungen, wenn die übergeordnete Datei über eine höhere Version verfügt. Beachten Sie, dass eine Datei, die der Schlüsselpfad für ihre Komponente ist, keine Begleitdatei sein darf, da dies dazu führt, dass die Versionslogik der Schlüsselpfaddatei von der übergeordneten Begleitdatei bestimmt wird.

Nichtversionierte Dateien mit [Begleitdateien:](companion-files.md)Eine Nichtversionsdatei, die mithilfe des Begleitmechanismus einer Datei mit Versionsveränderung zugeordnet ist und die Regeln für die Datei mit Versionsversionen erfüllt. Die einzige Ausnahme besteht darin, dass die Datei mit Versionsbelegung auf dem Computer und die installierte Datei mit Versionsversion die gleiche Version und Sprache aufweisen, aber die Begleitdatei auf dem Computer fehlt. In diesem Fall wird die begleite Datei verwendet, die installiert wird, obwohl die Datei mit Versionsfreigabe auf dem Computer verwendet wird. Darüber hinaus wird eine Nichtversionsdatei mit einer Begleitdatei installiert, wenn die [**REINSTALLMODE-Eigenschaft**](reinstallmode.md) die Optionen für ältere Versionen ("o" oder "e") enthält und die Version der Begleitdatei gleich einer Datei ist, die sich bereits auf dem Computer befindet.

Regeln sind global: Die Regeln zum Bestimmen, wann eine Datei installiert werden soll, befinden sich an einem Ort im Installationsprogramm und sind global, d. h. sie gelten für alle Dateien gleichermaßen.

Beispiele für das Format, das für [](version.md) Dateiversionen verwendet wird, finden Sie unter Versionsdatentyp. Ausführlichere Informationen finden Sie unter [Ersetzen vorhandener Dateien](replacing-existing-files.md) oder [Standarddateiversionsierung.](default-file-versioning.md)

 

 



