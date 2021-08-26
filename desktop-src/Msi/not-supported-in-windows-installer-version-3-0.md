---
description: Die auf dieser Seite aufgeführten Windows Installer-Funktionen, -Tabellen und -Eigenschaften werden von Windows Installer&\# 160;3.0 und früheren Versionen nicht unterstützt.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Nicht unterstützt in Windows Installer 3.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b4211433762c68ed39af012d895d65aeee8fdc5a17f1e6142df76fcbe056c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926300"
---
# <a name="not-supported-in-windows-installer-30"></a>Nicht unterstützt in Windows Installer 3.0

Die auf dieser Seite aufgeführten Windows Installer-Funktionen, -Tabellen und -Eigenschaften werden von Windows Installer 3.0 und früheren Versionen nicht unterstützt. Das Fehlen eines Features in dieser Liste garantiert nicht, dass das Feature unterstützt wird. In der Hauptdokumentation erfahren Sie, welche Windows Installer-Version für ein bestimmtes Feature erforderlich ist. Informationen zu anderen Windows Installer-Versionen finden Sie unter [Neuerungen in Windows Installer.](what-s-new-in-windows-installer.md)

Windows Installer 3.0 ist für Windows Server 2003, Windows XP oder Windows 2000 verfügbar. Eine Liste aller Windows Installer-Versionen und verteilbaren Versionen finden Sie unter [Veröffentlichte Versionen von Windows Installer.](released-versions-of-windows-installer.md)

Die folgenden Features werden in Windows Installer 3.0 und früheren Versionen nicht unterstützt.

[Installerfunktionen](installer-functions.md)

-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Rückruffunktionsprototyp

-   [**\_ \_ INSTALLUI-HANDLERDATENSATZ**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Datenbanktabellen](database-tables.md)

-   Die Spalte Value der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) akzeptiert **OptimizedInstallMode** und **MinorUpdateTargetRTM.**

[Eigenschaften](properties.md)

-   [**Msix64-Eigenschaft**](msix64.md)

[Windows Installationsprogramm unter 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md)

-   Die [**Vorlagenzusammenfassungseigenschaft**](template-summary.md) akzeptiert den Wert x64.

[Interne Konsistenzauswertungen – ICEs](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
