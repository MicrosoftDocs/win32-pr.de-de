---
description: Kernaudio-APIs
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: Kernaudio-APIs
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 69c0c83700dabd3aa0298bcd6474b95c4c38bdf933c9867a4c639edee1e43379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077644"
---
# <a name="core-audio-apis"></a>Kernaudio-APIs

> [!NOTE]
> Codebeispiele finden Sie unter [SDK-Beispiele, die die Kernaudio-APIs verwenden.](./sdk-samples-that-use-the-core-audio-apis.md)

Diese Dokumentation enthält Informationen zu den wichtigsten APIs (Audio Application Programming Interfaces) für die Microsoft Windows-Betriebssystemfamilie. Es enthält Richtlinien für Softwareentwickler, die bei der Entwicklung von Anwendungen befolgt werden müssen, die die Kernaudio-APIs in Windows Vista verwenden. Diese APIs waren in Windows Vista neu und sind in früheren Versionen von Windows nicht verfügbar.

Die Kernaudio-APIs bieten Audioanwendungen die Möglichkeit, auf Audioendpunktgeräte wie Mikrofone und Mikrofone zuzugreifen. Die Kernaudio-APIs dienen als Grundlage für Audio-APIs auf höherer Ebene wie Microsoft DirectSound und die Windows **Multimediafunktionen waveXxx.** Die meisten Anwendungen kommunizieren mit den übergeordneten APIs, aber einige Anwendungen mit besonderen Anforderungen müssen möglicherweise direkt mit den Kernaudio-APIs kommunizieren.

Ab Windows 7 wurden die vorhandenen APIs verbessert und neue APIs hinzugefügt, um neue Szenarien zu unterstützen. Die Datenstrom- und Sitzungsverwaltungs-APIs wurden verbessert, sodass die Anwendung jetzt aufzählen und erweiterte Kontrolle über die Audiositzung erhalten kann. Mithilfe der neuen APIs kann die Anwendung eine benutzerdefinierte Stream-Dämpfungserfahrung implementieren. Neue gerätebezogene APIs ermöglichen den Zugriff auf die Treibereigenschaften der Endpunktgeräte.

Diese Dokumentation enthält die folgenden Abschnitte.

| `Section`                                                                    | BESCHREIBUNG                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Informationen zu den Windows Core Audio-APIs](about-the-windows-core-audio-apis.md) | Bietet eine Übersicht über die Windows Core-Audio-APIs und beschreibt grundlegende Konzepte. |
| [Programmierhandbuch](programming-guide.md)                                 | Beschreibt die wichtigsten Features der Kernaudio-APIs und deren Verwendung.            |
| [Programmierverzeichnis](programming-reference.md)                         | Stellt C++-Referenzinformationen für die Kernaudio-APIs bereit.                       |

## <a name="related-topics"></a>Zugehörige Themen

[Medientechnologien für Windows](/previous-versions/bg125389(v=msdn.10))

[SDK-Beispiele, die die Kernaudio-APIs verwenden](./sdk-samples-that-use-the-core-audio-apis.md)