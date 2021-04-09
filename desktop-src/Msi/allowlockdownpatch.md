---
description: Wenn diese Computer spezifische System Richtlinie nicht festgelegt ist, können nur Administratoren vorhandene Produkte Patchen, die mit erhöhten Rechten installiert wurden.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: Allowlockdownpatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959540"
---
# <a name="allowlockdownpatch"></a>Allowlockdownpatch

Wenn diese Computer spezifische [System Richtlinie](system-policy.md) nicht festgelegt ist, können nur Administratoren vorhandene Produkte Patchen, die mit erhöhten Rechten installiert wurden. Wenn allowlockdownpatch auf "1" festgelegt ist, können Benutzer, die nicht Administratoren sind, in einigen Fällen Patches auf Produkte anwenden, während eine Installation mit erhöhten Rechten ausgeführt wird. Wenn die Richtlinie festgelegt ist, kann der Patch [kleinere Upgrades](minor-upgrades.md) installieren, während eine Installation mit erhöhten Rechten ausgeführt wird. der Patch kann keine [größeren Upgrades](major-upgrades.md)installieren. Wenn Sie diese Richtlinie festlegen, können Benutzer, die nicht Administratoren sind, auch bei einer erweiterten Installation Programme mit LocalSystem-Berechtigungen ausführen.

Die Standardeinstellung wird empfohlen, um eine sichere Umgebung sicherzustellen.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Jeder Benutzer kann einen Patch während einer Installation ohne erhöhte Rechte anwenden. Wenn Sie diese pro-Computer- [System Richtlinie](system-policy.md) auf "1" festlegen, erhalten nicht Administratoren zusätzliche Flexibilität bei der Anwendung von Patches auf beliebige Produkte. Wenn diese Richtlinie nicht festgelegt ist, können nicht-Administratoren einen Patch auf zugewiesene oder veröffentlichte Anwendungen anwenden.

Durch Festlegen dieser Richtlinie können nicht Administratoren beliebige Programme unter "LocalSystem"-Privilegien ausführen, wenn Sie über ein Windows Installer Patch-Paket verfügen, das diese Programme installiert oder gestartet.

 

 



