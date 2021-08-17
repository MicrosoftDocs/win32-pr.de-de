---
description: Wenn diese computerspezifische Systemrichtlinie auf &\# 0034;1&0034; festgelegt ist, verhindert das Installationsprogramm, dass \# Nichtadministratoren Benutzerkontensteuerungspatches (User Account Control, UAC) für anwendungen verwenden, die auf dem Computer installiert sind.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821eb480ac09a2fc0416d7b3a54c0df5699a7096b45e56a843afe691886296f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637777"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Wenn diese computerspezifische Systemrichtlinie auf "1" festgelegt ist, verhindert das Installationsprogramm, dass Nichtadministratoren Benutzerkontensteuerungspatches [(User Account Control, UAC)](user-account-control--uac--patching.md) für anwendungen verwenden, die auf dem Computer installiert sind. Wenn die Systemrichtlinie pro Computer nicht auf 0 festgelegt oder festgelegt ist, können Nichtadministratoren Benutzerpatches mit den geringsten Rechten auf Anwendungen anwenden, die für das Patchen von Benutzerkonten mit den geringsten Rechten aktiviert sind.

Verwenden Sie [**die MSIDISABLELUAPATCHING-Eigenschaft,**](msidisableluapatching.md) um das Patchen mit den geringsten Rechten einer Anwendung zu verhindern.

Die DisableLUAPatching-Richtlinie ist ab Windows Installer-Version 3.0 verfügbar.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_** \\ **MACHINE-Softwarerichtlinien** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



