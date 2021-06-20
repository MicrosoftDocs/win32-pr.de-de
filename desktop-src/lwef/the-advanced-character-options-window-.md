---
title: Fenster "Erweiterte Zeichenoptionen" (Fenster "Sprachbefehle")
description: Erfahren Sie mehr über das Fenster Erweiterte Zeichenoptionen, das Benutzern Optionen zum Anpassen ihrer Interaktion mit allen Zeichen bietet.
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd49ff2f3c948594756f8d02bd4417e4f4f684fc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404358"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Fenster "Erweiterte Zeichenoptionen" (Fenster "Sprachbefehle")

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Im Fenster Erweiterte Zeichenoptionen können Benutzer ihre Interaktion mit allen Zeichen anpassen. Beispielsweise können Benutzer spracheingaben deaktivieren oder Eingabeparameter ändern. Benutzer können auch die Ausgabeeinstellungen für das Wort Balloon ändern. Diese Einstellungen überschreiben alle von einer Clientanwendung festgelegten oder als Teil der Zeichendefinition festgelegten Einstellungen. Ihre Anwendung kann diese Optionen nicht ändern oder deaktivieren, da sie für die allgemeinen Benutzereinstellungen für den Betrieb aller Zeichen gelten. Der Server benachrichtigt Jedoch Ihre Anwendung ([**DefaultCharacterChange**](defaultcharacterchange-event.md)), wenn der Benutzer eine Option ändert und wendet. Sie können das Fenster auch mithilfe der [**Visible-Eigenschaft**](visible-property.md) des Fensters anzeigen oder schließen und über die Eigenschaften [**Oben**](top-property.md) und Links auf seine [**Position**](left-property.md) zugreifen.

Zusätzlich zur Unterstützung der Animation eines Zeichens unterstützt Microsoft Agent die Audioausgabe für das Zeichen. Dies schließt gesprochene Ausgaben und Soundeffekte ein. Bei gesprochener Ausgabe synchronisiert der Server automatisch die definierten Bilder des Zeichens mit der Ausgabe. Sie können die Sprachsynthese (Text-to-Speech, TTS), aufgezeichnete Audiodaten oder nur die Textausgabe des Wortsprechblasentexts auswählen.

 

 




