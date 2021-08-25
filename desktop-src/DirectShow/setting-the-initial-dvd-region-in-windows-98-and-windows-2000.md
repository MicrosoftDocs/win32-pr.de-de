---
description: Festlegen des anfänglichen DVD-Bereichs
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Festlegen des anfänglichen DVD-Bereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf019c7d5ddae8efb257435e1b23037575a37f809ef012190b49c619cc3211
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102320"
---
# <a name="setting-the-initial-dvd-region"></a>Festlegen des anfänglichen DVD-Bereichs

Es liegt in der Verantwortung des Systemherstellers, eine anfängliche DVD-Region für das DVD-Laufwerk auf den PCs auszuwählen.

> [!Note]  
> Nur verschlüsselte Datenträger können verwendet werden, um die Region festzulegen.

 

### <a name="windows-2000-and-later"></a>Windows 2000 und höher

Ab Windows 2000 wird der DVD-Standardbereich basierend auf dem Gebietsschema ausgewählt, für das der Computer eingerichtet ist. Windows 2000 wird immer die ursprüngliche Region für ein DVD-Laufwerk mit dieser Standardregion sowie die Region des Datenträgers festgelegt, wenn sich ein Datenträger auf dem Laufwerk befindet. Der Systemhersteller muss nichts unternehmen, um den anfänglichen Bereich für Windows 2000 oder höher-DVD-Laufwerke festzulegen.

Wenn bei RPC1-Laufwerken während des Starts kein Datenträger auf dem Laufwerk vorhanden ist, wird die Standardregion nur basierend auf dem Gebietsschema des Computers festgelegt. Wenn während des Starts ein DVD-Datenträger auf dem Laufwerk vorhanden ist, wird die Standardregion als Region des Laufwerks ausgewählt, sofern sie mit einem Bereich des Datenträgers übereinstimmt. Andernfalls wird der niedrigste Bereich auf dem Datenträger als erster Bereich des Laufwerks ausgewählt. Für den Benutzer (oder Systemhersteller) ist eine verbleibende Änderung zulässig, falls der Standardwert nicht korrekt war.

Wenn bei RPC2-Laufwerken während des Setupvorgangs Windows 2000 feststellt, dass auf dem Laufwerk keine Region festgelegt ist, wird wie oben beschrieben versucht, eine Region zu wählen, aber nur, wenn sich ein Datenträger auf dem Laufwerk befindet. (RPC1-Laufwerke wählen die Region ohne Datenträger im Laufwerk aus.) Sobald eine Region für RPC2-Laufwerke festgelegt wurde, wird sie weder durch eine Neuinstallation noch durch eine Neuinstallation des Betriebssystems automatisch geändert.

Der OEM kann einen Registrierungsschlüssel festlegen, der den DVD-Standardbereich für das System enthält. Beim ersten Start wird der Laufwerkbereich auf diesen Wert festgelegt. Der Registrierungsschlüssel für Windows 2000 und höher ist HKLM \\ System \\ CurrentControlSet \\ Control Class \\ \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion(binary) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung für DVD-Regionsänderungen in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



