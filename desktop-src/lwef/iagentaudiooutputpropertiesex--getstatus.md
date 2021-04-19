---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380744"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>IAgentAudioOutputPropertiesEx::GetStatus

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

Ruft den Status des Audiokanals ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Status des Audioausgabekanals, der einer der folgenden Werte sein kann:



| Wert                                                                         | Beschreibung                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **const unsigned short** **AUDIO STATUS AVAILABLE = \_ \_ 0;**<br/>         | Der Audioausgabekanal ist verfügbar (nicht ausgelastet).                                                              |
| **const unsigned short** **AUDIO STATUS \_ \_ NOAUDIO = 1;**<br/>           | Die Audioausgabe wird nicht unterstützt. z. B. weil keine Soundkarte ist.                             |
| **const unsigned short** **AUDIO STATUS \_ \_ CANTOPENAUDIO = 2;**<br/>     | Der Audioausgabekanal kann nicht geöffnet werden (ist ausgelastet). Dies liegt beispielsweise daran, dass eine andere Anwendung Audio abspielt. |
| **const unsigned short** **AUDIO STATUS \_ \_ USERSPEAKING = 3;**<br/>      | Der Audioausgabekanal ist ausgelastet, da der Server Spracheingaben des Benutzers verarbeitet.                            |
| **const unsigned short** **AUDIO STATUS \_ \_ CHARACTERSPEAKING = 4;**<br/> | Der Audioausgabekanal ist ausgelastet, da derzeit ein Zeichen spricht.                                    |
| **const unsigned short** **AUDIO STATUS \_ \_ SROVERRIDEABLE = 5;**<br/>    | Der Audioausgabekanal ist nicht ausgelastet, wartet aber auf die Spracheingabe des Benutzers.                                 |
| **const unsigned short** **AUDIO STATUS ERROR = \_ \_ 6;**<br/>             | Es gab ein anderes (unbekanntes) Problem beim Versuch, auf den Audioausgabekanal zu zugreifen.                       |



 

</dd> </dl>

Mit dieser Einstellung kann Ihre Clientanwendung den Status des Audioausgabekanals abfragen. Sie können damit bestimmen, ob Das Zeichen sprechen soll oder ob sie versuchen soll, den Lauschmodus zu aktivieren (mithilfe von **IAgentCharacterEx::Listen**).

 

 





