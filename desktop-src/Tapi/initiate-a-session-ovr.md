---
description: Die Hauptinformationen, die eine Anwendung zum Initiieren einer Kommunikationssitzung bereitstellt, sind der adrestyp, der Medientyp oder die Typen und die Zieladresse.
ms.assetid: 65e53587-0e40-411b-8d6c-d6adfc9d1e6c
title: Initiieren einer Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e925ba90460b88c85a9aab1624923acdbc4572a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863856"
---
# <a name="initiate-a-session"></a>Initiieren einer Sitzung

Die Hauptinformationen, die eine Anwendung zum Initiieren einer Kommunikationssitzung bereitstellt, sind der [adrestyp](address-type-ovr.md), der [Medientyp](media-type-ovr.md) oder die Typen und die Ziel [Adresse](address-ovr.md).

Die Zieladresse erfordert möglicherweise eine [Adressübersetzung](#address-translation) , um die von einem Benutzer eingegebenen Informationen in das richtige Format für einen bestimmten Adresstyp zu versetzen. Beispielsweise ist für eine Telefonnummer, die sich in einem elektronischen Adressbuch im [kanonischen](address-ovr.md) Format befunden hat, eine Übersetzung in ein [dialbares](address-ovr.md) Format erforderlich.

Einige Sitzungen erfordern möglicherweise spezielle Setup Parameter, wenn Sie vom Dienstanbieter unterstützt werden. Beispielsweise kann ein ISDN-TSP Benutzer Benutzerinformationen übertragen, und einige MSPs benötigen Informationen über die Richtung des Medien Stroms. Eine Überprüfung der Daten, die für eine Sitzung festgelegt oder abgerufen werden können, finden Sie unter [Sitzungsinformationen](session-information-ovr.md) .

Nachdem eine Sitzung initiiert wurde, wird die Anwendung über den Ereignis Benachrichtigungs Mechanismus, der während der Initialisierung eingerichtet wurde, von TAPI informiert.

**TAPI 2. x:** Anwendungen initiieren eine Sitzung mithilfe der [**linemakecall**](/windows/win32/api/tapi/nf-tapi-linemakecall) -Funktion. Bei Bedarf wird die [**linetranslateaddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) -Funktion verwendet, um die Adressübersetzung auszuführen.

Die Parameter zum Aufrufen von Setup können in der Datenstruktur [**linecallparameams**](/windows/win32/api/tapi/ns-tapi-linecallparams) gespeichert werden, und ein Zeiger auf diese Struktur wird dann als Parameter von [**linemakecall**](/windows/win32/api/tapi/nf-tapi-linemakecall)verwendet. Wenn **linemakecall** keine **linecallpara** -Struktur bereitgestellt wird, wird ein standardmäßiger Anruf in der sprachklasse mit einem Satz von Standardwerten angefordert.

Wenn die Sitzung erfolgreich eingerichtet wurde, wird ein Aufruf Handle mit *Besitzer* [rechten](privilege-ovr.md) an die Anwendung zurückgegeben, und TAPI sendet die Anwendungs [**Zeilen- \_ CallState**](./line-callstate.md) -Meldungen mit Informationen zum Fortschritt des Aufrufes. Anwendungen verwenden diese Nachrichten in der Regel, um dem Benutzer Statusberichte anzuzeigen.

**TAPI 3. x:** Anwendungen initiieren eine Kommunikationssitzung, indem Sie die [**itaddress:: anatecall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) -Methode für eine Adresse aufrufen, die den erforderlichen Adresstyp und Medientyp verarbeiten können. Wenn die Adresse die Schnittstelle [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) verfügbar macht, werden Terminals auf den Mediendaten Strömen des calljektes ausgewählt. Eine Veranschaulichung dieses Prozesses finden Sie im Beispiel " [make a callcode](make-a-call.md) ".

Setup Parameter aufrufen können mithilfe von Methoden, die von der [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) -Schnittstelle verfügbar gemacht werden, gespeichert oder geändert werden

Wenn die Sitzung erfolgreich eingerichtet wurde, gibt TAPI einen [**itbasiccallcontrol**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) -Schnittstellen Zeiger zurück, der für weitere Sitzungs Vorgänge verwendet werden kann, oder zum Abrufen eines [**itcallinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) -Schnittstellen Zeigers, der zum Abrufen zusätzlicher Sitzungsinformationen verwendet werden kann. Die [**itcallstateevent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) -Schnittstelle verarbeitet TAPI-Aufruf Zustands Ereignisse.

> [!Note]  
> TAPI sollte nicht für Faxübertragungen verwendet werden. Verwenden Sie stattdessen die Funktionen, die über MAPI verfügbar sind, die Microsoft Messaging-API.

 

## <a name="address-translation"></a>Adressübersetzung

Eine Endbenutzer-oder Serveranwendung kann Adressen in einem Format speichern, das nicht mit den Anforderungen eines bestimmten Dienstanbieters kompatibel ist. Eine Telefonnummer kann z. b. in einem elektronischen Adressbuch im [kanonischen Format](address-ovr.md)gespeichert werden, aber die meisten Dienstanbieter, die Telefonnummern verarbeiten, benötigen das [Format "dialable](address-ovr.md)".

TAPI stellt Adress Übersetzungs Vorgänge bereit, die einer Anwendung helfen, den richtigen Adresstyp für einen TSP anzugeben. Der Dienstanbieter gibt für TAPI an, welche Adresstypen unterstützt werden, und er muss keine Form der Adressübersetzung enthalten.

**TAPI 2. x:** Siehe [**linetranslateaddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress).

**TAPI 3:** Siehe [**itadresssstranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation), [**itadresstranslationinfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo).

## <a name="toll-lists"></a>Maut Listen

An manchen Stellen in Nordamerika sind alle Telefonanrufe, die im lokalen Code abgelegt werden, lokale Aufrufe. An anderen Standorten sind einige Aufrufe, die an den lokalen Code platziert werden, lange Distanz und benötigen ein Präfix "1", um gewählt zu werden. Die ersten drei Ziffern der Adresse (das Präfix) bestimmen, ob es sich bei einem-Befehl im lokalen Code um einen Maut Befehl handelt.

Eine *Maut Liste* ist eine Liste von Präfixen im lokalen Code, deren Adressen als Adressen mit langer Entfernung gewählt werden müssen und für die eine lange Entfernungs Gebühr geschätzt wird.

Maut Listen sind für Dienstanbieter oder Anwendungen, die nicht auf ein Telefon Netzwerk zugreifen, nicht relevant.

**TAPI 2. x:** Weitere Informationen finden Sie unter [**linetranslateaddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) (linetranslateresult \_ intolllist und linetranslateresult \_ notintolllist Bits in der [**linetranslateoutput**](/windows/win32/api/tapi/ns-tapi-linetranslateoutput) -Struktur), [**linesettolllist**](/windows/win32/api/tapi/nf-tapi-linesettolllist).

**TAPI 3:** Siehe [**itadresssstranslation:: TranslateAddress**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress), [**itadresssstranslationinfo:: get- \_ Übersetzungsergebnisse**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults).

 

 
