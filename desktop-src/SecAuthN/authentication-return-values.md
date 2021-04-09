---
description: Listet die von Funktionen in Authentifizierungs-APIs zurückgegebenen Werte auf.
ms.assetid: ea519e5c-98b0-4a01-b2cc-e5ff736a5396
title: Authentifizierungs Rückgabewerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2831fbce55523b3d55a649ef18fb6a622f3ec0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042490"
---
# <a name="authentication-return-values"></a>Authentifizierungs Rückgabewerte

## <a name="network-provider-values"></a>Netzwerkanbieter Werte

Die [Netzwerkanbieter-API](network-provider-api.md) verwendet die folgenden definierten Werte.



| Wert                                                                           | BESCHREIBUNG                                               |
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Rückgabewerte für die Netzwerksicherheit](network-security-return-values.md)<br/> | Rückgabewerte, die von einem Netzwerkanbieter festgelegt werden können.<br/> |



 

## <a name="smart-card-return-values"></a>Smartcard-Rückgabewerte

[Smartcardfunktionen](authentication-functions.md) geben die folgenden Rückgabewerte zurück. Diese Rückgabewerte werden in "scarderr. h" definiert.

> [!Note]  
> Einige Rückgabewerte haben möglicherweise denselben Wert wie vorhandene Windows-Rückgabewerte, die eine ähnliche Bedingung kennzeichnen. Weitere Informationen zu Fehlercodes, die hier nicht aufgeführt sind, finden Sie unter [System Fehlercodes](/windows/desktop/Debug/system-error-codes).

 



| Wert                                                               | BESCHREIBUNG                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fehler bei der \_ \_ Pipe.<br/> 0x00000109<br/>                | Der Client hat versucht, eine Smartcard-Operation in einer Remote Sitzung auszuführen, z. b. eine Client Sitzung, die auf einem Terminal Server ausgeführt wird, und das verwendete Betriebssystem unterstützt keine Smartcardumleitung.<br/> |
| Karte, ungültige \_ \_ \_ Suche<br/> 0x80100029<br/>                | Fehler beim Festlegen des Smartcarddatei-Objekt Zeigers.<br/>                                                                                                                                 |
| Karte \_ \_ abgebrochen<br/> 0x80100002<br/>                | Die Aktion wurde durch eine [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel) -Anforderung abgebrochen.<br/>                                                                                                                        |
| Card \_ 't \_ verwerfen \_<br/> 0x8010000e<br/>            | Das System konnte die Medien nicht auf die angeforderte Weise löschen.<br/>                                                                                                                               |
| \_Karten-E- \_ Karte \_ nicht unterstützt<br/> 0x8010001c<br/>        | Die Smartcard erfüllt nicht die Mindestanforderungen für den Support.<br/>                                                                                                                                   |
| Card \_ - \_ Zertifikat nicht \_ verfügbar<br/> 0x8010002d<br/> | Das angeforderte Zertifikat konnte nicht abgerufen werden.<br/>                                                                                                                                                 |
| "SCard"- \_ \_ \_ Daten \_ verloren<br/> 0x8010002f<br/>         | Ein Kommunikationsfehler mit der Smartcard wurde erkannt. <br/>                                                                                                                                   |
| "SCard \_ E \_ dir \_ nicht \_ gefunden"<br/> 0x80100023<br/>          | Das angegebene Verzeichnis ist nicht auf der Smartcard vorhanden.<br/>                                                                                                                                        |
| \_Leser mit \_ doppelter \_ Karte<br/> 0x8010001b<br/>        | Der [*Reader*](/windows/desktop/SecGloss/r-gly) -Treiber hat keinen eindeutigen Leser Namen erzeugt.<br/>                                                                            |
| die SCard- \_ \_ Datei wurde \_ nicht \_ gefunden.<br/> 0x80100024<br/>         | Die angegebene Datei ist nicht auf der Smartcard vorhanden.<br/>                                                                                                                                             |
| Karte "Bestellung" für " \_ \_ ICC" \_<br/> 0x80100021<br/>         | Die angeforderte Reihenfolge der Objekt Erstellung wird nicht unterstützt.<br/>                                                                                                                                         |
| Installation von "SCard \_ E" \_ \_<br/> 0x80100020<br/>        | Es wurde kein primärer Anbieter für die Smartcard gefunden.<br/>                                                                                                                                             |
| \_ \_ nicht genügend- \_ Puffer<br/> 0x80100008<br/>     | Der Datenpuffer für die zurückgegebenen Daten ist zu klein für die zurückgegebenen Daten.<br/>                                                                                                                            |
| Card \_ E \_ ungültig \_<br/> 0x80100015<br/>             | Eine aus der Registrierung erhaltene [*ATR-Zeichenfolge*](/windows/desktop/SecGloss/a-gly) ist keine gültige ATR-Zeichenfolge.<br/>                                                        |
| Karte \_ \_ ungültiger \_ CHV<br/> 0x8010002a<br/>             | Die angegebene PIN ist falsch.<br/>                                                                                                                                                                   |
| Karte \_ \_ mit ungültigem \_ handle<br/> 0x80100003<br/>          | Das angegebene Handle war ungültig.<br/>                                                                                                                                                               |
| "SCard" \_ \_ ungültiger \_ Parameter<br/> 0x80100004<br/>       | Mindestens einer der angegebenen Parameter konnte nicht ordnungsgemäß interpretiert werden.<br/>                                                                                                                        |
| Karte \_ \_ ungültiges \_ Ziel<br/> 0x80100005<br/>          | Die Registrierungs Startinformationen fehlen oder sind ungültig.<br/>                                                                                                                                            |
| Tabelle \_ mit \_ ungültigem \_ Wert<br/> 0x80100011<br/>           | Mindestens einer der angegebenen Parameterwerte konnte nicht ordnungsgemäß interpretiert werden.<br/>                                                                                                                  |
| Card \_ E \_ kein \_ Zugriff<br/> 0x80100027<br/>               | Der Zugriff auf die Datei wurde verweigert.<br/>                                                                                                                                                                    |
| SCard \_ E \_ nicht \_ dir<br/> 0x80100025<br/>                  | Der angegebene Pfad stellt kein Smartcardverzeichnis dar.<br/>                                                                                                                                     |
| Karte \_ \_ keine \_ Datei<br/> 0x80100026<br/>                 | Der angegebene Pfad stellt keine Smartcarddatei dar.<br/>                                                                                                                                          |
| SCard \_ E \_ kein \_ Schlüssel \_ Container<br/> 0x80100030<br/>       | Der angeforderte Schlüssel Container ist auf der Smartcard nicht vorhanden.<br/>                                                                                                                                    |
| \_nicht genügend \_ Arbeits \_ Speicher<br/> 0x80100006<br/>               | Zum Ausführen dieses Befehls ist nicht genügend Arbeitsspeicher verfügbar.<br/>                                                                                                                                            |
| SCard \_ E \_ kein \_ Pin- \_ Cache<br/> 0x80100033<br/>           | Die Smartcard-PIN kann nicht zwischengespeichert werden.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Fehlercode ist nicht verfügbar.<br/> <br/>                        |
| Karte \_ \_ keine \_ Leser \_ verfügbar<br/> 0x8010002e<br/>   | Es ist kein Smartcardleser verfügbar.<br/>                                                                                                                                                               |
| Karte \_ \_ ohne \_ Dienst<br/> 0x8010001d<br/>              | Der Smartcard- [*Ressourcen-Manager*](/windows/desktop/SecGloss/r-gly) wird nicht ausgeführt.<br/>                                                                |
| Karte \_ \_ keine \_ Smartcard<br/> 0x8010000c<br/>            | Der Vorgang erfordert eine Smartcard, aber zurzeit ist keine Smartcard auf dem Gerät.<br/>                                                                                                               |
| Karte \_ \_ kein \_ solches \_ Zertifikat<br/> 0x8010002c<br/>    | Das angeforderte Zertifikat ist nicht vorhanden.<br/>                                                                                                                                                        |
| Karte \_ \_ nicht \_ bereit<br/> 0x80100010<br/>               | Der Reader oder die Karte ist nicht bereit, Befehle zu akzeptieren.<br/>                                                                                                                                              |
| Karte \_ \_ nicht \_ transaktiv<br/> 0x80100016<br/>          | Es wurde versucht, eine nicht vorhandene Transaktion zu beenden.<br/>                                                                                                                                            |
| Karte \_ \_ PCI \_ zu \_ klein<br/> 0x80100019<br/>          | Der PCI-Empfangs Puffer war zu klein.<br/>                                                                                                                                                            |
| Card \_ - \_ Pin- \_ Cache \_ abgelaufen<br/> 0x80100032<br/>      | Der Smartcard-PIN-Cache ist abgelaufen.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Fehlercode ist nicht verfügbar.<br/> <br/>                       |
| nicht übereinstimmende Karte \_ \_ \_<br/> 0x8010000f<br/>          | Die angeforderten Protokolle sind nicht mit dem Protokoll kompatibel, das zurzeit mit der Karte verwendet wird.<br/>                                                                                                       |
| \_ \_ \_ \_ kartene-Karte mit Leseberechtigung<br/> 0x80100034<br/>         | Die Smartcard ist schreibgeschützt und kann nicht in geschrieben werden.<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieser Fehlercode ist nicht verfügbar.<br/> <br/>       |
| der Card Reader ist nicht \_ \_ \_ verfügbar.<br/> 0x80100017<br/>      | Der angegebene Reader ist zurzeit nicht für die Verwendung verfügbar.<br/>                                                                                                                                         |
| der \_ Card \_ Reader \_ wird nicht unterstützt.<br/> 0x8010001a<br/>      | Der Reader-Treiber erfüllt die Mindestanforderungen für die Unterstützung nicht.<br/>                                                                                                                                |
| Card \_ - \_ Server \_ ist \_ ausgelastet.<br/> 0x80100031<br/>        | Der Smartcard-Ressourcen-Manager ist zu stark ausgelastet, um diesen Vorgang abzuschließen.<br/>                                                                                                                          |
| der Card- \_ \_ Dienst wurde \_ beendet.<br/> 0x8010001e<br/>         | Der Smartcard-Ressourcen-Manager wurde heruntergefahren.<br/>                                                                                                                                                   |
| \_Zuteilungs \_ \_ Verletzung bei der Karte<br/> 0x8010000b<br/>       | Der Zugriff auf die Smartcard ist aufgrund anderer ausstehender Verbindungen nicht möglich.<br/>                                                                                                                      |
| Card \_ - \_ System \_ abgebrochen<br/> 0x80100012<br/>        | Die Aktion wurde vom System abgebrochen, vermutlich zum Abmelden oder Herunterfahren.<br/>                                                                                                                       |
| SCard \_ - \_ Timeout<br/> 0x8010000A<br/>                  | Der vom Benutzer angegebene Timeout Wert ist abgelaufen.<br/>                                                                                                                                                   |
| Karte \_ \_ unerwartet<br/> 0x8010001f<br/>               | Unerwarteter Kartenfehler.<br/>                                                                                                                                                           |
| \_Karte " \_ \_ Karte unbekannt"<br/> 0x8010000d<br/>            | Der angegebene smartcardname wird nicht erkannt.<br/>                                                                                                                                                 |
| Karte \_ \_ unbekannter \_ Reader<br/> 0x80100009<br/>          | Der angegebene Leser Name wird nicht erkannt.<br/>                                                                                                                                                     |
| Card \_ E \_ unbekannter \_ Res- \_ MNG<br/> 0x8010002b<br/>        | Ein Unbekannter Fehlercode wurde zurückgegeben.<br/>                                                                                                                                                         |
| \_ \_ nicht unterstützte \_ Funktion<br/> 0x80100022<br/>     | Die angeforderte Funktion wird von dieser Smartcard nicht unterstützt.<br/>                                                                                                                                          |
| Card \_ E \_ \_ zu \_ viele schreiben<br/> 0x80100028<br/>         | Es wurde versucht, mehr Daten zu schreiben, als in das Zielobjekt passen würden.<br/>                                                                                                                      |
| "SCard F"- \_ \_ \_ Fehler<br/> 0x80100013<br/>              | Ein interner Kommunikationsfehler wurde festgestellt.<br/>                                                                                                                                              |
| \_ \_ interner \_ Fehler bei der SCard-F<br/> 0x80100001<br/>          | Interner Konsistenzprüfung fehlgeschlagen.<br/>                                                                                                                                                            |
| \_ \_ unbekannter \_ Fehler bei "SCard F"<br/> 0x80100014<br/>           | Es wurde ein interner Fehler festgestellt, aber die Quelle ist unbekannt.<br/>                                                                                                                                  |
| "SCard F" hat \_ \_ \_ zu \_ lange gewartet<br/> 0x80100007<br/>        | Ein interner Konsistenz Timer ist abgelaufen.<br/>                                                                                                                                                       |
| Karte \_ \_ Herunterfahren<br/> 0x80100018<br/>                 | Der Vorgang wurde abgebrochen, damit die Serveranwendung beendet werden kann.<br/>                                                                                                                          |
| Karte \_ \_ erfolgreich<br/>                                        | Es ist kein Fehler aufgetreten.<br/>                                                                                                                                                                        |
| die \_ Karte \_ \_ wurde vom \_ Benutzer abgebrochen.<br/> 0x8010006e<br/>      | Die Aktion wurde vom Benutzer abgebrochen.<br/>                                                                                                                                                             |
| "SCard W"- \_ \_ Cache \_ Element \_ nicht \_ gefunden<br/> 0x80100070<br/>  | Das angeforderte Element wurde im Cache nicht gefunden.<br/>                                                                                                                                              |
| "SCard"- \_ \_ Cache \_ Element ist \_ veraltet<br/> 0x80100071<br/>       | Das angeforderte Cache Element ist zu alt und wurde aus dem Cache gelöscht.<br/>                                                                                                                              |
| SCard \_ - \_ Cache \_ Element \_ zu \_ groß<br/> 0x80100072<br/>    | Das neue Cache Element überschreitet die maximale pro-Element-Größe, die für den Cache definiert ist.<br/>                                                                                                                      |
| \_Karte der Karten-W \_ \_ nicht \_ authentifiziert<br/> 0x8010006f<br/> | Der Smartcard wurde keine PIN angezeigt.<br/>                                                                                                                                                          |
| Karten \_ - \_ CHV \_ blockiert<br/> 0x8010006c<br/>             | Auf die Karte kann nicht zugegriffen werden, da die maximale Anzahl von PIN-Eingabe versuchen erreicht wurde.<br/>                                                                                                   |
| Karte \_ \_<br/> 0x8010006d<br/>                      | Das Ende der Smartcarddatei wurde erreicht.<br/>                                                                                                                                                 |
| \_Karte der \_ \_ Karten Karte entfernt<br/> 0x80100069<br/>            | Die Smartcard wurde entfernt, sodass keine weitere Kommunikation möglich ist.<br/>                                                                                                                       |
| \_Karte " \_ Karte zurücksetzen \_ "<br/> 0x80100068<br/>              | Die Smartcard wurde zurückgesetzt.<br/>                                                                                                                                                                        |
| \_ \_ Sicherheits \_ Verletzung für "SCard W"<br/> 0x8010006a<br/>      | Der Zugriff wurde aufgrund einer Sicherheitsverletzung verweigert.<br/>                                                                                                                                               |
| \_Karte mit \_ nicht angegebener \_ Karte<br/> 0x80100067<br/>          | Die Stromversorgung wurde von der Smartcard entfernt, sodass keine weitere Kommunikation möglich ist.<br/>                                                                                                       |
| \_Karte mit \_ nicht reagierender \_ Karte<br/> 0x80100066<br/>       | Die Smartcard antwortet nicht auf eine zurück Setzung.<br/>                                                                                                                                                     |
| \_Karte mit \_ nicht unterstützter \_ Karte<br/> 0x80100065<br/>        | Der Reader kann aufgrund von Konfigurations Konflikten bei der ATR-Zeichenfolge nicht mit der Karte kommunizieren.<br/>                                                                                                          |
| Karten \_ \_ falscher \_ CHV<br/> 0x8010006b<br/>               | Auf die Karte kann nicht zugegriffen werden, weil die falsche PIN angezeigt wurde.<br/>                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Fehler Codes](/windows/desktop/Debug/system-error-codes)
</dt> </dl>

 

