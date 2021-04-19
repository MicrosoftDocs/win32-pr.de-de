---
description: Legen Sie die msinodisablemedia-Eigenschaft fest, um zu verhindern, dass das Installationsprogramm die disablemedia-Eigenschaft festlegt. Durch Festlegen der disablemedia-Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Msinodisablemedia (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361352"
---
# <a name="msinodisablemedia-property"></a>Msinodisablemedia (Eigenschaft)

Legen Sie die **msinodisablemedia** -Eigenschaft fest, um zu verhindern, dass das Installationsprogramm die [**disablemedia**](-disablemedia.md) -Eigenschaft festlegt. Durch Festlegen der **disablemedia** -Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert.

Wenn **msinodisablemedia** nicht festgelegt ist, fügt das Installationsprogramm beim Ausführen einer [administrativen Installation](administrative-installation.md)möglicherweise [**disablemedia**](-disablemedia.md) zum Verwaltungs Eigenschaftenstream hinzu. Dadurch wird verhindert, dass Benutzer, die aus dem administrativen Image installieren, von einem Medium installiert werden, z. b. CD-ROM.

-   Beim Ausführen einer administrativen [**Installation fügt das**](-disablemedia.md) Installationsprogramm den Verwaltungs Eigenschaftenstream nur dann hinzu, wenn die Zusammenfassungs Eigenschaft der [**Seitenanzahl**](page-count-summary.md) kleiner als 150 ist.

Wenn [**disablemedia**](-disablemedia.md) in der Eigenschaft [**adminproperties**](adminproperties.md) aufgeführt ist, wird durch Festlegen von **msinodisablemedia** verhindert, dass **disablemedia** während einer administrativen Installation festgelegt wird. In diesem Fall kann das Installationsprogramm eine Medienquelle registrieren, und ein Benutzer kann dann die Option zur erneuten Installation aus der Medienquelle auswählen, wenn das ursprüngliche administrative Installations Image später nicht mehr verfügbar war.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003, Windows XP und Windows 2000. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




