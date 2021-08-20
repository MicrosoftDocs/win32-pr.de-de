---
description: Die Win32 ServerFeature-Klasse stellt die Funktionen dar, die auf einem Computer mit Windows \_ Server installiert sind.
ms.assetid: fe3bb95c-7f69-47b5-9c3d-771cdc3ed9ca
ms.tgt_platform: multiple
title: Win32_ServerFeature-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ServerFeature
- Win32_ServerFeature.ID
- Win32_ServerFeature.ParentID
- Win32_ServerFeature.Name
api_type:
- DllExport
api_location:
- ServerCompProv.dll
ms.openlocfilehash: eddbd71108a5b6b65de329e1c110c965f437e4c24f7ba0a681935ba5075351fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312137"
---
# <a name="win32_serverfeature-class"></a>Win32 \_ ServerFeature-Klasse

\[Die **Win32 \_ ServerFeature-Klasse** steht für die Verwendung in den im Abschnitt Anforderungen angegebenen Betriebssystemen zur Verfügung. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [ServerManager Deploymentprovider Provider-Klassen.](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)\]

Die **Win32 \_ ServerFeature-Klasse** stellt die Funktionen dar, die auf einem Computer mit Windows Server installiert sind.

Diese Klasse kann von Entwicklern und Administratoren verwendet werden, die den Prozess der Bestimmung der auf einer Gruppe von Servercomputern installierten Features automatisieren müssen. Instanzen dieser Klasse sind auf Clientcomputern nicht verfügbar.

## <a name="syntax"></a>Syntax

``` syntax
[Deprecated("No value"), Dynamic, Provider("ServerFeatureProvider"), AMENDMENT]
class Win32_ServerFeature
{
  uint32 ID;
  uint32 ParentID;
  string Name;
};
```

## <a name="members"></a>Members

Die **Win32 \_ ServerFeature-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ ServerFeature-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ID**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**Schlüssel,**](key-qualifier.md) [**nicht \_ NULL**](optional-qualifiers.md)
</dt> </dl>

Serverfeature-ID. In der folgenden Liste sind die möglichen Werte der ID-Eigenschaft aufgeführt:



Wert

Name

1

[Anwendungsserver](/windows)

2

Webserver (IIS)

3

[Streaming Media-Dienste](/windows)

5

Faxserver

6

Datei- und iSCSI-Dienste<br/> [Namensänderung](/windows)<br/>

7

Druck- und Dokumentdienste<br/> [Namensänderung](/windows)<br/>

8

[Active Directory-Verbunddienste (AD FS)](/windows)

9

Active Directory Lightweight Directory Services

10

Active Directory Domain Services

11

[UDDI-Dienste](/windows)<br/>

12

[DHCP-Server](/windows)

13

[DNS-Server](/windows)

14

Network Policy and Access Services

16

Active Directory-Zertifikatdienste

17

Active Directory-Rechteverwaltungsdienste

18

[Remotedesktopdienste](/windows)<br/> [Namensänderung](/windows)<br/>

19

Windows-Bereitstellungsdienste

20

Hyper-V

21

[Windows Server Update Services](/windows)

33

[Failoverclustering](/windows)

34

[Netzwerklastenausgleich](/windows)

36

[.NET Framework 3.5.1-Features](/windows)<br/> [Namensänderung](/windows)<br/>

37

[Windows-Systemressourcen-Manager](/windows)

38

WLAN-Dienst

39

[Windows Serversicherungsfunktionen](/windows)

40

WINS-Server

41

Windows-Prozessaktivierungsdienst

42

[Remoteunterstützung](/windows)

43

Einfache TCP/IP-Dienste

44

[Telnet-Client](/windows)

45

[Telnet-Server](/windows)

46

[Subsystem für Unix-basierte Anwendungen](/windows)

47

RPC über HTTP-Proxy

48

SMTP-Server

49

Message Queuing

51

[Interne Windows-Datenbank](/windows)

52

[Storage Manager für SANs](/windows)

53

LPR-Portüberwachung

55

[Internet Storage Name Server](/windows)

57

[Multipfad-E/A](/windows)

58

TFTP-Client

59

[SNMP-Dienste](/windows)

60

[Wechselmedien Storage-Manager](/windows)

61

BitLocker-Laufwerkverschlüsselung

62

[Dienste für das Netzwerkdateisystem](/windows)

63

Internetdruckclient

64

[Peer Name Resolution-Protokoll (PNRP)](/windows)

65

Verbindungs-Manager-Verwaltungskit

66

[Windows PowerShell](/windows)<br/>

67

[Remoteserver-Verwaltungstools](/windows)

68

[Verbessertes Windows-Audio-/Video-Streaming](/windows)

69

[Gruppenrichtlinienverwaltung](/windows)

71

[Indexdienst](/windows)

72

[Ressourcen-Manager für Dateiserver (File Server Resource Manager, FSRM)](/windows)

73

Remotedifferenzialkomprimierung

310

Freihand- und Handschriftdienste<br/>

320

[Windows Server-Migrationstools](/windows)<br/>

321

[WinRM-IIS-Erweiterung](/windows)<br/>

324

[BranchCache](#branchcache)<br/>

334

[DirectAccess-Verwaltungskonsole](/windows)<br/>

335

[BITS (Background Intelligent Transfer Service, Intelligenter Hintergrundübertragungsdienst)](/windows)<br/>

338

[XPS-Viewer](/windows)<br/>

339

[Windows-Biometrieframework](/windows)<br/>

340

WoW64-Unterstützung<br/>

351

[Windows PowerShell Integrated Scripting Environment (ISE)](/windows)<br/>

352

Windows-TIFF-IFilter<br/>

404

[Windows Server Update Services](/windows)

409

[IP-Adressverwaltungsserver (IPAM-Server)](/windows)

417

[Windows PowerShell](/windows)

418

[.NET Framework 4.5](/windows)

432

[Windows Search-Dienst](/windows)

438

[Client für NFS](/windows)

441

[BitLocker-Netzwerkentsperrung](/windows)

442

[IIS-Erweiterung für OData Services for Management](/windows)

450

[.NET Framework 4.5 Advanced Services](/windows)

466

[.NET Framework 4.5-Features](/windows)

468

[Remotezugriff](/windows)<br/>

477

[Benutzeroberflächen und Infrastruktur](/windows)

478

[Grafische Verwaltungstools und Infrastruktur](/windows)

481

[Datei- und Speicherdienste](/windows)

485

[Windows Server Essentials Experience](/windows)

488

[DirectPlay](/windows)

Dateidienste – Rollendienste (6)

Wert

Name

100

[verteiltes Dateisystem](/windows)

101

DFS-Namespace

102

DFS-Replikation

103

[Dateireplikationsdienst](/windows)

104

[Ressourcen-Manager für Dateiserver (File Server Resource Manager, FSRM)](/windows)

105

[Dienste für das Netzwerkdateisystem](/windows)

106

[Einzelinstanz-Speicherung](/windows)

107

[Windows Search-Dienst](/windows)

108

[Indexdienst](/windows)

255

Dateiserver

350

BranchCache für Netzwerkdateien

431

[Server für NFS](/windows)<br/>

434

[Dateiserver-VSS-Agent-Dienst](/windows)<br/>

435

[iSCSI-Zielserver](/windows)<br/>

436

[Datendeduplizierung](/windows)<br/>

437

[iSCSI-Storage Anbieter (VDS- und VSS-Hardwareanbieter)](/windows)

486

[Arbeitsordner](/windows)

AD DS – Rollendienste (10)

Wert

Name

110

[Active Directory-Domänencontroller](/windows)

111

[Identitätsverwaltung für Unix](/windows)

112

[Server für Netzwerkinformationsdienste](/windows)

113

[Kennwortsynchronisierung](/windows)

294

[Remoteserver-Verwaltungstools](/windows)

Streamingmedien – Rollendienste (3)

Wert

Name

120

[Windows Medienserver](/windows)

121

[Webbasierte Verwaltung](/windows)

122

[Protokollierungs-Agent](/windows)

AD FS – Rollendienste (8)

Wert

Name

125

[Active Directory-Verbunddienste (AD FS)](/windows)

126

[Verbunddienst Richtlinie](/windows)

127

[AD FS-Web-Agents](/windows)

128

[Ansprüche unterstützender Agent](/windows)

129

[Windows Tokenbasierter Agent](/windows)

Remotedesktopdienste – Rollendienste (18)

Wert

Name

130

Remotedesktop-Sitzungshost<br/> [Namensänderung](/windows)<br/>

131

[Remotedesktoplizenzierung](/windows)<br/> [Namensänderung](/windows)<br/>

132

Remotedesktopgateway<br/> [Namensänderung](/windows)<br/>

133

Remotedesktop-Verbindungsbroker<br/> [Namensänderung](/windows)<br/>

134

Remotedesktop-Webzugriff<br/> [Namensänderung](/windows)<br/>

322

Remotedesktop-Virtualisierungshost<br/>

Remotedesktop Virtualization Host – Role Services (322)

Wert

Name

325

[Core Services](/windows)<br/>

327

[Remotedesktop virtuelle Grafiken](/windows)<br/>

Druck- und Dokumentdienste – Rollendienste (7)

Wert

Name

135

Druckerserver

136

Internetdrucken

137

LPD-Druckdienst

328

[Server für verteilte Scanvorgänge](/windows)<br/>

Webserver (IIS): Rollendienste (2)

Wert

Name

140

Webserver

141

Allgemeine HTTP-Funktionen

142

Statischer Inhalt

143

Standarddokument

144

Verzeichnissuche

145

HTTP-Fehler

146

HTTP-Umleitung

147

Anwendungsentwicklung

148

ASP.NET

149

.NET-Erweiterbarkeit

150

ASP

151

CGI

152

ISAPI-Erweiterungen

153

ISAPI-Filter

154

Serverseitige Includes (SSI)

155

Integrität und Diagnose

156

HTTP-Protokollierung

157

Protokollierungstools

158

Anforderungsüberwachung

159

Ablaufverfolgung

160

Benutzerdefinierte Protokollierung

161

ODBC-Protokollierung

162

Sicherheit

163

Standardauthentifizierung

164

Windows-Authentifizierung

165

Digestauthentifizierung

166

Authentifizierung durch Clientzertifikatszuordnung

167

Authentifizierung durch IIS-Clientzertifikatszuordnung

168

URL-Autorisierung

169

Anforderungsfilterung

170

IP- und Domäneneinschränkungen

171

Leistung

172

Komprimierung statischer Inhalte

173

Komprimierung dynamischer Inhalte

174

Verwaltungstools

175

IIS-Verwaltungskonsole

176

IIS-Verwaltungsskripts und -tools

177

Verwaltungsdienst

178

IIS 6-Verwaltungskompatibilität

179

IIS 6-Metabasiskompatibilität

180

IIS 6-WMI-Kompatibilität

181

IIS 6-Skripttools

182

IIS 6-Verwaltungskonsole

183

FTP-Publishingdienst<br/>

184

FTP-Server

185

FTP-Verwaltungskonsole<br/>

314

WebDAV-Veröffentlichung

316

FTP-Dienst<br/>

317

FTP-Erweiterbarkeit<br/>

336

Hostfähiger IIS-Webkern<br/>

413

[ASP.NET 4.5](/windows)

414

[.NET-Erweiterbarkeit 4.5](/windows)

445

[Appialisierung](/windows)

446

[Zentralisierte Unterstützung von SSL-Zertifikaten](/windows)

447

[WebSocket-Protokoll](/windows)

Message Queuing – Features (49)

Wert

Name

190

Message Queuing Services

191

Message Queuing Server

192

Verzeichnisdienstintegration

193

Message Queuing Trigger

194

HTTP-Unterstützung

195

Routingdienst

196

[Windows 2000-Clientunterstützung](/windows)<br/>

197

Message Queuing-DCOM-Proxy

228

Multicastunterstützung

Active Directory-Zertifikatdienste – Rollendienste (16)

Wert

Name

200

Zertifizierungsstelle

201

Zertifizierungsstellen-Webregistrierung

202

Online-Responder

204

Registrierungsdienst für Netzwerkgeräte

318

[Zertifikatregistrierungs-Webdienst](/windows)<br/>

319

[Zertifikatregistrierungsrichtlinien-Webdienst](/windows)<br/>

Netzwerkrichtlinie und Access Services – Rollendienste (14)

Wert

Name

205

[Netzwerkrichtlinienserver](/windows)

206

[VPN](#vpn)

207

[Remote Access Services](/windows)

208

[Routing](#routing)

210

[Integritätsregistrierungsstelle](/windows)

250

[Host Credential Authorization Protocol](/windows)

UDDI-Dienste – Rollendienste (11)

Wert

Name

215

[UDDI Services-Webanwendung](/windows)<br/>

216

[UDDI Services-Datenbank](/windows)<br/>

Windows Prozessaktivierungsdienst – Rollendienste (41)

Wert

Name

217

Konfigurations-API

218

.NET-Umgebung

219

Prozessmodell

.NET Framework 3.5.1 – Features (36)

Wert

Name

220

.NET Framework 3.5.1<br/> [Namensänderung](/windows)<br/>

221

WCF-Aktivierung

222

HTTP-Aktivierung

223

Nicht-HTTP-Aktivierung

227

XPS-Viewer<br/>

SNMP-Dienste – Features (59)

Wert

Name

224

[SNMP-Dienst](/windows)

225

[SNMP-WMI-Anbieter](/windows)

Anwendungsdienste – Rollendienste

Wert

Name

230

[.NET Framework 3.5.1](/windows)<br/> [Namensänderung](/windows)<br/>

231

[Webserver-Unterstützung (IIS)](/windows)

232

[COM+-Netzwerkzugriff](/windows)

233

[TCP-Portfreigabe](/windows)

234

[Windows Unterstützung des Prozessaktivierungsdiensts](/windows)

235

[HTTP-Aktivierung](/windows)

236

[Message Queuing Aktivierung](/windows)

237

[TCP-Aktivierung](/windows)

238

[Named Pipes-Aktivierung](/windows)

239

[Distributed Transactions](/windows) (Verteilte Transaktionen)

240

[Eingehende Remotetransaktionen](/windows)

241

[Ausgehende Remotetransaktionen](/windows)

242

[WS-Automatic Transactions](/windows)

353

[Anwendungsservererweiterungen für .NET 4.0](/windows)<br/>

Windows Bereitstellungsdienste – Rolle (19)

Wert

Name

251

Bereitstellungsserver

252

Transportserver

Active Directory Rights Management Services – Rollendienste (17)

Wert

Name

253

Active Directory-Rechteverwaltungsserver

254

Unterstützung für Identitätsverbund

Remoteserver-Verwaltungstools (67)

Wert

Name

256

[Rollenverwaltungstools](/windows)

257

[AD DS-Tools](/windows)<br/> [Namensänderung](/windows)<br/>

258

[AD LDS Snap-Ins und Command-Line Tools](/windows)<br/> [Namensänderung](/windows)<br/>

259

Tools für Active Directory-Zertifikatdienste

260

[Network Policy and Access Services](/windows)

261

Druck- und Dokumentdienste Tools<br/> [Namensänderung](/windows)<br/>

262

[Active Directory-Rechteverwaltungsdienste](/windows)

263

[Tools für Remotedesktopdienste](/windows)<br/> [Namensänderung](/windows)<br/>

264

Windows Bereitstellungsdienstetools

265

[Featureverwaltungstools](/windows)

266

Tools zur BitLocker-Laufwerkverschlüsselung

267

Tools für BITS-Servererweiterungen

268

[Failoverclusteringtools](/windows)

269

Tools für Netzwerklastenausgleich

270

SMTP-Servertools

273

[DNS-Servertools](/windows)

277

Tools für Dateidienste

278

verteiltes Dateisystem Tools

279

Tools für den Ressourcen-Manager für Dateiserver

280

[Dienste für Netzwerkdateisystemtools](/windows)

281

Webservertools (IIS)

284

[Remotedesktop-Sitzungshost Tools](/windows)<br/> [Namensänderung](/windows)<br/>

285

Remotedesktop Gatewaytools<br/> [Namensänderung](/windows)<br/>

286

Remotedesktop Lizenzierungstools<br/> [Namensänderung](/windows)<br/>

288

Faxservertools

290

WINS-Servertools

291

[UDDI-Diensttools](/windows)<br/>

292

Zertifizierungsstellentools

293

Online-Antworttools

297

[Server für NIS Tools](/windows)

299

[AD DS-Snap-Ins und -Befehlszeilentools](/windows)<br/> [Namensänderung](/windows)<br/>

300

[Active Directory-Verwaltungscenter](/windows)

301

Hyper-V-Tools

323

[BitLocker-Wiederherstellungskennwort-Viewer](/windows)<br/>

326

[Verwaltungsdienstprogramme für die BitLocker-Laufwerkverschlüsselung](/windows)<br/>

329

[AD DS- und AD LDS-Tools](/windows)<br/>

330

Active Directory-Verwaltungscenter<br/>

331

[Active Directory-Modul für Windows PowerShell](/windows)<br/>

337

[Remotedesktopverbindung Broker-Tools](/windows)<br/>

410

[IP-Adressverwaltung (IPAM) Client](/windows)

450

[Hyper-V-Modul für Windows PowerShell](/windows)

462

[Active Directory Rights Management Services Werkzeuge](/windows)

465

[Freigabe- und Storage Verwaltungstool](/windows)

471

[Tools für die Remotezugriffsverwaltung](/windows)

472

[RAS-Modul für Windows PowerShell](/windows)

473

[Remotezugriffs-GUI und Command-Line Tools](/windows)

474

[Windows Server Update Services-Tools](/windows)

476

[Remotedesktop Lizenzierungsdiagnosetools](/windows)

479

[SNMP-Tools](/windows)

480

[Volumenaktivierungstools](/windows)

Windows Serversicherung – Features (39)

Wert

Name

296

[Windows Server-Sicherung](/windows)

297

[Befehlszeilentools](/windows)

Freihand- und Handschriftdienste – Features (310)

Wert

Name

311

[Ink-Unterstützung](/windows)<br/>

312

[Handschrifterkennung](/windows)<br/>

Background Intelligent Transfer Service (BITS) – Features (335)

Wert

Name

54

IIS-Servererweiterung

332

[Compact Server](/windows)<br/>

Wow64-Unterstützung – Features (340)

Wert

Name

341

[WoW64](#wow64)<br/>

342

[WoW64 für .NET Framework 2.0 und Windows PowerShell](/windows)<br/>

343

[WoW64 für .NET Framework 2.0](/windows)<br/>

344

[WoW64 für PowerShell](/windows)<br/>

345

[WoW64 für .NET Framework 3.0 und 3.5](/windows)<br/>

346

[WoW64 für Druckdienste](/windows)<br/>

347

[WoW64 für Failoverclustering](/windows)<br/>

348

[WoW64 für den Eingabemethode-Editor](/windows)<br/>

349

[WoW64 für das Subsystem für UNIX-basierte Anwendungen](/windows)<br/>

Benutzeroberflächen und Infrastruktur – Rollendienste (447)

Wert

Name

35

[Desktopdarstellung](/windows)

99

[Grafische Shell des Servers](/windows)

Windows Server Update Services – Features (404)

Wert

Name

405

[API- und PowerShell-Cmdlets](/windows)

406

[SQL Server Verbindung](/windows)

407

[WSUS-Dienste](/windows)

408

[Benutzeroberfläche-Verwaltungskonsole](/windows)

449

[WID-Konnektivität](/windows)

Windows PowerShell – Features (417)

Wert

Name

411

[Windows PowerShell 2.0-Engine](/windows)

412

[Windows PowerShell 3.0](/windows)

448

[Windows PowerShell Web Access](/windows)

1000

[Windows PowerShell Desired State Configuration-Dienst](/windows)

.NET Framework 4.5: Features (418)

Wert

Name

419

[.NET Framework 4.5 Erweitert](/windows)

420

[WCF-Dienste](/windows)

421

[HTTP-Aktivierung](/windows)

422

[aktivierung von Message Queuing (MSMQ)](/windows)

423

[Named Pipe-Aktivierung](/windows)

424

[TCP-Aktivierung](/windows)

425

[TCP-Portfreigabe](/windows)

429

[ASP.NET 4.5](/windows)

Remotezugriff – Rolle (468)

Wert

Name

469

[DirectAccess und VPN (RAS)](/windows)

470

[Routing](#routing)

Datei- und Storage Dienste – Rolle (481)

Wert

Name

482

[Storage Dienstleistungen](/windows)

484

[Failoverclusterverwaltungstools](/windows)



 

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Anzeigename des Serverfeatures, z. B. "Dateiserver", "Druckserver" oder "Desktopdarstellung".

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

ID-Nummer des übergeordneten Serverfeatures. Diese Eigenschaft ist 0, wenn das von der aktuellen Instanz der -Klasse dargestellte Feature kein übergeordnetes Feature besitzt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Weitere Informationen zu Serverfeatures finden Sie in der [technischen Übersicht über Windows Server 2008 Server-Manager.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753319(v=ws.10))

Unternehmen, die keine Verwaltungssoftware verwenden, die Serverfeatures meldet, z. B. System Center Operations Manager mit installierten Management Packs, können diese Informationen abrufen, indem sie die **Win32 \_ ServerFeature-Klasse** abfragen.

Sie können die Remotingfeatures von WMI oder WinRM verwenden, um Informationen zu Serverfeatures von Remoteservern abzurufen. Weitere Informationen zu WMI-DCOM-Remoteverbindungen finden Sie unter [Herstellen einer Verbindung mit WMI auf einem Remotecomputer.](connecting-to-wmi-on-a-remote-computer.md) Weitere Informationen über WinRM finden Sie unter Windows-Remoteverwaltung.

Windows Server 2012: **Win32 \_ ServerFeature** ist veraltet. Um programmgesteuert auf Windows Server-Featureinformationen zuzugreifen, können Sie die [Server-Manager Cmdlets](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ee662311(v=technet.10))verwenden.

### <a name="windows-server-2012-r2"></a>Windows Server 2012 R2

<dl> <dt>

<span id="Application_Server"></span><span id="application_server"></span><span id="APPLICATION_SERVER"></span>Anwendungsserver
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Streaming_Media_Services"></span><span id="streaming_media_services"></span><span id="STREAMING_MEDIA_SERVICES"></span>Streaming Media Services
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Active_Directory_Federation_Services"></span><span id="active_directory_federation_services"></span><span id="ACTIVE_DIRECTORY_FEDERATION_SERVICES"></span>Active Directory-Verbunddienste (AD FS)
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="DHCP_Server"></span><span id="dhcp_server"></span><span id="DHCP_SERVER"></span>DHCP-Server
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="DNS_Server"></span><span id="dns_server"></span><span id="DNS_SERVER"></span>DNS-Server
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>Remotedesktopdienste
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_Server_Update_Services"></span><span id="windows_server_update_services"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Failover_Clustering"></span><span id="failover_clustering"></span><span id="FAILOVER_CLUSTERING"></span>Failoverclustering
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Netzwerklastenausgleich
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features"></span><span id=".net_framework_3.5.1_features"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES"></span>.NET Framework 3.5.1-Features
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_Server_Backup_Features"></span><span id="windows_server_backup_features"></span><span id="WINDOWS_SERVER_BACKUP_FEATURES"></span>Windows Serversicherungsfunktionen
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Remote_Assistance"></span><span id="remote_assistance"></span><span id="REMOTE_ASSISTANCE"></span>Remoteunterstützung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Telnet_Client"></span><span id="telnet_client"></span><span id="TELNET_CLIENT"></span>Telnet-Client
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Telnet_Server"></span><span id="telnet_server"></span><span id="TELNET_SERVER"></span>Telnet Server
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Subsystem_For_Unix-based_Applications"></span><span id="subsystem_for_unix-based_applications"></span><span id="SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>Subsystem für Unix-basierte Anwendungen
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_Internal_Database"></span><span id="windows_internal_database"></span><span id="WINDOWS_INTERNAL_DATABASE"></span>interne Windows-Datenbank
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Storage_Manager_For_SANs"></span><span id="storage_manager_for_sans"></span><span id="STORAGE_MANAGER_FOR_SANS"></span>Storage Manager für SANs
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Internet_Storage_Name_Server"></span><span id="internet_storage_name_server"></span><span id="INTERNET_STORAGE_NAME_SERVER"></span>Internet Storage Name Server
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Multipath_I_O"></span><span id="multipath_i_o"></span><span id="MULTIPATH_I_O"></span>Multipfad-E/A
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="SNMP_Services"></span><span id="snmp_services"></span><span id="SNMP_SERVICES"></span>SNMP-Dienste
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Dienste für das Netzwerkdateisystem
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Peer_Name_Resolution_Protocol"></span><span id="peer_name_resolution_protocol"></span><span id="PEER_NAME_RESOLUTION_PROTOCOL"></span>Peer Name Resolution Protocol
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Remote_Server_Administration_Tools"></span><span id="remote_server_administration_tools"></span><span id="REMOTE_SERVER_ADMINISTRATION_TOOLS"></span>Remoteserver-Verwaltungstools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Quality_Windows_Audio_Video_Experience"></span><span id="quality_windows_audio_video_experience"></span><span id="QUALITY_WINDOWS_AUDIO_VIDEO_EXPERIENCE"></span>Quality Windows Audio Video Experience
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Group_Policy_Management"></span><span id="group_policy_management"></span><span id="GROUP_POLICY_MANAGEMENT"></span>Gruppenrichtlinie Verwaltung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indizierungsdienst
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="File_Server_Resource_Manager__FSRM_"></span><span id="file_server_resource_manager__fsrm_"></span><span id="FILE_SERVER_RESOURCE_MANAGER__FSRM_"></span>Dateiserver-Resource Manager (FSRM)
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_Server_Migration_Tools"></span><span id="windows_server_migration_tools"></span><span id="WINDOWS_SERVER_MIGRATION_TOOLS"></span>Windows Servermigrationstools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="BranchCache"></span><span id="branchcache"></span><span id="BRANCHCACHE"></span>Branchcache
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess-Verwaltungskonsole
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64-Unterstützung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Window_Server_Update_Services"></span><span id="window_server_update_services"></span><span id="WINDOW_SERVER_UPDATE_SERVICES"></span>Windows Server Update Services
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="IP_Address_Management__IPAM__Server"></span><span id="ip_address_management__ipam__server"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>IP-Adressverwaltung (IPAM) Server
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id=".NET_Framework_4.5"></span><span id=".net_framework_4.5"></span><span id=".NET_FRAMEWORK_4.5"></span>.NET Framework 4.5
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Suchdienst
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Client_for_NFS"></span><span id="client_for_nfs"></span><span id="CLIENT_FOR_NFS"></span>Client für NFS
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="BitLocker_Network_Unlock"></span><span id="bitlocker_network_unlock"></span><span id="BITLOCKER_NETWORK_UNLOCK"></span>BitLocker-Netzwerkentsperrung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Management_OData_IIS_Extension"></span><span id="management_odata_iis_extension"></span><span id="MANAGEMENT_ODATA_IIS_EXTENSION"></span>OData IIS-Verwaltungserweiterung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id=".NET_Framework_4.5_Advanced_Services"></span><span id=".net_framework_4.5_advanced_services"></span><span id=".NET_FRAMEWORK_4.5_ADVANCED_SERVICES"></span>.NET Framework 4.5 Advanced Services
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id=".NET_Framework_4.5_Features"></span><span id=".net_framework_4.5_features"></span><span id=".NET_FRAMEWORK_4.5_FEATURES"></span>.NET Framework 4.5-Features
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Benutzeroberflächen und Infrastruktur
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Graphical_Management_Tools_and_Infrastructure"></span><span id="graphical_management_tools_and_infrastructure"></span><span id="GRAPHICAL_MANAGEMENT_TOOLS_AND_INFRASTRUCTURE"></span>Tools und Infrastruktur für die grafische Verwaltung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="File_and_Storage_Services"></span><span id="file_and_storage_services"></span><span id="FILE_AND_STORAGE_SERVICES"></span>Datei- und Storage Dienste
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_Server_Essentials_Experience"></span><span id="windows_server_essentials_experience"></span><span id="WINDOWS_SERVER_ESSENTIALS_EXPERIENCE"></span>Windows Server Essentials Experience
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Direct_Play"></span><span id="direct_play"></span><span id="DIRECT_PLAY"></span>Direct Play
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Distributed_File_System"></span><span id="distributed_file_system"></span><span id="DISTRIBUTED_FILE_SYSTEM"></span>verteiltes Dateisystem
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="File_Server_Resource_Manager"></span><span id="file_server_resource_manager"></span><span id="FILE_SERVER_RESOURCE_MANAGER"></span>Dateiserver-Resource Manager
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Services_For_Network_File_System"></span><span id="services_for_network_file_system"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM"></span>Dienste für das Netzwerkdateisystem
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Single_Instance_Storage"></span><span id="single_instance_storage"></span><span id="SINGLE_INSTANCE_STORAGE"></span>Einzelinstanz-Storage
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_Search_Service"></span><span id="windows_search_service"></span><span id="WINDOWS_SEARCH_SERVICE"></span>Windows Suchdienst
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Indexing_Service"></span><span id="indexing_service"></span><span id="INDEXING_SERVICE"></span>Indizierungsdienst
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="iSCSI_Target_Storage_Provider__VDS_and_VSS_hardware_providers_"></span><span id="iscsi_target_storage_provider__vds_and_vss_hardware_providers_"></span><span id="ISCSI_TARGET_STORAGE_PROVIDER__VDS_AND_VSS_HARDWARE_PROVIDERS_"></span>iSCSI-Storage Anbieter (VDS- und VSS-Hardwareanbieter)
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Arbeitsordner
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Active_Directory_Domain_Controller"></span><span id="active_directory_domain_controller"></span><span id="ACTIVE_DIRECTORY_DOMAIN_CONTROLLER"></span>Active Directory-Domäne Controller
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Identity_Management_For_Unix"></span><span id="identity_management_for_unix"></span><span id="IDENTITY_MANAGEMENT_FOR_UNIX"></span>Identitätsverwaltung für Unix
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Server_For_Network_Information_Services"></span><span id="server_for_network_information_services"></span><span id="SERVER_FOR_NETWORK_INFORMATION_SERVICES"></span>Server für Netzwerkinformationsdienste
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Password_Synchronization"></span><span id="password_synchronization"></span><span id="PASSWORD_SYNCHRONIZATION"></span>Kennwortsynchronisierung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Administration_Tools"></span><span id="administration_tools"></span><span id="ADMINISTRATION_TOOLS"></span>Verwaltungstools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_Media_Server"></span><span id="windows_media_server"></span><span id="WINDOWS_MEDIA_SERVER"></span>Windows Medienserver
</dt> <dd>

Wird nicht mehr unterstützt.

</dd> <dt>

<span id="Web-based_Administration"></span><span id="web-based_administration"></span><span id="WEB-BASED_ADMINISTRATION"></span>Webbasierte Verwaltung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Logging_Agent"></span><span id="logging_agent"></span><span id="LOGGING_AGENT"></span>Protokollierungs-Agent
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Federation_Service"></span><span id="federation_service"></span><span id="FEDERATION_SERVICE"></span>Verbunddienst
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Federation_Service_Policy"></span><span id="federation_service_policy"></span><span id="FEDERATION_SERVICE_POLICY"></span>Verbunddienst Richtlinie
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="AD_FS_Web_Agents"></span><span id="ad_fs_web_agents"></span><span id="AD_FS_WEB_AGENTS"></span>AD FS Web-Agents
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_Token-based_Agent"></span><span id="windows_token-based_agent"></span><span id="WINDOWS_TOKEN-BASED_AGENT"></span>Windows Tokenbasierter Agent
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Remote_Desktop_Licensing"></span><span id="remote_desktop_licensing"></span><span id="REMOTE_DESKTOP_LICENSING"></span>Remotedesktop Lizenzierung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Network_Policy_Server"></span><span id="network_policy_server"></span><span id="NETWORK_POLICY_SERVER"></span>Netzwerkrichtlinienserver
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="VPN"></span><span id="vpn"></span>Vpn
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Remote_Access_Services"></span><span id="remote_access_services"></span><span id="REMOTE_ACCESS_SERVICES"></span>Remote Access Services
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Health_Registration_Authority"></span><span id="health_registration_authority"></span><span id="HEALTH_REGISTRATION_AUTHORITY"></span>Integritätsregistrierungsstelle
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Host_Credential_Authorization_Protocol"></span><span id="host_credential_authorization_protocol"></span><span id="HOST_CREDENTIAL_AUTHORIZATION_PROTOCOL"></span>Host Credential Authorization Protocol
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS-Viewer
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="SNMP_Service"></span><span id="snmp_service"></span><span id="SNMP_SERVICE"></span>SNMP-Dienst
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="SNMP_WMI_Provider"></span><span id="snmp_wmi_provider"></span><span id="SNMP_WMI_PROVIDER"></span>SNMP-WMI-Anbieter
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id=".NET_Framework_3.5.1"></span><span id=".net_framework_3.5.1"></span><span id=".NET_FRAMEWORK_3.5.1"></span>.NET Framework 3.5.1
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Web_Server__IIS__Support"></span><span id="web_server__iis__support"></span><span id="WEB_SERVER__IIS__SUPPORT"></span>Webserverunterstützung (IIS)
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+-Netzwerkzugriff
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP-Portfreigabe
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_Process_Activation_Service_Support"></span><span id="windows_process_activation_service_support"></span><span id="WINDOWS_PROCESS_ACTIVATION_SERVICE_SUPPORT"></span>Windows Prozessaktivierungsdienst-Unterstützung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP-Aktivierung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Message_Queuing_Activation"></span><span id="message_queuing_activation"></span><span id="MESSAGE_QUEUING_ACTIVATION"></span>Message Queuing Aktivierung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP-Aktivierung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Named_Pipes_Activation"></span><span id="named_pipes_activation"></span><span id="NAMED_PIPES_ACTIVATION"></span>Named Pipes-Aktivierung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Distributed_Transactions"></span><span id="distributed_transactions"></span><span id="DISTRIBUTED_TRANSACTIONS"></span>Verteilte Transaktionen
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Incoming_Remote_Transactions"></span><span id="incoming_remote_transactions"></span><span id="INCOMING_REMOTE_TRANSACTIONS"></span>Eingehende Remotetransaktionen
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Outgoing_Remote_Transactions"></span><span id="outgoing_remote_transactions"></span><span id="OUTGOING_REMOTE_TRANSACTIONS"></span>Ausgehende Remotetransaktionen
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WS-Automatic_Transactions"></span><span id="ws-automatic_transactions"></span><span id="WS-AUTOMATIC_TRANSACTIONS"></span>Automatische WS-Transaktionen
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Anwendungsservererweiterungen für .NET 4.0
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Role_Administration_Tools"></span><span id="role_administration_tools"></span><span id="ROLE_ADMINISTRATION_TOOLS"></span>Rollenverwaltungstools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="AD_DS_Tools"></span><span id="ad_ds_tools"></span><span id="AD_DS_TOOLS"></span>AD DS Tools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_lds_snap-ins_and_command-line_tools"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD LDS Snap-Ins und Command-Line Tools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Network_Policy_and_Access_Services"></span><span id="network_policy_and_access_services"></span><span id="NETWORK_POLICY_AND_ACCESS_SERVICES"></span>Netzwerkrichtlinie und Access Services
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services"></span><span id="active_directory_rights_management_services"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES"></span>Active Directory Rights Management Services
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Remote_Desktop_Services_Tools"></span><span id="remote_desktop_services_tools"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS"></span>Remotedesktopdienste Tools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Feature_Administration_Tools"></span><span id="feature_administration_tools"></span><span id="FEATURE_ADMINISTRATION_TOOLS"></span>Featureverwaltungstools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Failover_Clustering_Tools"></span><span id="failover_clustering_tools"></span><span id="FAILOVER_CLUSTERING_TOOLS"></span>Failoverclusteringtools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="DNS_Server_Tools"></span><span id="dns_server_tools"></span><span id="DNS_SERVER_TOOLS"></span>DNS-Servertools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Services_For_Network_File_System_Tools"></span><span id="services_for_network_file_system_tools"></span><span id="SERVICES_FOR_NETWORK_FILE_SYSTEM_TOOLS"></span>Dienste für Netzwerkdateisystemtools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Web_Server__IIS__Tools"></span><span id="web_server__iis__tools"></span><span id="WEB_SERVER__IIS__TOOLS"></span>Webservertools (IIS)
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Server_for_NIS_Tools"></span><span id="server_for_nis_tools"></span><span id="SERVER_FOR_NIS_TOOLS"></span>Server für NIS Tools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools"></span><span id="ad_ds_snap-ins_and_command-line_tools"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS"></span>AD DS Snap-Ins und Command-Line Tools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS und AD LDS Tools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remotedesktopverbindung Brokertools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="IP_Address_Management__IPAM__Client"></span><span id="ip_address_management__ipam__client"></span><span id="IP_ADDRESS_MANAGEMENT__IPAM__CLIENT"></span>IP-Adressverwaltung (IPAM) Client
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Hyper-V_Module_for_Windows_PowerShell"></span><span id="hyper-v_module_for_windows_powershell"></span><span id="HYPER-V_MODULE_FOR_WINDOWS_POWERSHELL"></span>Hyper-V-Modul für Windows PowerShell
</dt> <dd></dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tool"></span><span id="active_directory_rights_management_services_tool"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOL"></span>Active Directory Rights Management Services Werkzeug
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Share_and_Storage_Management_Tool"></span><span id="share_and_storage_management_tool"></span><span id="SHARE_AND_STORAGE_MANAGEMENT_TOOL"></span>Freigabe- und Storage-Verwaltungstool
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Remote_Access_Management_Tools"></span><span id="remote_access_management_tools"></span><span id="REMOTE_ACCESS_MANAGEMENT_TOOLS"></span>Remotezugriffsverwaltungstools
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Remote_Access_module_for_Windows_PowerShell"></span><span id="remote_access_module_for_windows_powershell"></span><span id="REMOTE_ACCESS_MODULE_FOR_WINDOWS_POWERSHELL"></span>Remotezugriffsmodul für Windows PowerShell
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Remote_Access_GUI_and_Command-Line_Tools"></span><span id="remote_access_gui_and_command-line_tools"></span><span id="REMOTE_ACCESS_GUI_AND_COMMAND-LINE_TOOLS"></span>Remotezugriffs-GUI und Command-Line-Tools
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_Server_Update_Services_Tools"></span><span id="windows_server_update_services_tools"></span><span id="WINDOWS_SERVER_UPDATE_SERVICES_TOOLS"></span>Windows Server Update Services Werkzeuge
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Remote_Desktop_Licensing_Diagnoser_Tools"></span><span id="remote_desktop_licensing_diagnoser_tools"></span><span id="REMOTE_DESKTOP_LICENSING_DIAGNOSER_TOOLS"></span>Remotedesktop Licensing Diagnoser Tools
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="SNMP_Tools"></span><span id="snmp_tools"></span><span id="SNMP_TOOLS"></span>SNMP-Tools
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Volume_Activation_Tools"></span><span id="volume_activation_tools"></span><span id="VOLUME_ACTIVATION_TOOLS"></span>Volumenaktivierungstools
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_Server_Backup"></span><span id="windows_server_backup"></span><span id="WINDOWS_SERVER_BACKUP"></span>Windows Serversicherung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Command_Line_Tools"></span><span id="command_line_tools"></span><span id="COMMAND_LINE_TOOLS"></span>Befehlszeilentools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Ink_Support"></span><span id="ink_support"></span><span id="INK_SUPPORT"></span>Unterstützung für Ink-Daten
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Handwriting_Recognition"></span><span id="handwriting_recognition"></span><span id="HANDWRITING_RECOGNITION"></span>Handschrifterkennung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Compact_Server"></span><span id="compact_server"></span><span id="COMPACT_SERVER"></span>Compact Server
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and___________"></span><span id="wow64_for_.net_framework_2.0_and___________"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND___________"></span>WoW64 für .NET Framework 2.0 und PowerShell
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 für .NET Framework 2.0
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 für PowerShell
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 für .NET Framework 3.0 und 3.5
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 für Druckdienste
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 für Failoverclustering
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 für den Eingabemethoden-Editor
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 für das Subsystem für UNIX-basierte Anwendungen
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Desktop_Experience"></span><span id="desktop_experience"></span><span id="DESKTOP_EXPERIENCE"></span>Desktopdarstellung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Server_Graphical_Shell"></span><span id="server_graphical_shell"></span><span id="SERVER_GRAPHICAL_SHELL"></span>Grafische Shell des Servers
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="API_and_PowerShell_cmdlets"></span><span id="api_and_powershell_cmdlets"></span><span id="API_AND_POWERSHELL_CMDLETS"></span>API- und PowerShell-Cmdlets
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="SQL_Server_Connectivity"></span><span id="sql_server_connectivity"></span><span id="SQL_SERVER_CONNECTIVITY"></span>SQL Server Verbindung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WSUS_Services"></span><span id="wsus_services"></span><span id="WSUS_SERVICES"></span>WSUS-Dienste
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="User_Interface_Management_Console"></span><span id="user_interface_management_console"></span><span id="USER_INTERFACE_MANAGEMENT_CONSOLE"></span>Benutzeroberfläche-Verwaltungskonsole
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WID_Connectivity"></span><span id="wid_connectivity"></span><span id="WID_CONNECTIVITY"></span>WID-Konnektivität
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_PowerShell_2.0_Engine"></span><span id="windows_powershell_2.0_engine"></span><span id="WINDOWS_POWERSHELL_2.0_ENGINE"></span>Windows PowerShell 2.0-Engine
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_PowerShell_3.0"></span><span id="windows_powershell_3.0"></span><span id="WINDOWS_POWERSHELL_3.0"></span>Windows PowerShell 3.0
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_PowerShell_Web_Access"></span><span id="windows_powershell_web_access"></span><span id="WINDOWS_POWERSHELL_WEB_ACCESS"></span>Windows PowerShell Webzugriff
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_PowerShell_Desired_State_Configuration_Service"></span><span id="windows_powershell_desired_state_configuration_service"></span><span id="WINDOWS_POWERSHELL_DESIRED_STATE_CONFIGURATION_SERVICE"></span>Windows PowerShell Desired State Configuration-Dienst
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id=".NET_Framework_4.5_Extended"></span><span id=".net_framework_4.5_extended"></span><span id=".NET_FRAMEWORK_4.5_EXTENDED"></span>.NET Framework 4.5 Erweitert
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WCF_Services"></span><span id="wcf_services"></span><span id="WCF_SERVICES"></span>WCF-Dienste
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="HTTP_Activation"></span><span id="http_activation"></span><span id="HTTP_ACTIVATION"></span>HTTP-Aktivierung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Message_Queuing__MSMQ__Activation"></span><span id="message_queuing__msmq__activation"></span><span id="MESSAGE_QUEUING__MSMQ__ACTIVATION"></span>aktivierung von Message Queuing (MSMQ)
</dt> <dd></dd> <dt>

<span id="Named_Pipe_Activation"></span><span id="named_pipe_activation"></span><span id="NAMED_PIPE_ACTIVATION"></span>Named Pipe-Aktivierung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="TCP_Activation"></span><span id="tcp_activation"></span><span id="TCP_ACTIVATION"></span>TCP-Aktivierung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="TCP_Port_Sharing"></span><span id="tcp_port_sharing"></span><span id="TCP_PORT_SHARING"></span>TCP-Portfreigabe
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="ASP.NET_4.5"></span><span id="asp.net_4.5"></span>ASP.NET 4.5
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id=".NET_Extensibility_4.5"></span><span id=".net_extensibility_4.5"></span><span id=".NET_EXTENSIBILITY_4.5"></span>.NET-Erweiterbarkeit 4.5
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="DirectAccess_and_VPN__RAS_"></span><span id="directaccess_and_vpn__ras_"></span><span id="DIRECTACCESS_AND_VPN__RAS_"></span>DirectAccess und VPN (RAS)
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Routing"></span><span id="routing"></span><span id="ROUTING"></span>Routing
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Storage_Services"></span><span id="storage_services"></span><span id="STORAGE_SERVICES"></span>Storage Dienstleistungen
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Failover_Cluster_Management_Tools"></span><span id="failover_cluster_management_tools"></span><span id="FAILOVER_CLUSTER_MANAGEMENT_TOOLS"></span>Failoverclusterverwaltungstools
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Active_Directory_Rights_Management_Services_Tools"></span><span id="active_directory_rights_management_services_tools"></span><span id="ACTIVE_DIRECTORY_RIGHTS_MANAGEMENT_SERVICES_TOOLS"></span>Active Directory Rights Management Services Werkzeuge
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Application_Initialization"></span><span id="application_initialization"></span><span id="APPLICATION_INITIALIZATION"></span>Anwendungsinitialisierung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Centralized_SSL_Certificate_Support"></span><span id="centralized_ssl_certificate_support"></span><span id="CENTRALIZED_SSL_CERTIFICATE_SUPPORT"></span>Zentralisierte SSL-Zertifikatunterstützung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Claims-aware_Agent"></span><span id="claims-aware_agent"></span><span id="CLAIMS-AWARE_AGENT"></span>Ansprüche fähigen Agent
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools"></span><span id="remote_desktop_session_host_tools"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS"></span>Remotedesktop-Sitzungshost Tools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="WebSocket_Protocol"></span><span id="websocket_protocol"></span><span id="WEBSOCKET_PROTOCOL"></span>WebSocket-Protokoll
</dt> <dd>

wird nicht mehr unterstützt.

</dd> <dt>

<span id="COM__Network_Access"></span><span id="com__network_access"></span><span id="COM__NETWORK_ACCESS"></span>COM+-Netzwerkzugriff
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="File_and_iSCSI_Services_name_change"></span><span id="file_and_iscsi_services_name_change"></span><span id="FILE_AND_ISCSI_SERVICES_NAME_CHANGE"></span>Änderung des Datei- und iSCSI-Dienstnamens
</dt> <dd>

In Dateidienste geändert

</dd> </dl>

### <a name="windows-server-2012"></a>Windows Server 2012

<dl> <dt>

<span id="User_Interfaces_and_Infrastructure"></span><span id="user_interfaces_and_infrastructure"></span><span id="USER_INTERFACES_AND_INFRASTRUCTURE"></span>Benutzeroberflächen und Infrastruktur
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Server_for_NFS"></span><span id="server_for_nfs"></span><span id="SERVER_FOR_NFS"></span>Server für NFS
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="File_Server_VSS_Agent_Service"></span><span id="file_server_vss_agent_service"></span><span id="FILE_SERVER_VSS_AGENT_SERVICE"></span>Dateiserver-VSS-Agent-Dienst
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>iSCSI-Zielserver
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Data_Deduplication"></span><span id="data_deduplication"></span><span id="DATA_DEDUPLICATION"></span>Datendeduplizierung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Arbeitsordner
</dt> <dd>

Entfernt

</dd> <dt>

<span id="Core_Services"></span><span id="core_services"></span><span id="CORE_SERVICES"></span>Kerndienste
</dt> <dd>

Nur für diese Version hinzugefügt.

</dd> <dt>

<span id="Remote_Desktop_Virtual_Graphics"></span><span id="remote_desktop_virtual_graphics"></span><span id="REMOTE_DESKTOP_VIRTUAL_GRAPHICS"></span>Remotedesktop Virtuelle Grafiken
</dt> <dd>

Nur für diese Version hinzugefügt

</dd> <dt>

<span id="Remote_Access"></span><span id="remote_access"></span><span id="REMOTE_ACCESS"></span>Ras
</dt> <dd>

hinzugefügt

</dd> </dl>

### <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

<dl> <dt>

<span id="UDDI_Services"></span><span id="uddi_services"></span><span id="UDDI_SERVICES"></span>UDDI-Dienste
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_System_Resource_Manager"></span><span id="windows_system_resource_manager"></span><span id="WINDOWS_SYSTEM_RESOURCE_MANAGER"></span>Windows System Resource Manager
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Removable_Storage_Manager"></span><span id="removable_storage_manager"></span><span id="REMOVABLE_STORAGE_MANAGER"></span>Wechseldatenträger Storage-Manager
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Windows_PowerShell"></span><span id="windows_powershell"></span><span id="WINDOWS_POWERSHELL"></span>Windows PowerShell
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Ink_and_Handwriting_Services"></span><span id="ink_and_handwriting_services"></span><span id="INK_AND_HANDWRITING_SERVICES"></span>Freihand- und Handschriftdienste
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WinRM_IIS_Extension"></span><span id="winrm_iis_extension"></span><span id="WINRM_IIS_EXTENSION"></span>WinRM IIS-Erweiterung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="DirectAccess_Management_Console"></span><span id="directaccess_management_console"></span><span id="DIRECTACCESS_MANAGEMENT_CONSOLE"></span>DirectAccess-Verwaltungskonsole
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Background_Intelligent_Transfer_Service__BITS_"></span><span id="background_intelligent_transfer_service__bits_"></span><span id="BACKGROUND_INTELLIGENT_TRANSFER_SERVICE__BITS_"></span>Background Intelligent Transfer Service (BITS)
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="XPS_Viewer"></span><span id="xps_viewer"></span><span id="XPS_VIEWER"></span>XPS Viewer
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_Biometric_Framework"></span><span id="windows_biometric_framework"></span><span id="WINDOWS_BIOMETRIC_FRAMEWORK"></span>Windows Biometrisches Framework
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64_Support"></span><span id="wow64_support"></span><span id="WOW64_SUPPORT"></span>WoW64-Unterstützung
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Windows_PowerShell_Integrated_Scripting_Environment__ISE_"></span><span id="windows_powershell_integrated_scripting_environment__ise_"></span><span id="WINDOWS_POWERSHELL_INTEGRATED_SCRIPTING_ENVIRONMENT__ISE_"></span>Windows PowerShell Integrated Scripting Environment (ISE)
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="File_Replication_Service"></span><span id="file_replication_service"></span><span id="FILE_REPLICATION_SERVICE"></span>Dateireplikationsdienst
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="BranchCache_for_Network_Files"></span><span id="branchcache_for_network_files"></span><span id="BRANCHCACHE_FOR_NETWORK_FILES"></span>BranchCache für Netzwerkdateien
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>Arbeitsordner
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Distributed_Scan_Server"></span><span id="distributed_scan_server"></span><span id="DISTRIBUTED_SCAN_SERVER"></span>Server für verteilte Scanvorgänge
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="FTP_Publishing_Service"></span><span id="ftp_publishing_service"></span><span id="FTP_PUBLISHING_SERVICE"></span>FTP-Veröffentlichungsdienst
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="FTP_Management_Console"></span><span id="ftp_management_console"></span><span id="FTP_MANAGEMENT_CONSOLE"></span>FTP-Verwaltungskonsole
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="FTP_Service"></span><span id="ftp_service"></span><span id="FTP_SERVICE"></span>FTP-Dienst
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="FTP_Extensibility"></span><span id="ftp_extensibility"></span><span id="FTP_EXTENSIBILITY"></span>FTP-Erweiterbarkeit
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="IIS_Hostable_Web_Core"></span><span id="iis_hostable_web_core"></span><span id="IIS_HOSTABLE_WEB_CORE"></span>Hostfähiger IIS-Webkern
</dt> <dd></dd> <dt>

<span id="Windows_2000_Client_Support"></span><span id="windows_2000_client_support"></span><span id="WINDOWS_2000_CLIENT_SUPPORT"></span>Windows 2000-Clientunterstützung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Certificate_Enrollment_Web_Service"></span><span id="certificate_enrollment_web_service"></span><span id="CERTIFICATE_ENROLLMENT_WEB_SERVICE"></span>Zertifikatregistrierungs-Webdienst
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Certificate_Enrollment_Policy_Web_Service"></span><span id="certificate_enrollment_policy_web_service"></span><span id="CERTIFICATE_ENROLLMENT_POLICY_WEB_SERVICE"></span>Zertifikatregistrierungsrichtlinien-Webdienst
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="UDDI_Services_Web_Application"></span><span id="uddi_services_web_application"></span><span id="UDDI_SERVICES_WEB_APPLICATION"></span>UDDI Services-Webanwendung
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="UDDI_Services_Database"></span><span id="uddi_services_database"></span><span id="UDDI_SERVICES_DATABASE"></span>UDDI Services-Datenbank
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="Application_Server_Extensions_for_.NET_4.0"></span><span id="application_server_extensions_for_.net_4.0"></span><span id="APPLICATION_SERVER_EXTENSIONS_FOR_.NET_4.0"></span>Anwendungsservererweiterungen für .NET 4.0
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="UDDI_Services_Tools"></span><span id="uddi_services_tools"></span><span id="UDDI_SERVICES_TOOLS"></span>UDDI-Diensttools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="BitLocker_Drive_Encryption_Administration_Utilities"></span><span id="bitlocker_drive_encryption_administration_utilities"></span><span id="BITLOCKER_DRIVE_ENCRYPTION_ADMINISTRATION_UTILITIES"></span>BitLocker-Laufwerkverschlüsselung-Verwaltungsprogramme
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS und AD LDS Tools
</dt> <dd>

Nicht mehr unterstützt

</dd> <dt>

<span id="AD_DS_and_AD_LDS_Tools"></span><span id="ad_ds_and_ad_lds_tools"></span><span id="AD_DS_AND_AD_LDS_TOOLS"></span>AD DS und AD LDS Tools
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Active_Directory_Administrative_Center"></span><span id="active_directory_administrative_center"></span><span id="ACTIVE_DIRECTORY_ADMINISTRATIVE_CENTER"></span>Active Directory-Verwaltungscenter
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Active_Directory_module_for___________Windows_PowerShell"></span><span id="active_directory_module_for___________windows_powershell"></span><span id="ACTIVE_DIRECTORY_MODULE_FOR___________WINDOWS_POWERSHELL"></span>Active Directory-Modul für Windows PowerShell
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_Tools"></span><span id="remote_desktop_connection_broker_tools"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_TOOLS"></span>Remotedesktopverbindung Broker-Tools
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64"></span><span id="wow64"></span><span id="WOW64"></span>WoW64
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0_and_Windows_PowerShell"></span><span id="wow64_for_.net_framework_2.0_and_windows_powershell"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0_AND_WINDOWS_POWERSHELL"></span>WoW64 für .NET Framework 2.0 und Windows PowerShell
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64_for_.NET_Framework_2.0"></span><span id="wow64_for_.net_framework_2.0"></span><span id="WOW64_FOR_.NET_FRAMEWORK_2.0"></span>WoW64 für .NET Framework 2.0
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64_for___________"></span><span id="wow64_for___________"></span><span id="WOW64_FOR___________"></span>WoW64 für PowerShell
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64_for_.NET_Framework_3.0_and_3.5"></span><span id="wow64_for_.net_framework_3.0_and_3.5"></span><span id="WOW64_FOR_.NET_FRAMEWORK_3.0_AND_3.5"></span>WoW64 für .NET Framework 3.0 und 3.5
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64_for_Print_Services"></span><span id="wow64_for_print_services"></span><span id="WOW64_FOR_PRINT_SERVICES"></span>WoW64 für Druckdienste
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64_for_Failover_Clustering"></span><span id="wow64_for_failover_clustering"></span><span id="WOW64_FOR_FAILOVER_CLUSTERING"></span>WoW64 für Failoverclustering
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64_for_Input_Method_Editor"></span><span id="wow64_for_input_method_editor"></span><span id="WOW64_FOR_INPUT_METHOD_EDITOR"></span>WoW64 für den Eingabemethode-Editor
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="WoW64_for_Subsystem_for_UNIX-based_Applications"></span><span id="wow64_for_subsystem_for_unix-based_applications"></span><span id="WOW64_FOR_SUBSYSTEM_FOR_UNIX-BASED_APPLICATIONS"></span>WoW64 für Subsystem für UNIX-basierte Anwendungen
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="BitLocker_Recovery_Password_Viewer"></span><span id="bitlocker_recovery_password_viewer"></span><span id="BITLOCKER_RECOVERY_PASSWORD_VIEWER"></span>BitLocker-Wiederherstellungskennwort-Viewer
</dt> <dd>

hinzugefügt

</dd> <dt>

<span id="Print_and_Document_Services_name_change"></span><span id="print_and_document_services_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_NAME_CHANGE"></span>Druck- und Dokumentdienste Namensänderung
</dt> <dd>

benannten Druckdienste für diese Version

</dd> <dt>

<span id="Remote_Desktop_Services_name_change"></span><span id="remote_desktop_services_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_NAME_CHANGE"></span>Remotedesktopdienste namensänderung
</dt> <dd>

benannte Terminaldienste in dieser Version

</dd> <dt>

<span id=".NET_Framework_3.5.1_Features_name_change"></span><span id=".net_framework_3.5.1_features_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_FEATURES_NAME_CHANGE"></span>.NET Framework 3.5.1 Änderung des Namens von Features
</dt> <dd>

Benannte .NET Framework 3.0-Features in dieser Version

</dd> <dt>

<span id="Remote_Desktop_Session_Host_name_change"></span><span id="remote_desktop_session_host_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_NAME_CHANGE"></span>Remotedesktop-Sitzungshost namensänderung
</dt> <dd>

Benannter Terminalserver in dieser Version

</dd> <dt>

<span id="Remote_Desktop_Licensing_name_change"></span><span id="remote_desktop_licensing_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_NAME_CHANGE"></span>Remotedesktop Namensänderung der Lizenzierung
</dt> <dd>

Benannte TS-Lizenzierung in dieser Version

</dd> <dt>

<span id="Remote_Desktop_Gateway_name_change"></span><span id="remote_desktop_gateway_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_NAME_CHANGE"></span>Remotedesktop gateway name change (Ändern des Gatewaynamens)
</dt> <dd>

Benanntes TS Gateway in dieser Version

</dd> <dt>

<span id="Remote_Desktop_Connection_Broker_name_change"></span><span id="remote_desktop_connection_broker_name_change"></span><span id="REMOTE_DESKTOP_CONNECTION_BROKER_NAME_CHANGE"></span>Remotedesktopverbindung broker name change
</dt> <dd>

Benannter TS-Sitzungsbroker in dieser Version

</dd> <dt>

<span id="Remote_Desktop_Web_Access_name_change"></span><span id="remote_desktop_web_access_name_change"></span><span id="REMOTE_DESKTOP_WEB_ACCESS_NAME_CHANGE"></span>Remotedesktop Webzugriff Namensänderung
</dt> <dd>

Benannte TS Webzugriff in dieser Version

</dd> <dt>

<span id=".NET_Framework_3.5.1_name_change"></span><span id=".net_framework_3.5.1_name_change"></span><span id=".NET_FRAMEWORK_3.5.1_NAME_CHANGE"></span>.NET Framework 3.5.1-Namensänderung
</dt> <dd>

(220) Benannte Net FX 3.0-Features in dieser Version

(230) Named Application Server Core in diesem Release

</dd> <dt>

<span id="AD_DS_Tools_name_change"></span><span id="ad_ds_tools_name_change"></span><span id="AD_DS_TOOLS_NAME_CHANGE"></span>AD DS Namensänderung der Tools
</dt> <dd>

Named Active Directory Domain Services Tools in dieser Version

</dd> <dt>

<span id="AD_LDS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_lds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_LDS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD LDS Snap-Ins und Command-Line Tools ändern sich
</dt> <dd>

Named Active Directory Lightweight Directory Services Tools in dieser Version

</dd> <dt>

<span id="Print_and_Document_Services_Tools_name_change"></span><span id="print_and_document_services_tools_name_change"></span><span id="PRINT_AND_DOCUMENT_SERVICES_TOOLS_NAME_CHANGE"></span>Druck- und Dokumentdienste Namensänderung der Tools
</dt> <dd>

Benannte Druckdiensttools in dieser Version

</dd> <dt>

<span id="Remote_Desktop_Services_Tools_name_change"></span><span id="remote_desktop_services_tools_name_change"></span><span id="REMOTE_DESKTOP_SERVICES_TOOLS_NAME_CHANGE"></span>Remotedesktopdienste Namensänderung der Tools
</dt> <dd>

Benannte Terminaldienstetools in dieser Version

</dd> <dt>

<span id="Remote_Desktop_Session_Host_Tools_name_change"></span><span id="remote_desktop_session_host_tools_name_change"></span><span id="REMOTE_DESKTOP_SESSION_HOST_TOOLS_NAME_CHANGE"></span>Remotedesktop-Sitzungshost Namensänderung der Tools
</dt> <dd>

Benannte Terminalservertools in dieser Version

</dd> <dt>

<span id="Remote_Desktop_Gateway_Tools_name_change"></span><span id="remote_desktop_gateway_tools_name_change"></span><span id="REMOTE_DESKTOP_GATEWAY_TOOLS_NAME_CHANGE"></span>Remotedesktop des Namens der Gatewaytools
</dt> <dd>

Benannte TS-Gatewaytools in dieser Version

</dd> <dt>

<span id="Remote_Desktop_Licensing_Tools_name_change"></span><span id="remote_desktop_licensing_tools_name_change"></span><span id="REMOTE_DESKTOP_LICENSING_TOOLS_NAME_CHANGE"></span>Remotedesktop Namensänderung der Lizenzierungstools
</dt> <dd>

Benannte TS-Lizenzierungstools in dieser Version

</dd> <dt>

<span id="AD_DS_Snap-Ins_and_Command-Line_Tools_name_change"></span><span id="ad_ds_snap-ins_and_command-line_tools_name_change"></span><span id="AD_DS_SNAP-INS_AND_COMMAND-LINE_TOOLS_NAME_CHANGE"></span>AD DS Snap-Ins und Command-Line-Tools
</dt> <dd>

Active Directory-Domänencontroller-Tools

</dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Skript zeigt die Namen aller Serverfunktionen auf dem Computer mit dem Namen "FABRIKAM" an. Beachten Sie, dass auf dem Zielcomputer Windows Serverbetriebssystem 2008 oder höher ausgeführt werden muss.


```VB
strComputer = "FABRIKAM"

Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")

Set colFeatureList = objWMIService.ExecQuery("SELECT Name FROM Win32_ServerFeature")

For Each objFeature In colFeatureList
   WScript.Echo objFeature.Name

Next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>ServerCompProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ServerCompProv.dll</dt> </dl> |



 

