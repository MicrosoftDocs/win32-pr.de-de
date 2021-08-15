---
description: Wenn der Wert dieser computerspezifischen Systemrichtlinie auf &\# 0034;2&0034 festgelegt ist, ist das Installationsprogramm immer für alle Anwendungen \# deaktiviert. Wenn dieser Richtlinienwert auf &\# 0034;1&0034; festgelegt ist, ist das Installationsprogramm für nicht verwaltete Anwendungen deaktiviert, aber weiterhin für verwaltete Anwendungen \# aktiviert.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846b8fb8c2c1127e59c82cce138a0956756d3447d6628cb61ef170a91e6290b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378558"
---
# <a name="disablemsi"></a>DisableMSI

Wenn der Wert dieser computerspezifischen [Systemrichtlinie](system-policy.md) auf "2" festgelegt ist, ist das Installationsprogramm immer für alle Anwendungen deaktiviert. Wenn dieser Richtlinienwert auf "1" festgelegt ist, ist das Installationsprogramm für nicht verwaltete Anwendungen deaktiviert, aber weiterhin für verwaltete Anwendungen aktiviert.

In der folgenden Tabelle sind die möglichen Konfigurationen aufgeführt.



| DisableMSI | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Standard*  | Auf Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 und Windows Server 2008 R2 ist der Windows Installer für verwaltete Anwendungen aktiviert, wenn der Richtlinienwert NULL, absent oder eine beliebige Zahl als 1 oder 2 ist. Installationen nicht verwalteter Anwendungen werden blockiert.<br/> Auf Windows XP, Windows Vista und Windows 7 ist der Windows Installer für alle Anwendungen aktiviert. Alle Installationsvorgänge sind zulässig.<br/> |
| 0          | Windows Das Installationsprogramm ist für alle Anwendungen aktiviert. Alle Installationsvorgänge sind zulässig.                                                                                                                                                                                                                                                                                                                                                      |
| 1          | Der Windows Installer ist für nicht verwaltete Anwendungen deaktiviert, aber weiterhin für verwaltete Anwendungen aktiviert. Installationen ohne erhöhte Rechte pro Benutzer werden blockiert. Benutzerspezifische Installationen mit erhöhten Rechten und Installationen pro Computer sind zulässig.                                                                                                                                                                                                                        |
| 2          | Windows Das Installationsprogramm ist für alle Anwendungen immer deaktiviert. Es sind keine Installationen zulässig, einschließlich Reparaturen, Neuinstallationen oder bedarfsbasierte Installationen.                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




