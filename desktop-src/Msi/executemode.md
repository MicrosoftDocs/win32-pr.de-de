---
description: Die executemode-Eigenschaft gibt an, wie das Installationsprogramm Systemupdates ausführt.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Executemode (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370861"
---
# <a name="executemode-property"></a>Executemode (Eigenschaft)

Die **executemode** -Eigenschaft gibt an, wie das Installationsprogramm Systemupdates ausführt. Diese Eigenschaft ist möglicherweise nützlich, wenn es erforderlich ist, eine Installation auszuführen, ohne das System tatsächlich zu ändern. Die-Eigenschaft kann auf keine festgelegt werden, um Aktualisierungs Vorgänge wie die Installation von Dateien und Registrierungs Werten zu deaktivieren.

Diese Eigenschaft kann einen der folgenden beiden Werte aufweisen. Das Installationsprogramm überprüft nur den ersten Buchstaben des Werts und berücksichtigt die Groß-/Kleinschreibung nicht.

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>Gar
</dt> <dd>

Es werden keine Änderungen am System vorgenommen. Das Installationsprogramm führt die Benutzeroberfläche aus und fragt dann die Datenbank ab.

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Web
</dt> <dd>

Alle Änderungen am System werden durch die Skriptausführung vorgenommen. Dies ist der Standardmodus.

</dd> </dl>

## <a name="default-value"></a>Standardwert

Wenn diese Eigenschaft nicht definiert ist, wird für den Ausführungs Modus standardmäßig Script verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




