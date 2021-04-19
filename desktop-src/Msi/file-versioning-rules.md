---
description: Der Kern eines beliebigen Installers ist die eigentliche Installation von Dateien.
ms.assetid: e6f6d6a5-bdb0-4866-8d2c-56313d92c94c
title: Regeln für die Datei Versionsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c6f8e59b4f15774f898217690dbb1c4d57b1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359962"
---
# <a name="file-versioning-rules"></a>Regeln für die Datei Versionsverwaltung

Der Kern eines beliebigen Installers ist die eigentliche Installation von Dateien. Zu bestimmen, ob eine Datei installiert werden soll, ist ein komplexer Vorgang. Auf höchster Ebene hängt diese Bestimmung davon ab, ob die Komponente, zu der eine Datei gehört, für die Installation markiert ist. Nachdem festgestellt wurde, dass eine Datei kopiert werden soll, ist der Prozess kompliziert, wenn eine andere Datei mit demselben Namen im Zielordner vorhanden ist. In solchen Fällen erfordert die Bestimmung eines Satzes von Regeln, die die folgenden Eigenschaften einschließen:

-   Version
-   Date
-   Sprache

Das Installationsprogramm verwendet diese Regeln nur, wenn versucht wird, eine Datei an einem Speicherort zu installieren, der bereits eine Datei mit demselben Namen enthält. In diesem Fall verwendet die Windows Installer die folgenden Regeln, alle anderen Elemente sind gleich, um zu bestimmen, ob die Installation von erfolgt.

Höchste Version WINS – alle anderen Dinge, die gleich sind, die Datei mit der höchsten Version gewinnt, auch wenn die Datei auf dem Computer die höchste Version aufweist.

Dateien mit Versions Angabe gewinnen – eine Datei mit Versions Angabe wird über eine Datei mit Versions Angabe installiert.

Produktsprache bevorzugen – wenn die Datei, die installiert wird, eine andere Sprache als die Datei auf dem Computer hat, bevorzugen Sie die Datei mit der Sprache, die mit dem installierten Produkt übereinstimmt. Sprachneutrale Dateien werden nur als eine andere Sprache behandelt, sodass das Produkt, das installiert wird, erneut bevorzugt wird.

Mehrere Sprachen stimmen nicht überein – nachdem Sie alle allgemeinen Sprachen zwischen der zu installierenden Datei und der Datei auf dem Computer auskennen, werden alle verbleibenden Sprachen entsprechend den Anforderungen des installierten Produkts bevorzugt.

Übergeordnete Sprachen beibehalten – bewahren Sie die Datei auf, die mehrere Sprachen unterstützt, unabhängig davon, ob Sie sich bereits auf dem Computer befindet oder installiert wird.

Dateien mit nicht Versions Angabe sind Benutzerdaten – wenn das Änderungsdatum nach dem Erstellungsdatum der Datei auf dem Computer liegt, installieren Sie die Datei nicht, da Benutzeranpassungen gelöscht werden. Wenn das geänderte und das Create Date identisch sind, installieren Sie die-Datei. Wenn das Erstellungsdatum nach dem Änderungsdatum liegt, wird die Datei als unverändert angesehen, und die Datei wird installiert.

Die Installation einer [Begleit Datei](companion-files.md) ist nicht von ihren eigenen Datei Versionsinformationen abhängig, sondern von der Versionsverwaltung des zugehörigen übergeordneten Elements. Bei Begleit Dateien wird die Installation nur übersprungen, wenn die übergeordnete Datei eine höhere Version aufweist. Beachten Sie, dass es sich bei einer Datei, bei der es sich um den Schlüssel Pfad für Ihre Komponente handelt, nicht um eine Begleit Datei handeln darf, da dies dazu führt, dass die Versions Logik der Schlüssel Pfad Datei von der begleitenden übergeordneten Datei

Dateien mit nicht Versions Angabe mithilfe von [Begleit Dateien](companion-files.md): eine Datei mit Versions Angabe, die mit einer Datei mit Versions Angabe verknüpft ist, die den Begleit Mechanismus verwendet, hält die Regeln für die Datei mit Versions Angabe an. Die einzige Ausnahme besteht darin, dass die Datei mit Versions Angabe auf dem Computer und die installierte Datei mit Versions Angabe die gleiche Version und Sprache aufweisen, die Begleit Datei aber auf dem Computer fehlt. In diesem Fall wird die Datei, die installiert wird, auch dann verwendet, wenn die Datei mit Versions Angabe auf dem Computer verwendet wird. Außerdem wird eine Datei, die nicht mit Versions Angabe versehen ist, mit einer Begleit Datei installiert, wenn die Eigenschaft [**REINSTALLMODE**](reinstallmode.md) die Optionen ältere Versionen überschreiben ("o" oder "e") enthält und die Version der Begleit Datei mit einer Datei identisch ist, die sich bereits auf dem Computer befindet.

Regeln sind global – die Regeln, mit denen bestimmt wird, wann eine Datei installiert werden soll, sind innerhalb des Installers an einem Ort und Global, d. h., Sie gelten für alle Dateien gleichermaßen.

Beispiele für das Format, das für Dateiversionen verwendet wird, finden Sie unter dem Datentyp [Version](version.md) . Genauere Informationen finden Sie unter [Ersetzen vorhandener Dateien](replacing-existing-files.md) oder [Standarddatei Versions](default-file-versioning.md)Verwaltung.

 

 



