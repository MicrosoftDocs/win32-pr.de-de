---
title: Erweitertes Zeichenoptionenfenster (Fenster "Sprachbefehle")
description: Erfahren Sie mehr über das Fenster "Erweiterte Zeichenoptionen", das Optionen bereitstellt, mit denen Benutzer ihre Interaktion mit allen Zeichen anpassen können.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1b5ce1bc7cb42dc03fd35edbbaa6626f19389b0fd72bd507590ad1989d111c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715860"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Erweitertes Zeichenoptionenfenster (Fenster "Sprachbefehle")

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Das Fenster Erweiterte Zeichenoptionen enthält Optionen, mit deren Hilfe Benutzer ihre Interaktion mit allen Zeichen anpassen können. Beispielsweise können Benutzer spracheingaben deaktivieren oder Eingabeparameter ändern. Benutzer können auch die Ausgabeeinstellungen für die Wortsprechblase ändern. Diese Einstellungen überschreiben alle, die von einer Clientanwendung festgelegt oder als Teil der Zeichendefinition festgelegt werden. Ihre Anwendung kann diese Optionen nicht ändern oder deaktivieren, da sie für die allgemeinen Benutzereinstellungen für den Betrieb aller Zeichen gelten. Allerdings benachrichtigt der Server Ihre Anwendung ([**DefaultCharacterChange**](defaultcharacterchange-event.md)), wenn sich der Benutzer ändert und eine Option anwendet. Sie können das Fenster auch mithilfe der [**Visible-Eigenschaft**](visible-property.md) des Fensters anzeigen oder schließen und über die Eigenschaften [**Oben**](top-property.md) und [**Links**](left-property.md) auf seine Position zugreifen.

Zusätzlich zur Unterstützung der Animation eines Zeichens unterstützt der Microsoft-Agent die Audioausgabe für das Zeichen. Dies schließt gesprochene Ausgabe- und Soundeffekte ein. Für die gesprochene Ausgabe synchronisiert der Server automatisch die definierten Bilder des Zeichens mit der Ausgabe. Sie können die Sprachsynthese (Text-to-Speech, TTS), aufgezeichnete Audiodaten oder nur die Textausgabe der Wortsprechblase auswählen.

 

 




