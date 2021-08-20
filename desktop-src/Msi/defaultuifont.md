---
description: Die DefaultUIFont-Eigenschaft legt den Standardschriftstil fest, der für Steuerelemente verwendet wird. Um den Standardwert anzugeben, legen Sie DefaultUIFont auf einen der vordefinierten Stile in der TextStyle-Tabelle in der Property-Tabelle fest.
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: DefaultUIFont-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46bf4c432a0e75c933136cc11e1dd8a55cc6a4cdf2f09c923804132b743e88c9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289580"
---
# <a name="defaultuifont-property"></a>DefaultUIFont-Eigenschaft

Die **DefaultUIFont-Eigenschaft** legt den Standardschriftstil fest, der für Steuerelemente verwendet wird. Um den Standardwert anzugeben, legen Sie **DefaultUIFont** auf einen der vordefinierten Stile in der [TextStyle-Tabelle](textstyle-table.md) in der [Property-Tabelle](property-table.md)fest.

## <a name="remarks"></a>Hinweise

Die **DefaultUIFont-Eigenschaft** jedes Installationspakets mit einer Benutzeroberfläche sollte in der [Tabelle Property](property-table.md) auf einen der vordefinierten Stile festgelegt werden, die in der [TextStyle-Tabelle](textstyle-table.md)aufgeführt sind. Wenn diese Eigenschaft nicht angegeben ist, verwendet das Installationsprogramm die Schriftart System. Dies kann dazu führen, dass das Installationsprogramm Textzeichenfolgen nicht ordnungsgemäß anzeigt, wenn sich die Codepage des Pakets von der Standardcodepage der Benutzeroberfläche des Benutzers unterscheidet.

Der Text- und Schriftschnitt eines Steuerelements kann wie unter [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md)beschrieben festgelegt werden. Wenn die in der Spalte Text der [Tabelle Control](control-table.md) oder [BBControl](bbcontrol-table.md) aufgeführte Zeichenfolge den Schriftschnitt nicht angibt, verwendet das Steuerelement den Wert der **DefaultUIFont-Eigenschaft** als Schriftschnitt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den Windows Service [Pack-Mindestanforderungen,](windows-installer-portal.md) die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time Anforderungen für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




