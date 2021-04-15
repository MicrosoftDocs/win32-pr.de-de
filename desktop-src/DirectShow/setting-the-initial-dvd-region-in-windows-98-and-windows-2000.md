---
description: Festlegen des ersten DVD-Bereichs
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Festlegen des ersten DVD-Bereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520387"
---
# <a name="setting-the-initial-dvd-region"></a>Festlegen des ersten DVD-Bereichs

Es liegt in der Verantwortung des Systemherstellers, einen ersten DVD-Bereich für das DVD-Laufwerk auf ihren PCs auszuwählen.

> [!Note]  
> Zum Festlegen der Region können nur verschlüsselte Festplatten verwendet werden.

 

### <a name="windows-2000-and-later"></a>Windows 2000 und höher

Ab Windows 2000 wird der Standard-DVD-Bereich basierend auf dem Gebiets Schema ausgewählt, für das der Computer eingerichtet ist. Windows 2000 legt die Anfangs Region für ein DVD-Laufwerk immer mit dieser Standard Region und der Region des Datenträgers fest, wenn sich ein Festplattenlaufwerk auf dem Laufwerk befindet. Der Systemhersteller muss nichts tun, um die Anfangs Region für DVD-Laufwerke mit Windows 2000 oder höher festzulegen.

Wenn während des Starts keine Festplatte im Laufwerk vorhanden ist, wird die Standard Region für RPC1-Laufwerke nur basierend auf dem Gebiets Schema des Computers festgelegt. Wenn beim Start des Laufwerks eine DVD-CD vorhanden ist, wird die Standard Region als die Region des Laufwerks ausgewählt, sofern Sie mit einem Bereich der Festplatte übereinstimmt. Andernfalls wird die niedrigste Region auf der Festplatte als Ausgangsbereich des Laufwerks ausgewählt. Für den Benutzer (oder den Systemhersteller) ist eine verbleibende Änderung zulässig, falls die Standardeinstellung nicht korrekt war.

Wenn bei der Installation von rpc2-Laufwerken während des Setup Vorgangs Windows 2000 feststellt, dass für das Laufwerk keine Region festgelegt ist, wird versucht, eine Region wie oben auszuwählen. Dies gilt jedoch nur, wenn auf dem Laufwerk eine Platte vorhanden ist. (Bei RPC1-Laufwerken wird die Region ohne Laufwerk im Laufwerk ausgewählt.) Nachdem eine Region für rpc2-Laufwerke festgelegt wurde, wird Sie nicht automatisch durch eine Neuinstallation oder eine Neuinstallation des Betriebssystems geändert.

Der OEM kann einen Registrierungsschlüssel mit dem Standard-DVD-Bereich für das System festlegen. Beim ersten Start wird der Laufwerks Bereich auf diesen Wert festgelegt. Der Registrierungsschlüssel unter Windows 2000 und höher ist die HKLM \\ System \\ CurrentControlSet- \\ Steuerelement \\ Klasse \\ <CDROM GUID> \\ <instance number> \\ defaultdvdregion (Binary).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützung der Änderung von DVD-Regionen in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



