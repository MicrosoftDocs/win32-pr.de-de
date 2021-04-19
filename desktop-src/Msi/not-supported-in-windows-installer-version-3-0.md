---
description: Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer&\# 160; 3.0 und früheren Versionen nicht unterstützt.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: Wird in Windows Installer 3,0 nicht unterstützt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355644"
---
# <a name="not-supported-in-windows-installer-30"></a>Wird in Windows Installer 3,0 nicht unterstützt.

Die auf dieser Seite aufgeführten Windows Installer Funktionen, Tabellen und Eigenschaften werden von Windows Installer 3,0 und früheren Versionen nicht unterstützt. Das Fehlen eines Features aus dieser Liste garantiert nicht, dass das Feature unterstützt wird. In der Haupt Dokumentation finden Sie Informationen dazu, welche Windows Installer Version für eine bestimmte Funktion erforderlich ist. Weitere Informationen zu anderen Windows Installer Versionen finden Sie [unter What es New in Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 3,0 ist für Windows Server 2003, Windows XP oder Windows 2000 verfügbar. Eine Liste aller Windows Installer Versionen und verteilbaren Komponenten finden Sie unter [veröffentlichte Versionen von Windows Installer](released-versions-of-windows-installer.md).

Die folgenden Funktionen werden in Windows Installer 3,0 und früheren Versionen nicht unterstützt.

[Installer-Funktionen](installer-functions.md)

-   [**Msiseeltexternaluirecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**Msinotif ysidchange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Rückruf Funktionsprototyp

-   [**installui \_ - \_ handlerdatensatz**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Datenbanktabellen](database-tables.md)

-   In der Value-Spalte der [MsiPatchMetadata-Tabelle](msipatchmetadata-table.md) werden **OptimizedInstallMode** und **minorupdatetargetrtm** akzeptiert.

[Eigenschaften](properties.md)

-   [**Msix64-Eigenschaft**](msix64.md)

[Windows Installer auf 64-Bit-Betriebssystemen](windows-installer-on-64-bit-operating-systems.md)

-   Die [**Vorlagen Zusammenfassungs Eigenschaft**](template-summary.md) akzeptiert den Wert x64.

[Interne Konsistenz Auswertung-ICES](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
