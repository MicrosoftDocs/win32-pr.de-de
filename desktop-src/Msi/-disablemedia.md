---
description: Durch Festlegen der disablemedia-Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert. Wenn das Durchsuchen aktiviert ist, kann ein Benutzer jedoch trotzdem eine Medienquelle durchsuchen.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: Disablemedia (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc1cad17269541fdb60573ae11065d485af9bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369521"
---
# <a name="disablemedia-property"></a>Disablemedia (Eigenschaft)

Durch Festlegen der [**disablemedia**](disablemedia.md) -Eigenschaft wird verhindert, dass das Installationsprogramm eine Medienquelle, z. b. eine CD-ROM, als gültige Quelle für das Produkt registriert. Wenn das Durchsuchen aktiviert ist, kann ein Benutzer jedoch trotzdem eine Medienquelle durchsuchen.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass die [**disablemedia**](disablemedia.md) -Eigenschaft eine andere Auswirkung hat als das Festlegen der disablemedia-Richtlinie. Durch das Festlegen von **disablemedia** wird die Registrierung einer Medienquelle verhindert. Dadurch wird auch die erstmalige Installation einer Anwendung aus den Medienquellen verhindert.

Ausführliche Informationen zum Sichern der Medienquellen der [*verwalteten Anwendung*](m-gly.md) für das Durchsuchen und installieren durch nicht Administratoren finden Sie unter [Quellen Resilienz](source-resiliency.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




