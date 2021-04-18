---
description: Die Eigenschaft "patchnewpackagecode" aktualisiert während des Patchens die Zusammenfassungs Eigenschaft "Revisionsnummer" eines administrativen Bilds.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Patchnewpackagecode (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7c1c70c91ede5788258c67626cdf429df74e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364796"
---
# <a name="patchnewpackagecode-property"></a>Patchnewpackagecode (Eigenschaft)

Die Eigenschaft " **patchnewpackagecode** " aktualisiert während des Patchens die [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " eines administrativen Bilds. Diese Eigenschaft wird nur durch eine Transformation in einer MSP-Datei festgelegt. Die MSP-Datei muss eine Transformation enthalten, die diese Eigenschaft der [Eigenschaften Tabelle](property-table.md) hinzufügt und deren Wert festlegt. Das Installationsprogramm schreibt dann den Wert von " **patchnewpackagecode** " in die **Revisionsnummer-Zusammenfassungs** Eigenschaft.

## <a name="remarks"></a>Bemerkungen

Die Eigenschaften " **patchnewpackagecode**", " [**patchnewsummarycomments**](patchnewsummarycomments.md)" und " [**patchnewsummarysubject**](patchnewsummarysubject.md) " werden verwendet, um die Zusammenfassungs Informationen zu aktualisieren, wenn ein Patch für ein administratives Image installiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




