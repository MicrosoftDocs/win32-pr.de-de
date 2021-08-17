---
description: Im Laufe der Zeit können verschiedene Versionen für TAPI, Anwendungen und Dienstanbieter für eine Leitung oder ein Telefon vorhanden sein.
ms.assetid: 36a17ae8-31db-4db9-a401-097d47aa26ad
title: TAPI-Versionsaushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cd6d816c07cb1c6c93d9cc219509f257d9a2695671b5197002171f0f819f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404065"
---
# <a name="tapi-version-negotiation"></a>TAPI-Versionsaushandlung

Im Laufe der Zeit können verschiedene Versionen für TAPI, Anwendungen und Dienstanbieter für eine Leitung oder ein Telefon vorhanden sein. Neue Versionen können neue Features, neue Felder für Datenstrukturen usw. definieren. Versionsnummern geben daher an, wie verschiedene Datenstrukturen interpretiert werden.

Um eine optimale Interoperabilität verschiedener Versionen von Anwendungen, Versionen von TAPI selbst und Versionen von Dienstanbietern durch verschiedene Anbieter zu ermöglichen, bietet TAPI einen einfachen, zweistufigen Mechanismus für die Versionsaushandlung für Anwendungen. Zwei verschiedene Versionen müssen von der Anwendung, TAPI, und dem Dienstanbieter für jedes Zeilengerät vereinbart werden. Die erste ist die Versionsnummer für Basic und Ergänzende Telefonie und wird als API-Version bezeichnet. Das andere gilt für anbieterspezifische Erweiterungen, sofern vorhanden, und wird als Erweiterungsversion bezeichnet. Das Format der Datenstrukturen und Datentypen, die von den grundlegenden und ergänzenden Funktionen von TAPI verwendet werden, wird durch die API-Version definiert, während die Erweiterungsversion das Format der Datenstrukturen bestimmt, die von den anbieterspezifischen Erweiterungen definiert werden.

Die Versionsaushandlung wird in zwei Phasen fortgesetzt. In der ersten Phase wird die API-Versionsnummer ausgehandelt, und der Erweiterungsbezeichner, der allen anbieterspezifischen Erweiterungen zugeordnet ist, die auf dem Gerät unterstützt werden, wird abgerufen. In der zweiten Phase wird die Erweiterungsversion ausgehandelt. Wenn die Anwendung keine API-Erweiterungen verwendet, überspringt sie die zweite Phase, und Erweiterungen werden vom Dienstanbieter nicht aktiviert. Wenn die Anwendung Erweiterungen verwenden möchte, aber die Erweiterungen des Dienstanbieters (der Erweiterungsbezeichner) von der Anwendung nicht erkannt werden, sollte die Anwendung auch die Aushandlung für die Erweiterungsversion überspringen. Jeder Anbieter verfügt über einen eigenen Satz von rechtlichen (erkannten) Versionen für jeden Satz von Erweiterungsspezifikationen, die er verteilt.

Die [**funktion lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) wird verwendet, um die zu verwendende API-Versionsnummer auszuhandeln. Außerdem wird der vom Zeilengerät unterstützte Erweiterungsbezeichner abgerufen, und es werden Nullen zurückgegeben, wenn keine Erweiterungen unterstützt werden. Mit diesem Funktionsaufruf stellt die Anwendung den API-Versionsbereich bereit, mit dem sie kompatibel ist. TAPI handelt wiederum mit dem Dienstanbieter der Zeile aus, um zu bestimmen, welcher API-Versionsbereich unterstützt wird. TAPI wählt als Nächstes eine Versionsnummer (in der Regel jedoch nicht unbedingt die höchste Versionsnummer) im überlappenden Versionsbereich aus, den die Anwendung, die DLL und der Dienstanbieter bereitgestellt haben. Diese Zahl wird zusammen mit dem Erweiterungsbezeichner, der die erweiterungen definiert, die vom Dienstanbieter dieser Zeile verfügbar sind, an die Anwendung zurückgegeben.

Wenn die Anwendung die durch den zurückgegebenen Erweiterungsbezeichner definierten Erweiterungen verwenden möchte, muss sie zuerst [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) aufrufen, um die Erweiterungsversion auszuhandeln. In einer ähnlichen Aushandlungsphase gibt die Anwendung die bereits festgelegte API-Version und den unterstützten Erweiterungsversionsbereich an. TAPI übergibt diese Informationen an den Dienstanbieter für die Zeile. Der Dienstanbieter überprüft die API-Version und den Erweiterungsversionsbereich anhand seiner eigenen Versionsnummer und wählt ggf. die entsprechende Erweiterungsversionsnummer aus.

Wenn die Anwendung später [**lineGetDevCaps aufruft,**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)gibt sie eine Reihe von Gerätefunktionen für die Zeile zurück, die den Ergebnissen der Versionsaushandlung entsprechen. Dazu gehören die Gerätefunktionen der Zeile, die mit der API-Version konsistent sind, und die gerätespezifischen Funktionen der Zeile, die mit der Erweiterungsversion konsistent sind. Die Anwendung muss beim Öffnen einer Zeile beide Versionsnummern angeben. An diesem Punkt werden die Anwendung, die DLL und der Dienstanbieter dazu verpflichtet, die vereinbarungsbasierten Versionen zu verwenden. Wenn gerätespezifische Erweiterungen nicht verwendet werden sollen, sollte die Erweiterungsversion als 0 (null) angegeben werden.

In einer Umgebung, in der mehrere Anwendungen das gleiche Zeilengerät öffnen, wählt die erste Anwendung, die das Liniengerät öffnet, die Versionen für alle zukünftigen Anwendungen aus, die die Zeile verwenden möchten (Dienstanbieter unterstützen nicht mehrere Versionen gleichzeitig). Ebenso kann es für eine Anwendung, die mehrere Zeilengeräte öffnet, einfacher sein, alle Zeilengeräte unter derselben API-Versionsnummer zu betreiben.

Jede Funktion, die eine *dwAPIVersion* oder einen ähnlichen Parameter verwendet, muss diesen Parameter entweder auf die höchste API-Version festlegen, die von der Anwendung unterstützt wird, oder die API-Version, die mithilfe der [**Funktion lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) oder [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) auf einem bestimmten Gerät ausgehandelt wurde. Verwenden Sie die folgende Tabelle als Richtlinie:



| Funktion                                                     | Bedeutung                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)             | Verwenden Sie die von [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)zurückgegebene Version.   |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)                     | Verwenden Sie die höchste version, die von der Anwendung unterstützt wird.                                     |
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)                     | Verwenden Sie die von [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)zurückgegebene Version.   |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist)           | Verwenden Sie die höchste version, die von der Anwendung unterstützt wird.                                     |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)         | Verwenden Sie die höchste version, die von der Anwendung unterstützt wird.                                     |
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   | Verwenden Sie die höchste version, die von der Anwendung unterstützt wird.                                     |
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)   | Verwenden Sie die von [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)zurückgegebene Version.   |
| [**lineÖffnen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)                                 | Verwenden Sie die von [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)zurückgegebene Version.   |
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)         | Verwenden Sie die höchste version, die von der Anwendung unterstützt wird.                                     |
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog)           | Verwenden Sie die höchste version, die von der Anwendung unterstützt wird.                                     |
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)                   | Verwenden Sie die von [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion)zurückgegebene Version. |
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Verwenden Sie die höchste version, die von der Anwendung unterstützt wird.                                     |
| [**phoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Verwenden Sie die von [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion)zurückgegebene Version. |
| [**phoneÖffnen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)                               | Verwenden Sie die von [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion)zurückgegebene Version. |



 

> [!IMPORTANT]
> Legen Sie beim Aushandeln einer API-Version immer die hohen und niedrigen Versionsnummern auf den Bereich der Versionen fest, die Ihre Anwendung unterstützen kann. Verwenden Sie beispielsweise niemals 0x00000000 für die niedrige Version oder 0xFFFFFFFF für die hohe Version, da diese Werte erfordern, dass Ihre Anwendung alle TapI-Versionen unterstützt, sowohl in der Vergangenheit als auch in der Zukunft.

 

 

 



