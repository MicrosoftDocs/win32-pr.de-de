---
description: Die wichtigsten Informationen, die eine Anwendung zum Initiieren einer Kommunikationssitzung liefert, sind der Adresstyp, der Medientyp oder die Medientypen und die Zieladresse.
ms.assetid: 65e53587-0e40-411b-8d6c-d6adfc9d1e6c
title: Initiieren einer Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0226fc1b04ea5859bc4a96b6f5ca43e3749e7664a9ccf6810b586115171530b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975850"
---
# <a name="initiate-a-session"></a>Initiieren einer Sitzung

Die wichtigsten Informationen, die eine Anwendung zum Initiieren einer [](media-type-ovr.md) Kommunikationssitzung liefert, sind der Adresstyp, [](address-type-ovr.md)der Medientyp oder die Medientypen und die [Zieladresse.](address-ovr.md)

Die Zieladresse erfordert möglicherweise eine [Adressübersetzung,](#address-translation) um die von einem Benutzer eingegebenen Informationen in das richtige Format für einen bestimmten Adresstyp zu setzen. Beispielsweise erfordert eine Telefonnummer in einem elektronischen Adressbuch [im](address-ovr.md) kanonischen Format eine Übersetzung in das [Wählformat.](address-ovr.md)

Einige Sitzungen erfordern möglicherweise spezielle Setupparameter, wenn sie vom Dienstanbieter unterstützt werden. Beispielsweise kann ein ISDN-TSP Benutzer-Benutzerinformationen übertragen, und einige MSPs erfordern Informationen zur Richtung des Medienstreams. Eine Überprüfung [der Daten,](session-information-ovr.md) die für eine Sitzung festgelegt oder erhalten werden können, finden Sie unter Sitzungsinformationen.

Nachdem eine Sitzung initiiert wurde, informiert TAPI die Anwendung über den Aufruffortschritt mithilfe des während der Initialisierung eingerichteten Ereignisbenachrichtigungsmechanismus.

**TAPI 2.x:** Anwendungen initiieren eine Sitzung mithilfe der [**lineMakeCall-Funktion.**](/windows/win32/api/tapi/nf-tapi-linemakecall) Die [**lineTranslateAddress-Funktion**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) wird bei Bedarf zum Durchführen der Adressübersetzung verwendet.

Aufrufeinrichtungsparameter können in der [**LINECALLPARAMS-Datenstruktur**](/windows/win32/api/tapi/ns-tapi-linecallparams) gespeichert werden, und ein Zeiger auf diese Struktur wird dann als Parameter von [**lineMakeCall verwendet.**](/windows/win32/api/tapi/nf-tapi-linemakecall) Wenn **lineMakeCall** keine **LINECALLPARAMS-Struktur** bereitgestellt wird, wird ein STANDARD-VOICE-Anruf mit einem Satz von Standardwerten angefordert.

Wenn die Sitzung erfolgreich eingerichtet wurde,  wird ein Aufrufhand handle mit Besitzerberechtigungen an die Anwendung zurückgegeben, und TAPI sendet die LINE [**\_ CALLSTATE-Nachrichten**](./line-callstate.md) der Anwendung mit Informationen zum Status des [Aufrufs.](privilege-ovr.md) Anwendungen verwenden diese Meldungen in der Regel, um dem Benutzer Statusberichte anzuzeigen.

**TAPI 3.x:** Anwendungen initiieren eine Kommunikationssitzung, indem sie die [**ITAddress::CreateCall-Methode**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) für eine Adresse aufrufen, die den erforderlichen Adresstyp und Medientyp behandeln kann. Wenn die Adresse die [**ITTerminalSupport-Schnittstelle**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) verfügbar macht, werden Terminals in den Medienstreams des Aufrufobjekts ausgewählt. Eine [Veranschaulichung dieses Prozesses](make-a-call.md) finden Sie im Beispiel zum Ausführen eines Aufrufcodes.

Aufrufeinrichtungsparameter können mithilfe von Methoden gespeichert oder geändert werden, die von der [**ITCallInfo-Schnittstelle verfügbar gemacht**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) werden.

Wenn die Sitzung erfolgreich eingerichtet wurde, gibt TAPI einen [**ITBasicCallControl-Schnittstellenzeiger**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) zurück, der für weitere Sitzungsvorgänge oder zum Abrufen eines [**ITCallInfo-Schnittstellenzeigers**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) verwendet werden kann, der zum Abrufen zusätzlicher Sitzungsinformationen verwendet werden kann. Die [**ITCallStateEvent-Schnittstelle**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) verarbeitet TAPI-Aufrufzustandsereignisse.

> [!Note]  
> TAPI sollte nicht für Faxübertragungen verwendet werden. Verwenden Sie stattdessen die Funktionen, die über MAPI verfügbar sind, die Microsoft-Nachrichten API.

 

## <a name="address-translation"></a>Adressübersetzung

Eine Endbenutzer- oder Serveranwendung kann Adressen in einem Format speichern, das nicht mit den Anforderungen eines bestimmten Dienstanbieters kompatibel ist. Beispielsweise kann eine Telefonnummer in einem elektronischen Adressbuch im kanonischen Format gespeichert [werden,](address-ovr.md)aber die meisten Dienstanbieter, die Telefonnummern verarbeiten, benötigen das [Wählformat](address-ovr.md).

TAPI stellt Adressübersetzungsvorgänge zur Verfügung, die eine Anwendung bei der Präsentation des richtigen Adresstyps für einen TSP unterstützen. Der Dienstanbieter gibt TAPI an, welche Adresstypen unterstützt werden, und muss keine Form der Adressübersetzung enthalten.

**TAPI 2.x:** Siehe [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress).

**TAPI 3:** Siehe [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo).

## <a name="toll-lists"></a>Mautlisten

An einigen Orten in Nordamerika sind alle Telefonanrufe in der Ortsvorwahl Ortsanrufe. An anderen Orten sind einige Aufrufe der Ortsvorwahl weit entfernt und benötigen das Präfix "1", um gewählt werden zu können. Die ersten drei Ziffern der Adresse (das Präfix) bestimmen, ob ein Aufruf in der Ortsvorwahl ein Mautaufruf ist.

Eine *Mautliste* ist eine Liste von Präfixen in der Ortsvorwahl, deren Adressen als Fernadressen gewählt werden müssen und für die Gebühren für die Fernverbindung berechnet werden.

Mautlisten sind für Dienstanbieter oder Anwendungen, die nicht auf ein Telefonnetzwerk zugreifen, nicht relevant.

**TAPI 2.x:** Siehe [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) (LINETRANSLATERESULT \_ INTOLLLIST- und LINETRANSLATERESULT \_ NOTINTOLLLIST-Bits in der [**LINETRANSLATEOUTPUT-Struktur),**](/windows/win32/api/tapi/ns-tapi-linetranslateoutput) [**lineSetTollList**](/windows/win32/api/tapi/nf-tapi-linesettolllist).

**TAPI 3:** Weitere Informationen finden Sie unter [**ITAddressTranslation::TranslateAddress**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress), [**ITAddressTranslationInfo::get \_ TranslationResults**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults).

 

 
