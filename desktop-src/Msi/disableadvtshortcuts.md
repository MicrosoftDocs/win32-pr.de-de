---
description: Durch Festlegen der DISABLEADVTSHORTCUTS-Eigenschaft wird die Generierung von Verknüpfungen deaktiviert, die installation-on-demand und advertisement unterstützen. Durch Festlegen dieser Eigenschaft wird angegeben, dass diese Verknüpfungen stattdessen durch reguläre Verknüpfungen ersetzt werden sollen.
ms.assetid: 1b55ecbe-932f-4f08-98b1-8c5e7a57d2e8
title: DISABLEADVTSHORTCUTS-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86fd8465620abab56ebfe18f68254bf6d29b6e752a7550157231a0b1abe95ecd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745560"
---
# <a name="disableadvtshortcuts-property"></a>DISABLEADVTSHORTCUTS-Eigenschaft

Durch Festlegen der **DISABLEADVTSHORTCUTS-Eigenschaft** wird die Generierung von Verknüpfungen deaktiviert, die [installation-on-demand](installation-on-demand.md) und [advertisement](advertisement.md)unterstützen. Durch Festlegen dieser Eigenschaft wird angegeben, dass diese Verknüpfungen stattdessen durch reguläre Verknüpfungen ersetzt werden sollen.

## <a name="default-value"></a>Standardwert

Standardmäßig ist die Generierung von Bedarfsverknüpfungen für die Installation aktiviert.

## <a name="remarks"></a>Hinweise

Die Verknüpfungen, die die Ankündigung unterstützen, weisen den Namen eines Features anstelle eines formatierten Dateipfads des \[ \# Formulardateischlüssels \] auf, der in die Zielspalte der [Verknüpfungstabelle](shortcut-table.md)eingegeben wird. Wenn diese Eigenschaft festgelegt und das Feature installiert ist, generiert das Installationsprogramm eine reguläre Verknüpfung mit dem Feature.

Diese Eigenschaft wird häufig von Administratoren für Benutzer verwendet, die zwischen Umgebungen roaming, die Werbung nicht unterstützen. Diese Eigenschaft kann durch eine Transformation, im Verwaltungsstream oder in der [Property-Tabelle](property-table.md)festgelegt werden. Wenn sie über die Befehlszeile oder durch einen Aufruf von [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya)festgelegt wird, muss sie während jeder nachfolgenden Installation erneut zurückgesetzt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




