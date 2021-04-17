---
description: Wenn diese pro-Computer-System Richtlinie auf 1 festgelegt ist, ruft kein Paket auf dem System die Funktionalität der freigegebenen Komponente ab, die durch das msidbcomponentattributesshared-Attribut in der Component-Tabelle aktiviert wird.
ms.assetid: 28181f8c-8c03-4962-a142-c35d0dd88940
title: Disablesharedcomponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7a1d4c2bae3f499722890e06502c7a289e6921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527038"
---
# <a name="disablesharedcomponent"></a>Disablesharedcomponent

Wenn diese pro-Computer- [System Richtlinie](system-policy.md) auf 1 festgelegt ist, ruft kein Paket auf dem System die Funktionalität der freigegebenen Komponente ab, die durch das **msidbcomponentattributesshared** -Attribut in der [Component-Tabelle](component-table.md)aktiviert wird. Der Standardwert ist 0 (null). Dadurch wird die Funktionalität der freigegebenen Komponente für Komponenten aktiviert, die mit **msidbcomponentattributesshared** in allen Paketen gekennzeichnet sind.

**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt. Diese Funktion ist ab Windows Installer 4,5 verfügbar.

## <a name="registry-key"></a>Registrierungsschlüssel

**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Datentyp

**REG \_ DWORD**

 

 



