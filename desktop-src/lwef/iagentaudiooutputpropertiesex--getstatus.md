---
title: Iagentaudiooutputpropertiesex GetStatus
description: Iagentaudiooutputpropertiesex GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd89f4b3d8101ff15b868551626775e6f2e341f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388472"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>Iagentaudiooutputpropertiesex:: GetStatus

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

Ruft den Status des Audiokanals ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plstatus*
</dt> <dd>

Status des audioausgabekanals, bei dem es sich um einen der folgenden Werte handeln kann:



| Wert                                                                         | BESCHREIBUNG                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **Ganzzahl ohne Vorzeichen Short** **- \_ Audiostatus \_ verfügbar = 0;**<br/>         | Der audioausgabechannel ist verfügbar (nicht ausgelastet).                                                              |
| **Ganzzahl ohne Vorzeichen Short** -Audiostatus (Ganzzahl ohne Vorzeichen Short) **\_ \_ noaudio= 1;**<br/>           | Die Audioausgabe wird nicht unterstützt. Dies ist beispielsweise der Fall, weil keine Soundkarte vorhanden ist.                             |
| der Konstante **Ganzzahl ohne Vorzeichen Short** **\_ Audiostatus \_ kanopenaudio= 2;**<br/>     | Der audioausgabechannel kann nicht geöffnet werden (ist ausgelastet); beispielsweise, weil eine andere Anwendung Audiofunktionen wieder gibt. |
| " **Ganzzahl ohne Vorzeichen Short** **\_ \_ audiouser sprechender" = 3;**<br/>      | Der audioausgabechannel ist ausgelastet, weil der Server die Benutzer Spracheingabe verarbeitet.                            |
| Konstante **unsignierte** **\_ kurzaudiostatus \_ = 4;**<br/> | Der audioausgabechannel ist ausgelastet, weil zurzeit ein Zeichen spricht.                                    |
| " **Ganzzahl ohne Vorzeichen Short** **\_ Audiostatus" \_ sroverrideable = 5;**<br/>    | Der audioausgabechannel ist nicht ausgelastet, aber er wartet auf die Benutzer Spracheingabe.                                 |
| **Ganzzahl ohne Vorzeichen Short** **- \_ audiostatusfehler \_ = 6;**<br/>             | Beim Versuch, auf den audioausgabechannel zuzugreifen, ist ein anderes (Unbekanntes) Problem aufgetreten.                       |



 

</dd> </dl>

Mit dieser Einstellung kann Ihre Client Anwendung den Status des audioausgabekanals Abfragen. Sie können dies verwenden, um zu bestimmen, ob Ihr Zeichen sprechen soll oder zu versuchen, den Empfangsmodus zu aktivieren (mit [**iagentcharakteriex::**](lwef.iagentcharacterex::listen_method)Listening).

 

 





