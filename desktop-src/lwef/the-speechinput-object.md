---
title: Das SpeechInput-Objekt
description: Das SpeechInput-Objekt
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d96dd52d5847b3fbaa81bbc21d4015698655fba1fe2523aaddc065e6d2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975520"
---
# <a name="the-speechinput-object"></a>Das SpeechInput-Objekt

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Das [**SpeechInput-Objekt**](https://www.bing.com/search?q=**SpeechInput**) ermöglicht den Zugriff auf die spracheingabeeigenschaften, die vom -Agent-Server verwaltet werden. Die Eigenschaften sind schreibgeschützt für Clientanwendungen, aber der Benutzer kann sie im Eigenschaftenblatt des Microsoft-Agents ändern. Der Server gibt Nur werte zurück, wenn eine kompatible Sprach-Engine installiert wurde und aktiviert ist.

Die Eigenschaften [**Engine,**](https://www.bing.com/search?q=**Engine**) [**Installed**](https://www.bing.com/search?q=**Installed**)und [**Language**](https://www.bing.com/search?q=**Language**) werden nicht mehr unterstützt, geben jedoch (aus Gründen der Abwärtskompatibilität) NULL-Werte zurück, wenn sie abgefragt werden. Um den Modus einer Spracherkennung abzufragen oder festzulegen, verwenden Sie die [**SRModeID-Eigenschaft.**](srmodeid-property.md)

-   [SpeechInput-Eigenschaften](speechinput-properties.md)

 

 




