---
description: Das Konzept einer Adresse ist das Kernstück zu den meisten Kommunikations Vorgängen.
ms.assetid: 32fbd06b-f6f2-4024-b8d5-3d6eef16bca2
title: Adresse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6ad8f03b725a58d564c63f4c5c0d0165eed99a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363580"
---
# <a name="address"></a>Adresse

Das Konzept einer Adresse ist das Kernstück zu den meisten Kommunikations Vorgängen. Eine Adresse stellt einen Speicherort in einem Netzwerk dar. Die lokale Zuweisung einer Adresse zu einer Zeile oder einem Kanal erfolgt in der Regel während der Installation des Dienstanbieters, kann jedoch später geändert werden. Details zu den beteiligten Prozeduren finden Sie im Ressourcenkit des Betriebssystems für von Microsoft bereitgestellte Dienstanbieter und in der Dokumentation des Dienstanbieters für nicht-Microsoft-Produkte.

Eine einzelne Adresse kann von mehr als einem Zeilen Gerät gemeinsam genutzt werden. Verschiedene switchanbieter haben unterschiedliche Namen für dieses Konzept, z. b. Adress Überbrückung, mehrfache Darstellung der Verzeichnis Nummer (madn) oder eine überbrückte Darstellung. Ein eingehender-Befehl für eine freigegebene Adresse wird für alle Zeilen angeboten, die mit der Adresse verknüpft sind. Eine Beschreibung der Konfigurationen, die von TAPI erkannt werden, finden Sie unter [lineaddresssharing- \_ Konstanten](./lineaddresssharing--constants.md) .

Die Adresse selbst ist eine Zeichenfolge, die einen Speicherort in einem Netzwerk identifiziert. Bei einem Telefon Netzwerk ist die Adresse eine Telefonnummer, die mit nationalen oder internationalen Codes fertiggestellt wird. Wenn das Netzwerk IP-basiert ist, kann die Adresse eine IP-Adresse sein. Weitere Informationen finden Sie unter [lineadresstype- \_ Konstanten](lineaddresstype--constants.md) für TAPI-definierte Adresstypen. Ein Dienstanbieter kann zusätzliche Adresstypen definieren.

## <a name="address-related-capabilities-and-messages"></a>Address-Related Funktionen und Nachrichten

Verschiedene Adressen haben unterschiedliche Funktionen, Funktionen und Zustände. Die Dienstanbieter sind die Quelle solcher Informationen. Die Funktionen "Geräte Abfrage" und "Status" und "Ereignis Berichterstattung" von TAPI stellen der Anwendung die Informationen zum Verwalten von Adressen zur Verfügung.

Anwendungen erhalten diese Informationen, indem Sie Ereignisse aus TAPI oder mithilfe von Abfrage Vorgängen verarbeiten. Dies ermöglicht es einer Anwendung, Faktoren zu berücksichtigen, z. b. ob eine bestimmte Adresse eine bestimmte Funktion unterstützt, z. b. [Park](park-ovr.md).

**TAPI 2. x:** Anwendungen können die Funktion [**linegetaddresscaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) aufrufen, um die Telefoniefunktionen der einzelnen Adressen zu ermitteln. diese Informationen werden dann in einer [**lineaddresscaps**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) -Datenstruktur empfangen. Auf ähnliche Weise kann eine Anwendung [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) für ein liniengerät aufrufen, um die Anzahl der der Zeile zugewiesenen Adressen sowie andere Informationen zu bestimmen.

**TAPI 3. x:** Anwendungen verwenden die [Adress Objekt Schnittstellen](address-object-interfaces.md) zum Abrufen von Informationen zu Adress Funktionen und-Ereignissen.

## <a name="storing-phone-numbers-in-electronic-address-books"></a>Speichern von Telefonnummern in elektronischen Adressbüchern

Viele Benutzer wählen Personen, faxcomputer, Bulletin Boards und andere Entitäten aus, indem Sie deren Namen aus einem Adressbuch auswählen. Die tatsächliche Anzahl der gewählten Werte hängt vom geografischen Standort des Benutzers und der Art der Verbindungs Herstellung mit dem liniengerät ab. Beispielsweise kann ein Desktop Computer über Zugriff auf zwei Zeilen verfügen, von denen eine mit einer PBX verbunden ist, die andere mit der zentral Niederlassung des telefonunternehmens. Wenn Sie dieselbe Partei anrufen, müssen möglicherweise unterschiedliche Zahlen verwendet werden. (Um z. b. die PBX zu wählen, muss der Computer möglicherweise ein "9"-Präfix wählen, um eine Außenlinie zu erhalten, oder es ist ein anderes Präfix für einen durch die zentrale Niederlassung erfolgten Rückruf erforderlich.) Alternativ kann ein Benutzer Anrufe von einem tragbaren Computer ausführen und ein einzelnes, statisches Adressbuch verwenden, auch wenn er von unterschiedlichen Standorten oder Telefonieumgebungen aufruft. Die Adress Übersetzungsfunktionen von TAPI ermöglichen dem Benutzer, den Computer über den aktuellen Standort und das gewünschte liniengerät für den-Befehl zu informieren. TAPI verarbeitet dann alle Unterschiede, die keine Änderungen am Adressbuch des Benutzers erfordern. In einer Anwendung wird die [Adressübersetzung](initiate-a-session-ovr.md) verwendet, um eine Adresse aus dem [kanonischen Adress](#canonical-addresses) Format in das Format der ddbaren Adresse zu konvertieren. [](#dialable-addresses)

Bei einem verwandten Thema handelt es sich um die Verarbeitung der internationalen Überwachung für den Bereitschafts Status. dabei handelt es sich um den Prozess, bei dem auf akustische Töne wie z. b. Wählton, besondere Informations Töne, ausgelastete Signale und ringbacktöne zum Ermitteln des *Zustands* eines Aufrufes (der Fortschritt über das Netzwerk) Da sich die Rhythmus-und Häufigkeits Werte von aufrufsfortschritts-Tönen von Land oder Region zu Land oder Region unterscheiden, muss der Dienstanbieter wissen, welcher Fortschritt bei internationalen ausgehenden Anrufen befolgt werden muss. Daher geben Anwendungen den Zielländer-oder Regions Code an, wenn Sie ausgehende Aufrufe platzieren.

## <a name="canonical-addresses"></a>Kanonische Adressen

Das kanonische Adressformat ist als universell Konstante Verzeichnis Nummer vorgesehen. Aus diesem Grund werden Zahlen in Adressbüchern im kanonischen Format am besten gespeichert.

Die folgenden Informationen beziehen sich auf das, was für eine Telefon Adresse als Canonical angesehen wird.

Eine kanonische Telefon Adresse ist eine Text Zeichenfolge mit der folgenden Struktur:

\+*CountryCode* Leerzeichen \[ **(**_areaCode_*_)_* \]  \| *untergeordneter Adress*  ^  *Name* CRLF...

Die Komponenten dieser Struktur werden in der folgenden Tabelle beschrieben.



Komponente

Bedeutung

\+

Äquivalent zu Hex 2B. Gibt an, dass die Zahl, die darauf folgt, das kanonische Format verwendet.

*CountryCode*

Eine Zeichenfolge variabler Größen, die eine oder mehrere Ziffern "0" bis "9" (hexadezimal 30 bis 39, einschließlich) enthält. *CountryCode* wird durch den folgenden Bereich getrennt. Es identifiziert das Land oder die Region, in dem sich die Adresse befindet.

LeerZchn

Genau ein Leerzeichen (Hex 20). Sie wird verwendet, um das Ende des *CountryCode* -Teils einer Adresse zu begrenzen.

*AreaCode*

Eine Zeichenfolge mit variabler Größen, die 0 (null) oder mehr der Ziffern "0" bis "9" (hexadezimal 30 bis 39, einschließlich) enthält. *AreaCode* ist der Bereichs Code Teil der Adresse und optional. Wenn der flächencode vorhanden ist, muss ihm genau ein linkes Klammer Zeichen (28) vorangestellt sein, und es muss genau ein schließende Klammer Zeichen (29) und ein Leerzeichen (20) befolgt werden.

*Abonnementnummer*

Eine Zeichenfolge variabler Größen, die eine oder mehrere Ziffern "0" bis "9" (hexadezimal 30 bis 39, einschließlich) enthält. Es können auch andere Formatierungszeichen enthalten sein, einschließlich der im Format der dikable-Adresse beschriebenen Wähl Steuerzeichen:

 

Zeichen

Hexadezimale Codierung

 

! \#<br/> $<br/> \*<br/> ,<br/> ?<br/> @<br/> ABCD<br/> P<br/> T<br/> W<br/> abcd<br/> p<br/> t<br/> w<br/>

21 23<br/> 24<br/> 2a<br/> 2C<br/> 3F<br/> 40<br/> 41-44<br/> 50<br/> 54<br/> 77<br/> 61-64<br/> 70<br/> 74<br/> 79<br/>

 

Die Abonnentennummer darf nicht die linke Klammer oder das Rechte Klammer Zeichen (die nur zum Begrenzen des Bereichs Codes verwendet werden) enthalten, und Sie sollte auch nicht die Zeichen " \| ", "^" oder CRLF enthalten, die zum Starten der folgenden Felder verwendet werden. In den meisten Fällen sind nicht Ziffern in der Abonnentennummer nur Leerzeichen, Punkte (".") und Bindestriche ("-") enthalten. Alle zulässigen nicht Ziffern Zeichen, die in der Abonnentennummer angezeigt werden, werden in der von der [**linetranslateaddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) -Funktion zurückgegebenen " *dialablestring* " ausgelassen, aber in " *displayablestring*" beibehalten.

\|

Hex (7C). Wenn dieses optionale Zeichen vorhanden ist, werden die folgenden Informationen bis zum nächsten + \| ^ CRLF oder das Ende der kanonischen Adress Zeichenfolge als unter Adressinformationen behandelt, wie für eine ISDN-unter Adresse.

*Unter Adresse*

Eine Zeichenfolge mit variabler Größenanpassung, die eine unter Adresse enthält. Die Zeichenfolge wird durch + \| ^ CRLF oder das Ende der Adress Zeichenfolge getrennt. Während des Wählens werden die Informationen zur untergeordneten Adresse an den Remote Anbieter übergeben. Dies kann z. b. eine ISDN-unter Adresse oder eine e-Mail-Adresse sein.

^

Hex (5E). Wenn dieses optionale Zeichen vorhanden ist, werden die Informationen nach dem nächsten CRLF oder dem Ende der kanonischen Adress Zeichenfolge als ISDN-Name behandelt.

*Name*

Eine Zeichenfolge mit variabler Größen, die als Namensinformationen behandelt wird. Der Name ist durch CRLF oder das Ende der kanonischen Adress Zeichenfolge begrenzt und kann andere Trennzeichen enthalten. Während des Wählens werden die Namen Informationen an den Remote Anbieter übergeben.

CRLF

Hex (0d), gefolgt von Hex (0A), und ist optional. Wenn vorhanden, gibt dies an, dass eine andere kanonische Zahl diesem folgt. Sie wird verwendet, um mehrere kanonische Adressen als Teil einer einzelnen Adress Zeichenfolge (umgekehrtes Multiplexing) voneinander zu trennen. Die kanonische Darstellung der Haupt switchboardtelefonnummer bei Microsoft Corporation wäre beispielsweise wie folgt:<br/> + 1 (425) 882-8080<br/>



 

## <a name="dialable-addresses"></a>Ddbare Adressen

Das Format der dialable-Adresse ist das Formular, in dem eine Adresse an einen Dienstanbieter übermittelt wird, der Telefonnummern verarbeitet. In den folgenden Details werden die in einem Telefon Netzwerk ausführbaren Adressen behandelt.

Das Format der ddbaren Zahlen ermöglicht das gleichzeitige Bereitstellen mehrerer Zieladressen. Diese Fähigkeit kann nützlich sein, wenn der Dienstanbieter eine Art umgekehrter Multiplexing bietet, indem er Aufrufe für jedes der angegebenen Ziele einrichtet und dann den Informationsdaten Strom als einzelnen Medienstrom mit hoher Bandbreite verwaltet. Die Anwendung erkennt diese Gruppe von Aufrufen als einen einzelnen Aufruf, da Sie nur ein einzelnes Aufruf handle empfängt, das das Aggregat der einzelnen Telefonanrufe repräsentiert.

Es ist auch möglich, ein umgekehrtes Multiplexing auf Anwendungsebene zu unterstützen. Zu diesem Zweck würde die Anwendung eine Reihe einzelner Aufrufe einrichten und ihre Mediendaten Ströme synchronisieren.

Die *unter Adressierung* ist eine Funktion, die in ISDN-Linien zur Verfügung gestellt wird, die mehr Informationen als nur eine einzige Telefonnummer für die Wahl bietet. Diese zusätzlichen Informationen können eine einzelne telefonerweiterung zum klingeln oder in einer Computerumgebung angeben, in der eine bestimmte Anwendung benachrichtigt werden soll. Mit anderen Parametern können die erforderlichen Aspekte einer angeforderten Verbindung, z. b. Rate und zeitliche Steuerung, beschrieben werden.

Wenn die subadressierung von einem Dienstanbieter unterstützt wird, schließt die Anwendung dies in die Adresse ein, die an jeden Vorgang, der einen solchen erfordert, übermittelt

Eine dfonisch-Telefon Adresse enthält Informationen zur Teil Adressierung und ist Teil Navigation. Jede Eingabe Zeichenfolge, die nicht mit einem "+"-Zeichen beginnt, wird vermutlich nicht in einem kanonischen Format vorliegen und muss daher im Format der ddbaren Adresse vorliegen und unverändert an die Anwendung zurückgegeben werden. Eine nicht ausführbare Adresse ist eine Text Zeichenfolge mit der folgenden Struktur:

*Dialablennummer* \| *Unter Adresse*  ^  *Name* CRLF...

Die Komponenten dieser Struktur sind in der folgenden Tabelle angegeben.



| Komponente        | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Dialablennummer* | Ziffern und Modifizierer 0-9 A-D \* \# ,! W w p t t @ $? ; getrennt durch \| ^ CRLF oder das Ende der Adress Zeichenfolge für die dialable. Das Pluszeichen (+) ist ein gültiges Zeichen in ausführbaren Zeichen folgen. Gibt an, dass die Telefonnummer eine voll qualifizierte internationale Nummer ist. Beachten Sie in der *dialablennummer* die folgenden Definitionen:<br/> 0-9 A-D \*\#<br/> Zeichen, die den DTMF-und/oder-pulsziffern entsprechen.<br/> |
| !                | Hex (21). Gibt an, dass ein "huokflash" (ein halbsekundenwert, der vor dem Fortsetzen von einem halben Sekunden-OFFHOOK liegt) in die Wählzeichenfolge eingefügt werden soll.                                                                                                                                                                                                                                                                                   |
| P p              | Hex (50) oder Hex (70). Gibt an, dass die Pulse-Wahl für die folgenden Ziffern verwendet werden soll.                                                                                                                                                                                                                                                                                                                                                |
| T t              | Hex (54) oder Hex (74). Gibt an, dass die unter Wahl von Tone (DTMF) für die folgenden Ziffern verwendet werden soll.                                                                                                                                                                                                                                                                                                                                          |
| ,                | Hex (27). Gibt an, dass die Wähl Ausführung angehalten werden soll. Die Dauer einer Pause ist gerätespezifisch und kann aus den Gerätefunktionen der Zeile abgerufen werden. Mehrere Kommas können verwendet werden, um längere Pausen bereitzustellen.                                                                                                                                                                                                                                 |
| W w              | Hex (57) oder Hex (77). Ein groß-oder Kleinbuchstabe W gibt an, dass die Wahl nur fortgesetzt werden soll, nachdem ein Wählton erkannt wurde.                                                                                                                                                                                                                                                                                                            |
| @                | Hex (40). Gibt an, dass die Wahl von "auf eine stille Antwort warten" festgelegt wird, bevor die restliche Adresse der Adresse unterschieden wird. Dies bedeutet, dass auf mindestens einen ringbackton gewartet wird, gefolgt von mehreren Sekunden Ruhezustand.                                                                                                                                                                                                                               |
| $                | Hex (24). Gibt an, dass bei der Wahl der Abrechnungsinformationen auf ein "Abrechnungs Signal" (z. b. ein Kreditkarten-Eingabe Aufforderungs Signal) gewartet werden soll.                                                                                                                                                                                                                                                                                                              |
| ?                | Hex (3F). Gibt an, dass der Benutzer aufgefordert werden soll, bevor er mit der Wahl fortfahren kann. Der Anbieter führt die Eingabeaufforderung nicht aus, aber durch das vorhanden sein von "?" wird der Anbieter gezwungen, die Zeichenfolge als ungültig abzulehnen, und die Anwendung muss dazu aufgefordert werden, Sie in Teile zu zerlegen und den Benutzer aufzufordern.                                                                                                                           |
| ;                | Hex (3B). Wenn Sie am Ende einer teilweise angegebenen ID-Adress Zeichenfolge platziert wird, weist dies darauf hin, dass die Informationen zu den ddbaren Zahlen unvollständig sind und später weitere Adressinformationen bereitgestellt werden. Die Komponente ";" ist nur im Teil " *dialablennummer* " einer Adresse zulässig.                                                                                                                                                       |
| \|               | Hex (7C), und ist optional. Falls vorhanden, werden die folgenden Informationen bis zum nächsten + \| ^ CRLF oder das Ende der Adress Zeichenfolge als unter Adressinformationen behandelt (wie für eine ISDN-unter Adresse).                                                                                                                                                                                                                                  |
| *Unter Adresse*     | Eine Zeichenfolge mit variabler Größenanpassung, die eine unter Adresse enthält. Die Zeichenfolge wird durch den nächsten + \| ^ CRLF oder das Ende der Adress Zeichenfolge getrennt. Beim unterscheiden werden die Informationen zu untergeordneten Adressen an den Remote Anbieter übergeben. Dies kann für eine ISDN-unter Adresse, eine e-Mail-Adresse usw. sein.                                                                                                                                                                       |
| ^                | Hex (5E), und ist optional. Falls vorhanden, werden die Informationen, die nach dem nächsten CRLF oder dem Ende der Adress Zeichenfolge für die Adresse stehen, als ISDN-Name behandelt.                                                                                                                                                                                                                                                                                |
| *Name*           | Eine Zeichenfolge mit variabler Größen, die als Namensinformationen behandelt wird. Der Name wird durch CRLF oder das Ende der Adress Zeichenfolge für die Adresse getrennt. Bei der Wahl werden die Namen Informationen an die Remote Seite übergeben.                                                                                                                                                                                                                                                      |
| CRLF             | Hex (0d), gefolgt von Hex (0A). Wenn dieses optionale Zeichen vorhanden ist, weist dies darauf hin, dass dieser eine andere Nummer folgt. Sie wird verwendet, um mehrere dkus able-Adressen als Teil einer einzelnen Adress Zeichenfolge (bei umgekehrtem Multiplexing) voneinander zu trennen.                                                                                                                                                                                           |



 

Die Adressübersetzung kann verwendet werden, um eine Adresse aus dem kanonischen Format in das-Format zu übersetzen.

 

