---
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächenframeworks verwendet, um zu identifizieren, wie Benutzeroberflächenfeedback verarbeitet wird, wenn eine der aufgelisteten Stiftgesten erkannt wird.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Stiftvisualisierung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60b9f75493a361cc167b65fba1783bc01f909d76211b1076e2faccc2e6f00116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548490"
---
# <a name="pen-visualization"></a>Stiftvisualisierung

Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächenframeworks verwendet, um zu identifizieren, wie Benutzeroberflächenfeedback verarbeitet wird, wenn eine der aufgelisteten Stiftgesten erkannt wird.

Diese Konstanten werden mit den Parametern **SPI \_ GETPENVISUALIZATION** und **SPI \_ SETPENVISUALIZATION** und der [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) verwendet.

<dl> <dt>

<span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ OFF**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Gibt an, dass das Benutzeroberflächenfeedback für alle Stiftgesten deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_ ON**
</dt> <dd> <dl> <dt>

0x0023
</dt> <dt>



Gibt an, dass benutzeroberflächenfeedback für alle Stiftgesten eingeschaltet ist.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**TAP FÜR DIE \_ PENVISUALISIERUNG**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Gibt Benutzeroberflächenfeedback für einen Stifttipps an.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION \_ DOUBLETAP**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Gibt Benutzeroberflächenfeedback für einen Stift mit doppelter Tippung an.


</dt> </dl> </dd> <dt>

<span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION \_ CURSOR**
</dt> <dd> <dl> <dt>

0x0020
</dt> <dt>



Gibt Benutzeroberflächenfeedback für den Stiftcursor an.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                 |
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

 

