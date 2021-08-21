---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f9f888fcea9069ff31ccef6b2c1ef5a0148fbb34ba21d03ee881c52056f10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105538"
---
# <a name="iagentcharacterexgetsrstatus"></a>IAgentCharacterEx::GetSRStatus

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

Ruft den Status der Bedingung ab, die zur Unterstützung der Spracheingabe erforderlich ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Adresse einer Variablen, die einen der folgenden Werte für die Statuseinstellung empfängt:



| Wert                                                                               | Beschreibung                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const unsigned long** **LISTEN STATUS \_ \_ CANLISTEN = 0;**<br/>               | Bedingungen unterstützen Spracheingaben.                                                                                                                                                                                                          |
| **const unsigned long** **LISTEN STATUS \_ \_ NOAUDIO = 1;**<br/>                 | Auf diesem System ist kein Audioeingabegerät verfügbar. (Beachten Sie, dass dadurch nicht erkannt wird, ob ein Mikrofon installiert ist. Es kann nur erkannt werden, ob der Benutzer über eine ordnungsgemäß installierte eingabefähige Soundkarte mit einem funktionierenden Treiber verfügt.) |
| **const unsigned long** **LISTEN STATUS \_ \_ NOTTOPMOST = 2;**<br/>              | Ein anderer Client ist der aktive Client dieses Zeichens, oder das aktuelle Zeichen ist nicht ganz oben.                                                                                                                                           |
| **const unsigned long** **LISTEN STATUS \_ \_ CANTOPENAUDIO = 3;**<br/>           | Der Audioeingabe- oder -ausgabekanal ist derzeit ausgelastet, einige andere Anwendungen verwenden Audio.                                                                                                                                               |
| **const unsigned long** **LISTEN STATUS \_ \_ COULDNTINITIALIZESPEECH = 4;**<br/> | Beim Initialisieren des Spracherkennungssubsystems ist ein nicht angegebener Fehler aufgetreten. Dies schließt die Möglichkeit ein, dass keine Sprach-Engine verfügbar ist, die der Spracheinstellung des Zeichens entspricht.                          |
| **const unsigned long** **LISTEN STATUS \_ \_ SPEECHDISABLED = 5;**<br/>          | Der Benutzer hat die Spracheingabe im Fenster Erweiterte Zeichenoptionen deaktiviert.                                                                                                                                                              |
| **const unsigned long** **LISTEN STATUS ERROR = \_ \_ 6;**<br/>                   | Fehler beim Überprüfen des Audiostatus, aber die Ursache des Fehlers wurde vom System nicht zurückgegeben.                                                                                                                                |



 

</dd> </dl>

Mit dieser Funktion können Sie abfragen, ob aktuelle Bedingungen Spracherkennungseingaben unterstützen, einschließlich des Status des Audiogeräts. Wenn Ihre Anwendung die [**IAgentCharacterEx::Listen-Methode**](iagentcharacterex--listen.md) verwendet, können Sie diese Funktion verwenden, um besser sicherzustellen, dass der Aufruf erfolgreich ist. Wenn Sie diese Methode aufrufen, wird auch die Sprach-Engine geladen, wenn sie noch nicht geladen wurde. Der Überwachungsmodus wird jedoch nicht aktiviert.

Wenn die Spracheingabe im Eigenschaftenblatt des -Agents (Erweiterte Zeichenoptionen) aktiviert ist, wird beim Abfragen des Status die zugeordnete Engine geladen (sofern sie noch nicht geladen ist), und die Spracherkennungsdienste werden gestartet. Das heißt, der Überwachungsschlüssel ist verfügbar, und der Lauschtipp kann angezeigt werden. (Die Tasten "Lauschen" und "Lauschendes Tipp" sind nur aktiviert, wenn sie auch unter Erweiterte Zeichenoptionen aktiviert sind.) Wenn Sie jedoch die -Eigenschaft abfragen, wenn Sprache deaktiviert ist, startet der Server die Sprachdienste nicht.

Diese Funktion gibt nur die Einstellung für die Verwendung des Zeichens durch Ihre Clientanwendung zurück. Die Einstellung spiegelt keine anderen Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung wider.

 

 





