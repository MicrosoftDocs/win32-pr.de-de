---
description: Im Laufe der Zeit sind unter Umständen verschiedene Versionen für TAPI, Anwendungen und Dienstanbieter für eine Linie oder ein Telefon vorhanden.
ms.assetid: 36a17ae8-31db-4db9-a401-097d47aa26ad
title: Aushandlung der TAPI-Version
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f41f4ca6f12862d6fc19f982c48b90bdafe2aaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353617"
---
# <a name="tapi-version-negotiation"></a>Aushandlung der TAPI-Version

Im Laufe der Zeit sind unter Umständen verschiedene Versionen für TAPI, Anwendungen und Dienstanbieter für eine Linie oder ein Telefon vorhanden. Neue Versionen können neue Features, neue Felder für Datenstrukturen usw. definieren. Versionsnummern geben daher an, wie verschiedene Datenstrukturen interpretiert werden.

Um eine optimale Interoperabilität verschiedener Versionen von Anwendungen, Versionen von TAPI selbst und Versionen von Dienstanbietern durch verschiedene Lieferanten zu ermöglichen, bietet TAPI einen einfachen, zweistufigen Aushandlungs Mechanismus für-Anwendungen. Zwei verschiedene Versionen müssen von der Anwendung, TAPI und dem Dienstanbieter für jedes Zeilen Gerät vereinbart werden. Der erste ist die Versionsnummer für die einfache und ergänzende Telefonie und wird als API-Version bezeichnet. Die andere gilt für anbieterspezifische Erweiterungen, sofern vorhanden, und wird als Erweiterungs Version bezeichnet. Das Format der Datenstrukturen und Datentypen, die von den grundlegenden und ergänzenden Features von TAPI verwendet werden, wird durch die API-Version definiert, während die Erweiterungs Version das Format der Datenstrukturen bestimmt, die von den herstellerspezifischen Erweiterungen definiert werden.

Die Versions Aushandlung verläuft in zwei Phasen. In der ersten Phase wird die API-Versionsnummer ausgehandelt, und der Erweiterungs Bezeichner, der mit herstellerspezifischen, auf dem Gerät unterstützten Erweiterungen verknüpft ist, wird abgerufen. In der zweiten Phase wird die Erweiterungs Version ausgehandelt. Wenn die Anwendung keine API-Erweiterungen verwendet, überspringt Sie die zweite Phase, und Erweiterungen werden nicht vom Dienstanbieter aktiviert. Wenn die Anwendung Erweiterungen verwenden will, aber die Erweiterungen des Dienstanbieters (der Erweiterungs Bezeichner) von der Anwendung nicht erkannt werden, sollte die Anwendung auch die Aushandlung der Erweiterungs Version überspringen. Jeder Anbieter verfügt über einen eigenen Satz von zulässigen (anerkannten) Versionen für jeden Satz von Erweiterungs Spezifikationen, der von ihm verteilt wird.

Die [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) -Funktion wird verwendet, um die zu verwendende API-Versionsnummer auszuhandeln. Außerdem wird der vom liniengerät Unterstützte Erweiterungs Bezeichner abgerufen, und es werden Nullen zurückgegeben, wenn keine Erweiterungen unterstützt werden. Mit diesem Funktions aufrufbefehl stellt die Anwendung den API-Versions Bereich bereit, mit dem Sie kompatibel ist. TAPI verhandelt wiederum mit dem Dienstanbieter der Zeile, um zu bestimmen, welcher API-Versions Bereich unterstützt wird. TAPI wählt als nächstes eine Versionsnummer (in der Regel, auch wenn nicht unbedingt, die höchste Versionsnummer) im überlappenden Versions Bereich aus, den die Anwendung, die dll und der Dienstanbieter bereitgestellt haben. Diese Nummer wird an die Anwendung zurückgegeben, zusammen mit dem Erweiterungs Bezeichner, der die Erweiterungen definiert, die vom Dienstanbieter dieser Zeile verfügbar sind.

Wenn die Anwendung die Erweiterungen verwenden möchte, die durch den zurückgegebenen Erweiterungs Bezeichner definiert werden, muss zuerst [**linenegotiateextversion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) aufgerufen werden, um die Erweiterungs Version auszuhandeln. In einer ähnlichen Aushandlungs Phase gibt die Anwendung die bereits vereinbarte API-Version und den von ihr unterstützten Erweiterungs Versions Bereich an. TAPI übergibt diese Informationen an den Dienstanbieter für die Zeile. Der Dienstanbieter überprüft die API-Version und den Erweiterungs Versions Bereich gegen seinen eigenen und wählt die entsprechende Erweiterungs Versionsnummer aus, sofern vorhanden.

Wenn die Anwendung später [**linegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)aufruft, gibt Sie einen Satz von Gerätefunktionen für die Zeile zurück, die den Ergebnissen der Versions Aushandlung entsprechen. Hierzu gehören die Gerätefunktionen der Zeile, die mit der API-Version konsistent sind, sowie die gerätespezifischen Funktionen der Zeile, die der Erweiterungs Version entsprechen. Die Anwendung muss beide Versionsnummern angeben, wenn Sie eine Linie öffnet. An diesem Punkt werden die Anwendung, die dll und der Dienstanbieter für die Verwendung der vereinbarten Versionen verpflichtet. Wenn keine gerätespezifischen Erweiterungen verwendet werden sollen, sollte die Erweiterungs Version als 0 (null) angegeben werden.

In einer Umgebung, in der mehrere Anwendungen das gleiche Zeilen Gerät öffnen, wählt die erste Anwendung, die das liniengerät öffnet, die Versionen für alle zukünftigen Anwendungen aus, die die Zeile verwenden möchten (Dienstanbieter unterstützen nicht mehrere Versionen gleichzeitig). Auf ähnliche Weise kann eine Anwendung, die mehrere Linien Geräte öffnet, den Betrieb von allen Linien Geräten unter derselben API-Versionsnummer erleichtern.

Jede Funktion, die einen *dwapiversion* -Parameter oder einen ähnlichen Parameter annimmt, muss diesen Parameter entweder auf die höchste API-Version festlegen, die von der Anwendung unterstützt wird, oder auf die API-Version, die mit der Funktion [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) oder [**phonenegotiateapiversion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) auf einem bestimmten Gerät Verwenden Sie die folgende Tabelle als Richtlinie:



| Funktion                                                     | Bedeutung                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)             | Verwenden Sie die von [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)zurückgegebene Version.   |
| [**linegetcountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)                     | Verwenden Sie die höchste von der Anwendung unterstützte Version.                                     |
| [**linegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)                     | Verwenden Sie die von [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)zurückgegebene Version.   |
| [**linegetproviderlist**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist)           | Verwenden Sie die höchste von der Anwendung unterstützte Version.                                     |
| [**linegettranslatecaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)         | Verwenden Sie die höchste von der Anwendung unterstützte Version.                                     |
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   | Verwenden Sie die höchste von der Anwendung unterstützte Version.                                     |
| [**linenegotiateextversion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)   | Verwenden Sie die von [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)zurückgegebene Version.   |
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)                                 | Verwenden Sie die von [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)zurückgegebene Version.   |
| [**linetranslateaddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)         | Verwenden Sie die höchste von der Anwendung unterstützte Version.                                     |
| [**linetranslatedialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog)           | Verwenden Sie die höchste von der Anwendung unterstützte Version.                                     |
| [**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)                   | Verwenden Sie die von [**phonenegotiateapiversion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion)zurückgegebene Version. |
| [**phonenegotiateapiversion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Verwenden Sie die höchste von der Anwendung unterstützte Version.                                     |
| [**phonenegotiateextversion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Verwenden Sie die von [**phonenegotiateapiversion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion)zurückgegebene Version. |
| [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)                               | Verwenden Sie die von [**phonenegotiateapiversion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion)zurückgegebene Version. |



 

> [!IMPORTANT]
> Wenn Sie eine API-Version aushandeln, legen Sie die hohen und niedrigen Versionsnummern immer auf den Bereich von Versionen fest, der von der Anwendung unterstützt werden kann. Verwenden Sie z. b. niemals 0x00000000 für die niedrige Version oder 0xFFFFFFFF für den hohen Wert, da diese Werte erfordern, dass Ihre Anwendung alle Versionen von TAPI sowohl in der Vergangenheit als auch in der Zukunft unterstützt.

 

 

 



