---
title: Verwenden von Arrays, Zeichen folgen und Zeigern
description: Das Doctor-Programm (siehe \\ Beispiele \\ für den RPC- \\ Arzt im Platform Software Development Kit (SDK)) ist ein gutes Beispiel für eine Anwendung, die die Entwurfs Kompromisse im Hinblick auf Array-und Zeichen folgen Attribute veranschaulicht.
ms.assetid: 9aea94a1-ae1f-4bd6-9dd3-146edf0b5fec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542a174b9ffd742ecf88de7231449a780be8dca9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101763"
---
# <a name="using-arrays-strings-and-pointers"></a>Verwenden von Arrays, Zeichen folgen und Zeigern

Das Doctor-Programm (siehe \\ Beispiele \\ für den RPC- \\ Arzt im Platform Software Development Kit (SDK)) ist ein gutes Beispiel für eine Anwendung, die die Entwurfs Kompromisse im Hinblick auf Array-und Zeichen folgen Attribute veranschaulicht. Das Doktor Programm ist eine kleine Beispiel Version eines besser bekannten Programms, Eliza, das von künstlicher Intelligenz-Forscher Joseph Weizenbaums unter mit in den 1960er Jahren entwickelt wurde. Das Programm imitiert einen Therapeuten mithilfe eines einfachen Musterabgleich, um auf Eingaben in natürlicher Sprache zu reagieren.

Das Eliza-Programm hat die folgende Sitzung aufgezeichnet.



| Benutzer                                                | Eliza                                                     |
|-----------------------------------------------------|-----------------------------------------------------------|
| Alle Männer sind gleich.                                  | In welcher Weise?                                              |
| Sie sind immer etwas oder ein anderes. | Können Sie sich ein bestimmtes Beispiel vorstellen?                      |
| Nun, ich bin hier.               | Ihr Freund wurde Ihnen angezeigt.                        |
| Er sagt, dass ich viel Zeit gedrückt habe.             | Tut mir leid, dass Sie depressiv sind.                |
| Das ist richtig, ich bin unzufrieden.                            | Sollten Sie sich hier vorstellen, dass Sie nicht unzufrieden sein sollten? |
| Ich benötige Hilfe, Dies scheint sehr sicher zu sein.          | Was bedeutet es für Sie, wenn Sie Hilfe erhalten?           |
| Vielleicht habe ich gelernt, mit meiner Mutter zu gelangen.  | Weitere Informationen zu Ihrer Familie.                           |
| Meine Mutter kümmert mich um mich.                         | Welche anderen Personen in ihrer Familie kümmern sich um Sie?                |
| Mein Vater.                                          | Ihr Vater.                                              |
| Auf irgendeine Weise gefällt Ihnen mein Vater.                | Welche Ähnlichkeit sehen Sie?                              |



 

Das Doktor Programm kann in Client seitige und serverseitige Anwendungen aufgeteilt werden. Die Clientseite fordert den Patienten zur Eingabe auf und zeigt die Antwort des Arztes an. Die Serverseite verarbeitet die Patienten Eingaben und generiert die Antwort des Arztes. Dies ist ein klassisches Beispiel für eine Client/Server-Anwendung: der Client ist für die Benutzerinteraktion zuständig, während der Server die umfangreiche Rechen Last verarbeitet. Es werden nicht viele Daten an die Funktion übermittelt und von der Funktion zurückgegeben, aber da die Daten eine beträchtliche Menge an Verarbeitung erfordern, wird Sie vom Server verarbeitet.

Das Doktor Programm verwendet ein Zeichen Array für die Eingabe und gibt ein anderes Zeichen Array als Ausgabe zurück. In der folgenden Tabelle sind vier Möglichkeiten zum Übergeben von Zeichen Arrays zwischen Client und Server sowie die Attribute und Funktionen aufgeführt, die für die Implementierung der einzelnen Ansätze erforderlich sind.



| Vorgehensweise                       | Attribute oder Funktionen                                                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Arrays von gezählten Zeichen       | \[[Größe \_ ist](/windows/desktop/Midl/size-is) \] , \[ [Länge \_ ist](/windows/desktop/Midl/length-is) \] , \[ [ref](/windows/desktop/Midl/ref)\]                                         |
| Stub-verwaltete Zeichen folgen           | \[[Zeichenfolge](/windows/desktop/Midl/string) \] , \[ [ref](/windows/desktop/Midl/ref) \] , [Mittel l- \_ Benutzer \_ ](/windows/desktop/Midl/midl-user-allocate-1) Zuordnungen auf dem Server                  |
| Stub-verwaltete Zeichen folgen           | \[[Zeichenfolge](/windows/desktop/Midl/string) \] , \[ [eindeutig](/windows/desktop/Midl/unique) \] , [mittlere \_ Benutzer \_ ](/windows/desktop/Midl/midl-user-allocate-1) Zuordnungen auf Client und Server |
| Funktion, die eine Zeichenfolge zurückgibt | \[[eindeutig](/windows/desktop/Midl/unique)\]                                                                                                     |



 

Innerhalb der Einschränkungen, die diesen Kombinationen von Attributen zugeordnet sind, gibt es alternative Möglichkeiten, ein Zeichen Array vom Client an den Server zu senden und ein anderes Zeichen Array vom Server an den Client zurückzugeben.

In den folgenden Themen werden die Entwurfs Kompromisse zwischen den verschiedenen Schnittstellen veranschaulicht, mit denen diese Parameter verwaltet werden können.

-   [Arrays von gezählten Zeichen](counted-character-arrays.md)
-   [Zeichenfolgen](strings.md)
-   [Mehrere Ebenen von Zeigern](multiple-levels-of-pointers.md)

 

 