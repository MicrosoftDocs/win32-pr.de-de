---
description: Um die eingebettete Benutzeroberfläche für die in der msiembeddedui-Tabelle definierte Installation zu deaktivieren, legen Sie die msidisableeeui-Eigenschaft in der Befehlszeile auf 1 fest.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Msidisableeeui (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361310"
---
# <a name="msidisableeeui-property"></a>Msidisableeeui (Eigenschaft)

Um die eingebettete Benutzeroberfläche für die in der [msiembeddedui-Tabelle](msiembeddedui-table.md)definierte Installation zu deaktivieren, legen Sie die msidisableeeui-Eigenschaft in der Befehlszeile auf 1 fest.

**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt. In früheren Versionen als Windows Installer 4,5 wird die msidisableeeui-Eigenschaft ignoriert.

## <a name="remarks"></a>Bemerkungen

Bei einer Installation mit mehreren Paketen sollte ein untergeordnetes Paket in der Regel die Benutzeroberfläche des übergeordneten Pakets verwenden und seine eigene eingebettete Benutzeroberfläche nicht initialisieren. Wenn die msidisableeeui-Eigenschaft nicht innerhalb des übergeordneten Pakets festgelegt wird, verwendet das untergeordnete Paket standardmäßig die eingebettete Benutzeroberfläche des übergeordneten Pakets und ignoriert die msidisableeeui-Eigenschaft innerhalb des untergeordneten Pakets.

Die msidisableeeui-Eigenschaft deaktiviert die eingebettete Benutzeroberfläche für ein einzelnes Paket. Sie können die Richtlinie " [msidisableembeddedui](msidisableembeddedui.md) " verwenden, um eingebettete Benutzeroberflächen für alle Pakete auf dem Computer zu deaktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,5 unter Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




