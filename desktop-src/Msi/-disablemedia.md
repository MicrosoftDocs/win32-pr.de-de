---
description: Durch Festlegen der DISABLEMEDIA-Eigenschaft wird verhindert, dass das Installationsprogramm Medienquellen wie cd-ROM als gültige Quelle für das Produkt registriert. Wenn das Durchsuchen aktiviert ist, kann ein Benutzer jedoch weiterhin zu einer Medienquelle navigieren.
ms.assetid: 83c4e7f6-fced-447f-bfa2-847dce660139
title: DISABLEMEDIA-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d56e6e50bdfe8a6ead05ad467caa355a7b6051715b65ec624e3cec6eea2affcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640455"
---
# <a name="disablemedia-property"></a>DISABLEMEDIA-Eigenschaft

Durch Festlegen der [**DISABLEMEDIA-Eigenschaft**](disablemedia.md) wird verhindert, dass das Installationsprogramm Medienquellen wie cd-ROM als gültige Quelle für das Produkt registriert. Wenn das Durchsuchen aktiviert ist, kann ein Benutzer jedoch weiterhin zu einer Medienquelle navigieren.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass die [**DISABLEMEDIA-Eigenschaft**](disablemedia.md) eine andere Auswirkung als das Festlegen der DisableMedia-Richtlinie hat. Durch festlegen von **DISABLEMEDIA** wird die Registrierung von Medienquellen verhindert, und dies verhindert auch die erstmalige Installation einer Anwendung aus einer Medienquelle.

Ausführliche Informationen zum Schützen der Medienquellen einer [*verwalteten Anwendung*](m-gly.md) vor dem Durchsuchen und Installieren durch Benutzer ohne Administratorrechte finden Sie unter [Quellresilienz.](source-resiliency.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




