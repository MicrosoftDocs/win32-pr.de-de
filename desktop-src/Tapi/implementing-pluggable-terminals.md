---
description: Die allgemeinen Anforderungen für die austauschbare Terminal Implementierung sind unten aufgeführt.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implementieren austauschbarer Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 494b2f6bc5ccb214bc7101f570a4db3037fd8cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349463"
---
# <a name="implementing-pluggable-terminals"></a>Implementieren austauschbarer Terminals

Die allgemeinen Anforderungen für die austauschbare Terminal Implementierung lauten:

-   Der dem austauschbaren Terminal zugrunde liegende streamingcode sollte den Funktionen der gewünschten MSPs entsprechen.
-   Das Terminal muss DirectShow-Filter verwenden, um mit den meisten MSPs zu arbeiten (hier wird davon ausgegangen).
-   Audioterminals müssen für die meisten MSPs 8 kHz 16-Bit-Mono-PCM unterstützen.
-   Das Terminal sollte das Marshalling von freien Threads durch Implementieren von [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)ermöglichen. Das Terminal kann dies durch Aufrufen der com-API [**cocreatefreethreadedmarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) erreichen, indem Sie **IMarshal** auf den zurückgegebenen Zeiger aggregierte. Der Dekonstruktor des Terminal Objekts sollte " [**IMarshal->Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)" aufrufen.
-   Das Terminal sollte alle zusätzlichen Terminal spezifischen Schnittstellen implementieren oder Aggregieren, die geeignet sind.
-   Die Terminal Implementierung muss Thread sicher sein.
-   Die Terminal Implementierung muss \# termmgr. h für die Definition von [**itterminalcontrol**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol)enthalten. Dies gilt zusätzlich zu den üblichen includes-und-Bibliotheken, die für TAPI 3-oder TAPI 3-Anwendungen unter Windows 2000 SP1 benötigt werden.

Hinweise zur Implementierung der Schnittstelle und Methode:

Das Terminal muss [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) (Dual Interface – Vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)) implementieren.

[**Itterminal:: get \_ terminalclass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

Das Terminal muss eine **BSTR** -Darstellung einer GUID zurückgeben, die Sie ausgewählt haben, die ihren Terminaltyp identifiziert. Weisen Sie den **BSTR** über " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)" zu. Um von GUID in **BSTR** zu konvertieren, nennen Sie [**stringfromclsid**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid), **SysAllocString** und [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

[**Itterminal:: get \_ terminaltype**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

Das Terminal sollte in der Regel TT Dynamic zurückgeben, \_ Wenn eine Anwendung das Terminal implementiert. Die Rückgabe von "TT \_ static" funktioniert auch, und das zurückgeben dieses Werts kann sinnvoll sein, wenn das Terminal einem Hardware Gerät entspricht. Dies kann jedoch für Benutzer verwirrend sein, da ein statisches Terminal nicht in der statischen terminalenumeration von MSP vorhanden ist.

[**Itterminal:: get- \_ Status**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Wenn die Terminal Implementierung die Anzahl der Streams, mit denen das Terminal gleichzeitig verbunden sein kann, nicht willkürlich einschränkt, sollte das Terminal immer TS \_ notinuse zurückgeben.

Andernfalls schränkt die Terminal Implementierung willkürlich die Anzahl der Streams ein, mit denen das Terminal gleichzeitig verbunden werden kann. In diesem Fall sollte das Terminal die Anzahl der Datenströme, mit denen er verbunden ist, beibehalten. Das Terminal sollte diese interne Anzahl bei einem erfolgreichen [**itterminalcontrol:: connectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) -Befehl erhöhen und auf einem erfolgreichen [**itterminalcontrol::D isconnectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) -Befehl Dekrement verringern. Im [**itterminal:: get- \_ Zustand**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)sollte "TS InUse" zurückgegeben werden, \_ Wenn diese Anzahl gleich der maximalen Anzahl von Streams ist, für die das Terminal gleichzeitig ausgewählt werden kann. andernfalls sollte "TS \_ notinuse" zurückgegeben werden. Beachten Sie, dass die Anzahl einfach ein boolescher Wert oder ein Terminal Zustandswert sein kann, wenn der Grenzwert 1 ist \_ .

[**Itterminal:: get- \_ Name**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

Das Terminal sollte einen **BSTR** -Namen seiner Wahl zurückgeben, der über " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)" zugeordnet ist. Dieser Name sollte für den Benutzer aussagekräftig sein und lokalisiert werden.

[**Itterminal:: get- \_ mediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

Das Terminal sollte seinen Medientyp zurückgeben, entweder tapimediatype \_ Audiodatei oder tapimediatype \_ Video.

[**Itterminal:: get- \_ Richtung**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

Das Terminal gibt den \_ terminalumenumenumerationswert zurück, der die Richtung des Terminals angibt. Wenn das Terminal bidirektional ist (z. b. eine Bridge), muss es den TD- \_ bidirektionalen Wert zurückgeben.

Das Terminal muss [**itterminalcontrol**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (nur Vtable) implementieren.

[**Itterminalcontrol:: get \_ adresssshandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Ein von der Anwendung bereitgestelltes Terminal sollte immer **null** als Adress Handle zurückgeben. Dies gibt dem MSP an, dass dieses Terminal nicht für ein bestimmtes MSP-Adress Objekt erstellt wurde.

[**Itterminalcontrol:: connectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

Bei diesem Aufruf fügt das Terminal seine Filter dem angegebenen Diagramm hinzu und verbindet Sie ggf. miteinander. Das Terminal sollte dann die vom Terminal verfügbar gemachten PIN (s) für die angegebene Datenstrom Richtung zurückgeben.

Ein Terminal, das keine gleichzeitige Verbindung mit mehreren Streams unterstützt, würde \_ beim erfolgreichen Abschluss dieser Methode eine interne Variable auf Terminaldiensteverwendung festlegen.

Das Terminal kann den *dwterminaldirection* -Parameter dieses Aufrufes verwenden, um die Richtung des Streams zu bestimmen, mit dem eine Verbindung hergestellt wird. Dies ist für bidirektionale Terminals erforderlich.

> [!Note]  
> In der Regel (in den MSP-Basisklassen und in allen bekannten MSPs) schlägt der MSP-streamcode die Verbindung fehl, wenn das Terminal mehr als eine PIN von einem einzigen [**connectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) -Befehl zurückgibt. Das ist in Ordnung, da ein Terminal, das mehr als eine PIN während der Verbindung zurückgibt, erfordert, dass der MSP besondere Kenntnisse des Terminals hat, um die zusätzlichen Pins effektiv nutzen zu können.

 

[**Itterminalcontrol:: completeconnectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

Das Terminal sollte nur S OK zurückgeben \_ . Das Terminal kann auch nach der Verbindungs Initialisierung durchführen, wenn dies erforderlich ist.

[**Itterminalcontrol::D isconnectterminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

Das Terminal sollte alle erforderlichen Aktionen ausführen, um die Verbindung mit dem Terminal vom Rest des Diagramms getrennt zu werden. In der Regel umfasst dies das Entfernen aller Terminals-Filter aus dem Diagramm und das Festlegen des Terminal Zustands auf \_ terminaldienstedienste.

[**Itterminalcontrol:: runrenderfilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

Das Terminal sollte nur E \_ notimpl zurückgeben.

[**Itterminalcontrol:: stoprenderfilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

Das Terminal sollte nur E \_ notimpl zurückgeben.

 

 
