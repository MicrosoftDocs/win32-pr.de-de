---
title: Ereignisablaufverfolgung in ADSI
description: Unter Windows Server 2008 und Windows Vista wird die Ereignisablaufverfolgung in Active Directory Service Interfaces (ADSI) eingeführt.
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- Ereignisablaufverfolgung ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b26aee00404f5cf97d228698f64fec804c28e62
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423711"
---
# <a name="event-tracing-in-adsi"></a>Ereignisablaufverfolgung in ADSI

Unter Windows Server 2008 und Windows Vista wird die [Ereignisablaufverfolgung](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI) eingeführt. Bestimmte Bereiche des ADSI LDAP-Anbieters verfügen über eine zugrunde liegende Implementierung, die komplex ist oder eine Abfolge von Schritten umfasst, die die Diagnose von Problemen erschwert. Um Anwendungsentwickler bei der Problembehandlung zu unterstützen, wurde die Ereignisablaufverfolgung zu den folgenden Bereichen hinzugefügt:

## <a name="schema-parsing-and-downloading"></a>Schema analysieren und herunterladen

Die IADs-Schnittstelle in ADSI erfordert, dass das LDAP-Schema auf dem Client zwischengespeichert wird, damit Attribute ordnungsgemäß gemarshallt werden können (wie im [ADSI-Schemamodell](adsi-schema-model.md)beschrieben). Um dies zu erreichen, lädt ADSI das Schema für jeden Prozess (und für jeden LDAP-Server/jede LDAP-Domäne) entweder aus einer Schemadatei (SCH), die auf dem lokalen Datenträger gespeichert ist, oder durch Herunterladen vom LDAP-Server in den Arbeitsspeicher. Verschiedene Prozesse auf demselben Clientcomputer verwenden das zwischengespeicherte Schema auf dem Datenträger, wenn es verfügbar und anwendbar ist.

Wenn das Schema nicht vom Datenträger oder Server abgerufen werden kann, verwendet ADSI ein hartcodiertes Standardschema. In diesem Fall können Attribute, die nicht Teil dieses Standardschemas sind, nicht gemarshallt werden, und ADSI gibt beim Abrufen dieser Attribute einen Fehler zurück. Dies kann durch eine Reihe von Faktoren verursacht werden, z. B. Probleme beim Analysieren des Schemas und unzureichende Berechtigungen zum Herunterladen des Schemas. Es ist oft schwierig zu bestimmen, warum ein bestimmtes Standardschema verwendet wird. Die Verwendung der Ereignisablaufverfolgung in diesem Bereich hilft, das Problem schneller zu diagnostizieren und zu beheben.

## <a name="changing-and-setting-the-password"></a>Ändern und Festlegen des Kennworts

[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) und [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) verwenden mehrere Mechanismen, um den angeforderten Vorgang basierend auf der verfügbaren Konfiguration auszuführen (wie unter [Festlegen und Ändern von Benutzerpasswörtern mit dem LDAP-Anbieter](setting-user-passwords-for-ldap-providers.md)beschrieben). Wenn **ChangePassword und** **SetPassword** fehlschlagen, kann es schwierig sein, genau den Grund zu ermitteln, und die Ereignisablaufverfolgung hilft bei der Behandlung von Problemen mit diesen Methoden.

## <a name="adsi-bind-cache"></a>ADSI-Bindungscache

ADSI versucht intern, LDAP-Verbindungen nach Möglichkeit wiederzuverwenden (siehe [Verbindungszwischenspeicherung](connection-caching.md)). Bei der Problembehandlung ist es hilfreich zu verfolgen, ob eine neue Verbindung für die Kommunikation mit dem Server geöffnet wurde oder ob eine vorhandene Verbindung verwendet wurde. Es kann auch nützlich sein, den Lebenszyklus des Verbindungscaches (manchmal auch als Bindungscache bezeichnet) und dessen Erstellung oder Abschluss zu verfolgen und zu überprüfen, ob eine Verbindungsempfehlung stattgefunden hat. Bei einer serverlosen Bindung ruft ADSI den DC-Locator [auf,](/windows/desktop/AD/serverless-binding-and-rootdse)um einen Server für die Domäne des Kontexts des Benutzers auszuwählen. ADSI verwaltet dann einen Cache der Domänenserverzuordnung für nachfolgende Verbindungen. Die Ereignisablaufverfolgung hilft bei der Nachverfolgung der Auswahl des Domänencontrollers und ist daher hilfreich bei der Behandlung von verbindungsbezogenen Problemen.

## <a name="enabling-tracing-and-starting-a-tracing-session"></a>Aktivieren der Ablaufverfolgung und Starten einer Ablaufverfolgungssitzung

Um die ADSI-Ablaufverfolgung zu aktivieren, erstellen Sie den folgenden Registrierungsschlüssel:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **_ProcessName_**

*ProcessName* ist der vollständige Name des Prozesses, den Sie verfolgen möchten, einschließlich der Erweiterung (z. B. "Svchost.exe"). Darüber hinaus können Sie einen optionalen Wert vom Typ **DWORD** mit dem Namen PID in diesen Schlüssel platzieren. Es wird dringend empfohlen, diesen Wert zu setzen und dadurch nur einen bestimmten Prozess zu verfolgen. Andernfalls werden alle Durch *ProcessName* angegebenen Instanzen der Anwendung nachverfolgt.

Führen Sie dann den folgenden Befehl aus:

**tracelog.exe -start** *sessionname* **-guid \#** provider _\_ guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*

*sessionname* ist einfach ein beliebiger Bezeichner, der zum Bezeichnen der Ablaufverfolgungssitzung verwendet wird (Sie müssen später auf diesen Sitzungsnamen verweisen, wenn Sie die Ablaufverfolgungssitzung beenden). Die GUID für den ADSI-Nachverfolgungsanbieter lautet "7288c9f8-d63c-4932-a345-89d6b060174d". *filename* gibt die Protokolldatei an, in die Ereignisse geschrieben werden. *traceFlags* sollte einer der folgenden Werte sein:



|         Flag                        |         Wert              |
|---------------------------------|-----------------------|
| **\_DEBUGSCHEMA**<br/>    | 0x00000001<br/> |
| **DEBUGGEN \_ VON CHANGEPWD**<br/> | 0x00000002<br/> |
| **DEBUGGEN \_ VON SETPWD**<br/>    | 0x00000004<br/> |
| **DEBUGGEN \_ VON BINDCACHE**<br/> | 0x00000008<br/> |



 

Diese Flags bestimmen gemäß der folgenden Tabelle, welche [ADSI-Methoden](active-directory-service-interfaces-adsi.md) nachverfolgt werden:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>DEBUG_SCHEMA</strong><br/></td>
<td><ul>
<li>LdapGetSchema</li>
<li>GetSchemaInfoTime</li>
<li>LdapReadSchemaInfoFromServer</li>
<li>ProcessSchemaInfo</li>
<li>HelperReadLdapSchemaInfo</li>
<li>ProcessClassInfoArray</li>
<li>ReadSchemaInfoFromRegistry</li>
<li>StoreSchemaInfoFromRegistry</li>
<li>AttributeTypeDescription</li>
<li>ObjectClassDescription</li>
<li>DITContentRuleDescription</li>
<li>DirectoryString</li>
<li>DirectoryStrings</li>
<li>DITContentRuleDescription</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_CHANGEPWD</strong><br/></td>
<td><ul>
<li>CADsUser::ChangePassword</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><strong>DEBUG_SETPWD</strong><br/></td>
<td><ul>
<li>CADsUser::SetPassword</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_BINDCACHE</strong><br/></td>
<td><ul>
<li>GetServerBasedObject</li>
<li>GetServerLessBasedObject</li>
<li>GetGCDomainName</li>
<li>GetDefaultDomainName</li>
<li>GetUserDomainFlatName</li>
<li>BindCacheLookup</li>
<li>EquivalentPortNumbers</li>
<li>CanCredentialsBeReused</li>
<li>BindCacheAdd</li>
<li>BindCacheAddRef</li>
<li>AddReferralLink</li>
<li>CommonRemoveEntry</li>
<li>BindCacheDerefHelper</li>
<li>NotifyNewConnection</li>
<li>QueryForConnection</li>
<li>LdapOpenBindWithCredentials</li>
<li>LdapOpenBindWithDefaultCredentials</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

Sie können Flags kombinieren, indem Sie die entsprechenden Bits im *traceFlags-Argument* kombinieren. Um beispielsweise die **FLAGS DEBUG \_ SCHEMA** und **DEBUG \_ BINDCACHE** anzugeben, wird der entsprechende *traceFlags-Wert* 0x00000009.

Schließlich sollte das *flag traceLevel* einen der folgenden Werte aufweisen:



|      Flag                                    |       Wert                |
|------------------------------------------|-----------------------|
| **\_FEHLER AUF ABLAUFVERFOLGUNGSEBENE \_**<br/>       | 0x00000002<br/> |
| **\_INFORMATIONEN AUF ABLAUFVERFOLGUNGSEBENE \_**<br/> | 0x00000004<br/> |



 

**TRACE \_ LEVEL \_ INFORMATION** bewirkt, dass der Ablaufverfolgungsprozess alle Ereignisse aufzeichnet, während **TRACE LEVEL \_ \_ ERROR** bewirkt, dass der Ablaufverfolgungsprozess nur Fehlerereignisse aufzeichnet.

Führen Sie den folgenden Befehl aus, um die Ablaufverfolgung zu beenden:

**tracelog.exe -stop** *sessionname*

Im vorherigen Beispiel ist *sessionname* derselbe Name wie der, der mit dem Befehl bereitgestellt wurde, der den Ablaufverfolgungsabschnitt gestartet hat.

## <a name="remarks"></a>Hinweise

Es ist effektiver, nur bestimmte Prozesse durch Angabe einer bestimmten PID nachzuverfolgen, als alle Prozesse auf einem Computer nachzuverfolgen. Wenn Sie mehrere Anwendungen auf demselben Computer nachverfolgen müssen, kann dies auswirkungen auf die Leistung haben. in leistungsorientierten Abschnitten des Codes gibt es umfangreiche Debugausgaben. Außerdem müssen Administratoren darauf achten, die Berechtigungen der Protokolldateien bei der Ablaufverfolgung mehrerer Prozesse ordnungsgemäß festzulegen. Andernfalls kann jeder Benutzer die Ablaufverfolgungsprotokolle lesen, und andere Benutzer können Prozesse nachverfolgen, die sichere Informationen enthalten.

Angenommen, der Administrator richtet die Ablaufverfolgung für eine Anwendung "Test.exe" ein und gibt keine PID in der Registrierung an, um mehrere Instanzen des Prozesses zu verfolgen. Nun möchte ein anderer Benutzer die Anwendung "Secure.exe" verfolgen. Wenn die Ablaufverfolgungsprotokolldateien nicht ordnungsgemäß eingeschränkt sind, muss der Benutzer nur "Secure.exe" in "Test.exe" umbenennen, und er wird nachverfolgt. Im Allgemeinen ist es am besten, bei der Problembehandlung nur bestimmte Prozesse zu verfolgen und den Registrierungsschlüssel für die Ablaufverfolgung zu entfernen, sobald die Problembehandlung durchgeführt wurde.

Da die Aktivierung der Ereignisablaufverfolgung zusätzliche Protokolldateien erzeugt, sollten Administratoren die Protokolldateigrößen sorgfältig überwachen. Fehlender Speicherplatz auf dem lokalen Computer kann zu einem Denial-of-Service-Angriff führen.

## <a name="example-scenarios"></a>Beispielszenarien

Szenario 1: Der Administrator sieht einen unerwarteten Fehler in einer Anwendung, die Kennwörter für Benutzerkonten festgelegt, sodass er die folgenden Schritte ausführen würde, um das Problem mithilfe der Ereignisablaufverfolgung zu beheben.

1.  Schreiben Sie ein Skript, das das Problem reproduziert, und erstellen Sie den Registrierungsschlüssel.

    **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**

2.  Starten Sie mithilfe des folgenden Befehls eine Ablaufverfolgungssitzung, indem Sie *traceFlags* auf 0x2 (**DEBUG \_ CHANGEPASSWD**) und *traceLevel* auf 0x4 (**TRACE LEVEL \_ \_ INFORMATION)** festlegen:

    **tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**

3.  Führen cscript.exe Testskript aus, um das Problem zu reproduzieren, und beenden Sie dann die Ablaufverfolgungssitzung:

    **tracelog.exe -stop scripttrace**

4.  Löschen des Registrierungsschlüssels

    **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**

5.  Führen Sie das ETW-Tool Tracerpt.exe, um die Ablaufverfolgungsinformationen aus dem Protokoll zu analysieren:

    **tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**

Szenario 2: Der Administrator möchte die Schemaparsing- und Downloadvorgänge in einer [ASP-Anwendung](https://msdn.microsoft.com/asp.net/default.aspx) mit dem Namen w3wp.exe, die bereits ausgeführt wird, nachverfolgen. Dazu würde der Administrator die folgenden Schritte ausführen:

1.  Erstellen des Registrierungsschlüssels

    **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**

    erstellen Sie in diesem Schlüssel einen Wert vom Typ DWORD mit dem Namen PID, und legen Sie ihn auf die Prozess-ID der Instanz von w3wp.exe fest, die derzeit auf dem lokalen Computer ausgeführt wird.

2.  Anschließend erstellen sie eine Ablaufverfolgungssitzung und legen *traceFlags* auf 0x1 (**DEBUG \_ SCHEMA**) und *traceLevel* auf 0x4 (**TRACE LEVEL \_ \_ INFORMATION**) fest:

    **tracelog.exe -start w3wptrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ w3wp.etl -flag 0x1 -level 0x4**

3.  Reproduzieren Sie den Vorgang, für den eine Problembehandlung erforderlich ist.
4.  Beenden Sie die Ablaufverfolgungssitzung:

    **tracelog.exe -stop w3wptrace**

5.  Löschen Sie den Registrierungsschlüssel **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**.
6.  Führen Sie das ETW-Tool tracerpt.exe aus, um die Ablaufverfolgungsinformationen aus dem Protokoll zu analysieren:

    **tracerpt.exe . \\ w3wp.etl -o -report**

 

