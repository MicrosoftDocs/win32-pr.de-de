---
description: Erstellen Sie symbolische Verknüpfungen, die entweder einen absoluten oder relativen Pfad verwenden, indem Sie die CreateSymbolicLink-Funktion verwenden.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Erstellen symbolischer Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0340dc362ff550ab2d74e533ac66e74622c965266440103d6f6ec155bfa80f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150856"
---
# <a name="creating-symbolic-links"></a>Erstellen symbolischer Verknüpfungen

Mit der [**Funktion CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) können Sie symbolische Verknüpfungen mit einem absoluten oder relativen Pfad erstellen.

Symbolische Verknüpfungen können entweder absolute oder relative Verknüpfungen sein. Absolute Links sind Links, die jeden Teil des Pfadnamens angeben. Relative Links werden relativ dazu bestimmt, wo sich relative-link-Spezifizierer in einem angegebenen Pfad befinden. Relative Links werden mithilfe der folgenden Konventionen angegeben:

-   Punkt (. und ..) -Konventionen, z. B. \\ ".." löst den Pfad relativ zum übergeordneten Verzeichnis auf.
-   Namen ohne Schrägstriche ( ) – beispielsweise löst "tmp" den Pfad \\ relativ zum aktuellen Verzeichnis auf.
-   Root relative – z.B. wird \\ "Windows System32" in das aktuelle Laufwerk \\ " : Windows \\ \\ System32" auflösen. directory
-   Aktuelles Arbeitsverzeichnis relativ– Wenn das aktuelle Arbeitsverzeichnis beispielsweise "C: \\ Windows \\ System32" ist, wird "C:File.txt" in "C: \\ Windows \\ System32 \\File.txt" auflösen.

    **Hinweis:**  Wenn Sie einen aktuellen Arbeitsverzeichnis-relativ-Link angeben, wird er aufgrund der Art und Weise, wie das aktuelle Arbeitsverzeichnis basierend auf dem Benutzer und dem Thread verarbeitet wird, als absoluter Link erstellt.

Eine symbolische Verknüpfung kann auch Sowohl Verbindungspunkte als auch bereitgestellte Ordner als Teil des Pfadnamens enthalten.

Symbolische Verknüpfungen können mithilfe des UNC-Pfads direkt auf eine Remotedatei oder ein Remoteverzeichnis verweisen.

Relative symbolische Verknüpfungen sind auf ein einzelnes Volume beschränkt.

## <a name="example-of-an-absolute-symbolic-link"></a>Beispiel für eine absolute symbolische Verknüpfung

In diesem Beispiel enthält der ursprüngliche Pfad die Komponente *"x",* die eine absolute symbolische Verknüpfung ist. Wenn '*x*' gefunden wird, wird das Fragment des ursprünglichen Pfads bis einschließlich '*x*' vollständig durch den Pfad ersetzt, auf den durch '*x*' verwiesen wird. Der Rest des Pfads nach '*x*' wird an diesen neuen Pfad angefügt. Dies wird jetzt zum geänderten Pfad.

X: "C: \\ alpha \\ beta \\ absLink gamma \\ \\ file"

Link: "absLink" wird \\ \\ "machineB \\ share"

Geänderter Pfad: " \\ \\ machineB \\ share \\ gamma \\ file"

## <a name="example-of-a-relative-symbolic-links"></a>Beispiel für relative symbolische Verknüpfungen

In diesem Beispiel enthält der ursprüngliche Pfad die Komponente *"x",* bei der es sich um eine relative symbolische Verknüpfung handelt. Wenn '*x*' gefunden wird, wird '*x*' vollständig durch das neue Fragment ersetzt, auf das durch '*x*' verwiesen wird. Der Rest des Pfads nach '*x*' wird an den neuen Pfad angefügt. Alle Punkte (..) in diesem neuen Pfad ersetzen Komponenten, die vor den Punkten (..) angezeigt werden. Jeder Satz von Punkten ersetzt die vorangehende Komponente. Wenn die Anzahl der Punkte (..) die Anzahl der Komponenten überschreitet, wird ein Fehler zurückgegeben. Andernfalls bleibt der letzte geänderte Pfad erhalten, wenn der Komponentenaustausch abgeschlossen ist.

X: C: \\ Alpha beta link gamma \\ \\ \\ \\ file

Link: "link" ist ".. \\ .. \\ theta"

Geänderter Pfad: "C: \\ alpha \\ beta \\ .. \\ .. \\ theta \\ gamma \\ file"

Final Path: "C: \\ theta \\ gamma \\ file"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Symbolische Verknüpfungen](symbolic-links.md)
</dt> <dt>

[Harte Links und Verknüpfungen](hard-links-and-junctions.md)
</dt> <dt>

[Benennen von Dateien, Pfaden und Namespaces](naming-a-file.md)
</dt> </dl>

 

 



