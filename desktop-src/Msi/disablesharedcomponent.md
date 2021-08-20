---
description: Wenn diese Systemrichtlinie pro Computer auf 1 festgelegt ist, ruft kein Paket auf dem System die freigegebene Komponentenfunktionalität ab, die durch das msidbComponentAttributesShared-Attribut in der Tabelle Komponente aktiviert wird.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: DisableSharedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7576406e14b0f9ac48a26735b984302c2d765b784484022a85ec50244ee8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143101"
---
# <a name="disablesharedcomponent"></a>DisableSharedComponent

Wenn diese [Systemrichtlinie](system-policy.md) pro Computer auf 1 festgelegt ist, ruft kein Paket auf dem System die freigegebene Komponentenfunktionalität ab, die vom **msidbComponentAttributesShared-Attribut** in der [Komponententabelle](component-table.md)aktiviert wird. Der Standardwert ist 0, wodurch die Funktionalität der freigegebenen Komponente für Komponenten aktiviert wird, die mit **msidbComponentAttributesShared** in allen Paketen markiert sind.

**[Windows Installer 4.0 und früher:](not-supported-in-windows-installer-4-0.md)** Wird nicht unterstützt. Diese Funktion ist ab Windows Installer 4.5 verfügbar.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



