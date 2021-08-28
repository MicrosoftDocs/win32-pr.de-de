---
description: Installieren Sie Windows Installer-Paket mit erhöhten (System-)Berechtigungen.
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc015dad8096db16d8b70238a5fd7e07544b83f9a9e3d1a5045be9d12bbb30cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650240"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated

Sie können die AlwaysInstallElevated-Richtlinie verwenden, um ein Windows Installer-Paket mit erhöhten (System-)Berechtigungen zu installieren.

**Warnung: **

Diese Option entspricht dem Gewähren vollständiger Administratorrechte, was ein großes Sicherheitsrisiko darstellen kann. Microsoft rät dringend davon ab, diese Einstellung zu verwenden.

Legen Sie zum Installieren eines Pakets mit erhöhten (System-)Berechtigungen den AlwaysInstallElevated-Wert unter den beiden folgenden Registrierungsschlüsseln auf "1" fest:

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Wenn der AlwaysInstallElevated-Wert unter beiden vorherigen Registrierungsschlüsseln nicht auf "1" festgelegt ist, verwendet das Installationsprogramm erhöhte Rechte, um verwaltete Anwendungen zu installieren, und verwendet die Berechtigungsstufe des aktuellen Benutzers für nicht verwaltete Anwendungen.

Da diese Richtlinie Benutzern die Installation von Anwendungen ermöglicht, die Zugriff auf Verzeichnisse und Registrierungsschlüssel erfordern, für die der Benutzer möglicherweise nicht über die Berechtigung zum Anzeigen oder Ändern verfügt, sollten Sie überlegen, ob sie ihren Benutzern ein angemessenes Maß an Sicherheit bietet. Wenn Sie diese Richtlinie festlegen, Windows Installer die Systemberechtigungen verwenden, wenn die Anwendung auf dem System installiert wird. Wenn diese Richtlinie nicht festgelegt ist, werden Anwendungen, die nicht vom Administrator verteilt werden, mit den Berechtigungen des Benutzers installiert, und nur verwaltete Anwendungen erhalten erhöhte Rechte.

Beachten Sie, dass nach der Aktivierung der Richtlinie pro Computer für AlwaysInstallElevated jeder Benutzer seine Benutzereinstellung festlegen kann.

## <a name="remarks"></a>Hinweise

Informationen zur Interaktion dieser Richtlinie mit Installationsquellen finden Sie unter [Verwalten von Installationsquellen.](managing-installation-sources.md)

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



