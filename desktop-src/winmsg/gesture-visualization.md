---
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn eine der aufgelisteten Gesten erkannt wird.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Gesten Visualisierung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351042"
---
# <a name="gesture-visualization"></a>Gesten Visualisierung

Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn eine der aufgelisteten Gesten erkannt wird.

Diese Konstanten werden mit den **SPI \_ getgesturevisualisierungs** -und **SPI \_ setgesturevisualisierungs** -Parametern und der [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion verwendet.

**Hinweis**  

Zum Abrufen oder Festlegen von Pen-Visualisierungs Informationen wird empfohlen, dass Sie die **SPI \_ getpenvisualisierungs** -und **SPI \_ setpenvisualisierungs** Parameter und die in [**Pen-Visualisierung**](pen-visualization.md)aufgeführten Konstanten verwenden.

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**gesturevisualisierungen \_ aus**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Gibt an, dass das UI-Feedback für alle Gesten deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**gesturevisualisierung \_ in**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



Gibt an, dass Benutzeroberflächen Feedback für alle Gesten auf ON festgelegt ist


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**gesturevisualisierungs \_ tippen**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Gibt das UI-Feedback für eine Tap an.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**gesturevisualisierungs- \_ Double Tap**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Gibt das UI-Feedback für eine doppelte Tap an.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**gesturevisualisierungs- \_ pressandtap**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



Gibt das UI-Feedback für ein drücken und tippen an.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**gesturevisualisierungs- \_ pressandhold**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



Gibt das Benutzeroberflächen Feedback für einen Press-und-Halt an.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**gesturevisualisierungs- \_ RightTap**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



Gibt das UI-Feedback für einen richtigen Tap an.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                 |
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

 

