---
description: Wenn diese Systemrichtlinie pro Computer nicht festgelegt ist, können nur Administratoren vorhandene Produkte patchen, die mit erhöhten Rechten installiert wurden.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c827b23f8beecf02d3312358d7ece6b835619111428349850f4e597ce379cd53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145903"
---
# <a name="allowlockdownpatch"></a>AllowLockdownPatch

Wenn diese [Systemrichtlinie](system-policy.md) pro Computer nicht festgelegt ist, können nur Administratoren vorhandene Produkte patchen, die mit erhöhten Rechten installiert wurden. Wenn AllowLockdownPatch auf "1" festgelegt ist, können nicht administrative Benutzer in einigen Fällen Patches auf Produkte anwenden, während sie eine Installation mit erhöhten Rechten ausführen. Wenn die Richtlinie festgelegt ist, kann der Patch [kleinere Upgrades](minor-upgrades.md) installieren, während eine Installation mit erhöhten Rechten ausgeführt wird. Der Patch kann keine [größeren Upgrades](major-upgrades.md)installieren. Wenn Sie diese Richtlinie festlegen, können nicht administrative Benutzer während einer Installation mit erhöhten Rechten programme mit LocalSystem-Berechtigungen ausführen.

Die Standardeinstellung wird empfohlen, um eine sichere Umgebung sicherzustellen.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

## <a name="remarks"></a>Hinweise

Jeder Benutzer kann während einer nicht aktualisierten Installation einen Patch anwenden. Wenn Sie diese [Systemrichtlinie](system-policy.md) pro Computer auf "1" festlegen, erhalten nicht administrative Benutzer zusätzliche Flexibilität beim Anwenden von Patches auf jedes Produkt während einer Installation mit erhöhten Rechten. Wenn diese Richtlinie nicht festgelegt ist, können nicht administrative Benutzer keinen Patch auf zugewiesene oder veröffentlichte Anwendungen anwenden.

Durch Festlegen dieser Richtlinie können nicht administrative Benutzer auch beliebige Programme mit LocalSystem-Berechtigungen ausführen, wenn sie über ein Windows Installer-Patchpaket verfügen, das diese Programme installiert oder startet.

 

 



