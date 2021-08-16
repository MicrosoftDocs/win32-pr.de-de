---
title: Windows Remoteverwaltungsglossar
description: Glossarseite
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 532562a45090040cebbefae2bfff601727efb8bca794a9d9833e61a53ad63a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743264"
---
# <a name="windows-remote-management-glossary"></a>Windows Remoteverwaltungsglossar


<dl> <dt>

wsman:Items**
</dt> <dd>

Ein WS-Management Protokollelement, das in einer Enumeration zurückgegeben wird, die sowohl die -Instanzen als auch die [*Instanz-EPRs erhält.*](/windows) **wsman:Items** ist ein Container, der eine Instanz und deren EPR enthält. Dieser Enumerationstyp wird initiiert, wenn das **Flag WSManFlagReturnObjectAndEPR** in der Anforderung festgelegt wird.

</dd> </dl>

## <a name="b"></a>B

<dl> <dt>

**Baseboard-Verwaltungscontroller (Baseboard Management Controller, BMC)**
</dt> <dd>

Ein mikrocontroller, der lokal an einen Server angefügt ist. BMCs verfügen über Sensoren, die den physischen Zustand des Servers überwachen, und eine separate Netzwerkverbindung, die über das Netzwerk kommunizieren kann, auch wenn der Server offline ist. Sie haben Zugriff auf BMC-Daten über den [*WMI-Anbieter (Intelligent Platform Management Interface, IPMI).*](windows-remote-management-glossary.md)

</dd> <dt>

**Standardauthentifizierung**
</dt> <dd>

Der Benutzername und das Kennwort, die beim Authentifizierungsaustausch gesendet werden. Die Standardauthentifizierung kann für die Verwendung des HTTP- oder HTTPS-Transports in einer Domäne oder Arbeitsgruppe konfiguriert werden. Diese Methode ist die am wenigsten sichere Authentifizierungsmethode.

</dd> <dt>

**BMC**
</dt> <dd>

Weitere Informationen [*finden Sie unter Baseboard Management Controller (BMC).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Cim**
</dt> <dd>

Siehe [*Common Information Model (CIM).*](windows-remote-management-glossary.md)

</dd> <dt>

**client**
</dt> <dd>

Die Clientanwendung, die das WS-Management verwendet, um auf den Verwaltungsdienst auf dem lokalen oder einem Remotecomputer zu zugreifen.

</dd> <dt>

**Common Information Model (CIM)**
</dt> <dd>

Das [*DMTF-Modell (Distributed Management Task Force),*](windows-remote-management-glossary.md) das beschreibt, wie reale Computer- und Netzwerkobjekte repräsentiert werden. CIM verwendet ein objektorientiertes Paradigma, in dem verwaltete Objekte mit den Konzepten von Klassen und Instanzen modelliert werden.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**Digestauthentifizierung**
</dt> <dd>

Ein Austausch, bei dem der Server eine Anforderung von einem Client empfängt und Daten über den Client an einen authentifizierenden Server sendet, in der Regel an einen Domänencontroller. Wenn der Client authentifiziert ist, erhält der Server einen Digestsitzungsschlüssel, der zum Authentifizieren nachfolgender Anforderungen vom Client verwendet wird.

</dd> <dt>

**Distributed Management Task Force (DMTF)**
</dt> <dd>

Die Branchenorganisation, die Verwaltungsstandards und Integrationstechnologie für Unternehmens- und Internetumgebungen entwickelt.

</dd> <dt>

**DMTF**
</dt> <dd>

Weitere Informationen [*finden Sie unter Distributed Management Task Force (DMTF).*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**endpoint**
</dt> <dd>

Eine Ressource, die durch einen [*Endpunktverweis (EPR) adressiert werden kann.*](windows-remote-management-glossary.md)

</dd> <dt>

**Endpunktverweis (Endpoint Reference, EPR)**
</dt> <dd>

Eine Kombination aus WS-Addressing und WS-Management Adressierungselementen, die zusammen eine Adresse für eine Ressource im SOAP-Nachrichtenheader beschreiben. Dies ist ein Webdienstbegriff.

</dd> <dt>

**Enumeration**
</dt> <dd>

Ein Satz oder eine Sammlung von [*Ressourceninstanzen*](windows-remote-management-glossary.md) oder die Aktion zum Anfordern eines solchen Sets. Im WS-Management wird [*die WS-Enumeration*](windows-remote-management-glossary.md) verwendet, um die Auflistung zu erhalten. In der WinRM-Dienstskriptimplementierung der -Enumeration werden [**Session.Enumerate**](session-enumerate.md) und das [**Enumerator-Objekt**](enumerator.md) verwendet. Die entsprechende C++-Methode und -Schnittstelle sind [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) und [**IWSManEnumerator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)

</dd> <dt>

**EPR**
</dt> <dd>

Weitere Informationen [*finden Sie unter Endpunktreferenz (EPR).*](windows-remote-management-glossary.md)

</dd> <dt>

**Ereignissammlungsdienst**
</dt> <dd>

Die Betriebssystemkomponente, die Ereignisse vom BMC und anderen Betriebssystemkomponenten oder -anwendungen empfängt.

</dd> <dt>

**Ereignisweiterleitung**
</dt> <dd>

Eine Benachrichtigung über Ereignisse, die auf Remotecomputern auftreten, kann an abonnierende Anwendungen gesendet werden. Die Ereignisweiterleitung ist kein Feature von WinRM, sondern Windows [Ereignisprotokolls.](/windows/desktop/WES/windows-event-log) Die Ereignisweiterleitung wird zum ersten Mal in Windows Vista verfügbar. Die Verwaltungsanwendungen, z. B. Microsoft Operations Manager (MOM), verwenden ereignisweiterleitung.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filter**
</dt> <dd>

Ein Abfragemechanismus zum Angeben einer begrenzten Anzahl von Instanzen in der Anforderung für eine [*Ressource.*](windows-remote-management-glossary.md) Sie können einen *Filterparameter für* Aufrufe von [**Session.Enumerate**](session-enumerate.md) oder [**IWSManSession::Enumerate angeben.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)

</dd> <dt>

**Filterdialekt**
</dt> <dd>

Eine XML-Zeichenfolge, die den XML-Dialekt identifiziert, der zum Angeben eines Filters [*in*](windows-remote-management-glossary.md) einem Aufruf von [**Session.Enumerate**](session-enumerate.md) oder [**IWSManSession::Enumerate verwendet wird.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) Der WinRM-Dienst unterstützt [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) als Filterdialekt beim Empfangen von Anforderungen.

</dd> <dt>

**Fragment**
</dt> <dd>

Eine XML-Zeichenfolge, die einen Teil einer Instanz einer Ressource anstelle der gesamten Ressource identifiziert. Fragmentunterstützung finden Sie im [**ResourceLocator-Objekt.**](resourcelocator.md)

</dd> <dt>

**Fragmentdialekt**
</dt> <dd>

Eine XML-Zeichenfolge, die den XML-Dialekt identifiziert, der zum Angeben eines Fragments [*verwendet wird.*](windows-remote-management-glossary.md) Fragmentunterstützung finden Sie im [**ResourceLocator-Objekt.**](resourcelocator.md) Der WinRM-Dienst unterstützt [*XPath für fragmentierten*](windows-remote-management-glossary.md) Dialekt beim Empfangen von Anforderungen.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**In-Band**
</dt> <dd>

Die Clientanwendung erhält BMC-Daten über den [*WinRM-Listener*](windows-remote-management-glossary.md) im Betriebssystem.

</dd> <dt>

**Intelligent Platform Management Interface (IPMI)**
</dt> <dd>

Ein IT-Branchenstandard für die Architektur des [*Baseboard Management Controllers (BMC).*](windows-remote-management-glossary.md) Die Windows Hardwareverwaltungsfeatures stellen einen [*IPMI-Treiber*](windows-remote-management-glossary.md) und einen [*WMI-IPMI-Anbieter*](windows-remote-management-glossary.md) zur Verfügung, mit denen Verwaltungsskripts, Befehlszeilentools und Anwendungen BMC-Daten abrufen können. Der IPMI-Anbieter verfügt über [WMI-Klassen.](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)

</dd> <dt>

**IPMI**
</dt> <dd>

Weitere Informationen [*finden Sie unter Intelligent Platform Management Interface (IMPI).*](windows-remote-management-glossary.md)

</dd> <dt>

**IPMI-Treiber**
</dt> <dd>

Der Kerneltreiber, der den Zugriff auf [*BMC-Geräte (Baseboard Management Controller)*](windows-remote-management-glossary.md) über die Betriebssystemkomponenten ermöglicht.

</dd> <dt>

**IPMI-Anbieter**
</dt> <dd>

Ein WMI-Standardanbieter, der Klassen definiert, die [*die IPMI und*](windows-remote-management-glossary.md) ihre Daten modellieren. Der [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) ist eine COM-DLL, die Daten vom BMC erhält.

</dd> </dl>

## <a name="k"></a>K

<dl> <dt>

**Kcs**
</dt> <dd>

Weitere Informationen [*finden Sie unter Tastaturcontrollerstil (KCS).*](windows-remote-management-glossary.md)

</dd> <dt>

**Kerberos-Authentifizierung**
</dt> <dd>

Eine Methode der gegenseitigen Authentifizierung zwischen Client und Server, die verschlüsselte Schlüssel verwendet. Bei Computern, die auf einem Windows-basierten Betriebssystem ausgeführt werden, muss das Clientkonto ein Domänenkonto in derselben Domäne wie der Server sein. Wenn ein Client Standardanmeldeinformationen verwendet, ist Kerberos die Authentifizierungsmethode, wenn es sich bei der Verbindungszeichenfolge nicht um eine der folgenden Handelt: localhost, 127.0.0.1 oder \[ ::1 \] .

</dd> <dt>

**Tastaturcontrollerstil (Keyboard Controller Style, KCS)**
</dt> <dd>

Das Protokoll, das vom [*IPMI-Treiber für*](windows-remote-management-glossary.md) die Kommunikation mit dem [*Baseboard Management Controller (BMC) verwendet wird.*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**listener**
</dt> <dd>

Ein Verwaltungsdienst, der ein WS-Management zum Senden und Empfangen von Nachrichten implementiert. WinRM ist ein Listenerdienst. Ein Listener wird durch einen Transport (HTTP oder HTTPS) und eine IPv4- oder IPv6-Adresse definiert. Sie können mehrere WinRM-Listenerinstanzen auf einem einzelnen Computer erstellen, indem Sie ihnen eine andere TCP/IP-Adresse oder Portnummer geben.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**Nachricht**
</dt> <dd>

Ein Paket von Informationen, die zwischen Computern oder separaten Netzwerken übertragen werden, die mit dem [*SOAP-Protokoll erstellt*](windows-remote-management-glossary.md) wurden. Das Paket verfügt über einen Header, der das Nachrichtenziel und den Transport beschreibt, sowie einen Text, der den Inhalt enthält, der beim Eintreffen der Nachricht verwendet werden soll. Eine Nachricht ist eine Kombination aus Elementen aus Spezifikationen wie [*WS-Adressierung,*](windows-remote-management-glossary.md) [*WS-Transfer*](windows-remote-management-glossary.md)und [*WS-Management.*](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**namespace**
</dt> <dd>

Ein [*WMI-Namespace,*](windows-remote-management-glossary.md) bei dem es sich um eine logische Gruppierung von WMI-Klassen und -Instanzen zum Steuern von Bereich und Zugriff handelt. Die häufigste Quelle für Verwaltungsdaten für Systeme, auf denen Windows ausgeführt wird, ist der \\ Stammnamespace cimv2, der Klassen wie [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process)enthält. Namespaces werden im Ressourcen-URI für WMI-Klassen angezeigt, https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service z. B. .

</dd> <dt>

**Aushandeln der Authentifizierung**
</dt> <dd>

Ein ausgehandelter Authentifizierungstyp für einmaliges Anmelden, der die Windows Implementierung von [*Simple and Protected GSSAPI Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md)darstellt. Die SPNEGO-Aushandlung bestimmt, ob die Authentifizierung von Kerberos oder NTLM verarbeitet wird. Kerberos ist der bevorzugte Mechanismus. Die Aushandlung der Authentifizierung auf Windows-basierten Systemen wird auch als Windows integrierte Authentifizierung bezeichnet.

</dd> <dt>

**Numerischer Sensor**
</dt> <dd>

Ein numerischer Sensortyp in einem [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md), z. B. Temperatur oder Spannung.

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**Option**
</dt> <dd>

Die zusätzlichen Daten, die der Ressourcenanbieter zum Verarbeiten einer Anforderung benötigt. Einige WMI-Anbieter erfordern beispielsweise zusätzliche Daten, die als [**IWbemContext-**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) oder [**SWbemNamedValueSet-Objekte**](/windows/desktop/WmiSdk/swbemnamedvalueset) bereitgestellt werden. Optionsunterstützung finden Sie im [**ResourceLocator-Objekt.**](resourcelocator.md)

</dd> <dt>

**Out-of-Band**
</dt> <dd>

Die Clientanwendung ruft Daten direkt vom [*Baseboard-Verwaltungscontroller (Baseboard Management Controller, BMC)*](windows-remote-management-glossary.md) eines anderen Computers ab, anstatt über den WinRM-Listener im Betriebssystem. [](windows-remote-management-glossary.md)

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**pull**
</dt> <dd>

Eine [*WS-Enumeration-Pullnachricht*](windows-remote-management-glossary.md) wird gesendet, um eine Enumeration fortzusetzen, die durch einen ersten Aufruf von WS-Enumeration:Enumerate gestartet wurde. Der Pullvorgang im WinRM-Dienst wird von [**Enumerator.ReadItem**](enumerator-readitem.md) oder [**IWSManEnumerator::ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem)ausgeführt.

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**resource**
</dt> <dd>

Ein [*Endpunkt,*](windows-remote-management-glossary.md) der einen unterschiedlichen Typ von Verwaltungsvorgang oder -wert darstellt. Ein Dienst macht eine oder mehrere Ressourcen verfügbar, und einige Ressourcen können über mehrere Instanzen verfügen. Eine Verwaltungsressource ähnelt einer WMI-Klasse oder einer Datenbanktabelle, und eine -Instanz ähnelt einer Instanz der -Klasse oder einer Zeile in der Tabelle. Beispielsweise stellt die [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) eine Ressource dar. `Win32_LogicalDisk="C:\"` ist eine bestimmte Instanz der Ressource.

</dd> <dt>

**Ressourcen-URI**
</dt> <dd>

Der [*URI (Uniform Resource Identifier),*](windows-remote-management-glossary.md) der verwendet wird, um einen bestimmten Ressourcentyp, z. B. Datenträger oder Prozesse, auf einem System zu identifizieren.

</dd> </dl>

## <a name="s"></a>E

<dl> <dt>

**Sel**
</dt> <dd>

Weitere Informationen finden Sie unter [*Systemereignisprotokoll (SEL).*](windows-remote-management-glossary.md)

</dd> <dt>

**SEL-Adapter**
</dt> <dd>

Der Adapter, der [*BMC-Daten (Baseboard Management Controller)*](windows-remote-management-glossary.md) an den [*Ereignissammler*](windows-remote-management-glossary.md)sendet.

</dd> <dt>

**Selector**
</dt> <dd>

Ein Name-Wert-Paar, das eine bestimmte Instanz einer [*Ressource*](windows-remote-management-glossary.md)darstellt. Dies ist im Wesentlichen ein Filter oder "Schlüssel", der die gewünschte Instanz der Ressource identifiziert. Selektorunterstützung befindet sich im [**ResourceLocator-Objekt.**](resourcelocator.md)

</dd> <dt>

**Sensor**
</dt> <dd>

Ein Messgerät in einem [*Baseboard-Verwaltungscontroller (BMC).*](windows-remote-management-glossary.md)

</dd> <dt>

**service**
</dt> <dd>

Eine Anwendung, die Verwaltungsdienste für Clients über das WS-Management-Protokoll und andere [*Webdienste*](windows-remote-management-glossary.md)bereitstellt. Ein Dienst ist in der Regel mit dem [*Listener*](windows-remote-management-glossary.md) in einem Netzwerk identisch. Der Dienst verfügt über eine physische Transportadresse.

</dd> <dt>

**Sitzung**
</dt> <dd>

Eine Verbindung zwischen einem Windows [*Remoteverwaltungsclient*](windows-remote-management-glossary.md) und dem lokalen oder Remote-WinRM-Listener oder -Dienst. [](windows-remote-management-glossary.md) Diese Verbindung ähnelt der Verbindung zwischen einem WMI-Clientskript und WMI auf einem Remoteserver. Die Sitzungsvorgänge wie das Aufzählen einer Ressource (Aufzählen), das Abrufen einer Instanz einer Ressource (Get) oder das Ausführen einer Ressourcenmethode (Invoke) sind Methoden des **Session-Objekts.** Ein **Session-Objekt** wird von [**WSMan.CreateSession**](wsman-createsession.md)erstellt.

</dd> <dt>

**Einfacher und geschützter GSS-API-Aushandlungsmechanismus (SPNEGO)**
</dt> <dd>

Ein Authentifizierungsmechanismus, der vom Client oder Server verwendet wird, der Anforderungen für Daten über WinRM in einem Active Directory-Kontext empfängt. SPNEGO basiert auf einem RFC-Protokoll (Request For Comments), das von der Internet Engineering Task Force (IETF) erstellt wurde. SPNEGO wird auch als [*Windows Integrierte Authentifizierung*](windows-remote-management-glossary.md)bezeichnet. Dieser Begriff wird in den Hilfethemen Windows Remoteverwaltung verwendet.

</dd> <dt>

**Simple Object Access-Protokoll (SOAP)**
</dt> <dd>

Ein XML-basiertes Protokoll, das von Webdiensten verwendet wird.

</dd> <dt>

**SOAP**
</dt> <dd>

Weitere Informationen finden Sie unter [*Simple Object Access Protocol (SOAP).*](windows-remote-management-glossary.md)

</dd> <dt>

**Spnego**
</dt> <dd>

Weitere Informationen finden Sie unter [*Simple and Protected GSS-API Negotiation Mechanism (SPNEGO) (Einfacher und geschützter GSS-API-Aushandlungsmechanismus (SPNEGO) ).*](windows-remote-management-glossary.md)

</dd> <dt>

**Systemereignisprotokoll (SEL)**
</dt> <dd>

Die Datenbank der Ereignisse auf der [*BMC-Hardware (Baseboard Management Controller).*](windows-remote-management-glossary.md) Der [*SEL-Adapter*](windows-remote-management-glossary.md) übermittelt diese Ereignisse an das Betriebssystem.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**Uniform Resource Identifier (URI)**
</dt> <dd>

Eine Zeichenfolge, die eine Ressource im Unternehmen identifiziert, z. B. einen Computer, einen Prozess, ein Laufwerk oder einen Temperatursensor in einem [*Baseboard Management Controller (BMC).*](windows-remote-management-glossary.md) Der URI ist der Webdienstadressierungsmechanismus, der in internet engineering task force (IETF) Uniform Resource Identifier (URI) definiert ist: Generische Syntax \[ RFC3986 \] .

</dd> <dt>

**URI**
</dt> <dd>

Siehe [*Uniform Resource Identifier (URI)*](windows-remote-management-glossary.md).

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Webdienst**
</dt> <dd>

Eine Softwareanwendung, die für die Interaktion zwischen Computern über das Internet oder ein Netzwerk verwendet wird. Webdienste werden von [*WSDL (Web Service Description Language)*](windows-remote-management-glossary.md)beschrieben. Die spezifische Beschreibung des Webdiensts teilt anderen Diensten mit, wie mithilfe von SOAP-Nachrichten mit dem Webdienst interagiert werden soll. Die Nachrichten werden zwischen Computern über einen Transport übermittelt, in der Regel HTTP oder HTTPS. [*WS-Adressierung,*](windows-remote-management-glossary.md) [*WS-Eventing*](windows-remote-management-glossary.md)und [*WS-Management*](windows-remote-management-glossary.md) sind Beispiele für Protokolle, die von Webdienstanwendungen für die Kommunikation miteinander verwendet werden.

</dd> <dt>

**Web Service Description Language (WSDL)**
</dt> <dd>

Eine XML-basierte Sprache, die verwendet wird, um zu definieren, wie mit einem Webdienst interagiert wird. In der Regel beschreibt die WSDL, welche SOAP-Nachrichten der Webdienst benötigt, um Daten zurückzugeben oder Vorgänge auszuführen. Die WSDL ermöglicht einer Implementierung eines Betriebssystems die Kommunikation mit dem Webdienst, der unter einem anderen Betriebssystem implementiert ist, solange die Anforderungen der WSDL erfüllt sind.

</dd> <dt>

**Integrierte Windows-Authentifizierung**
</dt> <dd>

Weitere Informationen finden Sie unter [*Aushandeln der Authentifizierung.*](windows-remote-management-glossary.md)

</dd> <dt>

**Windows-Verwaltungsinstrumentation (WMI)**
</dt> <dd>

Die Microsoft-Implementierung des WBEM-Standards (Web-Based Enterprise Management), der von der [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md)veröffentlicht wurde. Mit WMI können Sie lokale und Remotecomputer verwalten und Computer- und Netzwerkobjekte modellieren, indem Sie eine Erweiterung des [*CIM-Standards (Common Information Model)*](windows-remote-management-glossary.md) verwenden.

</dd> <dt>

**Windows-Remoteverwaltung (WinRM)**
</dt> <dd>

Die Microsoft-Implementierung eines Verwaltungswebdiensts, der auf dem öffentlichen [*WS-Management-Standardprotokoll*](windows-remote-management-glossary.md) basiert.

</dd> <dt>

**Windows Remote Shell (WinRS)**
</dt> <dd>

Ein Shelltool, das auf [*Windows Remoteverwaltung*](windows-remote-management-glossary.md) basiert, um Remotebefehle auszuführen, insbesondere für headlose Server. Das Befehlszeilentool ist Winrs.

</dd> <dt>

**WMI**
</dt> <dd>

Weitere Informationen finden Sie [*unter Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).

</dd> <dt>

**WMI-Plug-In**
</dt> <dd>

Das WinRM-Plug-In, das WMI-Daten für WinRM-Clients verfügbar macht.

</dd> <dt>

**WS-Adressierung (wsa)**
</dt> <dd>

Ein öffentliches, SOAP-basiertes Standardprotokoll, das ein Adressierungssystem erstellt, das in den Headern von Nachrichten verwendet wird, die über das Internet gesendet werden. Der Standard definiert, wie Ressourcen in Netzwerken und Firewalls angeordnet werden können. WS-Addressing ist eines der Webdienstprotokolle, aus denen das WS-Management-Protokoll besteht.

</dd> <dt>

**WS-Enumeration (wsen)**
</dt> <dd>

Ein öffentliches, SOAP-basiertes Standardprotokoll zum Auflisten einer Sequenz von XML-Elementen, die Datenauflistungen, Protokolle oder andere lineare Informationsstrukturen darstellen können. WS-Enumeration ist eines der Webdienstprotokolle, aus denen das WS-Management-Protokoll besteht.

</dd> <dt>

**WS-Eventing (wse)**
</dt> <dd>

Ein öffentliches, SOAP-basiertes Standardprotokoll, mit dem ein Webdienst (der Abonnent) Ereignisbenachrichtigungen von einem anderen Webdienst (der Ereignisquelle) abonnieren und akzeptieren kann. WS-Eventing ist eines der Webdienstprotokolle, aus denen das WS-Management-Protokoll besteht.

</dd> <dt>

**WS-Verwaltung**
</dt> <dd>

Ein öffentliches Standardprotokoll, das SOAP-basiert ist, um Verwaltungsdaten für alle Betriebssysteme, Computer und Geräte gemeinsam zu nutzen. Alle [*nachrichten,*](windows-remote-management-glossary.md) die von den WinRM-Client- oder -Serverkomponenten gesendet werden, verwenden dieses Protokoll.

</dd> <dt>

**WS-Transfer (wxf)**
</dt> <dd>

Ein öffentliches, SOAP-basiertes Standardprotokoll für den Zugriff auf XML-Darstellungen von webdienstbasierten Ressourcen über einen einfachen Satz von Verben wie Get, Put, Invoke oder Delete. WS-Transfer definiert Vorgänge zum Senden und Empfangen der Darstellung einer bestimmten Ressource und Vorgänge zum Erstellen oder Löschen einer Ressource und ihrer entsprechenden Darstellung.

</dd> </dl>

## <a name="x"></a>X

<dl> <dt>

**XPath**
</dt> <dd>

Eine Pfad notation zum Adressieren von Teilen eines XML-Dokuments, ähnlich einer URL. Ein XPath-Ausdruck ist eine Sequenz von Ausdrücken, die vom aktuellen Speicherort im XML-Dokument auf einen anderen Knoten oder eine Andere Gruppe von Knoten übertragen werden sollen. Die Ausdrücke werden durch Schrägstriche ("/") getrennt. Der WinRM-Dienst unterstützt [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) für [*Fragmentdialekte.*](windows-remote-management-glossary.md)

</dd> </dl>

 

 