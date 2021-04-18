---
title: Aktualisieren aus vorheriger Version
description: Aktualisieren aus vorheriger Version
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341636"
---
# <a name="updating-from-previous-version"></a>Aktualisieren aus vorheriger Version

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Anwendungen, die mit der vorherigen Version 1,5 des Microsoft-Agents erstellt und kompiliert wurden, sollten unverändert unter der neuen 2,0-Version ausgeführt werden. Die [**verbundene**](connected-property.md) Eigenschaft kann nicht mehr auf **false** festgelegt werden. bestimmte Eigenschaften des bereits ersetzten speechinput-Objekts sind immer noch vorhanden, aber keine Werte mehr, und der Server löst nicht mehr die [**Neustart**](https://www.bing.com/search?q=**Restart**) -und [**Shutdown**](https://www.bing.com/search?q=**Shutdown**) -Ereignisse aus.

Wenn Sie Ihre Anwendungen jedoch für die Verwendung des Agent 2,0-Steuer Elements aktualisieren, müssen Sie möglicherweise den Code ändern. Wenn Sie die 2,0-Version des Microsoft-Agents installiert haben und ein Visual Basic-Projekt laden, verwenden Sie die frühere Version des-Agent-Steuer Elements. Visual Basic enthält eine Option, die automatisch eine Meldung anzeigt, die anzeigt, dass eine neue Version des-Steuer Elements erkannt wurde. Um den ordnungsgemäßen Betrieb Ihrer Anwendung sicherzustellen, sollten Sie immer die spätere Version verwenden.

Für andere Programmiersprachen (z. b. Microsoft Office 97 VBA) müssen Sie, um das Steuerelement zu aktualisieren, möglicherweise zuerst das Steuerelement 1,5-Agent entfernen und den Code speichern. Beenden Sie dann die Programmierumgebung, starten Sie die Programmierumgebung neu, laden Sie den Code neu, und fügen Sie das neue Steuerelement ein. Vermeiden Sie die Bearbeitung einer Anwendung mit Agent 2,0-Aktivierung in derselben Instanz der Programmierumgebung, in der Sie eine mit Agents 1,5 aktivierte Anwendung bearbeiten. In einigen Programmierumgebungen werden die Unterschiede zwischen den beiden Versionen von Steuerelementen möglicherweise nicht behandelt.

Sie sollten in der Lage sein, die-Agent-Version 1,5 auf Ihrem System zu deinstallieren, nachdem Sie die-2,0 Agent-Version von Wenn jedoch der Agent 1,5 über die 2,0-Version installiert ist, müssen Sie möglicherweise 2,0 neu installieren.

 

 




