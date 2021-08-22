---
description: Die PATCHSUMMEMARYSUBJECT-Eigenschaft aktualisiert die Subject Summary-Eigenschaft eines administrativen Images während des Patchens.
ms.assetid: 8aee1905-59a4-4818-b073-4bc401a6963d
title: PATCHUMAUMMARYSUBJECT-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912fe9ea21605625135b385a400fd5136c993c1d0dd0e3bfadd6a2b6699d21e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926167"
---
# <a name="patchnewsummarysubject-property"></a>PATCHUMAUMMARYSUBJECT-Eigenschaft

Die **PATCHSUMMEMARYSUBJECT-Eigenschaft** aktualisiert die [**Subject Summary-Eigenschaft**](subject-summary.md) eines administrativen Images während des Patchens. Diese Eigenschaft wird nur durch eine Transformation in einer MSP-Datei festgelegt. Die MSP-Datei muss eine Transformation enthalten, die diese Eigenschaft der [Tabelle Property](property-table.md) hinzufügt und deren Wert festlegt. Das Installationsprogramm schreibt dann den Wert von **PATCHINSTALLERUMMARYSUBJECT** in die [**Revision Number Summary**](revision-number-summary.md) -Eigenschaft.

## <a name="remarks"></a>Hinweise

Die Eigenschaften [**PATCHNEWPACKAGECODE,**](patchnewpackagecode.md) [**PATCHINSTALLUMMARYCOMMENTS**](patchnewsummarycomments.md)und **PATCHINSTALLUMMARYSUBJECT** werden verwendet, um die Zusammenfassungsinformationen zu aktualisieren, wenn ein Patch auf einem administrativen Image installiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




