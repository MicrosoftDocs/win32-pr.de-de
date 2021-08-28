---
description: Wenn diese Systemrichtlinie pro Computer auf einen Wert größer als 0 festgelegt ist, speichert Windows Installer ältere Versionen von Dateien in einem Cache, wenn ein Patch auf eine Anwendung angewendet wird.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85291977073d1ab65c43ce9c4307e7c97519133330769e56c4b9dc7a883972dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013058"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

Wenn diese [Systemrichtlinie](system-policy.md) pro Computer auf einen Wert größer als 0 festgelegt ist, speichert Windows Installer ältere Versionen von Dateien in einem Cache, wenn ein Patch auf eine Anwendung angewendet wird. Das Zwischenspeichern kann die Leistung zukünftiger Installationen erhöhen, die andernfalls die alten Dateien aus einer ursprünglichen Anwendungsquelle abrufen müssen.

Der Wert der MaxPatchCacheSize-Richtlinie ist der maximale Prozentsatz des Speicherplatzes, den das Installationsprogramm für den Cache alter Dateien verwenden kann. Beispielsweise gibt der Wert 20 an, dass nicht mehr als 20 % verwendet werden. Wenn die Gesamtgröße des Caches den angegebenen Prozentsatz des Speicherplatzes erreicht, werden keine zusätzlichen Dateien im Cache gespeichert. Die Richtlinie wirkt sich nicht auf Dateien aus, die bereits gespeichert wurden.

Wenn der Wert der MaxPatchCacheSize-Richtlinie auf 0 festgelegt ist, werden keine zusätzlichen Dateien gespeichert.

Wenn die MaxPatchCacheSize-Richtlinie nicht festgelegt ist, ist der Standardwert 10, und es können maximal 10 % des Speicherplatzes verwendet werden, um alte Dateien zu speichern.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



