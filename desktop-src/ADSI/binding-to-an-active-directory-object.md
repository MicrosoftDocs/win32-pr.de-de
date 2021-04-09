---
title: Binden an ein Active Directory Objekt
description: Die gängigste Methode, eine Bindung an ein Active Directory Objekt herzustellen, besteht darin, die GetObject-Funktion zwischen einem ADSI-Client und einem ADSI-Anbieter zu verwenden.
ms.assetid: d278ea26-2fd5-4343-8d87-ff85515325fb
ms.tgt_platform: multiple
keywords:
- Binden an ein Active Directory Objekt ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59992dbc88c00be6306dec24523ec4e030d4a516
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858467"
---
# <a name="binding-to-an-active-directory-object"></a>Binden an ein Active Directory Objekt

Die gängigste Methode, eine Bindung an ein Active Directory Objekt herzustellen, besteht darin, die **GetObject** -Funktion zwischen einem ADSI-Client und einem ADSI-Anbieter zu verwenden. Dies ist auch die einfachste Möglichkeit, um anzuzeigen, wie die Anbieter Komponente Anforderungen empfängt und verarbeitet. Sowohl die ADSI-API-Funktion [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) als auch die Visual Basic-Funktion " **GetObject** " führen die gleichen Schritte für die Bindung aus.

Nehmen Sie für dieses Beispiel an, dass der ADSI-Client eine ADSI Viewer-Anwendung ist, die den ADsPath "Sample://Seattle/Redmond/Shelly" von der zugehörigen Benutzeroberfläche erhalten hat (1). In der folgenden Abbildung wird die Abfolge der Ereignisse durch Nummerieren der Fluss Pfeile ausführlich erläutert.

![Ausführliche Ansicht der ADSI-Komponenten](images/dscsex.png)

In der obigen Abbildung initiiert der Client die Anforderung eines Schnittstellen Zeigers auf dem Active Directory Objekt, das durch den ADsPath "Sample://Seattle/Redmond/Shelly" aus ADSI Services (2) dargestellt wird. Während der Initialisierung hat die Dienst Software eine Tabelle installierter Anbieter Programm-IDs (ProgIDs) aus der Registrierung ("LDAP:", "Sample:", "Winnt:" usw.) aufgefüllt und mit den passenden **CLSID**-Werten gekoppelt, die das entsprechende Softwaremodul identifizieren.

Der ADSI-Server überprüft, ob die ProgID, in diesem Fall "Sample:", im ADsPath vorhanden ist. Anschließend wird ein Bindungs Kontext erstellt, um weitere Verweise auf dieses Objekt zu optimieren, und die Standard-com-Funktion " [**mkparamesedisplayname**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) " wird aufgerufen, um einen com-Moniker zu erstellen, der verwendet werden kann, um das Objekt zu suchen und zu binden, das den Benutzer "Shelly" darstellt.

Im folgenden Abschnitt sind die Dateinamen des Beispiel Quellcodes der Anbieter Komponente ggf. in Klammern eingeschlossen.

Wie bei anderen com-Server Implementierungen prüft " [**mkparser-Display Name**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) " die ProgID und sucht die richtige **CLSID** in der Registrierung (3), um den entsprechenden vom Anbieter bereitgestellten klassenfactorycode (cprovcf. cpp) in der entsprechenden Anbieter Implementierung (4) zu finden. Dieser Code erstellt ein ursprüngliches Objekt der obersten Ebene, das die [**icsedisplayname::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) -Methode (cprov. cpp) implementiert. Die Implementierung von " **Parser Name** " des Anbieters löst den Pfad im eigenen Namespace des Anbieters auf. Dadurch wird AdsObject schließlich aufgerufen und der mit der Anbieter Komponente (Parse. cpp) bereitgestellte Parser aufgerufen, um zu überprüfen, ob der ADsPath für diesen Namespace syntaktisch richtig ist.

**GetObject**, das in getobj. cpp definiert ist, bestimmt dann, ob das angeforderte Objekt ein Namespace Objekt, ein Schema Objekt oder ein anderer Objekttyp ist. Wenn einer der ersten beiden ist, wird dieser Typ von Schema Klassenobjekt erstellt und der entsprechende Schnittstellen Zeiger abgerufen. Andernfalls wird der Beispiel Verzeichnispfad aus dem ADsPath erstellt (z. b. " \\ Seattle \\ Redmond \\ Shelly", aber in einem anderen Verzeichnisdienst muss Sie " \\ OU = Seattle \\ OU = Redmond \\ CN = Shelly" lauten, und die Steuerung wird an sampledsopenobject weitergeleitet, das das Objekt im Beispiel Datenspeicher öffnet und seinen Objekttyp (in diesem Fall "Benutzer") abruft.

Nachdem die Daten gesammelt wurden, wird ein neues-Objekt erstellt (6), um das durch den ADsPath beschriebene Element darzustellen, und ein Zeiger auf die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für dieses Objekt wird abgerufen. In diesem Fall wird ein generisches Active Directory Objekt erstellt, das die **IUnknown** -und [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Methode (cgenobj. cpp, Core. cpp) unterstützt. Die csampledsgenobject:: zuordnungsegenobject-Routine liest die Typbibliotheks Daten, um die richtigen dispatcheinträge für diese neuen Objekte zu erstellen, um [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)zu unterstützen.

Wenn Sie diesen Schnittstellen Zeiger in einen Moniker einschließen, wird die resolvepathname (cprov. cpp)-Funktion abgeschlossen und der Anzeige Name analysiert.

Alle COM-Objekte, die während dieses Prozesses erstellt werden, werden aus Leistungsgründen zwischengespeichert und über den Bindungs Kontext verwaltet. Dies verbessert die Leistung für andere Vorgänge auf demselben Objekt, das direkt auf die Monikerbindung folgt.

Dieses wohlgeformte Active Directory Objekt wird nun für den für den anfänglichen [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) -Befehl angeforderten Schnittstellen Bezeichner abgefragt, und ein Zeiger auf diese Schnittstelle wird abgerufen (7) und über den ADSI-Server an den Client zurückgegeben (8&9). Von diesem Zeitpunkt an arbeitet der Client direkt mit der Anbieter Komponente über die Schnittstellen Methoden, bis die anfängliche Anforderung erfüllt ist (10).

Außerdem verwenden Anforderungen für Objektdaten vom Client normalerweise die Form von Anforderungen für das Abrufen und Einfügen von Eigenschaften, die alle durch die Anbieter Implementierung eines Eigenschafts Caches (Crequi. cpp) optimiert werden. Intelligent packen und entpacken von Daten (häufig einschließlich kopieren und Freigeben von Strukturen und Zeichen folgen) zwischen den nativen Datentypen im Betriebssystem der Beispiel Anbieter Komponente [](/windows/win32/api/oaidl/ns-oaidl-variant) und dem von ADSI unterstützten Automatisierungstyp für die Automatisierung findet statt, bevor die Eigenschaften in den Cache (smpoper. cpp) geladen werden.

Die Beispiel Anbieter Komponente ist so konzipiert, dass die tatsächlichen Aufrufe an das Betriebssystem logisch von der Anbieter Komponente isoliert sind. Dadurch wird Software erstellt, die für mehr als ein Betriebssystem (regdsapi. cpp) portabel ist.

 

 