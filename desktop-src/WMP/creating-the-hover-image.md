---
title: Erstellen des Hover-Bilds
description: Erstellen des Hover-Bilds
ms.assetid: 169a99ba-96a0-4487-aa1c-07c83c0bc237
keywords:
- Erstellen von Skins, Hover-Bildern
- Windows Media Player Skins, Grafikdateien
- Skins, Art Dateien
- Dateien für Skins, Art
- kunstdateien für Skins, Hover-Bilder
- Windows Media Player Skins, Hover-Bilder
- Skins, Hover Bilder
- Bilder in Skins bewegen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d7f5bbb8b57820c2805b9b9d6ea79762933035
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309296"
---
# <a name="creating-the-hover-image"></a>Erstellen des Hover-Bilds

Das primäre Bild dieses Skin ist zwei Schaltflächen, die in einem Oval sitzen. Um dem Benutzer einen Hinweis zu geben, was zu tun ist, können Sie hover-Bilder hinzufügen. Dabei handelt es sich um alternative Bilder, die angezeigt werden, wenn der Benutzer mit der Maus auf eine Schaltfläche bewegt wird. Die Schaltflächen mit dem Mauszeiger enthalten außerdem die Symbole für das Abspielen und das Abbrechen von VCR-Steuerelementen, damit Benutzer genau wissen, was Sie tun können. Mithilfe von Hover-Bildern können Sie komplexe, selbst dokumentierende, künstlerische Skins erstellen.

Um das Hover-Bild zu erstellen, müssen Sie die beiden Schaltflächen, die Sie für die primäre Grafikdatei erstellt haben, in neue Ebenen kopieren und weitere Ebenen für den Text hinzufügen. Führen Sie die folgenden Schritte durch:

1.  Kopieren Sie die Schaltflächen Ebene schließen, und benennen Sie Sie "Close Hover" um.
2.  Verwenden Sie die Farbauswahl, um eine Vordergrundfarbe mit hellgelb ( \# CCFF33) zu erstellen. Dies wurde für den Gegensatz zu den Schaltflächen Farben ausgewählt. Verwenden Sie dann das Füllwerkzeug Tool, um die Innenseite des Kreises auf der Close-Hover-Ebene auszufüllen.
3.  Kopieren Sie die Wiedergabe Schaltfläche, und benennen Sie Sie in "Play Hover" um.
4.  Verwenden Sie das Füllwerkzeug Tool, um die Innenseite des Kreises in der Wiedergabe-Hover-Ebene mit derselben Farbe wie der Close-Hover-Kreis auszufüllen.
5.  Erstellen Sie eine neue Ebene, und nennen Sie Sie "Close Square". Verwenden Sie die Farbauswahl, um eine Vordergrundfarbe zu erstellen, die dunkelblau ist. Verwenden Sie das Stift Werkzeug, um ein Quadrat zu zeichnen, es in eine Auswahl umzuwandeln, es auszufüllen und den Pfad zu löschen. Verschieben Sie das Quadrat mithilfe des Verschiebungs Tools, und zentrieren Sie es über die Schaltfläche "Schließen".
6.  Erstellen Sie eine neue Ebene, und nennen Sie Sie "Play Triangle". Verwenden Sie das Stift Werkzeug, um das Dreieck für "Play" mit denselben Techniken zu erstellen, die Sie zum Erstellen der quadratischen Ebene "Schließen" verwendet haben. Zentrieren Sie Sie über die Schaltfläche "wiedergeben"

Sie sind jetzt bereit, die Hover-Art-Datei zu erstellen. Blenden Sie alle Ebenen aus, und zeigen Sie in dieser Reihenfolge (von oben nach unten) nur die folgenden Ebenen an:

Dreiecks Wiedergabe

Quadrat schließen

Maus spielen

Mauszeiger schließen

Speichern Sie die Datei in einer neuen Datei, indem Sie im Menü Datei den Befehl Kopie speichern verwenden. Wählen Sie im Bereich speichern als des Dialog Felds Kopie speichern die Option BMP aus, und geben Sie einen Dateinamen ein, auf den Sie später in der Skin-Definitionsdatei verweisen werden. Im Idealfall sollten Sie diese im gleichen Verzeichnis speichern wie Ihre Skin-Definitionsdatei. Beispielsweise können Sie diese hover.bmp nennen. Wählen Sie die Standardeinstellungen aus, und speichern Sie die Datei.

Ihre Hover-Kunst Datei sollte wie in der folgenden Abbildung aussehen.

![Bild mit Hover](images/absam01h.png)

Die Gelbe Schaltfläche mit dem Mauszeiger wird anstelle der normalen Schaltfläche angezeigt. Wenn Sie den Mauszeiger über die Rechte Schaltfläche in der Skin bewegen, wird die Gelbe Schaltfläche mit der Bezeichnung "Play" angezeigt, und wenn Sie auf die linke Schaltfläche zeigen, wird dem Benutzer "Schließen" angezeigt. Die beiden hover-Bilder werden nie gleichzeitig angezeigt, da die Maus nicht gleichzeitig auf beide Schaltflächen zeigen kann. Sie müssen auf den Mauszeiger zeigen und eine Hover-Art-Datei haben, die den Bereichen der Zuordnungsdateien zu Bereichen der Hover-Datei entspricht.

Wenn Sie die Datei speichern, wird der von Ihnen gewählte Dateiname später als Wert für das **hoverimage** -Attribut des **ButtonGroup** -Elements in der Skin-Definitionsdatei verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aufbauen Ihrer ersten Skin**](building-your-first-skin.md)
</dt> </dl>

 

 




