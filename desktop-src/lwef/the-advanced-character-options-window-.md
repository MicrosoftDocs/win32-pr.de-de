---
title: Fenster "erweiterte Zeichen Optionen" (Fenster "Sprachbefehle")
description: Das Fenster "erweiterte Zeichen Optionen"
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f481871d3861da99b54829e5c6e1b34c9137060a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339968"
---
# <a name="advanced-character-options-window-voice-commands-window"></a>Fenster "erweiterte Zeichen Optionen" (Fenster "Sprachbefehle")

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Das Fenster Erweiterte Zeichen Optionen stellt Optionen bereit, mit denen Benutzer ihre Interaktion mit allen Zeichen anpassen können. Beispielsweise können Benutzer die Spracheingabe deaktivieren oder Eingabeparameter ändern. Benutzer können auch die Ausgabeeinstellungen für die Word-Sprechblase ändern. Diese Einstellungen überschreiben beliebige, die von einer Client Anwendung festgelegt oder als Teil der Zeichen Definition festgelegt werden. Diese Optionen können von Ihrer Anwendung nicht geändert oder deaktiviert werden, da Sie auf die allgemeinen Benutzereinstellungen für den Betrieb aller Zeichen zutreffen. Der Server benachrichtigt jedoch Ihre Anwendung ([**defaultcharakterienänderung**](defaultcharacterchange-event.md)), wenn der Benutzer sich ändert, und wendet eine Option an. Sie können das Fenster auch mit der [**Visible**](visible-property.md) -Eigenschaft des Fensters anzeigen oder schließen und über seine [**oberen**](top-property.md) und [**linken**](left-property.md) Eigenschaften auf seinen Speicherort zugreifen.

Zusätzlich zur Unterstützung der Animation eines Zeichens unterstützt der Microsoft-Agent die Audioausgabe für das Zeichen. Dies umfasst gesprochene Ausgabe und Soundeffekte. Bei der gesprochenen Ausgabe synchronisiert der Server automatisch die für das Zeichen definierten Mund Bilder mit der Ausgabe. Sie können die Text-zu-Sprache-Synthese (TTS), die aufgezeichnete Audiodaten oder nur die Textausgabe der Wort Sprechblase auswählen.

 

 




