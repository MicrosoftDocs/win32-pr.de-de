---
description: Die PATCHNEWPACKAGECODE-Eigenschaft aktualisiert die Eigenschaft Zusammenfassung der Revisionsnummer eines administrativen Images während des Patchens.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: PATCHNEWPACKAGECODE(Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d7e64729643fa1b6449838496416d10e1ec12374762b3f702b306a146338f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926162"
---
# <a name="patchnewpackagecode-property"></a>PATCHNEWPACKAGECODE(Eigenschaft)

Die **PATCHNEWPACKAGECODE-Eigenschaft** aktualisiert die [**Eigenschaft Zusammenfassung der Revisionsnummer**](revision-number-summary.md) eines administrativen Images während des Patchens. Diese Eigenschaft wird nur durch eine Transformation in einer MSP-Datei festgelegt. Die MSP-Datei muss eine Transformation enthalten, die diese Eigenschaft der [Property-Tabelle](property-table.md) hinzufügt und ihren Wert fest legt. Das Installationsprogramm schreibt dann den Wert von **PATCHNEWPACKAGECODE** in die **Eigenschaft Zusammenfassung der Revisionsnummer.**

## <a name="remarks"></a>Hinweise

Mit den Eigenschaften **PATCHNEWPACKAGECODE,** [**PATCH PATCHUMMARYCOMMENTS**](patchnewsummarycomments.md)und [**PATCH PATCHUMMARYSUBJECT**](patchnewsummarysubject.md) werden die Zusammenfassungsinformationen aktualisiert, wenn ein Patch auf ein administratives Image installiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




