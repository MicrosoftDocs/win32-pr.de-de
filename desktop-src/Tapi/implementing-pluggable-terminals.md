---
description: Die allgemeinen Anforderungen für die Implementierung von pluggable-Terminals sind unten aufgeführt.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implementieren von pluggable-Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75dd7b085377c8474c9a89d74a297c3ca66c6740c01c7428e7b6f250e16c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762902"
---
# <a name="implementing-pluggable-terminals"></a>Implementieren von pluggable-Terminals

Die allgemeinen Anforderungen für die Implementierung von pluggable-Terminalen sind:

-   Der zugrunde liegende Streamingcode eines pluggable-Terminals sollte mit den Funktionen der gewünschten MSPs übereinstimmen.
-   Das Terminal muss DirectShow-Filter verwenden, um mit den meisten MSPs zu arbeiten (dies wird von hier aus vorausgesetzt).
-   Audioterminals müssen für die meisten MSPs ein 16-Bit-Mono-PCM mit 8 kHz unterstützen.
-   Das Terminal sollte free threaded marshalling durch Implementierung von [**IMarshal aktivieren.**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) Das Terminal kann dies durch Aufrufen der COM-API [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) und Aggregieren von **IMarshal** zum zurückgegebenen Zeiger tun. Der Destruktor des Terminalobjekts sollte [**IMarshal->Release aufrufen.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
-   Das Terminal sollte alle zusätzlichen terminalspezifischen Schnittstellen implementieren oder aggregieren, die geeignet sind.
-   Die Terminalimplementierung muss threadsicher sein.
-   Die Terminalimplementierung \# muss Termmgr.h für die Definition von [**ITTerminalControl enthalten.**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) Dies gilt zusätzlich zu den üblichen Includes und Bibliotheken, die für TAPI 3- oder TAPI 3-Anwendungen unter Windows 2000 SP1 erforderlich sind.

Hinweise zur Implementierung von Schnittstellen und Methoden:

Das Terminal muss [**itTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) implementieren (duale Schnittstelle – vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)).

[**ITTerminal::get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

Das Terminal muss eine **BSTR-Darstellung** einer von Ihnen gewählten GUID zurückgeben, die Ihren Terminaltyp identifiziert. Ordnen Sie **den BSTR** über [**SysAllocString zu.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) Rufen Sie zum Konvertieren von GUID in **BSTR** [**StringFromCLSID,**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) **SysAllocString** und [**CoTaskMemFree auf.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

[**ITTerminal::get \_ TerminalType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

Das Terminal sollte im Allgemeinen TT \_ DYNAMIC zurückgeben, wenn eine Anwendung das Terminal implementiert. Die Rückgabe von TT STATIC funktioniert ebenfalls, und die Rückgabe dieses Werts kann geeignet sein, wenn das Terminal einem Hardwaregerät entspricht. Dies kann jedoch für Benutzer verwirrend sein, da in der statischen Terminalenumeration des MSP kein statisches Terminal vorhanden \_ ist.

[**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Wenn die Terminalimplementierung die Anzahl der Streams, mit denen das Terminal gleichzeitig verbunden werden kann, nicht willkürlich einschränkt, sollte das Terminal immer TS \_ NOTINUSE zurückgeben.

Andernfalls schränkt die Terminalimplementierung die Anzahl der Streams, mit denen das Terminal gleichzeitig verbunden werden kann, willkürlich ein. In diesem Fall sollte das Terminal die Anzahl der Streams, mit der es verbunden ist, behalten. Das Terminal sollte diese interne Anzahl bei einem erfolgreichen [**ITTerminalControl::ConnectTerminal-Aufruf**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) erhöhen und bei einem erfolgreichen [**ITTerminalControl::D isconnectTerminal-Aufruf**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) dekrementiert werden. In [**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)sollte TS INUSE zurückgeben werden, wenn diese Anzahl der maximalen Anzahl von Streams entspricht, für die das Terminal gleichzeitig ausgewählt werden kann. Andernfalls sollte \_ TS \_ NOTINUSE zurückgeben werden. Beachten Sie, dass die Anzahl bei einem Grenzwert einfach ein boolescher Wert oder ein TERMINAL \_ STATE-Wert sein kann.

[**ITTerminal::get \_ Name**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

Das Terminal sollte einen **BSTR-Namen** seiner Wahl zurückgeben, der über [**SysAllocString zugeordnet wird.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) Dieser Name sollte für den Benutzer aussagekräftig sein und lokalisiert werden.

[**ITTerminal::get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

Das Terminal sollte seinen Medientyp zurückgeben, entweder TAPIMEDIATYPE \_ AUDIO oder TAPIMEDIATYPE \_ VIDEO.

[**ITTerminal::get \_ Direction**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

Das Terminal gibt den Terminal \_ DIRECTION-enum-Wert zurück, der die Richtung des Terminals angibt. Wenn das Terminal bidirektional ist (z. B. eine Brücke), muss es TD \_ BIDIRECTIONAL zurückgeben.

Das Terminal muss [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) (nur vtable) implementieren.

[**ITTerminalControl::get \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Ein von der Anwendung bereitgestelltes Terminal sollte immer **NULL** als Adresshand handle zurückgeben. Dies weist den MSP darauf hin, dass dieses Terminal nicht für ein bestimmtes MSP-Adressobjekt erstellt wurde.

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

Bei diesem Aufruf fügt das Terminal dem angegebenen Diagramm seine Filter hinzu und verbindet sie ggf. miteinander. Anschließend sollte das Terminal die Pins zurückgeben, die vom Terminal für die angegebene Streamrichtung verfügbar gemacht werden.

Ein Terminal, das keine gleichzeitige Verbindung mit mehreren Streams unterstützt, würde bei erfolgreichem Abschluss dieser Methode eine interne Variable auf TS \_ INUSE festlegen.

Das Terminal kann den *dwTerminalDirection-Parameter* aus diesem Aufruf verwenden, um die Richtung des Streams zu bestimmen, mit dem eine Verbindung besteht. Dies ist für bidirektionale Terminals erforderlich.

> [!Note]  
> In der Regel (in den MSP-Basisklassen und in allen bekannten MSPs) tritt beim MSP-Streamcode ein Fehler bei der Verbindung auf, wenn das Terminal mehr als einen Pin aus einem einzelnen [**ConnectTerminal-Aufruf**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) zurückgibt. Dies ist in Ordnung, da für ein Terminal, das während der Verbindung mehr als einen Pin zurückgibt, der MSP besondere Kenntnisse über das Terminal benötigt, um die zusätzlichen Pins effektiv nutzen zu können.

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

Das Terminal sollte nur S \_ OK zurückgeben. Das Terminal kann bei Bedarf auch eine Initialisierung nach der Verbindung verwenden.

[**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

Das Terminal sollte alles tun, was erforderlich ist, um das Terminal vom Rest des Graphen zu trennen. In der Regel umfasst dies das Entfernen aller Filter der Terminals aus dem Diagramm und das Festlegen des Terminalzustands auf TS \_ NOTINUSE.

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

Das Terminal sollte nur E \_ NOTIMPL zurückgeben.

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

Das Terminal sollte nur E \_ NOTIMPL zurückgeben.

 

 
