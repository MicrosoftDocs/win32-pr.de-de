---
description: Erstellen Sie symbolische Verknüpfungen, die entweder einen absoluten oder relativen Pfad verwenden, indem Sie die CreateSymbolicLink-Funktion verwenden.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Erstellen symbolischer Verknüpfungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252b999b05004fd7735b16582783ef0c3afb0013
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387706"
---
# <a name="creating-symbolic-links"></a>Erstellen symbolischer Verknüpfungen

Mit der [**Funktion CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) können Sie symbolische Verknüpfungen mit einem absoluten oder relativen Pfad erstellen.

Symbolische Verknüpfungen können entweder absolute oder relative Links sein. Absolute Links sind Links, die jeden Teil des Pfadnamens angeben. Relative Links werden relativ dazu bestimmt, wo sich relative-link-Spezifizierer in einem angegebenen Pfad befinden. Relative Links werden mit den folgenden Konventionen angegeben:

-   Punkt (. und ..) -Konventionen, z. B. ".. \\ " löst den Pfad relativ zum übergeordneten Verzeichnis auf.
-   Namen ohne Schrägstriche ( \\ ), z.B. "tmp" löst den Pfad relativ zum aktuellen Verzeichnis auf.
-   Root relative, z.B. " \\ Windows \\ System32" wird in das *"aktuelle Laufwerk*: \\ Windows \\ System32" aufgelöst. directory
-   Aktuelles Arbeitsverzeichnis relativ: Wenn das aktuelle Arbeitsverzeichnis z. B. "C: \\ Windows \\ System32" lautet, wird "C:File.txt" in "C: \\ Windows \\ System32 \\File.txt" aufgelöst.

    **Hinweis**  Wenn Sie einen aktuellen Link vom Typ Arbeitsverzeichnis –relativ angeben, wird er aufgrund der Verarbeitung des aktuellen Arbeitsverzeichnisses basierend auf dem Benutzer und dem Thread als absoluter Link erstellt.

Eine symbolische Verknüpfung kann auch Verbindungspunkte und bereitgestellte Ordner als Teil des Pfadnamens enthalten.

Symbolische Verknüpfungen können mithilfe des UNC-Pfads direkt auf eine Remotedatei oder ein Remoteverzeichnis verweisen.

Relative symbolische Verknüpfungen sind auf ein einzelnes Volume beschränkt.

## <a name="example-of-an-absolute-symbolic-link"></a>Beispiel für einen absoluten symbolischen Link

In diesem Beispiel enthält der ursprüngliche Pfad die Komponente "*x*", die eine absolute symbolische Verknüpfung ist. Wenn *"x"* gefunden wird, wird das Fragment des ursprünglichen Pfads bis einschließlich *"x"* vollständig durch den Pfad ersetzt, auf den *"x"* zeigt. Der Rest des Pfads nach "*x*" wird an diesen neuen Pfad angefügt. Dies wird nun zum geänderten Pfad.

X: "C: \\ alpha \\ beta \\ absLink gamma \\ \\ file"

Link: "absLink" wird \\ \\ "machineB \\ share" zugeordnet.

Geänderter Pfad: \\ \\ "machineB \\ share \\ gamma \\ file"

## <a name="example-of-a-relative-symbolic-links"></a>Beispiel für relative symbolische Verknüpfungen

In diesem Beispiel enthält der ursprüngliche Pfad eine Komponente "*x*", die eine relative symbolische Verknüpfung ist. Wenn '*x*' gefunden wird, wird '*x*' vollständig durch das neue Fragment ersetzt, auf das von '*x*' gezeigt wird. Der Rest des Pfads nach '*x*' wird an den neuen Pfad angefügt. Alle Punkte (..) in diesem neuen Pfad ersetzen Komponenten, die vor den Punkten (..) angezeigt werden. Jeder Satz von Punkten ersetzt die vorangehende Komponente. Wenn die Anzahl der Punkte (..) die Anzahl der Komponenten überschreitet, wird ein Fehler zurückgegeben. Andernfalls verbleibt der letzte geänderte Pfad, wenn der Austausch aller Komponenten abgeschlossen ist.

X: C: \\ Alpha beta link gamma \\ \\ \\ \\ file

Link: "link" entspricht ".. \\ .. \\ theta"

Geänderter Pfad: "C: \\ alpha \\ beta \\ .. \\ .. \\ theta \\ gamma \\ file"

Endgültiger Pfad: "C: \\ theta \\ gamma \\ file"

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Symbolische Verknüpfungen](symbolic-links.md)
</dt> <dt>

[Hard Links and Junctions](hard-links-and-junctions.md)
</dt> <dt>

[Benennen von Dateien, Pfaden und Namespaces](naming-a-file.md)
</dt> </dl>

 

 



