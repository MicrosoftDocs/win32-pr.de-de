---
title: Die Schnittstellenproxydatei
description: Die Schnittstellenproxydatei (U \_ p.c) ist eine C-Datei, die Routinen enthält, die denen in den Clientstub- und Serverstubdateien einer Objektschnittstelle (COM) entsprechen.
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL und COM MIDL, Schnittstellen, Proxydateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedb9de50d00524b1e038f027448be5aaab369aa5d92243d2a3425bf603cd65a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013538"
---
# <a name="the-interface-proxy-file"></a>Die Schnittstellenproxydatei

Die Schnittstellenproxydatei (U \_ p.c) ist eine C-Datei, die Routinen enthält, die denen in den Clientstub- und Serverstubdateien einer Objektschnittstelle (COM) entsprechen. Diese Datei enthält Implementierungen der Ersatzroutinen für Client und Server im Inlinemodus des Compilers oder entsprechende Daten und Thunks in den interpretierten Modi sowie andere geeignete COM-Glue-Daten, z. B. proxy- und stub-Vtables.

Die Schnittstellenproxydatei enthält die unterstützenden Routinen und Daten nur für Methoden der Schnittstellen, die in der aktuellen IDL-Datei definiert sind. Um dieses Verhalten zu verdeutlichen, wird in diesem Abschnitt ein erweitertes Beispiel verwendet. Beim Kompilieren einer IDL-Datei mit einer Schnittstelle wie IFaceB, die von IFaceA erbt, werden IFaceB-bezogene Hilfsdaten und Routinen in der aktuellen Proxydatei generiert, während die IFaceA-bezogenen Hilfsdaten und Routinen der Basisschnittstelle im Proxy gefunden werden, der aus der IDL-Datei generiert wurde, die die IFaceA-Definition enthält. Der Compiler generiert alle Daten, die erforderlich sind, um die Ersatzzeichen der Basisschnittstelle zu identifizieren und bei Bedarf an sie zu delegieren, um die IFaceA-Methoden zu unterstützen, die über die IFaceB-Schnittstelle verwendet werden.

Für jede Methode in einer Schnittstelle in der aktuellen IDL-Datei enthält die Proxydatei die folgenden beiden Ersatzmethoden, wenn sie im gemischten Modus kompiliert wird ([/Os](-os.md)) und entsprechende Interpreterdaten, wenn sie im Interpretermodus kompiliert werden ([/Oi](-oi.md)).

-   Das clientseitige Ersatzzeichen, z. B. \_ der IFaceB-Methodenproxy \_ in diesem Beispiel.

    Dieses clientseitige Ersatzzeichen ist der virtuelle Einstiegspunkt, an den der Client , z. B. IFaceB::Method, gesendet wird. Sie marshallt die Eingabeargumente in eine übertragbare Form, überträgt die gemarshallten Argumente zusammen mit Informationen, die die Schnittstelle und den Vorgang identifizieren, und entpackt dann den Rückgabewert und alle Ausgabeargumente, wenn der aufgerufene Vorgang zurückgegeben wird.

-   Das serverseitige Ersatzzeichen, z. B. \_ \_ IFaceB-Methodenstub.

    Dieses serverseitige Ersatzzeichen ist der virtuelle Einstiegspunkt, an den die zugrunde liegende Runtime auf dem Server verteilt, um den Client zu emulieren. Es entmarshaliert die Eingabeargumente, um die Clientdaten zu replizieren, ruft die Implementierung der Schnittstellenfunktion des Servers auf und marshallt dann den Rückgabewert und alle Ausgabeargumente zurück an den Client.

Der Standardname für eine Proxydatei, die aus einer datei.idl generiert wird, ist die Datei \_ p.c. Verwenden Sie den [**/proxy**](-proxy.md) MIDL-Compilerschalter, um den Standardnamen der Schnittstellenproxydatei zu überschreiben. Die Schalter [**/env**](-env.md) und [**/out**](-out.md) wirken sich auf diese Datei aus.

 

 




