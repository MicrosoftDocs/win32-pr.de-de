---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb161a72b536f85a8a82923841e2cd14ecd9e3525ab993f8b7c71f34630b0d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601310"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>IAgentAudioOutputPropertiesEx::GetStatus

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

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
| **const unsigned short** **AUDIO STATUS \_ \_ NOAUDIO = 1;**<br/>           | Audioausgabe wird nicht unterstützt. beispielsweise, weil keine Soundkarte vorhanden ist.                             |
| **const unsigned short** **AUDIO STATUS \_ \_ CANTOPENAUDIO = 2;**<br/>     | Der Audioausgabekanal kann nicht geöffnet werden (ist ausgelastet). z. B. , weil eine andere Anwendung Audio wieder gibt. |
| **const unsigned short** **AUDIO STATUS \_ \_ USERSPEAKING = 3;**<br/>      | Der Audioausgabekanal ist ausgelastet, da der Server die Spracheingabe von Benutzern verarbeitet.                            |
| **const unsigned short** **AUDIO STATUS \_ \_ CHARACTERSPEAKING = 4;**<br/> | Der Audioausgabekanal ist ausgelastet, da derzeit ein Zeichen spricht.                                    |
| **const unsigned short** **AUDIO STATUS \_ \_ SROVERRIDEABLE = 5;**<br/>    | Der Audioausgabekanal ist nicht ausgelastet, wartet jedoch auf die Spracheingabe des Benutzers.                                 |
| **const unsigned short** **AUDIO STATUS ERROR = \_ \_ 6;**<br/>             | Es gab ein anderes (unbekanntes) Problem beim Versuch, auf den Audioausgabekanal zuzugreifen.                       |



 

</dd> </dl>

Mit dieser Einstellung kann Ihre Clientanwendung den Status des Audioausgabekanals abfragen. Sie können damit bestimmen, ob Ihr Zeichen sprechen soll, oder um zu versuchen, den Überwachungsmodus zu aktivieren (mithilfe von **IAgentCharacterEx::Listen**).

 

 





