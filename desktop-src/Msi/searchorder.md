---
description: Durch Festlegen dieser Systemrichtlinie pro Benutzer wird die Reihenfolge angegeben, in der das Installationsprogramm drei Arten von Quellen durchsucht.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfaab6ff8d4b40b966b5ab1785ddd5fd473316732833fc32be7102acaa7c4877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041040"
---
# <a name="searchorder"></a>SearchOrder

Durch Festlegen dieser [Systemrichtlinie](system-policy.md) pro Benutzer wird die Reihenfolge angegeben, in der das Installationsprogramm drei Arten von Quellen durchsucht. Die Arten von Quellen sind:

"n" – Netzwerk

"m" – Medien (CD-ROM oder DVD)

"u" – Uniform Resource Locator (URL)

Legen Sie diese Richtlinie beispielsweise auf den Wert "nmu" fest, um netzwerkquellen zuerst, medienquellen second und URL-Quellen zu durchsuchen. Um die Suche nach einem bestimmten Quelltyp auszulassen, lassen Sie den entsprechenden Buchstaben aus dem Wert weg.

Wenn SearchOrder nicht festgelegt ist, lautet die Standardsuchreihenfolge Netzwerk, Medien und dann URL.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ SZ**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellresilienz](source-resiliency.md)
</dt> </dl>

 

 



