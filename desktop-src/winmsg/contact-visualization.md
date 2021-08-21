---
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächenframeworks verwendet, um zu identifizieren, wie Feedback zur Benutzeroberfläche verarbeitet wird, wenn ein Eingabekontakt erkannt wird.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Kontaktvisualisierung (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea196017b1731bb176cd21a7dc02aaa360f4fe70503bd204b9c488d38eff99ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437253"
---
# <a name="contact-visualization"></a>Kontaktvisualisierung

Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächenframeworks verwendet, um zu identifizieren, wie Feedback zur Benutzeroberfläche verarbeitet wird, wenn ein Eingabekontakt erkannt wird.

Diese Konstanten werden mit den **Parametern \_ SPI GETCONTACTVISUALIZATION** und **SPI \_ SETCONTACTVISUALIZATION** und der [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) verwendet.

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ OFF**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Gibt an, dass das Feedback zur Benutzeroberfläche für alle Kontakte deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_ ON**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Gibt Feedback zur Benutzeroberfläche für alle Kontakte an.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ PRESENTATIONMODE**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Gibt Benutzeroberflächenfeedback für alle Kontakte an, die mit visuellen Elementen im Präsentationsmodus aktiviert sind.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Konfigurationskonst constants (Konfigurationskonst constants](configuration-constants.md)
</dt> <dt>

[**Gestenvisualisierung**](gesture-visualization.md)
</dt> <dt>

[**Systemparametersinfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Konfiguration des Eingabefeedbacks](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

