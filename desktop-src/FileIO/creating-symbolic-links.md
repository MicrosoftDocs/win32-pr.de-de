---
description: Erstellen Sie symbolische Verknüpfungen, die einen absoluten oder relativen Pfad verwenden, indem Sie die Funktion "kreatesymboliclink" verwenden.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Erstellen von symbolischen Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c978532ffc11e44615d4de0ea902152438ecc7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347829"
---
# <a name="creating-symbolic-links"></a>Erstellen von symbolischen Verknüpfungen

Die Funktion " [**kreatesymboliclink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) " ermöglicht es Ihnen, symbolische Verknüpfungen mit einem absoluten oder relativen Pfad zu erstellen.

Symbolische Verknüpfungen können entweder absolute oder relative Links sein. Absolute Links sind Links, die jeden Teil des Pfadnamens angeben. relative Verknüpfungen werden relativ zu bestimmt, wo sich relative –-linkspezifier in einem angegebenen Pfad befinden. Relative Links werden mithilfe der folgenden Konventionen angegeben:

-   Punkt (. und..) Konventionen – z. b. ".. \\ " löst den Pfad relativ zum übergeordneten Verzeichnis auf.
-   Namen ohne Schrägstriche ( \) – z. b. "tmp" löst den Pfad relativ zum aktuellen Verzeichnis auf.
-   Root relative – beispielsweise wird " \\ Windows \\ system32" in das *aktuelle Laufwerk*: \\ Windows System32 aufgelöst \\ . directory
-   Aktuelles Arbeitsverzeichnis-relativ – wenn das aktuelle Arbeitsverzeichnis z. b. "c: \\ Windows \\ system32" ist, wird "C:File.txt" in "c: \\ Windows \\ system32 \\File.txt" aufgelöst.

    **Hinweis**  Wenn Sie ein Aktuelles Arbeitsverzeichnis angeben – relative Verknüpfung, wird es als absoluter Link erstellt, weil das aktuelle Arbeitsverzeichnis basierend auf dem Benutzer und dem Thread verarbeitet wird.

Eine symbolische Verknüpfung kann auch sowohl Verknüpfungs Punkte als auch eingebundene Ordner als Teil des Pfadnamens enthalten.

Symbolische Verknüpfungen können mithilfe des UNC-Pfads direkt auf eine Remote Datei oder ein Remote Verzeichnis verweisen.

Relative symbolische Verknüpfungen sind auf ein einzelnes Volume beschränkt.

## <a name="example-of-an-absolute-symbolic-link"></a>Beispiel für einen absoluten symbolischen Link

In diesem Beispiel enthält der ursprüngliche Pfad die Komponente "*x*", bei der es sich um einen absoluten symbolischen Link handelt. Wenn '*x*' gefunden wird, wird das Fragment des ursprünglichen Pfads bis zu und einschließlich '*x*' vollständig durch den Pfad ersetzt, auf den von '*x*' verwiesen wird. Der restliche Pfad nach "*x*" wird an diesen neuen Pfad angehängt. Dies wird jetzt zum geänderten Pfad.

X: "C: \\ alpha \\ Beta \\ abslink \\ Gamma \\ Datei"

Link: "abslink" ist " \\ \\ machineB \\ share" zugeordnet

Geänderter Pfad: " \\ \\ machineB \\ share \\ Gamma \\ file"

## <a name="example-of-a-relative-symbolic-links"></a>Beispiel für relative symbolische Verknüpfungen

In diesem Beispiel enthält der ursprüngliche Pfad die Komponente "*x*", bei der es sich um einen relativen symbolischen Link handelt. Wenn "*x*" gefunden wird, wird "*x*" vollständig durch das neue Fragment ersetzt, auf das von "*x*" gezeigt wird. Der restliche Pfad nach "*x*" wird an den neuen Pfad angehängt. Beliebige Punkte (..) in diesem neuen Pfad ersetzen Komponenten, die vor den Punkten (..) angezeigt werden. Jede Gruppe von Punkten ersetzt die vorangehende Komponente. Wenn die Anzahl der Punkte (..) die Anzahl der Komponenten überschreitet, wird ein Fehler zurückgegeben. Wenn alle Komponenten Ersetzung abgeschlossen ist, bleibt der abschließende, geänderte Pfad.

X: C: \\ alpha- \\ Beta \\ Link- \\ Gamma \\ Datei

Link: "Link" ist zugeordnet zu "... \\ . \\ Theta

Modifizierter Pfad: "C: \\ alpha \\ Beta \\ .. \\ . \\ Datei- \\ Gamma \\ Datei "

Abschließender Pfad: "C: die \\ \\ \\ Datei Gamma Datei"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Symbolische Verknüpfungen](symbolic-links.md)
</dt> <dt>

[Feste Links und Verbindungen](hard-links-and-junctions.md)
</dt> <dt>

[Benennen von Dateien, Pfaden und Namespaces](naming-a-file.md)
</dt> </dl>

 

 



