---
description: Um die eingebettete Benutzeroberfläche für die installation zu deaktivieren, die in der MsiEmbeddedUI-Tabelle definiert ist, legen Sie die MSIDISABLEEEUI-Eigenschaft in der Befehlszeile auf 1 fest.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: MSIDISABLEEEUI-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1e599ed0786c7d2c55644eb5759db3917757d3b41f6107161d72a3cc559484
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039950"
---
# <a name="msidisableeeui-property"></a>MSIDISABLEEEUI-Eigenschaft

Um die eingebettete Benutzeroberfläche für die installation zu deaktivieren, die in der [MsiEmbeddedUI-Tabelle](msiembeddedui-table.md)definiert ist, legen Sie die MSIDISABLEEEUI-Eigenschaft in der Befehlszeile auf 1 fest.

**[Windows Installer 4.0 und früher:](not-supported-in-windows-installer-4-0.md)** Wird nicht unterstützt. Versionen vor Windows Installer 4.5 ignorieren die MSIDISABLEEEUI-Eigenschaft.

## <a name="remarks"></a>Hinweise

Bei einer Installation mit mehreren Paketen sollte ein untergeordnetes Paket in der Regel die Benutzeroberfläche des übergeordneten Pakets verwenden und nicht seine eigene eingebettete Benutzeroberfläche initialisieren. Wenn die MSIDISABLEEEUI-Eigenschaft nicht innerhalb des übergeordneten Pakets festgelegt ist, verwendet das untergeordnete Paket standardmäßig die eingebettete Benutzeroberfläche des übergeordneten Pakets und ignoriert die MSIDISABLEEEUI-Eigenschaft innerhalb des untergeordneten Pakets.

Die MSIDISABLEEEUI-Eigenschaft deaktiviert die eingebettete Benutzeroberfläche für ein einzelnes Paket. Sie können die [Richtlinie MsiDisableEmbeddedUI](msidisableembeddedui.md) verwenden, um eingebettete Benutzeroberflächen für alle Pakete auf dem Computer zu deaktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installationsprogramm 4.5 auf Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP. Informationen zu den mindestens erforderlichen Windows Service Packs, die für eine Windows Installer-Version erforderlich sind, finden Sie unter Run-Time [Anforderungen](windows-installer-portal.md) für Windows Installer.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




