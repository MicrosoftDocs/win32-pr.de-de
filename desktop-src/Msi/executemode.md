---
description: Die EXECUTEMODE-Eigenschaft gibt an, wie das Installationsprogramm Systemupdates ausführt.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: EXECUTEMODE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 750b6c3a20ab05388fcd6926463dde8259440bd6087306b1bf0cc1a6c387cd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082870"
---
# <a name="executemode-property"></a>EXECUTEMODE-Eigenschaft

Die **EXECUTEMODE-Eigenschaft** gibt an, wie das Installationsprogramm Systemupdates ausführt. Diese Eigenschaft kann nützlich sein, wenn es erforderlich ist, eine Installation auszuführen, ohne das System tatsächlich zu ändern. Die -Eigenschaft kann auf Keine festgelegt werden, um Aktualisierungsvorgänge wie die Installation von Dateien und Registrierungswerten zu deaktivieren.

Diese Eigenschaft kann einen der folgenden beiden Werte aufweisen. Das Installationsprogramm untersucht nur den ersten Buchstaben des Werts und beachtet die Groß-/Kleinschreibung.

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>nichts
</dt> <dd>

Es werden keine Änderungen am System vorgenommen. Das Installationsprogramm führt die Benutzeroberfläche aus und fragt dann die Datenbank ab.

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Skript
</dt> <dd>

Alle Änderungen am System werden über die Skriptausführung vorgenommen. Dies ist der Standardmodus.

</dd> </dl>

## <a name="default-value"></a>Standardwert

Wenn diese Eigenschaft nicht definiert ist, wird der Ausführungsmodus standardmäßig auf Skript festgelegt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




