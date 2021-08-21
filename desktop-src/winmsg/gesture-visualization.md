---
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächenframeworks verwendet, um zu identifizieren, wie Benutzeroberflächenfeedback verarbeitet wird, wenn eine der aufgelisteten Gesten erkannt wird.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Gestenvisualisierung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f572addf2ad7a98dbe3afc63c69a305ea15546e9533918d952271372cf52b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849819"
---
# <a name="gesture-visualization"></a>Gestenvisualisierung

Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächenframeworks verwendet, um zu identifizieren, wie Benutzeroberflächenfeedback verarbeitet wird, wenn eine der aufgelisteten Gesten erkannt wird.

Diese Konstanten werden mit den Parametern **SPI \_ GETGESTUREVISUALIZATION** und **SPI \_ SETGESTUREVISUALIZATION** und der [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) verwendet.

**Hinweis**  

Zum Abrufen oder Festlegen von Stiftvisualisierungsinformationen wird empfohlen, die Parameter **SPI \_ GETPENVISUALIZATION** und **SPI \_ SETPENVISUALIZATION** sowie die konstanten zu verwenden, die unter [**Stiftvisualisierung**](pen-visualization.md)aufgeführt sind.

<dl> <dt>

<span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ OFF**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Gibt an, dass das Benutzeroberflächenfeedback für alle Gesten deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_ ON**
</dt> <dd> <dl> <dt>

0x001F
</dt> <dt>



Gibt an, dass benutzeroberflächenfeedback für alle Gesten eingeschaltet ist.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**\_GESTENVISUALISIERUNGS-TAP**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Gibt Benutzeroberflächenfeedback für einen Tippen an.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Gibt Benutzeroberflächenfeedback für einen doppelten Tippen an.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**
</dt> <dd> <dl> <dt>

0x0004
</dt> <dt>



Gibt Benutzeroberflächenfeedback für ein Drücken und Tippen an.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**
</dt> <dd> <dl> <dt>

0x0008
</dt> <dt>



Gibt Benutzeroberflächenfeedback für ein Drücken und Halten an.


</dt> </dl> </dd> <dt>

<span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**
</dt> <dd> <dl> <dt>

0x0010
</dt> <dt>



Gibt Benutzeroberflächenfeedback für einen Tippen mit der rechten Seite an.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Konfigurationskonstanten](configuration-constants.md)
</dt> <dt>

[**Kontaktvisualisierung**](contact-visualization.md)
</dt> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Konfiguration des Eingabefeedbacks](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

