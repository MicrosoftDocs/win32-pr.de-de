---
description: Durch Festlegen dieser pro-Benutzer-System Richtlinie wird die Reihenfolge angegeben, in der das Installationsprogramm drei Arten von Quellen durchsucht.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869047"
---
# <a name="searchorder"></a>SearchOrder

Durch Festlegen dieser pro-Benutzer- [System Richtlinie](system-policy.md) wird die Reihenfolge angegeben, in der das Installationsprogramm drei Arten von Quellen durchsucht. Die Typen der Quellen sind:

"n" – Netzwerk

"m" – Medium (CD-ROM oder DVD)

"u" – Uniform Resource Locator (URL)

Wenn Sie z. b. zuerst nach Netzwerk Quellen suchen möchten, legen die Medienquellen und die URL-Quellen zuletzt diese Richtlinie auf den Wert "NMU" fest. Wenn Sie die Suche nach einem bestimmten Quelltyp weglassen möchten, lassen Sie den entsprechenden Buchstaben aus dem Wert aus.

Wenn SearchOrder nicht festgelegt ist, lautet die Standard Such Reihenfolge Network, Media und then URL.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG- \_ SZ**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> </dl>

 

 



