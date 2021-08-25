---
title: Vorbereiten ihrer Entwicklungsumgebung
description: Vorbereiten ihrer Entwicklungsumgebung
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: 8245326ba0d7862836336cf050eb3abf1873139873bde8b9bab238ff5a738942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896970"
---
# <a name="prepare-your-development-environment"></a>Vorbereiten ihrer Entwicklungsumgebung

Um ein Windows in C oder C++ zu schreiben, müssen Sie das Microsoft Windows Software Development Kit (SDK) oder Microsoft Visual Studio. Das Windows SDK enthält die Header und Bibliotheken, die zum Kompilieren und Verknüpfen Ihrer Anwendung erforderlich sind. Das Windows SDK enthält auch Befehlszeilentools zum Erstellen Windows Anwendungen, einschließlich Visual C++ Compiler und Linker. Obwohl Sie mit den Befehlszeilentools Windows kompilieren und erstellen können, empfehlen wir die Verwendung Microsoft Visual Studio. Sie können einen kostenlosen Download von Visual Studio Community oder kostenlose Testversionen anderer Versionen von Visual Studio [herunterladen.](https://visualstudio.microsoft.com/downloads/)

Jedes Release des Windows SDK ist auf die neueste Version Windows sowie auf mehrere frühere Versionen. In den Versionshinweisen werden die unterstützten Plattformen aufgeführt. Wenn Sie jedoch keine Anwendung für eine sehr alte Version von Windows verwalten, sollten Sie die neueste Version des Windows SDK installieren. Sie können das neueste Windows SDK hier [herunterladen.](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

Das Windows SDK unterstützt die Entwicklung von 32-Bit- und 64-Bit-Anwendungen. Die Windows-APIs sind so konzipiert, dass derselbe Code ohne Änderungen für 32-Bit oder 64-Bit kompiliert werden kann.

> [!Note]  
> Das Windows SDK unterstützt die Entwicklung von Hardwaretreibern nicht, und in dieser Reihe wird die Treiberentwicklung nicht beschrieben. Informationen zum Schreiben eines Hardwaretreibers finden Sie unter [Erste Schritte mit Windows Treibern.](/windows-hardware/drivers/gettingstarted/)

## <a name="next"></a>Nächste

[Windows Codierungskonventionen](windows-coding-conventions.md)

## <a name="related-topics"></a>Zugehörige Themen

* [Visual Studio herunterladen](https://visualstudio.microsoft.com/downloads/)
* [Herunterladen Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)