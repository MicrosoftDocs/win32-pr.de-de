---
title: Verwenden von Arrays, Zeichenfolgen und Zeigern
description: Das Programm "Doctor" (siehe Beispiele für \\ rpc doctor im Platform Software Development Kit \\ \\ (SDK)) ist ein gutes Beispiel für eine Anwendung, die die entwurfsbezogenen Vor- und Vorzeichen im Zusammenhang mit Array- und Zeichenfolgenattributen veranschaulicht.
ms.assetid: 9aea94a1-ae1f-4bd6-9dd3-146edf0b5fec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8371c9c60f19e6ce59c62da637cbe2e844e919984b9c2c905053b61e6deb251b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010839"
---
# <a name="using-arrays-strings-and-pointers"></a>Verwenden von Arrays, Zeichenfolgen und Zeigern

Das Programm "Doctor" (siehe Beispiele für \\ rpc doctor im Platform Software Development Kit \\ \\ (SDK)) ist ein gutes Beispiel für eine Anwendung, die die entwurfsbezogenen Vor- und Vorzeichen im Zusammenhang mit Array- und Zeichenfolgenattributen veranschaulicht. Das Doctor-Programm ist eine kleine Beispielversion eines bekannteren Programms, Eliza, das in den 1960er Jahren von dem Künstlichen Intelligenz-ForscherIfiziellenIfizär Heißtbaum am MIT entwickelt wurde. Das Programm imitiert eine Ante mithilfe eines einfachen Musterabgleichs, um auf Eingaben in natürlicher Sprache zu reagieren.

Das Eliza-Programm hat die folgende Sitzung aufgezeichnet.



| Benutzer                                                | Eliza                                                     |
|-----------------------------------------------------|-----------------------------------------------------------|
| Die Menschen sind alle gleich.                                  | In welcher Weise?                                              |
| Sie stoßen uns immer auf etwas oder andere Fehler an. | Können Sie sich ein bestimmtes Beispiel vorstellen?                      |
| Nun, mein Freund hat mich hierher gebracht.               | Ihr Freund hat Sie hierher gebracht.                        |
| Er sagt, dass ich einen Großteil der Zeit ausgelastet habe.             | Ich habe leider gehört, dass Sie ausgelastet sind.                |
| Das ist richtig, ich bin unentmutbar.                            | Denken Sie, dass die Ankunft hier Ihnen hilft, nicht unzumutbar zu sein? |
| Ich benötige Hilfe. so viel scheint sicher zu sein.          | Was würde es für Sie bedeuten, wenn Sie Hilfe erhalten würden?           |
| Vielleicht könnte ich lernen, mich mit meinen Eltern zu machen.  | Teilen Sie mir mehr über Ihre Familie mit.                           |
| Meine Mutter kümmert sich um mich.                         | Wer sich andere Personen in Ihrer Familie um Sie kümmern?                |
| Mein Vater.                                          | Ihr Familienpate.                                              |
| Sie sind in gewisser Weise wie mein Freund.                | Welche Ähnlichkeit sehen Sie?                              |



 

Das Programm "Doctor" kann in clientseitige und serverseitige Anwendungen aufgeteilt werden. Die Clientseite fordert den Patienten zur Eingabe auf und zeigt die Antwort des Arztes an. Die Serverseite verarbeitet die Patienteneingabe und generiert die Antwort des Arztes. Dies ist ein klassisches Beispiel für eine Client-Server-Anwendung: Der Client ist für die Benutzerinteraktion verantwortlich, während der Server die umfangreiche Rechenlast verarbeitet. Es werden nicht viele Daten an die Funktion übergeben und zurückgegeben, aber da die Daten eine erhebliche Verarbeitung erfordern können, verarbeitet der Server sie.

Das Programm "Doctor" verwendet ein Zeichenarray für die Eingabe und gibt ein weiteres Zeichenarray als Ausgabe zurück. In der folgenden Tabelle sind vier Möglichkeiten zum Übergeben von Zeichenarrays zwischen Client und Server sowie die Attribute und Funktionen aufgeführt, die zum Implementieren der einzelnen Ansätze erforderlich sind.



| Vorgehensweise                       | Attribute oder Funktionen                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Gezählte Zeichenarrays       | \[[size \_ ist](/windows/desktop/Midl/size-is) \] , length \[ [ \_ ist](/windows/desktop/Midl/length-is) \] , \[ [ref](/windows/desktop/Midl/ref)\]                                         |
| Stubverwaltete Zeichenfolgen           | \[[string](/windows/desktop/Midl/string) \] , \[ [ref](/windows/desktop/Midl/ref) \] , [midl user \_ \_ allocate](/windows/desktop/Midl/midl-user-allocate-1) on server                  |
| Stubverwaltete Zeichenfolgen           | \[[String](/windows/desktop/Midl/string) \] , \[ [eindeutig](/windows/desktop/Midl/unique) \] , [midl user \_ \_ allocate](/windows/desktop/Midl/midl-user-allocate-1) on client and server |
| Funktion, die eine Zeichenfolge zurückgibt | \[[unique](/windows/desktop/Midl/unique)\]                                                                                                     |



 

Innerhalb der Einschränkungen, die diesen Kombinationen von Attributen zugeordnet sind, gibt es alternative Möglichkeiten, ein Zeichenarray vom Client an den Server zu senden und ein anderes Zeichenarray von Server zu Client zurückzugeben.

Die folgenden Themen veranschaulichen die Entwurfsabstände zwischen den verschiedenen Schnittstellen, die diese Parameter verwalten können.

-   [Gezählte Zeichenarrays](counted-character-arrays.md)
-   [Zeichenfolgen](strings.md)
-   [Mehrere Zeigerebenen](multiple-levels-of-pointers.md)

 

 