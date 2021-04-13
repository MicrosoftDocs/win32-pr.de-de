---
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn eine der aufgelisteten Stift Gesten erkannt wird.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Stift Visualisierung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529162"
---
# <a name="pen-visualization"></a>Stift Visualisierung

Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn eine der aufgelisteten Stift Gesten erkannt wird.

Diese Konstanten werden mit den Parametern für die **SPI \_ getpvisualisierung** und **SPI \_ setpvisualisierungen** und der [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion verwendet.

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**"pvisualisierung" \_ aus**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Gibt an, dass das UI-Feedback für alle Stift Gesten deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**pvisualisierung \_ am**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



Gibt an, dass das UI-Feedback für alle Stift Gesten eingeschaltet ist.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**pvisualisierung \_ tippen**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Gibt das UI-Feedback für eine Stift Abzweigung an.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**\_tavisualisierungs-Double Tap**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Gibt das Benutzeroberflächen Feedback für eine Stift-Doppel tippen an.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**pvisualisierung- \_ Cursor**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



Gibt das UI-Feedback für den Stift Cursor an.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konfigurations Konstanten](configuration-constants.md)
</dt> <dt>

[**Kontakt Visualisierung**](contact-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Eingabe-Feedback-Konfiguration](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

