---
title: Das speechinput-Objekt
description: Das speechinput-Objekt
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947870"
---
# <a name="the-speechinput-object"></a>Das speechinput-Objekt

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Das [**speechinput**](https://www.bing.com/search?q=**SpeechInput**) -Objekt ermöglicht den Zugriff auf die Spracheingabe Eigenschaften, die vom Agent-Server verwaltet werden. Die Eigenschaften sind für Client Anwendungen schreibgeschützt, aber der Benutzer kann Sie auf der Eigenschaften Seite des Microsoft-Agents ändern. Der Server gibt nur dann Werte zurück, wenn eine kompatible Sprach-Engine installiert und aktiviert ist.

Die Eigenschaften [**Engine**](https://www.bing.com/search?q=**Engine**), [**installiert**](https://www.bing.com/search?q=**Installed**)und [**Language**](https://www.bing.com/search?q=**Language**) werden nicht mehr unterstützt, aber (aus Gründen der Abwärtskompatibilität) geben NULL-Werte zurück, wenn Sie abgefragt werden. Um den Modus einer Spracherkennung abzufragen oder festzulegen, verwenden Sie die [**srmodeid**](srmodeid-property.md) -Eigenschaft.

-   [Speechinput-Eigenschaften](speechinput-properties.md)

 

 




