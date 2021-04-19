---
description: Das Festlegen der disableadvtverknüpfungs-Eigenschaft deaktiviert die Generierung von Verknüpfungen, die Installation bei Bedarf und Ankündigung unterstützen. Durch Festlegen dieser Eigenschaft wird angegeben, dass diese Tastenkombinationen stattdessen durch reguläre Verknüpfungen ersetzt werden sollen.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: Disableadvtverknüpfungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c3f7d2cf800745691dde6011e6ab62232b94117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360261"
---
# <a name="disableadvtshortcuts-property"></a>Disableadvtverknüpfungs Eigenschaft

Das Festlegen der **disableadvtverknüpfungs** [-Eigenschaft](advertisement.md)deaktiviert die Generierung von Verknüpfungen, die [Installation bei Bedarf](installation-on-demand.md) und Ankündigung unterstützen. Durch Festlegen dieser Eigenschaft wird angegeben, dass diese Tastenkombinationen stattdessen durch reguläre Verknüpfungen ersetzt werden sollen.

## <a name="default-value"></a>Standardwert

Standardmäßig ist die Option für die Bedarfs gesteuerte Verknüpfung bei Bedarf aktiviert.

## <a name="remarks"></a>Bemerkungen

Die Verknüpfungen, die Ankündigungen unterstützen, haben den Namen eines Features und keinen formatierten Dateipfad der Form " \[ \# filekey" \] , der in der Ziel Spalte der Verknüpfungs [Tabelle](shortcut-table.md)eingegeben wurde. Wenn diese Eigenschaft festgelegt ist und die Funktion installiert ist, generiert das Installationsprogramm eine reguläre Verknüpfung mit der Funktion.

Diese Eigenschaft wird häufig von Administratoren für Benutzer verwendet, die sich zwischen Umgebungen bewegen, von denen keine Werbung unterstützt wird. Diese Eigenschaft kann durch eine Transformation, den administrativen Stream oder in der [Eigenschaften Tabelle](property-table.md)festgelegt werden. Wenn Sie über die Befehlszeile oder einen [**msisetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)-aufrufstyp festgelegt wird, muss Sie bei jeder nachfolgenden Installation erneut zurückgesetzt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




