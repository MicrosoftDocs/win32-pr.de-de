---
description: Die Patch PATCHUMMARYCOMMENTS -Eigenschaft aktualisiert die Eigenschaft Comments Summary einer Administrative Installation während des Patchens.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: PATCH PATCHUMMARYCOMMENTS (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eef7a67b960b41e55caf5251a33ac6d3198147b92bcab895a2ca711af330acd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074780"
---
# <a name="patchnewsummarycomments-property"></a>PATCH PATCHUMMARYCOMMENTS (Eigenschaft)

Die **Patch PATCHUMMARYCOMMENTS** -Eigenschaft aktualisiert die [**Eigenschaft Comments Summary**](comments-summary.md) einer Administrative Installation während des Patchens. Diese Eigenschaft wird nur durch eine Transformation in einer MSP-Datei festgelegt. Die MSP-Datei muss eine Transformation enthalten, die diese Eigenschaft der [Property-Tabelle](property-table.md) hinzufügt und ihren Wert fest legt. Das Installationsprogramm schreibt dann den Wert von **PATCHINSTALLERUMMARYCOMMENTS** in die [**Eigenschaft Zusammenfassung der Revisionsnummer.**](revision-number-summary.md)

## <a name="remarks"></a>Hinweise

Mit den Eigenschaften [**PATCHNEWPACKAGECODE,**](patchnewpackagecode.md) **PATCH PATCHUMMARYCOMMENTS** und [**PATCH PATCHUMMARYSUBJECT**](patchnewsummarysubject.md) werden die Zusammenfassungsinformationen aktualisiert, wenn ein Patch auf ein administratives Image installiert wird.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




