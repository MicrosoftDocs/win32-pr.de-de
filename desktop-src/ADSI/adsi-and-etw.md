---
title: Ereignis Ablauf Verfolgung in ADSI
description: Windows Server 2008 und Windows Vista stellen die Ereignis Ablauf Verfolgung in Active Directory Service Interfaces (ADSI) vor.
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- Ereignis Ablauf Verfolgung ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f43c0d840cd1f3f70d293a0a4f5c299fd129efe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340734"
---
# <a name="event-tracing-in-adsi"></a>Ereignis Ablauf Verfolgung in ADSI

Windows Server 2008 und Windows Vista stellen die [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI) vor. Bestimmte Bereiche des ADSI LDAP-Anbieters haben eine zugrunde liegende Implementierung, die komplex ist oder eine Abfolge von Schritten umfasst, die das Diagnostizieren von Problemen erschwert. Zur Unterstützung der Problembehandlung für Anwendungsentwickler wurde die Ereignis Ablauf Verfolgung den folgenden Bereichen hinzugefügt:

## <a name="schema-parsing-and-downloading"></a>Schema-und Download

Die IADs-Schnittstelle in ADSI erfordert, dass das LDAP-Schema auf dem Client zwischengespeichert wird, damit Attribute ordnungsgemäß gemarshallt werden können (wie im [ADSI-Schema Modell](adsi-schema-model.md)beschrieben). Um dies zu erreichen, lädt ADSI das Schema für jeden Prozess (und für jeden LDAP-Server/jede LDAP-Domäne) entweder aus einer Schema Datei (. sch), die auf dem lokalen Datenträger gespeichert ist, oder durch Herunterladen vom LDAP-Server in den Arbeitsspeicher. Bei verschiedenen Prozessen auf dem gleichen Client Computer wird das zwischengespeicherte Schema auf dem Datenträger verwendet, wenn es verfügbar und anwendbar ist.

Wenn das Schema nicht vom Datenträger oder vom Server abgerufen werden kann, verwendet ADSI ein hart codiertes Standardschema. In diesem Fall können Attribute, die nicht Teil dieses Standard Schemas sind, nicht gemarshallt werden, und ADSI gibt beim Abrufen dieser Attribute einen Fehler zurück. Dies kann zu einer Reihe von Faktoren führen, einschließlich Problemen bei der Paket Ausführung und unzureichender Berechtigungen zum Herunterladen des Schemas. Es ist oft schwierig zu bestimmen, warum ein bestimmtes Standardschema verwendet wird. Die Verwendung der Ereignis Ablauf Verfolgung in diesem Bereich hilft, das Problem schneller zu diagnostizieren und zu beheben.

## <a name="changing-and-setting-the-password"></a>Ändern und Festlegen des Kennworts

[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) und [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) verwenden mehr als einen Mechanismus, um den angeforderten Vorgang basierend auf der verfügbaren Konfiguration auszuführen (wie unter [festlegen und Ändern von Benutzer Kennwörtern mit dem LDAP-Anbieter](setting-user-passwords-for-ldap-providers.md)beschrieben). Wenn **ChangePassword** und **SetPassword** ausfallen, kann es schwierig sein, genau zu bestimmen, warum und die Ereignis Ablauf Verfolgung bei der Behebung von Problemen mit diesen Methoden hilfreich ist.

## <a name="adsi-bind-cache"></a>ADSI-Bindungs Cache

ADSI versucht nach Möglichkeit intern, LDAP-Verbindungen wiederzuverwenden (siehe [Verbindungs Caching](connection-caching.md)). Bei der Problembehandlung ist es sinnvoll, zu verfolgen, ob eine neue Verbindung für die Kommunikation mit dem Server geöffnet wurde oder ob eine vorhandene Verbindung verwendet wurde. Dies kann auch hilfreich sein, um den Lebenszyklus des Verbindungs Caches (auch als Bindungs Cache bezeichnet) und die Erstellung oder Schließung zu verfolgen, und ob ein Verbindungs Verweis stattfindet. Bei einer Server [losen Bindung](/windows/desktop/AD/serverless-binding-and-rootdse)ruft ADSI den DC-Serverlocatorpunkt auf, um einen Server für die Domäne des Benutzer Kontexts auszuwählen. ADSI verwaltet dann einen Cache der Domänen Server Zuordnung für nachfolgende Verbindungen. Die Ereignis Ablauf Verfolgung hilft bei der Nachverfolgung der Auswahl des Domänen Controllers und ist daher bei der Behandlung von Verbindungs bezogenen Problemen hilfreich.

## <a name="enabling-tracing-and-starting-a-tracing-session"></a>Aktivieren der Ablauf Verfolgung und Starten einer Ablauf Verfolgungs Sitzung

Um die ADSI-Ablauf Verfolgung zu aktivieren, erstellen Sie den folgenden Registrierungsschlüssel:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ ***ProcessName***

*ProcessName* ist der vollständige Name des Prozesses, den Sie verfolgen möchten, einschließlich seiner Erweiterung (z. b. "Svchost.exe"). Außerdem können Sie in diesem Schlüssel einen optionalen Wert des Typs **DWORD** mit dem Namen PID platzieren. Es wird dringend empfohlen, diesen Wert festzulegen und damit nur einen bestimmten Prozess nachzuverfolgen. Andernfalls werden alle Instanzen der Anwendung, die von *ProcessName* angegeben werden, nachverfolgt.

Führen Sie dann den folgenden Befehl aus:

**tracelog.exe-Start** *Sessionname*  * *-GUID \# * * * Anbieter \_ GUID* **-f** *Dateiname* **-Flag** *TraceFlags* **-Level** *TraceLevel*

*Sessionname* ist einfach ein beliebiger Bezeichner, der zum bezeichnen der Ablauf Verfolgungs Sitzung verwendet wird (Sie müssen später auf diesen Sitzungs Namen verweisen, wenn Sie die Ablauf Verfolgungs Sitzung beenden). Die GUID für den ADSI-Überwachungs Anbieter lautet "7288c9f8-d63c-4932-A345-89d6b060174d". *filename* gibt die Protokolldatei an, in die Ereignisse geschrieben werden. *TraceFlags* muss einer der folgenden Werte sein:



|                                 |                       |
|---------------------------------|-----------------------|
| **Debug- \_ Schema**<br/>    | 0x00000001<br/> |
| **\_CHANGEPWD Debuggen**<br/> | 0x00000002<br/> |
| **Debuggen von \_ SetPwd**<br/>    | 0x00000004<br/> |
| **bindcache Debuggen \_**<br/> | 0x00000008<br/> |



 

Diese Flags bestimmen, welche [ADSI](active-directory-service-interfaces-adsi.md) -Methoden gemäß der folgenden Tabelle verfolgt werden:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>DEBUG_SCHEMA</strong><br/></td>
<td><ul>
<li>Ldapgetschema</li>
<li>Getschemainfotime</li>
<li>Ldapreadschemainfofromserver</li>
<li>Processschemainfo</li>
<li>Helperlesldapschemainfo</li>
<li>Processclassinfoarray</li>
<li>"Read schemainfofromregistry"</li>
<li>Storeschemainfofromregistry</li>
<li>Attributetypedescription</li>
<li>Objectclassdescription</li>
<li>Ditcontentruledescription</li>
<li>Directoriystring</li>
<li>Directoriystrings</li>
<li>Ditcontentruledescription</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_CHANGEPWD</strong><br/></td>
<td><ul>
<li>Cadsuser:: ChangePassword</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><strong>DEBUG_SETPWD</strong><br/></td>
<td><ul>
<li>Cadsuser:: SetPassword</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_BINDCACHE</strong><br/></td>
<td><ul>
<li>Getserverbasedobject</li>
<li>Getserverlessbasedobject</li>
<li>Getgcdomainname</li>
<li>GetDefaultDomain Name</li>
<li>Getuserdomainflatname</li>
<li>Bindcachelookup</li>
<li>Equivalentportnumbers</li>
<li>Cankredentialsbereused</li>
<li>Bindcacheadd</li>
<li>Bindcacheadressf</li>
<li>Adressferrallink</li>
<li>Commonremoveentry</li>
<li>Bindcachederefhelper</li>
<li>NotifyNewConnection</li>
<li>QueryForConnection</li>
<li>Ldapoprebindwithanmelde Informationen</li>
<li>Ldapoprebindwithdefaultanmeldeinformationen</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

Sie können Flags kombinieren, indem Sie die entsprechenden Bits im *TraceFlags* -Argument kombinieren. Um z. b. das **Debug- \_ Schema** und das **Debug- \_ bindcache** -Flags anzugeben, wäre der geeignete *TraceFlags* -Wert 0x00000009.

Schließlich sollte das *TraceLevel* -Flag einen der folgenden Werte aufweisen:



|                                          |                       |
|------------------------------------------|-----------------------|
| **Fehler auf Ablauf Verfolgungs \_ Ebene \_**<br/>       | 0x00000002<br/> |
| **Informationen der Ablauf Verfolgungs \_ Ebene \_**<br/> | 0x00000004<br/> |



 

Ablauf **Verfolgung \_ Die Ebene der \_ Informationen** bewirkt, dass der Ablauf Verfolgungs Prozess alle Ereignisse zeichnet, wohingegen der Ablauf Verfolgungs Prozess bewirkt, dass der Ablauf Verfolgungs Prozess nur Fehlerereignisse erfasst. **\_ \_**

Führen Sie den folgenden Befehl aus, um die Ablauf Verfolgung zu beenden:

**tracelog.exe-** " *Sessionname* " wird beendet.

Im vorherigen Beispiel ist *Sessionname* derselbe Name wie der, der mit dem Befehl bereitgestellt wurde, der den Abschnitt Ablauf Verfolgung gestartet hat.

## <a name="remarks"></a>Bemerkungen

Es ist effektiver, nur bestimmte Prozesse zu verfolgen, indem eine bestimmte PID angegeben wird, als alle Prozesse auf einem Computer zu verfolgen. Wenn Sie mehrere Anwendungen auf demselben Computer verfolgen müssen, wirkt sich dies möglicherweise auf die Leistung aus. Es gibt eine beträchtliche Debugausgabe in leistungsorientierten Abschnitten des Codes. Außerdem müssen Administratoren darauf achten, die Berechtigungen der Protokolldateien ordnungsgemäß festzulegen, wenn Sie mehrere Prozesse verfolgen. Andernfalls können alle Benutzer die Ablauf Verfolgungs Protokolle lesen, und andere Benutzer können Prozesse nachverfolgen, die sichere Informationen enthalten.

Nehmen Sie beispielsweise an, dass der Administrator die Ablauf Verfolgung für eine Anwendung "Test.exe" einrichtet und keine PID in der Registrierung angibt, um mehrere Instanzen des Prozesses zu verfolgen. Jetzt möchte ein anderer Benutzer die Anwendung "Secure.exe" verfolgen. Wenn die Ablauf Verfolgungs Protokolldateien nicht ordnungsgemäß eingeschränkt sind, muss der Benutzer nur "Secure.exe" in "Test.exe" umbenennen, und er wird nachverfolgt. Im Allgemeinen ist es am besten, bei der Problembehandlung nur bestimmte Prozesse zu verfolgen und den Registrierungsschlüssel für die Ablauf Verfolgung zu entfernen, sobald die Problembehandlung erfolgt ist.

Da durch Aktivieren der Ereignis Ablauf Verfolgung zusätzliche Protokolldateien erzeugt werden, sollten Administratoren die Protokolldatei Größen sorgfältig überwachen. fehlender Speicherplatz auf dem lokalen Computer kann zu einem Denial-of-Service-Angriff führen.

## <a name="example-scenarios"></a>Beispielszenarien

Szenario 1: dem Administrator wird ein unerwarteter Fehler in einer Anwendung angezeigt, mit der Kenn Wörter für Benutzerkonten festgelegt werden, sodass die folgenden Schritte ausgeführt werden, um das Problem mithilfe der Ereignis Ablauf Verfolgung zu beheben.

1.  Schreiben Sie ein Skript, das das Problem erneut erzeugt, und erstellen Sie den Registrierungsschlüssel.

    **HKEY \_ System für lokale \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **cscript.exe**

2.  Starten Sie eine Ablauf Verfolgungs Sitzung, und legen Sie *TraceFlags* auf 0x2 (**Debug \_ changepasswd**) und *TraceLevel* auf 0x4 (**\_ \_ Informationen** der Ablauf Verfolgungs Ebene) fest, indem Sie den folgenden Befehl verwenden:

    **tracelog.exe-Start scripttrace-GUID \# 7288c9o8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL-Flag 0x2-Ebene 0x4**

3.  Führen Sie cscript.exe mit dem zugehörigen Testskript aus, um das Problem zu reproduzieren, und beenden Sie dann die Ablauf Verfolgungs Sitzung:

    **Abbrechen von scripttracetracelog.exe**

4.  Registrierungsschlüssel löschen

    **HKEY \_ System für lokale \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **cscript.exe**

5.  Führen Sie das ETW-Tool Tracerpt.exe aus, um die Ablauf Verfolgungs Informationen aus dem Protokoll zu analysieren:

    **tracelog.exe-Start scripttrace-GUID \# 7288c9o8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL-Flag 0x2-Ebene 0x4**

Szenario 2: der Administrator möchte die Schema Analyse-und Download Vorgänge in einer [ASP](https://msdn.microsoft.com/asp.net/default.aspx) -Anwendung mit dem Namen w3wp.exe verfolgen, die bereits ausgeführt wird. Hierzu führt der Administrator die folgenden Schritte aus:

1.  Registrierungsschlüssel erstellen

    **HKEY \_ System für lokale \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**

    Erstellen Sie in diesem Schlüssel einen Wert vom Typ DWORD, der den Namen PID hat, und legen Sie ihn auf die Prozess-ID der Instanz von w3wp.exe fest, die derzeit auf dem lokalen Computer ausgeführt wird.

2.  Anschließend erstellen Sie eine Ablauf Verfolgungs Sitzung, indem Sie *TraceFlags* auf 0x1 (**\_ debugschema**) und *TraceLevel* auf 0x4 (**\_ \_ Informationen** der Ablauf Verfolgungs Ebene) festlegen:

    **tracelog.exe-Start w3wptrace-GUID \# 7288c9o8-d63c-4932-A345-89d6b060174d-f. \\ w3wp. ETL-Flag 0x1-Ebene 0x4**

3.  Reproduzieren Sie den Vorgang, der die Problembehandlung erfordert.
4.  Beenden Sie die Ablauf Verfolgungs Sitzung:

    **tracelog.exe w3wptrace**

5.  Löschen Sie den Registrierungsschlüssel **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**.
6.  Führen Sie das ETW-Tool tracerpt.exe aus, um die Ablauf Verfolgungs Informationen aus dem Protokoll zu analysieren:

    **tracerpt.exe. \\ w3wp. ETL-o-Report**

 

