---
title: Windows-Remoteverwaltung Glossar
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106355742"
---
# <a name="windows-remote-management-glossary"></a>Windows-Remoteverwaltung Glossar


<dl> <dt>

WSMAN: Items * * * *
</dt> <dd>

Ein WS-Management Protocol-Element, das in einer Enumeration zurückgegeben wird, die sowohl die Instanzen als auch die [*EPRS*](/windows)-Instanz erhält. **WSMAN: Items** ist ein Container, der eine Instanz und seine EPR enthält. Diese Art von Enumeration wird initiiert, wenn das Flag " **wsmanflagreturnobjectandepr** " in der Anforderung festgelegt wird.

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**Baseboard-Verwaltungs Controller (BMC)**
</dt> <dd>

Ein lokal an einen Server angefügter Mikrocontroller. BMCs verfügen über Sensoren, die den physischen Zustand des Servers und eine separate Netzwerkverbindung überwachen, die über das Netzwerk kommunizieren kann, auch wenn der Server offline ist. Sie haben Zugriff auf BMC-Daten über den WMI-Anbieter [*(Intelligent Platform Management Interface)*](windows-remote-management-glossary.md) .

</dd> <dt>

**Standardauthentifizierung**
</dt> <dd>

Der Benutzername und das Kennwort, die im Authentifizierungs Austausch gesendet werden. Die Standard Authentifizierung kann so konfiguriert werden, dass der http-oder HTTPS-Transport in einer Domäne oder Arbeitsgruppe verwendet wird. Diese Methode ist die am wenigsten sichere Authentifizierungsmethode.

</dd> <dt>

**BMC**
</dt> <dd>

Weitere Informationen finden Sie unter [*Baseboard-Verwaltungs Controller (BMC)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Gerufen**
</dt> <dd>

Weitere Informationen finden Sie unter [*Common Information Model (CIM)*](windows-remote-management-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

Die Client Anwendung, die das WS-Management-Protokoll verwendet, um auf den Verwaltungsdienst auf dem lokalen oder einem Remote Computer zuzugreifen.

</dd> <dt>

**Common Information Model (CIM)**
</dt> <dd>

Das [*DMTF-Modell (verteiltes Management Task Force)*](windows-remote-management-glossary.md) , das beschreibt, wie reale Computer-und Netzwerk Objekte dargestellt werden. CIM verwendet ein objektorientiertes Paradigma, in dem verwaltete Objekte mit den Konzepten von Klassen und Instanzen modelliert werden.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Digestauthentifizierung**
</dt> <dd>

Ein Exchange-Server, in dem der Server eine Anforderung von einem Client empfängt und Daten zum Client an einen authentifizier enden Server sendet (in der Regel ein Domänen Controller). Wenn der Client authentifiziert ist, erhält der Server einen Digest-Sitzungsschlüssel, der zum Authentifizieren der nachfolgenden Anforderungen vom Client verwendet wird.

</dd> <dt>

**Task Force für verteilte Verwaltung (DMTF)**
</dt> <dd>

Die Branchenorganisation entwickelt Verwaltungsstandards und Integrationstechnologien für Unternehmen-und Internet Umgebungen.

</dd> <dt>

**DMTF**
</dt> <dd>

Siehe [*verteilte Verwaltung Task Force (DMTF)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**Dreher**
</dt> <dd>

Eine Ressource, die von einem [*Endpunkt Verweis (EPR)*](windows-remote-management-glossary.md)adressiert werden kann.

</dd> <dt>

**Endpunkt Verweis (EPR)**
</dt> <dd>

Eine Kombination aus WS-Addressing und WS-Management Adressierungs Elementen, die zusammen eine Adresse für eine Ressource im SOAP-Header der Nachricht beschreiben. Dies ist ein Webdienst Begriff.

</dd> <dt>

**Enumeration**
</dt> <dd>

Eine Menge oder Auflistung von [*Ressourcen*](windows-remote-management-glossary.md) Instanzen oder die Aktion, die eine solche Menge anfordert. In WS-Management Protokoll wird zum Abrufen der [*Auflistung WS-Enumeration*](windows-remote-management-glossary.md) verwendet. In der WinRM-Dienst Skript Implementierung von Enumeration werden [**Session. Enumerate**](session-enumerate.md) und das [**Enumeratorobjekt**](enumerator.md) verwendet. Die entsprechende C++-Methode und-Schnittstelle sind [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) und [**iwsmanenumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

**EPR**
</dt> <dd>

Siehe [*EndPoint Reference (EPR)*](windows-remote-management-glossary.md).

</dd> <dt>

**Ereignis Sammlungs Dienst**
</dt> <dd>

Die Betriebssystem Komponente, die Ereignisse vom BMC und anderen Betriebssystemkomponenten oder-Anwendungen empfängt.

</dd> <dt>

**Ereignis Weiterleitung**
</dt> <dd>

Eine Benachrichtigung über Ereignisse, die auf Remote Computern auftreten, kann an Abonnement Anwendungen gesendet werden. Bei der Ereignis Weiterleitung handelt es sich nicht um eine Funktion von WinRM, sondern um das [Windows-Ereignisprotokoll](/windows/desktop/WES/windows-event-log). Die Ereignis Weiterleitung wird zum ersten Mal in Windows Vista verfügbar. Die Verwaltungs Anwendungen, wie z. b. Microsoft Operations Manager (MOM), verwenden die Ereignis Weiterleitung.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

Ein Abfrage Mechanismus zum Angeben einer begrenzten Anzahl von-Instanzen in der Anforderung für eine [*Ressource*](windows-remote-management-glossary.md). Sie können einen *Filter* Parameter bei Aufrufen von [**Session. Enumerate**](session-enumerate.md) oder [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)angeben.

</dd> <dt>

**Filter Dialekt**
</dt> <dd>

Eine XML-Zeichenfolge, die den XML-Dialekt angibt, mit dem ein [*Filter*](windows-remote-management-glossary.md) in einem Aufrufen von [**Session. Enumerate**](session-enumerate.md) oder [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)angegeben wird. Der WinRM-Dienst unterstützt [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) beim Empfangen von Anforderungen als Filter Dialekt.

</dd> <dt>

**Bruch**
</dt> <dd>

Eine XML-Zeichenfolge, die einen Teil einer Instanz einer Ressource anstelle der gesamten Ressource angibt. Die fragmentunterstützung wurde im [**ResourceLocator**](resourcelocator.md) -Objekt gefunden.

</dd> <dt>

**Fragmentdialekt**
</dt> <dd>

Eine XML-Zeichenfolge, die den XML-Dialekt angibt, mit dem ein [*Fragment*](windows-remote-management-glossary.md)angegeben wird. Die fragmentunterstützung wurde im [**ResourceLocator**](resourcelocator.md) -Objekt gefunden. Der WinRM-Dienst unterstützt [*XPath*](windows-remote-management-glossary.md) für den Fragmentdialekt beim Empfangen von Anforderungen.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**in-Band**
</dt> <dd>

Die Client Anwendung erhält BMC-Daten über den WinRM- [*Listener*](windows-remote-management-glossary.md) im Betriebssystem.

</dd> <dt>

**Intelligent Platform Management Interface (IPMI)**
</dt> <dd>

Einen IT-Industriestandard für die Architektur des [*Baseboard-Verwaltungs Controllers (Baseboard Management Controller, BMC)*](windows-remote-management-glossary.md). Die Windows-Hardware Verwaltungsfunktionen stellen einen [*IPMI-Treiber*](windows-remote-management-glossary.md) und einen WMI- [*IPMI-Anbieter*](windows-remote-management-glossary.md) bereit, mit denen Verwaltungs Skripts, Befehlszeilen Tools und Anwendungen BMC-Daten abrufen können. Der IPMI-Anbieter verfügt über WMI- [Klassen](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

</dd> <dt>

**IPMI**
</dt> <dd>

Weitere Informationen finden Sie unter [*Intelligent Platform Management Interface (IMPI)*](windows-remote-management-glossary.md).

</dd> <dt>

**IPMI-Treiber**
</dt> <dd>

Der Kernel Treiber, der den Zugriff auf die BMC-Geräte [*(Baseboard Management Controller)*](windows-remote-management-glossary.md) über die Betriebssystemkomponenten ermöglicht.

</dd> <dt>

**IPMI-Anbieter**
</dt> <dd>

Ein standardmäßiger WMI-Anbieter, der Klassen definiert, die den [*IPMI*](windows-remote-management-glossary.md) und seine Daten modellieren. Der [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) ist eine com-dll, die Daten aus dem BMC abruft.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**KCS**
</dt> <dd>

Siehe [*Tastatur Controller Stil (KCS)*](windows-remote-management-glossary.md).

</dd> <dt>

**Kerberos-Authentifizierung**
</dt> <dd>

Eine Methode der gegenseitigen Authentifizierung zwischen dem Client und dem Server, der verschlüsselte Schlüssel verwendet. Bei Computern, auf denen ein Windows-basiertes Betriebssystem ausgeführt wird, muss es sich bei dem Client Konto um ein Domänen Konto in derselben Domäne wie der Server handeln. Wenn ein Client Standard Anmelde Informationen verwendet, ist Kerberos die Authentifizierungsmethode, wenn es sich bei der Verbindungs Zeichenfolge nicht um einen der folgenden handelt: localhost, 127.0.0.1 oder \[ :: 1 \] .

</dd> <dt>

**Tastatur Controller Stil (KCS)**
</dt> <dd>

Das Protokoll, das vom [*IPMI-Treiber*](windows-remote-management-glossary.md) für die Kommunikation mit dem [*Baseboard-Verwaltungs Controller (BMC)*](windows-remote-management-glossary.md)verwendet wird.

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

Ein Verwaltungsdienst, der WS-Management Protokoll zum Senden und empfangen von Nachrichten implementiert. WinRM ist ein Listenerdienst. Ein Listener wird durch einen Transport (http oder HTTPS) und eine IPv4-oder IPv6-Adresse definiert. Sie können mehr als eine WinRM-listenerinstanz auf einem einzelnen Computer erstellen, indem Sie Ihnen eine andere TCP/IP-Adresse oder Portnummer angeben.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**Nachricht**
</dt> <dd>

Ein Paket mit Informationen, die zwischen Computern übertragen werden, oder mit dem [*SOAP*](windows-remote-management-glossary.md) -Protokoll erstellte Netzwerke. Das Paket verfügt über einen-Header, der das Nachrichten Ziel und den Transport beschreibt, sowie einen Text, der den Inhalt enthält, der beim Eintreffen der Nachricht verwendet werden soll. Bei einer Nachricht handelt es sich um eine Kombination aus Elementen aus Spezifikationen, wie z. b. [*WS-Adressierung*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)und [*WS-Management*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**namespace**
</dt> <dd>

Ein [*WMI*](windows-remote-management-glossary.md) -Namespace, bei dem es sich um eine logische Gruppierung von WMI-Klassen und-Instanzen handelt, um den Bereich und Zugriff zu steuern Die häufigste Quelle von Verwaltungsdaten für Systeme, die Windows ausführen, ist der root \\ CIMV2-Namespace, der Klassen wie z. b. den [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process)enthält. Namespaces werden im Ressourcen-URI für WMI-Klassen angezeigt, z https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service . b..

</dd> <dt>

**Authentifizierung aushandeln**
</dt> <dd>

Ein Aushandlungs-Authentifizierungstyp, bei dem es sich um die Windows-Implementierung von [*einfachem und geschütztem GSSAPI-Aushandlungs Mechanismus (spnetgo)*](windows-remote-management-glossary.md)handelt. Die spnetgo-Aushandlung bestimmt, ob die Authentifizierung von Kerberos oder NTLM verarbeitet wird. Kerberos ist der bevorzugte Mechanismus. Die Aushandlung der Authentifizierung auf Windows-basierten Systemen wird auch als integrierte Windows-Authentifizierung bezeichnet.

</dd> <dt>

**numerischer Sensor**
</dt> <dd>

Ein numerischer Sensortyp in einem [*Baseboard-Verwaltungs Controller (BMC)*](windows-remote-management-glossary.md), z. b. Temperatur oder Spannung.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Option**
</dt> <dd>

Die zusätzlichen Daten, die vom Ressourcenanbieter für die Verarbeitung einer Anforderung benötigt werden. Einige WMI-Anbieter benötigen beispielsweise zusätzliche Daten, die als [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) -oder [**Swap-namedvalueset**](/windows/desktop/WmiSdk/swbemnamedvalueset) -Objekte bereitgestellt werden. Die Options Unterstützung ist im [**ResourceLocator**](resourcelocator.md) -Objekt enthalten.

</dd> <dt>

**Out-of-Band**
</dt> <dd>

Die Client Anwendung ruft Daten direkt vom [*Baseboard-Verwaltungs Controller (BMC)*](windows-remote-management-glossary.md) eines anderen Computers und nicht über den WinRM- [*Listener*](windows-remote-management-glossary.md) im Betriebssystem ab.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**auszu**
</dt> <dd>

Eine [*WS-Enumeration*](windows-remote-management-glossary.md) -Pull-Nachricht wird gesendet, um eine Enumeration fortzusetzen, die durch einen anfänglichen WS-Enumeration: Enumerate gestartet wurde. Der Pull-Vorgang im WinRM-Dienst wird von [**Enumerator. ReadItem**](enumerator-readitem.md) oder [**iwsmanenumerator:: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem)ausgeführt.

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**resource**
</dt> <dd>

Ein [*Endpunkt*](windows-remote-management-glossary.md) , der einen unterschiedlichen Typ von Verwaltungsvorgang oder Wert darstellt. Ein Dienst macht eine oder mehrere Ressourcen verfügbar, und einige Ressourcen können mehr als eine Instanz aufweisen. Eine Verwaltungs Ressource ähnelt einer WMI-Klasse oder einer Datenbanktabelle, und eine Instanz ähnelt einer Instanz der-Klasse oder einer Zeile in der Tabelle. Die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse stellt z. b. eine Ressource dar. `Win32_LogicalDisk="C:\"` ist eine bestimmte Instanz der Ressource.

</dd> <dt>

**Ressourcen-URI**
</dt> <dd>

Der [*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md) , der verwendet wird, um einen bestimmten Ressourcentyp (z. b. Datenträger oder Prozesse) auf einem System zu identifizieren.

</dd> </dl>

## <a name="s"></a>E

<dl> <dt>

**Essel**
</dt> <dd>

Weitere Informationen finden Sie unter [*System Ereignisprotokoll (SEL)*](windows-remote-management-glossary.md).

</dd> <dt>

**SEL-Adapter**
</dt> <dd>

Der Adapter, der [*Baseboard-Verwaltungs Controller (BMC)*](windows-remote-management-glossary.md) -Daten an den [*Ereignis Sammler*](windows-remote-management-glossary.md)sendet.

</dd> <dt>

**ktor**
</dt> <dd>

Ein Name-Wert-Paar, das eine bestimmte Instanz einer [*Ressource*](windows-remote-management-glossary.md)darstellt. Dabei handelt es sich im Wesentlichen um einen Filter oder einen Schlüssel, der die gewünschte Instanz der Ressource identifiziert. Im [**ResourceLocator**](resourcelocator.md) -Objekt wurde eine Auswahl Unterstützung gefunden.

</dd> <dt>

**Sensor**
</dt> <dd>

Ein Messgerät in einem [*Baseboard-Verwaltungs Controller (BMC)*](windows-remote-management-glossary.md).

</dd> <dt>

**service**
</dt> <dd>

Eine Anwendung, die Verwaltungsdienste über das WS-Management-Protokoll und andere [*Webdienste*](windows-remote-management-glossary.md)für Clients bereitstellt. Ein Dienst ist in der Regel mit dem [*Listener*](windows-remote-management-glossary.md) in einem Netzwerk identisch. Der Dienst verfügt über eine physische Transport Adresse.

</dd> <dt>

**Sitzung**
</dt> <dd>

Eine Verbindung zwischen einem Windows-Remoteverwaltung- [*Client*](windows-remote-management-glossary.md) und dem lokalen oder Remote-WinRM- [*Listener*](windows-remote-management-glossary.md)oder-Dienst. Diese Verbindung ähnelt der Verbindung zwischen einem WMI-Client Skript und WMI auf einem Remote Server. Die Sitzungs Vorgänge, z. b. das Auflisten einer Ressource (aufzählenden), das erhalten einer Instanz einer Ressource (Get) oder das Ausführen einer Ressourcen Methode (aufrufen) sind Methoden des **Sitzungs** Objekts. Ein **Sitzungs** Objekt wird von " [**WSMAN. kreatesession**](wsman-createsession.md)" erstellt.

</dd> <dt>

**Einfacher und geschützter GSS-API-Aushandlungs Mechanismus (spnetgo)**
</dt> <dd>

Ein Authentifizierungsmechanismus, der vom Client oder Server zum Empfangen von Datenanforderungen über WinRM in einem Active Directory Kontext verwendet wird. Spnetgo basiert auf einem von der Internet Engineering Task Force (IETF) erstellten RFC-Protokoll (Request for Comments). Spargo wird auch als [*integrierte Windows-Authentifizierung*](windows-remote-management-glossary.md)bezeichnet und ist der Begriff, der in den Windows-Remoteverwaltung Hilfe Themen verwendet wird.

</dd> <dt>

**Simple Object Access-Protokoll (SOAP)**
</dt> <dd>

Ein XML-basiertes Protokoll, das von Webdiensten verwendet wird.

</dd> <dt>

**SOAP**
</dt> <dd>

Siehe [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).

</dd> <dt>

**SPNEGO**
</dt> <dd>

Weitere Informationen finden Sie unter [*Simple and Protected GSS-API Aushandlungs Mechanismus (spnetgo)*](windows-remote-management-glossary.md).

</dd> <dt>

**System Ereignisprotokoll (SEL)**
</dt> <dd>

Die Datenbank der Ereignisse in der [*BMC-Hardware (Baseboard Management Controller)*](windows-remote-management-glossary.md) . Diese Ereignisse werden vom [*SEL-Adapter*](windows-remote-management-glossary.md) an das Betriebssystem übermittelt.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**Uniform Resource Identifier (URI)**
</dt> <dd>

Eine Zeichenfolge, die eine Ressource im Unternehmen identifiziert, z. b. ein Computer, ein Prozess, ein Laufwerk oder ein Temperatursensor in einem [*Baseboard-Verwaltungs Controller (BMC)*](windows-remote-management-glossary.md). Der URI ist der in der IETF (Internet Engineering Task Force)-Uniform Resource Identifier (URI) definierte Webdienst Adressierungs Mechanismus: generische Syntax \[ RFC3986 \] .

</dd> <dt>

**URI**
</dt> <dd>

Siehe [*Uniform Resource Identifier (URI)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Webdienst**
</dt> <dd>

Eine Software Anwendung, die für die Interaktion zwischen Computern über das Internet oder ein Netzwerk verwendet wird. Webdienste werden von [*WSDL (Web Service Description Language)*](windows-remote-management-glossary.md)beschrieben. Die spezifische Beschreibung des Webdiensts teilt anderen Diensten mit, wie mit dem Webdienst mithilfe von SOAP-Nachrichten interagiert werden soll. Die Nachrichten werden von einem Transport (in der Regel über HTTP oder HTTPS) zwischen Computern übermittelt. [*WS-Adressierung*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md)und [*WS-Management*](windows-remote-management-glossary.md) sind Beispiele für Protokolle, die von Webdienst Anwendungen für die Kommunikation untereinander verwendet werden.

</dd> <dt>

**WSDL (Web Service Description Language)**
</dt> <dd>

Eine XML-basierte Sprache, die verwendet wird, um zu definieren, wie mit einem Webdienst interagiert wird. In der Regel beschreibt die WSDL, welche SOAP-Nachrichten der Webdienst benötigt, um Daten zurückzugeben oder Vorgänge auszuführen. Mithilfe der WSDL kann eine Implementierung von einem Betriebssystem mit dem Webdienst kommunizieren, der unter einem anderen Betriebssystem implementiert ist, solange die Anforderungen der WSDL erfüllt sind.

</dd> <dt>

**Integrierte Windows-Authentifizierung**
</dt> <dd>

Siehe [*Aushandeln der Authentifizierung*](windows-remote-management-glossary.md).

</dd> <dt>

**Windows-Verwaltungsinstrumentation (WMI)**
</dt> <dd>

Die Microsoft-Implementierung des Web-Based Enterprise Management (WBEM)-Standards, der von der [*verteilten Verwaltungs Task Force (DMTF)*](windows-remote-management-glossary.md)veröffentlicht wurde. Mit WMI können Sie lokale und Remote Computer verwalten und Computer-und Netzwerk Objekte mithilfe einer Erweiterung des [*Common Information Model (CIM)*](windows-remote-management-glossary.md) -Standards modelliert werden.

</dd> <dt>

**Windows-Remoteverwaltung (WinRM)**
</dt> <dd>

Die Microsoft-Implementierung eines verwaltungsweb Diensts basierend auf dem öffentlichen Standard- [*WS-Verwaltungs*](windows-remote-management-glossary.md) Protokoll.

</dd> <dt>

**Windows-Remoteshell (Winrs)**
</dt> <dd>

Ein shelltool, das [*Windows-Remoteverwaltung*](windows-remote-management-glossary.md) zum Ausführen von Remote Befehlen, insbesondere für Server ohne Server, unterstützt. Das Befehlszeilen Tool ist Winrs.

</dd> <dt>

**WMI**
</dt> <dd>

Weitere Informationen finden Sie unter [*Windows-Verwaltungsinstrumentation (WMI)*](windows-remote-management-glossary.md).

</dd> <dt>

**WMI-Plug-in**
</dt> <dd>

Das WinRM-Plug-in, das die WMI-Daten für WinRM-Clients verfügbar macht.

</dd> <dt>

**WS-Adressierung (WSA)**
</dt> <dd>

Ein öffentliches Standardprotokoll (SOAP-basiert), das ein Adressierungs System erstellt, das in den Headern der über das Internet gesendeten Nachrichten verwendet wird. Der Standard definiert, wie Ressourcen in Netzwerken und Firewalls gefunden werden können. WS-Addressing ist eines der Webdienst Protokolle, die das WS-Management Protokoll bilden.

</dd> <dt>

**WS-Enumeration (wsen)**
</dt> <dd>

Ein öffentliches Standardprotokoll (SOAP-basiert) zum Auflisten einer Sequenz von XML-Elementen, die Daten Auflistungen, Protokolle oder andere lineare Informationsstrukturen darstellen kann. WS-Enumeration ist eines der Webdienst Protokolle, die das WS-Management Protokoll bilden.

</dd> <dt>

**WS-Eventing (WSE)**
</dt> <dd>

Ein öffentliches Standardprotokoll (SOAP-basiert), das es einem Webdienst (dem Abonnenten) gestattet, Ereignis Benachrichtigungs Meldungen von einem anderen Webdienst (der Ereignis Quelle) zu abonnieren und zu akzeptieren. WS-Eventing ist eines der Webdienst Protokolle, die das WS-Management Protokoll bilden.

</dd> <dt>

**WS-Verwaltung**
</dt> <dd>

Ein öffentliches Standardprotokoll (SOAP-basiert) für die Freigabe von Verwaltungsdaten für alle Betriebssysteme, Computer und Geräte. Alle [*Nachrichten*](windows-remote-management-glossary.md) , die von WinRM-Client oder-Serverkomponenten gesendet werden, verwenden dieses Protokoll.

</dd> <dt>

**WS-Transfer (wxf)**
</dt> <dd>

Ein öffentliches Standardprotokoll, das SOAP-basiert ist, für den Zugriff auf XML-Darstellungen von Webdienst basierten Ressourcen über einen einfachen Satz von Verben wie Get, Put, Aufruf oder DELETE. WS-Transfer definiert Vorgänge für das Senden und empfangen der Darstellung einer bestimmten Ressource und Vorgänge zum Erstellen oder Löschen einer Ressource und ihrer entsprechenden Darstellung.

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

Eine Pfad Notation zur Adressierung von Teilen eines XML-Dokuments, ähnlich einer URL. Ein XPath-Ausdruck ist eine Sequenz von Ausdrücken, die vom aktuellen Speicherort im XML-Dokument zu einem anderen Knoten oder einer Gruppe von Knoten zu erhalten sind. Die Ausdrücke werden durch Schrägstriche ("/") getrennt. Der WinRM-Dienst unterstützt [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) für den [*Fragment-Dialekt*](windows-remote-management-glossary.md).

</dd> </dl>

 

 