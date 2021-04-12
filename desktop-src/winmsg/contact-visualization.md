---
description: Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn ein Eingabe Kontakt erkannt wird.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Kontakt Visualisierung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348189"
---
# <a name="contact-visualization"></a>Kontakt Visualisierung

Die folgenden Konstanten werden von Anwendungen oder Benutzeroberflächen-Frameworks verwendet, um zu ermitteln, wie das UI-Feedback verarbeitet wird, wenn ein Eingabe Kontakt erkannt wird.

Diese Konstanten werden mit den Parametern **SPI \_ getcontactvisuand** **SPI \_ setcontactvisuund** der Funktion [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) verwendet.

<dl> <dt>

<span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**contactvisualisierung \_ aus**
</dt> <dd> <dl> <dt>

0x0000
</dt> <dt>



Gibt an, dass das UI-Feedback für alle Kontakte deaktiviert ist.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**contactvisualisierung \_ in**
</dt> <dd> <dl> <dt>

0x0001
</dt> <dt>



Gibt an, dass das UI-Feedback für alle Kontakte on ist.


</dt> </dl> </dd> <dt>

<span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**"contactvisualisierung" ( \_ presentationmode)**
</dt> <dd> <dl> <dt>

0x0002
</dt> <dt>



Gibt an, dass Benutzeroberflächen Feedback für alle Kontakte mit visuellen Darstellung im Präsentationsmodus angezeigt wird.


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

[**Gesten Visualisierung**](gesture-visualization.md)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[Eingabe-Feedback-Konfiguration](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

