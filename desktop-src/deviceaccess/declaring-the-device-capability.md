---
title: Deklarieren der Geräte Funktion
description: In diesem Thema wird erläutert, wie Sie die Geräte Funktions-GUID deklarieren.
ms.assetid: C663F8D2-2CB6-4C3C-A1EB-A3D93AA71FC8
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 0b1f98717c7e9487874aa71691beefbac635660a
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103949202"
---
# <a name="declaring-the-device-capability"></a>Deklarieren der Geräte Funktion

In diesem Thema wird erläutert, wie Sie die Geräte Funktions-GUID deklarieren. Alle Anwendungen, die auf benutzerdefinierte Treiber abzielen, müssen diese Funktion deklarieren.

Im Anwendungs Manifest müssen Sie wie folgt eine Geräte Funktion hinzufügen:

Dies ist ein Beispiel für eine Funktionsdeklaration für ein benutzerdefiniertes Gerät. Die GUID ist die GUID der Geräteschnittstellen Klasse.

```XML
<DeviceCapability Name="0B1F1048-B64B-FC9A-CED7-7E4FED3A0DEB" />
```

## <a name="related-topics"></a>Zugehörige Themen

[Beispiel für benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware dev Center](/windows-hardware/drivers/)
