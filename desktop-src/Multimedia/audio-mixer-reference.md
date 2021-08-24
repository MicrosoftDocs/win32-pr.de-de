---
title: Audio Mixer Referenz
description: Audio Mixer Referenz
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- Multimediaaudio,Audiomixer
- Audio,Audiomixer
- Multimediaaudio, Mixerreferenz
- Audio, Mixerreferenz
- Audiomixer,Referenz
- Mixer, Referenz
- Referenz für Audiomixer,Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1602a9ac0631a3e81430285c8cd862215a437c72b03b41d87fad6cefa7e41827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786220"
---
# <a name="audio-mixer-reference"></a>Audio Mixer Referenz

In diesem Abschnitt werden die Funktionen, Strukturen und Meldungen beschrieben, die Audiomixern zugeordnet sind. Diese Elemente sind wie folgt gruppiert.

## <a name="querying-devices"></a>Abfragen von Geräten

-   [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>Öffnen und Schließen

-   [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>Abrufen Mixer Bezeichnern

-   [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>Abrufen von Liniensteuerelementen

-   [**MIXERCONTROL**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>Ändern von Steuerelementattributen

-   [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**MIXERCONTROLDETAILS \_ BOOLEAN**](/previous-versions//dd757295(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ SIGNED**](/previous-versions//dd757297(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ UNSIGNED**](/previous-versions//dd757298(v=vs.85))
-   [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>Abrufen von Zeileninformationen

-   [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**ÄNDERUNG \_ DES MM \_ MIXM-STEUERELEMENTS \_**](mm-mixm-control-change.md)
-   [**MM \_ MIXM \_ LINE \_ CHANGE**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>Senden User-Defined Nachrichten

-   [**mixerMessage**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio Mixer Referenz](audio-mixer-reference.md)
</dt> </dl>

 

 