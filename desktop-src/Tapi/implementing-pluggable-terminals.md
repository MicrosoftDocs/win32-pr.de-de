---
description: Die allgemeinen Anforderungen für die Implementierung eines austauschbaren Terminals sind unten aufgeführt.
ms.assetid: 7cee19b1-ceea-494a-b576-4deede759905
title: Implementieren von austauschbaren Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75dd7b085377c8474c9a89d74a297c3ca66c6740c01c7428e7b6f250e16c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762902"
---
# <a name="implementing-pluggable-terminals"></a>Implementieren von austauschbaren Terminals

Die allgemeinen Anforderungen für die Implementierung eines austauschbaren Terminals sind:

-   Der zugrunde liegende Streamingcode eines austauschbaren Terminals sollte den Funktionen der gewünschten MSPs entsprechen.
-   Das Terminal muss DirectShow-Filter verwenden, um mit den meisten MSPs zu arbeiten (dies wird von hier aus angenommen).
-   Audioterminals müssen für die meisten MSPs ein lineares MONO-PCM mit 8 kHz und 16 Bit unterstützen.
-   Das Terminal sollte das freie Threading marshallen, indem [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)implementiert wird. Hierzu kann das Terminal die COM-API [**CoCreateFreeThreadedMarshaler**](/windows/win32/api/combaseapi/nf-combaseapi-cocreatefreethreadedmarshaler) aufrufen und **IMarshal** auf den zurückgegebenen Zeiger aggregieren. Der Destruktor des Terminalobjekts sollte [**IMarshal->Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)aufrufen.
-   Das Terminal sollte alle zusätzlichen terminalspezifischen Schnittstellen implementieren oder aggregieren, die geeignet sind.
-   Die Terminalimplementierungen müssen threadsicher sein.
-   Die Terminalimplementierung muss \# Termmgr.h für die Definition von [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol)enthalten. Dies ist zusätzlich zu den üblichen Includes und Bibliotheken, die für TAPI 3- oder TAPI 3-Anwendungen unter Windows 2000 SP1 erforderlich sind.

Hinweise zur Implementierung von Schnittstellen und Methoden:

Das Terminal muss [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) implementieren (duale Schnittstelle – vtable + [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)).

[**ITTerminal::get \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)

Das Terminal muss eine **BSTR-Darstellung** einer von Ihnen ausgewählten GUID zurückgeben, die Ihren Terminaltyp identifiziert. Ordnen Sie den **BSTR** über [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)zu. Um von GUID in **BSTR** zu konvertieren, rufen [**Sie StringFromCLSID,**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) **SysAllocString** und [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)auf.

[**ITTerminal::get \_ TerminalType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminaltype)

Das Terminal sollte in der Regel TT \_ DYNAMIC zurückgeben, wenn eine Anwendung das Terminal implementiert. Die Rückgabe von TT \_ STATIC funktioniert ebenfalls, und die Rückgabe dieses Werts kann sinnvoll sein, wenn das Terminal einem Hardwaregerät entspricht. Dies kann jedoch für Benutzer verwirrend sein, da ein statisches Terminal in der statischen Terminalenumeration des MSP nicht vorhanden ist.

[**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)

Wenn die Terminalimplementierungen die Anzahl der Streams, mit denen das Terminal gleichzeitig verbunden werden kann, nicht beliebig begrenzen, sollte das Terminal immer TS \_ NOTINUSE zurückgeben.

Andernfalls schränkt die Terminalimplementierungen beliebig die Anzahl der Streams ein, mit denen das Terminal gleichzeitig verbunden werden kann. In diesem Fall sollte das Terminal die Anzahl der Streams beibehalten, mit der es verbunden ist. Das Terminal sollte diese interne Anzahl bei einem erfolgreichen [**ITTerminalControl::ConnectTerminal-Aufruf**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) erhöhen und bei einem erfolgreichen [**ITTerminalControl::D isconnectTerminal-Aufruf**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal) dekrementieren. In [**ITTerminal::get \_ State**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_state)sollte TS INUSE zurückgegeben \_ werden, wenn diese Anzahl der maximalen Anzahl von Datenströmen entspricht, für die das Terminal gleichzeitig ausgewählt werden kann. Andernfalls sollte TS \_ NOTINUSE zurückgegeben werden. Beachten Sie Folgendes: Wenn der Grenzwert 1 ist, kann die Anzahl einfach ein boolescher Wert oder ein TERMINAL \_ STATE-Wert sein.

[**ITTerminal::get \_ Name**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_name)

Das Terminal sollte einen **BSTR-Namen** seiner Wahl zurückgeben, der über [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)zugeordnet wird. Dieser Name sollte für den Benutzer aussagekräftig sein und lokalisiert werden.

[**ITTerminal::get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype)

Das Terminal sollte seinen Medientyp zurückgeben, entweder TAPIMEDIATYPE \_ AUDIO oder TAPIMEDIATYPE \_ VIDEO.

[**ITTerminal::get \_ Direction**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_direction)

Das Terminal gibt den TERMINAL \_ DIRECTION-Enumerationswert zurück, der die Richtung des Terminals angibt. Wenn das Terminal bidirektional ist (z. B. eine Bridge), muss es TD \_ BIDIRECTIONAL zurückgeben.

Das Terminal muss [**ITTerminalControl**](/windows/desktop/api/Termmgr/nn-termmgr-itterminalcontrol) implementieren (nur vtable).

[**ITTerminalControl::get \_ AddressHandle**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-get_addresshandle)

Ein von der Anwendung bereitgestelltes Terminal sollte immer **NULL** als Adresshandle zurückgeben. Dies gibt dem MSP an, dass dieses Terminal nicht für ein bestimmtes MSP-Adressobjekt erstellt wurde.

[**ITTerminalControl::ConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal)

Bei diesem Aufruf fügt das Terminal seine Filter dem angegebenen Graphen hinzu und verbindet sie ggf. miteinander. Anschließend sollte das Terminal die pin(s) zurückgeben, die vom Terminal für die angegebene Streamrichtung verfügbar gemacht werden.

Ein Terminal, das keine gleichzeitige Verbindung mit mehreren Streams unterstützt, würde bei erfolgreichem Abschluss dieser Methode eine interne Variable auf TS \_ INUSE festlegen.

Das Terminal kann den *dwTerminalDirection-Parameter* aus diesem Aufruf verwenden, um die Richtung des Streams zu bestimmen, mit dem eine Verbindung hergestellt wird. Dies ist für bidirektionale Terminals erforderlich.

> [!Note]  
> In der Regel (in den MSP-Basisklassen und in allen bekannten MSPs) schlägt der MSP-Streamcode die Verbindung fehl, wenn das Terminal mehrere Pins von einem einzelnen [**ConnectTerminal-Aufruf**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-connectterminal) zurückgibt. Dies ist in Ordnung, da ein Terminal, das während der Verbindung mehrere Pins zurückgibt, über spezielle Kenntnisse des Terminals verfügen muss, um die zusätzlichen Pins effektiv nutzen zu können.

 

[**ITTerminalControl::CompleteConnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-completeconnectterminal)

Das Terminal sollte einfach S \_ OK zurückgeben. Das Terminal kann ggf. auch eine Initialisierung nach der Verbindung durchführen.

[**ITTerminalControl::D isconnectTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-disconnectterminal)

Das Terminal sollte alles tun, was erforderlich ist, um das Terminal vom Rest des Diagramms zu trennen. In der Regel umfasst dies das Entfernen aller Filter der Terminals aus dem Diagramm und das Festlegen des Endzustands auf TS \_ NOTINUSE.

[**ITTerminalControl::RunRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-runrenderfilter)

Das Terminal sollte einfach E \_ NOTIMPL zurückgeben.

[**ITTerminalControl::StopRenderFilter**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalcontrol-stoprenderfilter)

Das Terminal sollte einfach E \_ NOTIMPL zurückgeben.

 

 
