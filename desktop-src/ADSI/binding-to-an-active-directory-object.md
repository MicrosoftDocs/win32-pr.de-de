---
title: Binden an ein Active Directory-Objekt
description: Die gängigste Methode zum Binden an ein Active Directory-Objekt ist die Verwendung der GetObject-Funktion zwischen einem ADSI-Client und einem ADSI-Anbieter.
ms.assetid: d278ea26-2fd5-4343-8d87-ff85515325fb
ms.tgt_platform: multiple
keywords:
- Binden an ein Active Directory-Objekt ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc788ed9eb124e1da6c21848f02393d46608f00dd3a9e779788fa54429922400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429133"
---
# <a name="binding-to-an-active-directory-object"></a>Binden an ein Active Directory-Objekt

Die gängigste Methode zum Binden an ein Active Directory-Objekt ist die Verwendung der **GetObject-Funktion** zwischen einem ADSI-Client und einem ADSI-Anbieter. Dies ist auch die einfachste Möglichkeit, um zu zeigen, wie die Anbieterkomponente Anforderungen und Dienste empfängt. Sowohl die ADSI-API-Funktion [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) als auch die Visual Basic Funktion **GetObject** führen die gleichen Schritte für die Bindung aus.

In diesem Beispiel wird davon ausgegangen, dass der ADSI-Client eine ADSI-Viewer-Anwendung ist, die den ADsPath -Sample://Seattle/Redmond/Shelly von seiner Benutzeroberfläche (1) empfangen hat. In der folgenden Abbildung wird die Reihenfolge der Ereignisse durch Nummerieren der Flusspfeile detailliert dargestellt.

![Detaillierte Ansicht der Adsi-Komponenten](images/dscsex.png)

In der obigen Abbildung initiiert der Client die Anforderung eines Schnittstellenzeigers für das Active Directory-Objekt, das durch den ADsPath -Sample://Seattle/Redmond/Shelly von ADSI-Diensten dargestellt wird (2). Während der Initialisierung hat die Dienstsoftware eine Tabelle der installierten programmgesteuerten Anbieterbezeichner (ProgIDs) aus der Registrierung aufgefüllt ("LDAP:", "Sample:", "WinNT:" usw.) und sie mit den entsprechenden **CLSID** s gekoppelt, die das entsprechende Softwaremodul identifizieren.

Der ADSI-Server überprüft, ob die ProgID (in diesem Fall "Sample:" ) im ADsPath vorhanden ist. Anschließend wird ein Bindungskontext erstellt, um weitere Verweise auf dieses Objekt zu optimieren, und die COM-Standardfunktion [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) wird zum Erstellen eines COM-Monikers verwendet, der zum Suchen und Binden an das Objekt verwendet werden kann, das den Benutzer "Shelly" darstellt.

Im folgenden Abschnitt sind die Dateinamen des Quellcodes der Beispielanbieterkomponente ggf. in Klammern enthalten.

Wie bei anderen COM-Serverimplementierungen untersucht [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) die ProgID und sucht die richtige **CLSID** in der Registrierung (3), um den entsprechenden vom Anbieter bereitgestellten Klassenfactorycode (Cprovcf.cpp) in der entsprechenden Anbieterimplementierungen (4) zu finden. Dieser Code erstellt ein anfängliches Objekt der obersten Ebene, das die [**IParseDisplayName::P arseDisplayName-Methode**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) (Cprov.cpp) implementiert. Die Implementierung des Anbieters **von ParseDisplayName** löst den Pfad im eigenen Namespace des Anbieters auf. Dadurch wird schließlich ADsObject aufgerufen und der mit der Anbieterkomponente (Parse.cpp) bereitgestellte Parser aufgerufen, um zu überprüfen, ob der ADsPath für diesen Namespace syntaktisch korrekt ist.

**GetObject**, das in Getobj.cpp definiert ist, bestimmt dann, ob das angeforderte Objekt ein Namespaceobjekt, ein Schemaobjekt oder ein anderer Objekttyp ist. Wenn einer der ersten beiden objekte erstellt wird, wird dieser Typ des Schemaklassenobjekts erstellt und der entsprechende Schnittstellenzeiger abgerufen. Andernfalls wird der Beispielverzeichnispfad aus dem ADsPath erstellt (z. B. \\ "Seattle \\ Redmond \\ Shelly", aber in einem anderen Verzeichnisdienst muss er möglicherweise \\ "OU=Seattle \\ OU=Redmond \\ CN=Shelly") lauten, und die Steuerung wird an SampleDSOpenObject übergeben, wodurch das Objekt im Beispieldatenspeicher geöffnet wird und auch dessen Objekttyp (in diesem Fall "User") (5) abgerufen wird.

Mit den gesammelten Daten wird ein neues -Objekt (6) erstellt, um das von ADsPath beschriebene Element darzustellen, und ein Zeiger auf die [**IUnknown-Schnittstelle**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für dieses Objekt wird abgerufen. In diesem Fall wird ein generisches Active Directory-Objekt erstellt, das die **IUnknown-** und [**IADs-Methoden**](/windows/desktop/api/Iads/nn-iads-iads) (Cgenobj.cpp, Core.cpp) unterstützt. Die CSampleDSGenObject::AllocateGenObject-Routine liest die Typbibliotheksdaten, um die richtigen Dispatcheinträge für diese neuen Objekte zu erstellen, um [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)zu unterstützen.

Das Umschließen dieses Schnittstellenzeigers in einen Moniker schließt die ResolvePathName (Cprov.cpp)-Funktion ab und analysiert den Anzeigenamen.

Alle COM-Objekte, die während dieses Prozesses erstellt wurden, werden aus Leistungsgründen zwischengespeichert und über den Bindungskontext verwaltet. Dies verbessert die Leistung für andere Vorgänge für dasselbe Objekt, das unmittelbar auf die Monikerbindung folgt.

Dieses wohlgeformte Active Directory-Objekt wird nun nach dem Schnittstellenbezeichner abgefragt, der für den ersten [**ADsGetObject-Aufruf**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) angefordert wurde, und ein Zeiger auf diese Schnittstelle wird abgerufen (7) und über den ADSI-Server an den Client übergeben (8&9). Von da an arbeitet der Client direkt mit der Anbieterkomponente über die Schnittstellenmethoden, bis die erste Anforderung erfüllt ist (10).

Darüber hinaus haben Anforderungen für Objektdaten vom Client in der Regel die Form von Anforderungen für Das-Eigenschaft-Abruf- und -Puts-Objekt, die alle durch die Anbieterimplementierungen eines Eigenschaftencaches (Cprops.cpp) optimiert werden. Das intelligente Packen und Entpacken von Daten, z. B. das Kopieren und Freigeben von Strukturen und Zeichenfolgen, zwischen den nativen Datentypen im Betriebssystem der Beispielanbieterkomponente und dem von ADSI unterstützten Automation [**VARIANT-Typ**](/windows/win32/api/oaidl/ns-oaidl-variant) findet statt, bevor die Eigenschaften in den Cache geladen werden (Smpoper.cpp).

Die Beispielanbieterkomponente ist so konzipiert, dass die tatsächlichen Aufrufe des Betriebssystems logisch von der Anbieterkomponente isoliert werden, wodurch Software erstellt wird, die auf mehrere Betriebssysteme portierbar ist (RegDSAPI.cpp).

 

 