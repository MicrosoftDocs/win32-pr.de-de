---
description: Wenn der Wert dieser pro-Computer-System Richtlinie auf &\# 0034; 2&0034 festgelegt ist \# , wird das Installationsprogramm für alle Anwendungen immer deaktiviert. Wenn dieser Richtlinien Wert auf &\# 0034; 1&0034; festgelegt ist \# , ist das Installationsprogramm für nicht verwaltete Anwendungen deaktiviert, aber weiterhin für verwaltete Anwendungen aktiviert.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042395"
---
# <a name="disablemsi"></a>DisableMSI

Wenn der Wert dieser pro-Computer- [System Richtlinie](system-policy.md) auf "2" festgelegt ist, wird das Installationsprogramm für alle Anwendungen immer deaktiviert. Wenn dieser Richtlinien Wert auf "1" festgelegt ist, ist das Installationsprogramm für nicht verwaltete Anwendungen deaktiviert, aber weiterhin für verwaltete Anwendungen aktiviert.

In der folgenden Tabelle sind die möglichen Konfigurationen aufgelistet.



| DisableMSI | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Standard*  | Bei Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 und Windows Server 2008 R2 ist der Windows Installer für verwaltete Anwendungen aktiviert, wenn der Richtlinien Wert NULL, nicht vorhanden oder eine andere Zahl als 1 oder 2 ist. Nicht verwaltete Anwendungs Installationen werden blockiert.<br/> Unter Windows XP, Windows Vista und Windows 7 ist der Windows Installer für alle Anwendungen aktiviert. Alle Installations Vorgänge sind zulässig.<br/> |
| 0          | Windows Installer ist für alle Anwendungen aktiviert. Alle Installations Vorgänge sind zulässig.                                                                                                                                                                                                                                                                                                                                                      |
| 1          | Der Windows Installer ist für nicht verwaltete Anwendungen deaktiviert, aber weiterhin für verwaltete Anwendungen aktiviert. Nicht erhöhte Installationen pro Benutzer werden blockiert. Pro Benutzer-und Computer spezifische Installationen sind zulässig.                                                                                                                                                                                                                        |
| 2          | Windows Installer ist für alle Anwendungen immer deaktiviert. Es sind keine Installationen zulässig, einschließlich Reparaturen, Neuinstallationen oder Bedarfs gesteuerte Installationen.                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




