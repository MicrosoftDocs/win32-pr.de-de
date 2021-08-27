---
description: Der Wert der ProductVersion-Eigenschaft ist die Version des Produkts im Zeichenfolgenformat.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: ProductVersion-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e09d2fb436dffba5ae2fa98144d39e5824d09796472297db116a2a4543d55168
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074640"
---
# <a name="productversion-property"></a>ProductVersion-Eigenschaft

Der Wert der **ProductVersion-Eigenschaft** ist die Version des Produkts im Zeichenfolgenformat. Diese Eigenschaft ist REQUIRED.

Das Format der Zeichenfolge lautet wie folgt:

<dl> Hauptversion.Nebenversion.Build  
</dl>

Das erste Feld ist die Hauptversion und hat einen Höchstwert von 255. Das zweite Feld ist die Nebenversion und hat einen Höchstwert von 255. Das dritte Feld wird als Buildversion oder Updateversion bezeichnet und hat einen Maximalwert von 65.535.

## <a name="remarks"></a>Hinweise

Mindestens eines der drei Felder von **ProductVersion** muss für ein Upgrade mithilfe der Upgradetabelle geändert [werden.](upgrade-table.md) Jedes Update, bei dem nur der Paketcode geändert wird, **productVersion** und [**ProductCode**](productcode.md) jedoch unverändert bleiben, wird als [kleines Update](small-updates.md)bezeichnet. Die Drei-Versionen-Felder werden hauptsächlich der Einfachheit halber bereitgestellt. Wenn Sie z. B. **ProductVersion** ändern möchten, aber weder die Haupt- noch die Nebenversion ändern möchten, können Sie die Buildversion ändern.

Beachten Sie, dass Windows Installer nur die ersten drei Felder der Produktversion verwendet. Wenn Sie ein viertes Feld in Ihre Produktversion einfügen, ignoriert das Installationsprogramm das vierte Feld.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Unter [Windows Installer Run-Time Requirements (Anforderungen für](windows-installer-portal.md) Windows Installer) finden Sie Informationen zu den mindest erforderlichen Windows Service Packs für eine Windows Installer-Version.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Patchen und Upgrades](patching-and-upgrades.md)
</dt> <dt>

[Kleines Update](small-updates.md)
</dt> </dl>

 

 




