---
description: Wenn diese pro-Computer-System Richtlinie auf einen Wert größer als 0 festgelegt ist, speichert Windows Installer ältere Versionen von Dateien in einem Cache, wenn ein Patch auf eine Anwendung angewendet wird.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: Maxpatchcachesize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485262"
---
# <a name="maxpatchcachesize"></a>Maxpatchcachesize

Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf einen Wert größer als 0 festgelegt ist, speichert Windows Installer ältere Versionen von Dateien in einem Cache, wenn ein Patch auf eine Anwendung angewendet wird. Das Caching kann die Leistung zukünftiger Installationen erhöhen, die andernfalls die alten Dateien aus einer ursprünglichen Anwendungs Quelle abrufen müssen.

Der Wert der maxpatchcachesize-Richtlinie ist der maximale Prozentsatz des Speicherplatzes, den das Installationsprogramm für den Cache Alter Dateien verwenden kann. Der Wert 20 gibt z. b. an, dass nicht mehr als 20% verwendet werden. Wenn die Gesamtgröße des Caches den angegebenen Prozentsatz des Speicherplatzes erreicht, werden keine zusätzlichen Dateien im Cache gespeichert. Die Richtlinie wirkt sich nicht auf Dateien aus, die bereits gespeichert wurden.

Wenn der Wert der maxpatchcachesize-Richtlinie auf 0 festgelegt ist, werden keine weiteren Dateien gespeichert.

Wenn die maxpatchcachesize-Richtlinie nicht festgelegt ist, ist der Standardwert 10, und es können maximal 10% des Speicherplatzes zum Speichern alter Dateien verwendet werden.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



