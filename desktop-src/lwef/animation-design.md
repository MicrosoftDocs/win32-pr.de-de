---
title: Animationsentwurf
description: Animationsentwurf
ms.assetid: 8812e4cc-9062-4c65-81ef-229bd29534cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225a500d94b4de6f9133650a6aed415a49329585bc9bc9f83dec028668e51215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752291"
---
# <a name="animation-design"></a>Animationsentwurf

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

### <a name="image-design"></a>Bildentwurf

Verwenden Sie die Microsoft Office Palette, wenn Sie Ihre Zeichen entwerfen, um potenzielle Probleme bei der Umsetzung der Palette zu minimieren. Vermeiden Sie es, eine Transparenzfarbe auszuwählen, die den Farben ähnelt, die Sie in Ihrem Dokument verwenden.

### <a name="sounds"></a>Sounds

Mit dem Microsoft-Agent können Sie Sounds in Ihren Animationen wiedergeben. Es wird empfohlen, keine  Sounds für Ihre Leerlaufanimationen einzufügen. Dies ist der Grund dafür, dass es in der Mitte der Animation keine Verzögerung gibt, wenn der -Agent die Multimedia-DLL des Systems laden muss.

### <a name="frame-size"></a>Framegröße

Typische Office-Assistenten sind 123 x 93 Pixel. Obwohl Sie Zeichen anderer Größen erstellen können, werden sie im Assistentenkatalog auf 123 x 93 skaliert.

### <a name="frame-transition"></a>Frameübergang

Alle Animationen außer **"Goodbye",** **"Greeting",** **"Show"** und **"Hide"** sollten mit der RestPose-Animation beginnen und enden. Microsoft Office keine expliziten **Return-Animationen** wiedergibt, sollten Sie sie daher nicht definieren. Alle Animationen sollten auch Exit Branching aufweisen. Die Exitverzweigung ermöglicht es uns, die aktuelle Animation zu "überholen und abzuschließen", bevor wir die nächste Animation aufrufen. Wenn Sie Exit Branching nicht bereitstellen, kann der Übergang zwischen Animationen ruckartig sein.

### <a name="character-properties"></a>Zeicheneigenschaften

Mit dem Microsoft-Agent können Sie die Eigenschaften [**Name**](name-property.md), [**Description**](description-property.md) und [**ExtraData**](extradata-property.md) des Zeichens festlegen. Microsoft Office verwendet das Feld **ExtraData,** um ein oder mehrere Einführungsphrasen und Erinnerungsphrasen zu speichern. Microsoft Office wählt aus den anderen Einführungsphrasen aus, die in den Sprachsprechblasen im Assistentenkatalog eingefügt werden sollen. Wir verwenden die Erinnerungsausdrücke, wenn Sie eine Erinnerung von Outlook erhalten.

Das Feld [**ExtraData**](extradata-property.md) ist wie folgt formatiert:

IntroPhrase1~~IntroPhrase2~~IntroPhrase3^^ReminderPhrase1~~ReminderPhrase2~~ReminderPhrase3

Einführungsphrasen werden durch ein Paar von Tildezeichen (~) getrennt, gefolgt von Erinnerungsausdrücken. Diese Erinnerungsausdrücke werden auch durch ein Paar von Tildezeichen getrennt. Die beiden Sätze von Ausdrücken werden durch zwei Caretzeichen (^^) getrennt. Es gibt keine Beschränkung für die Anzahl der einzelnen Arten von Ausdrücken, außer dass mindestens einer vorhanden sein muss.

 

 




