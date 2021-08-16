---
title: Aktualisieren von früheren Versionen
description: Aktualisieren von früheren Versionen
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de894f220db7ee09847a8fa767e1f99c38cee8014cb86b65c1251e0579eaabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745723"
---
# <a name="updating-from-previous-version"></a>Aktualisieren von früheren Versionen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Anwendungen, die mit der vorherigen Version 1.5 des Microsoft-Agents erstellt und kompiliert wurden, sollten ohne Änderungen unter der neuen Version 2.0 ausgeführt werden. Die [**Connected-Eigenschaft**](connected-property.md) kann nicht mehr auf **False** festgelegt werden. Bestimmte Eigenschaften des SpeechInput-Objekts, die ersetzt wurden, sind weiterhin vorhanden, ändern jedoch keine Werte mehr, und der Server löst die Ereignisse [**Neustart**](https://www.bing.com/search?q=**Restart**) und [**Herunterfahren**](https://www.bing.com/search?q=**Shutdown**) nicht mehr aus.

Wenn Sie Ihre Anwendungen jedoch so aktualisieren, dass sie das Agent 2.0-Steuerelement verwenden, müssen Sie möglicherweise Ihren Code ändern. Wenn Sie die Version 2.0 des Microsoft-Agents installiert haben und ein Visual Basic Projekt laden, verwenden Sie die frühere Version des -Agent-Steuerelements, Visual Basic eine Option enthält, die automatisch eine Meldung anzeigt, die angibt, dass eine neue Version des Steuerelements erkannt wurde. Um den ordnungsgemäßen Betrieb Ihrer Anwendung sicherzustellen, wählen Sie immer die spätere Version aus.

Für andere Programmiersprachen (z. B. Microsoft Office 97 VBA) müssen Sie zum Aktualisieren des Steuerelements möglicherweise zuerst das 1.5-Agent-Steuerelement entfernen und Ihren Code speichern. Beenden Sie dann die Programmierumgebung, starten Sie die Programmierumgebung neu, laden Sie den Code neu, und fügen Sie das neue Steuerelement ein. Vermeiden Sie das Bearbeiten einer Agent 2.0-fähigen Anwendung in derselben Instanz der Programmierumgebung, in der Sie eine Agent 1.5-fähige Anwendung bearbeiten. In einigen Programmierumgebungen werden die Unterschiede zwischen den beiden Versionen von Steuerelementen möglicherweise nicht behandelt.

Sie sollten das Agent 1.5-Release auf Ihrem System deinstallieren können, nachdem Sie das Agent 2.0-Release installiert haben. Wenn Agent 1.5 jedoch über version 2.0 installiert ist, müssen Sie 2.0 möglicherweise neu installieren.

 

 




