---
description: Geräte Nachrichten sind Systemmeldungen, die Anwendungen und andere Features von Geräte Änderungs Ereignissen benachrichtigen.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Gerätemeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343000"
---
# <a name="device-messages"></a>Gerätemeldungen

Geräte Nachrichten sind Systemmeldungen, die Anwendungen und andere Features von Geräte Änderungs Ereignissen benachrichtigen. Diese Ereignisse treten immer dann auf, wenn das System eine Änderung an der System Hardware erkennt, z. b. wenn der Benutzer einen Laptop andockt und ihn abdockt oder ein Gerät wie eine PCMCIA-Karte einfügt oder entfernt. Geräte Ereignisse können auftreten, während das System ausgeführt wird, oder wenn der Vorgang fortgesetzt wird, nachdem das System vorübergehend angehalten wurde.

Um sicherzustellen, dass Anwendungen keine Daten verlieren, wenn Geräte nicht mehr verfügbar sind, überwacht das System die Hardwarekonfiguration und sendet Geräte Nachrichten an die Anwendungen, um Sie über die Änderungen zu informieren und Ihnen die Möglichkeit zu geben, die Änderungen vorzubereiten, bevor Sie auftreten.

Das System überträgt für jedes Geräte Ereignis eine [**WM- \_ devicechange**](wm-devicechange.md) -Nachricht an alle Anwendungen. In dieser Meldung identifiziert der *wParam* -Parameter den [Geräte Ereignistyp](device-event-types.md) , und der *LPARAM* -Parameter ist ein Zeiger auf ereignisspezifische Daten.

 

 



