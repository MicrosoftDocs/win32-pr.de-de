---
title: Vorbereiten der Entwicklungsumgebung
description: Vorbereiten der Entwicklungsumgebung
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314931"
---
# <a name="prepare-your-development-environment"></a>Vorbereiten der Entwicklungsumgebung

Wenn Sie ein Windows-Programm in C oder C++ schreiben möchten, müssen Sie das Microsoft Windows Software Development Kit (SDK) oder Microsoft Visual Studio installieren. Die Windows SDK enthält die Header und Bibliotheken, die erforderlich sind, um Ihre Anwendung zu kompilieren und zu verknüpfen. Die Windows SDK enthält auch Befehlszeilen Tools zum Entwickeln von Windows-Anwendungen, einschließlich Visual C++ Compiler und Linker. Obwohl Sie Windows-Programme mit den Befehlszeilen Tools kompilieren und erstellen können, empfiehlt es sich, Microsoft Visual Studio zu verwenden. Sie können einen kostenlosen Download von Visual Studio Community oder kostenlose Testversionen von Visual Studio [hier](https://visualstudio.microsoft.com/downloads/)herunterladen.

Jede Version des Windows SDK ist für die aktuelle Version von Windows und für mehrere frühere Versionen vorgesehen. In den Anmerkungen zu dieser Version werden die unterstützten Plattformen aufgeführt. Wenn Sie jedoch keine Anwendung für eine frühere Windows-Version verwalten, sollten Sie die neueste Version der Windows SDK installieren. Sie können den neuesten Windows SDK [hier](https://developer.microsoft.com/windows/downloads/windows-10-sdk)herunterladen.

Der Windows SDK unterstützt die Entwicklung von 32-Bit-und 64-Bit-Anwendungen. Die Windows-APIs sind so konzipiert, dass der gleiche Code ohne Änderungen für 32-Bit oder 64-Bit kompiliert werden kann.

> [!Note]  
> Der Windows SDK unterstützt die Entwicklung von Hardware Treibern nicht, und in dieser Serie wird die Treiberentwicklung nicht erörtert. Informationen zum Schreiben eines Hardware Treibers finden Sie unter [Getting Started with Windows Drivers](/windows-hardware/drivers/gettingstarted/).

## <a name="next"></a>Nächste

[Windows-Codierungs Konventionen](windows-coding-conventions.md)

## <a name="related-topics"></a>Zugehörige Themen

* [Herunterladen von Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [Download Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)