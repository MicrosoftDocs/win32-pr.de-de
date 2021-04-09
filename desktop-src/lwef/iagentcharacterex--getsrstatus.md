---
title: Iagentcharakteriex gezrstatus
description: Iagentcharakteriex gezrstatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036776"
---
# <a name="iagentcharacterexgetsrstatus"></a>Iagentcharakteriex:: gezrstatus

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

Ruft den Status der Bedingung ab, die zur Unterstützung der Spracheingabe erforderlich ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plstatus*
</dt> <dd>

Adresse einer Variablen, die einen der folgenden Werte für die Zustands Einstellung empfängt:



| Wert                                                                               | BESCHREIBUNG                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Status von **konstant gestattenunsigned Long** - **lauschen \_ \_ = 0;**<br/>               | Bedingungen unterstützen Spracheingaben.                                                                                                                                                                                                          |
| "Konstante **nicht signiertes langes** **lauschen" \_ -Status " \_ noaudio= 1;** "<br/>                 | Auf diesem System ist kein Audioeingabegerät verfügbar. (Beachten Sie, dass hierdurch nicht erkannt wird, ob ein Mikrofon installiert ist. es kann nur erkennen, ob der Benutzer über eine ordnungsgemäß installierte Audiokarte mit einem funktionierenden Treiber verfügt.) |
| konstanter **nicht signierter Long** **- \_ \_ lausch Status, Status:**<br/>              | Ein anderer Client ist der aktive Client dieses Zeichens, oder das aktuelle Zeichen ist nicht oberstes Zeichen.                                                                                                                                           |
| konstanter **nicht signierter langer** lausch **\_ Status \_ kanopenaudio= 3;**<br/>           | Die Audioeingabe oder der Ausgabekanal ist derzeit ausgelastet, eine andere Anwendung verwendet Audiodaten.                                                                                                                                               |
| der Konstante **Ganzzahl ohne Vorzeichen long** -lausch **\_ Status \_ konnte dntinitializespeech = 4;**<br/> | Beim Initialisieren des sprach Erkennungs Subsystems ist ein nicht spezifizierter Fehler aufgetreten. Dies schließt die Möglichkeit ein, dass keine Sprach-Engine verfügbar ist, die der Spracheinstellung des Zeichens entspricht.                          |
| **Ganzzahl ohne Vorzeichen long** -lausch **\_ Status \_ -Status**<br/>          | Der Benutzer hat die Spracheingabe im Fenster "erweiterte Zeichen Optionen" deaktiviert.                                                                                                                                                              |
| Status Fehler für "lange Überwachung ( **lange) nicht signiert** **\_ \_ = 6;** "<br/>                   | Beim Überprüfen des Audiostatus ist ein Fehler aufgetreten, aber die Ursache des Fehlers wurde vom System nicht zurückgegeben.                                                                                                                                |



 

</dd> </dl>

Mit dieser Funktion können Sie Abfragen, ob aktuelle Bedingungen sprach Erkennungs Eingaben unterstützen, einschließlich des Status des Audiogeräts. Wenn Ihre Anwendung die [**iagentcharakteriex::**](iagentcharacterex--listen.md) Listener-Methode verwendet, können Sie diese Funktion verwenden, um sicherzustellen, dass der-Vorgang erfolgreich ausgeführt wird. Wenn Sie diese Methode aufrufen, wird auch die Sprach-Engine geladen, wenn Sie nicht bereits geladen ist. Der Überwachungsmodus wird jedoch nicht aktiviert.

Wenn die Spracheingabe auf der Eigenschaften Seite des-Agents aktiviert ist (erweiterte Zeichen Optionen), wird durch Abfragen des Status die zugeordnete Engine geladen (sofern Sie nicht bereits geladen wurde) und Sprachdienste starten. Das heißt, der lauschende Schlüssel ist verfügbar, und der Abhör Tipp kann angezeigt werden. (Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server die Sprachdienste nicht.

Diese Funktion gibt nur die Einstellung für die Verwendung des Zeichens durch die Client Anwendung zurück. die Einstellung entspricht nicht anderen Clients des Zeichens oder anderen Zeichen ihrer Client Anwendung.

 

 





