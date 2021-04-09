---
title: Animations Design
description: Animations Design
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7d6cf86cfe115ec209fb305f0ae017951bd7f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947597"
---
# <a name="animation-design"></a>Animations Design

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

### <a name="image-design"></a>Bild Entwurf

Verwenden Sie die Microsoft Office Palette beim Entwerfen der Zeichen, um potenzielle Probleme bei der palettenrealisierung zu minimieren. Wählen Sie eine Transparenz Farbe aus, die den Farben ähnelt, die Sie in Ihrem Dokument verwenden.

### <a name="sounds"></a>Sounds

Mit dem Microsoft-Agent können Sie Sounds in ihren Animationen abspielen. Es wird empfohlen, keine Sounds für Ihre nicht im **Leerlauf** befindlichen Animationen einzuschließen. Dies ist also keine Verzögerung in der Mitte der Animation, wenn der Agent die System-Multimedia-DLL laden muss.

### <a name="frame-size"></a>Frame Größe

Typische Office-Assistenten sind 123 x 93 Pixel. Obwohl Sie Zeichen anderer Größen erstellen können, werden Sie im Assistant Gallery auf 123 x 93 skaliert.

### <a name="frame-transition"></a>Frame Übergang

Alle Animationen außer " **Goodbye**", " **Gruß**", " **anzeigen** " und " **Ausblenden** " sollten mit der restpose-Animation beginnen und enden. Microsoft Office keine expliziten **Rückgabe Animationen wieder** gibt, sollten Sie Sie nicht definieren. Alle Animationen sollten auch Exit-Verzweigungen aufweisen. Durch das Beenden der Verzweigung können wir die aktuelle Animation vor der nächsten Animation "beeilen und Fertigstellen". Wenn Sie keine Beendigungs Verzweigung angeben, ist der Übergang zwischen Animationen möglicherweise ruckartig.

### <a name="character-properties"></a>Zeichen Eigenschaften

Mit dem Microsoft-Agent können Sie den [**Namen**](name-property.md), die [**Beschreibung**](description-property.md) und die [**ExtraData**](extradata-property.md) -Eigenschaften für den Zeichensatz festlegen. Microsoft Office verwendet das **ExtraData** -Feld, um einen oder mehrere Einführungs Ausdrücke und Erinnerungs Ausdrücke zu speichern. Microsoft Office wählt die anderen Einführungs Ausdrücke aus, die in die Sprechblase im Assistant Gallery eingefügt werden sollen. Wir verwenden die Erinnerungs Ausdrücke, wenn Sie eine Erinnerung aus Outlook erhalten.

Das Feld " [**ExtraData**](extradata-property.md) " ist wie folgt formatiert:

IntroPhrase1~~IntroPhrase2~~IntroPhrase3 ^ ^ ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3

Intro-Ausdrücke werden durch ein paar aus Tildezeichen (~) getrennt, gefolgt von Erinnerungs Ausdrücken. Diese Erinnerungs Ausdrücke sind auch durch ein paar Tilde Zeichen getrennt. Die zwei Sätze von Ausdrücken sind durch zwei Caretzeichen (^^) getrennt. Es gibt keine Beschränkung für die Anzahl der einzelnen Ausdrücke, es sei denn, es muss mindestens eine vorhanden sein.

 

 




