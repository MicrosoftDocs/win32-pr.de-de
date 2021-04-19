---
description: Die Eigenschaft "patchnewsummarysubject" aktualisiert die Eigenschaft "betreffzusammenfassung" eines administrativen Images während des Patchens.
ms.assetid: 8aee1905-59a4-4818-b073-4bc401a6963d
title: Patchnewsummarysubject (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5916d5ed63e792a3b1ae2a69b4ac09999475b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370595"
---
# <a name="patchnewsummarysubject-property"></a>Patchnewsummarysubject (Eigenschaft)

Die Eigenschaft " **patchnewsummarysubject** " aktualisiert die Eigenschaft " [**betreffzusammenfassung**](subject-summary.md) " eines administrativen Images während des Patchens. Diese Eigenschaft wird nur durch eine Transformation in einer MSP-Datei festgelegt. Die MSP-Datei muss eine Transformation enthalten, die diese Eigenschaft der [Eigenschaften Tabelle](property-table.md) hinzufügt und deren Wert festlegt. Das Installationsprogramm schreibt dann den Wert von **patchnewsummarysubject** in die [**Revisionsnummer-Zusammenfassungs**](revision-number-summary.md) Eigenschaft.

## <a name="remarks"></a>Bemerkungen

Die Eigenschaften " [**patchnewpackagecode**](patchnewpackagecode.md)", " [**patchnewsummarycomments**](patchnewsummarycomments.md)" und " **patchnewsummarysubject** " werden verwendet, um die Zusammenfassungs Informationen zu aktualisieren, wenn ein Patch für ein administratives Image installiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




