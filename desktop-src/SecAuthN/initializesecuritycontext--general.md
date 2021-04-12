---
description: Initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informations handle.
ms.assetid: 21d965d4-3c03-4e29-a70d-4538c5c366b0
title: InitializeSecurityContext (General)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: bc96fe74202f1380d2d85946a373f176e14dfd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348078"
---
# <a name="initializesecuritycontext-general-function"></a>InitializeSecurityContext (allgemein)-Funktion

Die Funktion **InitializeSecurityContext (allgemein)** initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informationen-handle. Die-Funktion wird verwendet, um einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen der Client Anwendung und einem Remotepeer zu erstellen. **InitializeSecurityContext (allgemein)** gibt ein Token zurück, das der Client an den Remotepeer übergeben muss, den der Peer wiederum über den [**calltsecuritycontext (General)**](acceptsecuritycontext--general.md) -Befehl an die lokale Sicherheits Implementierung übermittelt. Das generierte Token sollte von allen Aufrufern als nicht transparent angesehen werden.

In der Regel wird die **InitializeSecurityContext (General)** -Funktion in einer Schleife aufgerufen, bis ein ausreichender [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wird.

Weitere Informationen zur Verwendung dieser Funktion mit einem bestimmten [*Security Support Provider*](../secgloss/s-gly.md) (SSP) finden Sie in den folgenden Themen.



| Thema                                                                                  | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSecurityContext (kredssp)**](initializesecuritycontext--credssp.md)     | Initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informations Handle mithilfe des [*Sicherheitspakets*](../secgloss/s-gly.md)für die Anmelde Informationen Security Support Provider (kredssp).  
| [**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)       | Initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informationen-Handle mithilfe des Digest- [*Sicherheitspakets*](../secgloss/s-gly.md).                        |
| [**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)   | Initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informations Handle mithilfe des Kerberos- [*Sicherheitspakets*](../secgloss/s-gly.md).                      |
| [**InitializeSecurityContext (aushandeln)**](initializesecuritycontext--negotiate.md) | Initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informations Handle mithilfe des Aushandlungs [*Sicherheitspakets*](../secgloss/s-gly.md).                     |
| [**InitializeSecurityContext (NTLM)**](initializesecuritycontext--ntlm.md)           | Initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informationen-Handle mithilfe des NTLM- [*Sicherheitspakets*](../secgloss/s-gly.md).                          |
| [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md)   | Initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informationen-Handle mithilfe des SChannel- [*Sicherheitspakets*](../secgloss/s-gly.md).                      |



 

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_Entry InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        ULONG          fContextReq,
  _In_        ULONG          Reserved1,
  _In_        ULONG          TargetDataRep,
  _In_opt_    PSecBufferDesc pInput,
  _In_        ULONG          Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Inout_opt_ PSecBufferDesc pOutput,
  _Out_       PULONG         pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phcredential* \[ in, optional\]
</dt> <dd>

Ein Handle für die Anmelde Informationen, die von [**AcquireCredentialsHandle (allgemein)**](acquirecredentialshandle--general.md)zurückgegeben werden. Dieses Handle wird zum Erstellen des [*Sicherheits Kontexts*](../secgloss/s-gly.md)verwendet. Die Funktion **InitializeSecurityContext (allgemein)** erfordert mindestens ausgehende Anmelde Informationen.

</dd> <dt>

*phcontext* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten Aufrufe von **InitializeSecurityContext (allgemein)** ist dieser Zeiger **null**. Beim zweiten-Befehl ist dieser Parameter ein Zeiger auf das Handle des partiell formatierten Kontexts, der durch den ersten-Befehl im *phnewcontext* -Parameter zurückgegeben wird.

Dieser Parameter ist mit dem Microsoft Digest SSP optional und kann auf **null** festgelegt werden.

Wenn Sie den Schannel-SSP verwenden, geben Sie bei der ersten **Initialisierung von InitializeSecurityContext (allgemein)** **null** an. Geben Sie bei zukünftigen aufrufen das Token an, das nach dem ersten Aufruf dieser Funktion im Parameter " *phnewcontext* " empfangen wurde.

</dd> <dt>

*ptargetname* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die das Ziel des Kontexts angibt. Der Inhalt der Zeichenfolge ist [*Sicherheitspaket*](../secgloss/s-gly.md) spezifisch, wie in der folgenden Tabelle beschrieben. Diese Liste ist nicht vollständig. Einem System können zusätzliche System-SSPs und SSPs von Drittanbietern hinzugefügt werden.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>SSP wird verwendet</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="Digest"></span><span id="digest"></span><span id="DIGEST"></span><dl> <dt><strong>Digest</strong></dt><dt></dt> </dl></td><td>Eine mit NULL beendete Zeichenfolge, die den URI der angeforderten Ressource eindeutig identifiziert. Die Zeichenfolge muss aus Zeichen bestehen, die in einem URI zulässig sind und vom US-ASCII-Codesatz darstellbar sein müssen. Prozent Codierung kann verwendet werden, um Zeichen außerhalb des US-ASCII-Codesatzes darzustellen.<br/></td></tr><tr class="even"><td><span id="Kerberos_or_Negotiate"></span><span id="kerberos_or_negotiate"></span><span id="KERBEROS_OR_NEGOTIATE"></span><dl> <dt><strong>Kerberos oder aushandeln</strong></dt><dt></dt> </dl></td><td>Dienst Prinzipal Name (Service Principal Name, SPN) oder der [*Sicherheitskontext*](../secgloss/s-gly.md) des Zielservers.<br/></td></tr><tr class="odd"><td><span id="NTLM"></span><span id="ntlm"></span><dl> <dt><strong>NTLM</strong></dt><dt></dt> </dl></td><td>Dienst Prinzipal Name (Service Principal Name, SPN) oder der [*Sicherheitskontext*](../secgloss/s-gly.md) des Zielservers.<br/></td></tr><tr class="even"><td><span id="Schannel_SSL"></span><span id="schannel_ssl"></span><span id="SCHANNEL_SSL"></span><dl> <dt><strong>SChannel/SSL</strong></dt><dt></dt> </dl></td><td>Eine mit NULL beendete Zeichenfolge, die den Zielserver eindeutig identifiziert. SChannel verwendet diesen Wert, um das Serverzertifikat zu überprüfen. SChannel verwendet diesen Wert auch, um die Sitzung im Sitzungs Cache zu finden, wenn eine Verbindung wieder hergestellt wird. Die zwischengespeicherte Sitzung wird nur verwendet, wenn alle der folgenden Bedingungen erfüllt sind:<ul><li>Der Zielname ist identisch.</li><li>Der Cache Eintrag ist nicht abgelaufen.</li><li>Der Anwendungsprozess, der die Funktion aufruft, ist identisch.</li><li>Die Anmelde Sitzung ist identisch.</li><li>Das Anmelde Informations Handle ist identisch.</li></ul><br/></td></tr></tbody></table>



 

</dd> <dt>

*"f"* \[ in\]
</dt> <dd>

Bitflags, die Anforderungen für den Kontext angeben. Nicht alle Pakete können alle Anforderungen unterstützen. Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC \_ req \_ , z \_ . b. ISC req-Delegat \_ . Dieser Parameter kann mindestens eines der folgenden Attributflags sein.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>Das [*Sicherheitspaket*](../secgloss/s-gly.md) weist Ihnen Ausgabepuffer zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie Sie frei, indem Sie die [<strong>freecontextbuffer</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-freecontextbuffer)-Funktion aufrufen.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Verschlüsseln Sie Nachrichten mithilfe der [<strong>verschlüsseltmessage</strong>] (EncryptMessage--General.MD)-Funktion.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungs Meldungen. Dieser Wert ist der Standardwert für die eingeschränkte Kerberos-, Aushandlungs-und NTLM- [*Delegierung*](../secgloss/s-gly.md).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt><strong>ISC_REQ_DELEGATE</strong></dt> </dl></td><td>Der Server kann den Kontext verwenden, um sich bei anderen Servern als Client zu authentifizieren. Das ISC_REQ_MUTUAL_AUTH-Flag muss festgelegt werden, damit dieses Flag funktioniert. Gültig für Kerberos. Dieses Flag für die [*eingeschränkte Delegierung*](../secgloss/c-gly.md)ignorieren.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Wenn Fehler auftreten, wird die Remote Partei benachrichtigt.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_HTTP"></span><span id="isc_req_http"></span><dl> <dt><strong>ISC_REQ_HTTP</strong></dt> </dl></td><td>Verwenden Sie Digest für http. Lassen Sie dieses Flag aus, um Digest als SASL-Mechanismus zu verwenden.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Signieren von Nachrichten und Überprüfen von Signaturen mithilfe der Funktionen [<strong>verschlüsseltmessage</strong>] (EncryptMessage--General.MD) und [<strong>makesignature</strong>] (makesignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt> </dl></td><td>SChannel darf den Server nicht automatisch authentifizieren.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Die Richtlinie für die gegenseitige Authentifizierung des Dienstanbieter wird erfüllt.<br/><blockquote>[!Caution]<br />
Dies bedeutet nicht notwendigerweise, dass die gegenseitige Authentifizierung durchgeführt wird, sondern nur, dass die Authentifizierungs Richtlinie des Dienstanbieter erfüllt ist. Um sicherzustellen, dass die gegenseitige Authentifizierung erfolgt, wenden Sie die [<strong>QueryContextAttributes (General)</strong>] (QueryContextAttributes--General.MD)-Funktion an.</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_NO_INTEGRITY"></span><span id="isc_req_no_integrity"></span><dl> <dt><strong>ISC_REQ_NO_INTEGRITY</strong></dt> </dl></td><td>Wenn dieses Flag festgelegt ist, wird das <strong>ISC_REQ_INTEGRITY</strong> -Flag ignoriert.<br/> Dieser Wert wird nur von der Aushandlungs-und der eingeschränkten Kerberos- [*Delegierung*](../secgloss/s-gly.md)unterstützt.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Erkennen von wiedergegebenen Nachrichten, die mithilfe der Funktionen [<strong>verschlüsseltmessage</strong>] (EncryptMessage--General.MD) oder [<strong>makesignature</strong>] (makesignature.MD) codiert wurden.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Erkennen, dass Nachrichten außerhalb der Reihenfolge empfangen wurden.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Unterstützen einer Datenstrom orientierten Verbindung.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_USE_SESSION_KEY"></span><span id="isc_req_use_session_key"></span><dl> <dt><strong>ISC_REQ_USE_SESSION_KEY</strong></dt> </dl></td><td>Ein neuer [*Sitzungsschlüssel*](../secgloss/s-gly.md) muss ausgehandelt werden.<br/> Dieser Wert wird nur von der eingeschränkten Kerberos- [*Delegierung*](../secgloss/s-gly.md)unterstützt.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt> </dl></td><td>SChannel darf nicht versuchen, Anmelde Informationen für den Client automatisch bereitzustellen.<br/></td></tr></tbody></table>



 

Die angeforderten Attribute werden möglicherweise nicht vom Client unterstützt. Weitere Informationen finden Sie unter dem Parameter *pfContextAttr* .

Weitere Beschreibungen der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md).

</dd> <dt>

*"Reserved1"* \[ in\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*Targetdatarep* \[ in\]
</dt> <dd>

Die Datendarstellung (z. b. Byte Reihenfolge) für das Ziel. Dieser Parameter kann entweder "Security \_ native \_ drep" oder "Security \_ Network \_ drep" lauten.

Dieser Parameter wird nicht mit Digest oder SChannel verwendet. Legen Sie den Wert auf NULL fest.

</dd> <dt>

*pinput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die Zeiger auf die Puffer enthält, die als Eingabe für das Paket bereitgestellt werden. Der Wert dieses Parameters muss beim ersten Aufrufen der Funktion **null** sein, es sei denn, der Client Kontext wurde vom Server initiiert. Bei nachfolgenden Aufrufen der Funktion oder wenn der Client Kontext vom Server initiiert wurde, ist der Wert dieses Parameters ein Zeiger auf einen Puffer, der ausreichend Arbeitsspeicher für das vom Remote Computer zurückgegebene Token zugeordnet ist.

</dd> <dt>

*"Reserved2"* \[ in\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*phnewcontext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten Aufrufe von **InitializeSecurityContext (allgemein)** empfängt dieser Zeiger das neue Kontext handle. Beim zweiten-Befehl kann *phnewcontext* mit dem im *phcontext* -Parameter angegebenen Handle identisch sein.

Wenn Sie Schannel SSP verwenden, übergeben Sie bei aufrufen nach dem ersten Aufruf das hier zurückgegebene Handle als *phcontext* -Parameter, und geben Sie für *phnewcontext* **null** an.

</dd> <dt>

*poutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die Zeiger auf die [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur enthält, die die Ausgabedaten empfängt. Wenn ein Puffer \_ in der Eingabe als Sek. gelesen wurde, wird er in der Ausgabe angezeigt. Das System weist einen Puffer für das Sicherheits Token zu, wenn dies angefordert wird (über den ISC \_ -req \_ \_ -Speicher Belegungs Speicher), und gibt die Adresse im Puffer Deskriptor für das Sicherheits Token ein.

Wenn Sie die Microsoft Digest SSP verwenden, empfängt dieser Parameter die Challenge-Antwort, die an den Server gesendet werden muss.

Wenn das Schannel-SSP verwendet wird, \_ \_ wird das \_ Flag für den Schannel-SSP für den Puffer belegt und die entsprechenden Informationen in [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)abgelegt. Außerdem muss der Aufrufer einen Puffer vom Typ " **secbuffer- \_ Warnung**" übergeben. Wenn bei der Ausgabe eine Warnung generiert wird, enthält dieser Puffer Informationen zu dieser Warnung, und die Funktion schlägt fehl.

</dd> <dt>

*pfContextAttr* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die einen Satz von Bitflags empfangen soll, die die [*Attribute*](../secgloss/a-gly.md#_security_attribute_gly) des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md).

Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC \_ RET, wie z \_ \_ . b. ISC Eine Liste gültiger Werte finden Sie unter dem Parameter *fContextReq* .

Suchen Sie erst nach sicherheitsbezogenen Attributen, wenn der abschließende Funktions aufruger erfolgreich zurückgegeben wurde. Attributflags, die sich nicht auf die Sicherheit beziehen, wie z. b. das von ASC \_ ret \_ zugewiesene \_ arbeitsspeicherflag, können vor der letzten Rückgabe geprüft werden.

> [!Note]  
> Bestimmte Kontext Attribute können während der Aushandlung mit einem Remotepeer geändert werden.

 

</dd> <dt>

*ptsexpiry* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das [*Sicherheitspaket*](../secgloss/s-gly.md) diesen Wert immer in der lokalen Zeit zurückgibt. Dieser Parameter ist optional, und für kurzlebige Clients sollte **null** übergeben werden.

Es gibt keine Ablaufzeit für Microsoft Digest SSP- [*Sicherheitskontext*](../secgloss/s-gly.md)-oder-Anmelde Informationen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion einen der folgenden Erfolgs Codes zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEK \_ . \_ \_ und \_ fortfahren**</dt> </dl> | Der Client muss das [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) -Element aufzurufen und die Ausgabe dann an den Server übergeben. Der Client wartet dann auf ein zurück gegebenes Token und übergibt es in einem anderen-Befehl an [**InitializeSecurityContext (allgemein)**](initializesecuritycontext--general.md).<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**SEK \_ . \_ \_**</dt> </dl>        | Der Client muss die Erstellung der Nachricht abschließen und dann die [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) -Funktion aufzurufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**SEK \_ . \_ \_**</dt> </dl>        | Der Client muss das Ausgabe Token an den Server senden und auf ein Rückgabe Token warten. Das zurückgegebene Token wird dann in einem anderen Befehl von [**InitializeSecurityContext (allgemein)**](initializesecuritycontext--general.md)übergeben. Das Ausgabe Token kann leer sein.<br/>                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Sek., \_ \_ unvollständige \_ Anmelde Informationen**</dt> </dl> | Verwendung mit Schannel. Der Server hat die Client Authentifizierung angefordert, und die angegebenen Anmelde Informationen enthalten entweder kein Zertifikat, oder das Zertifikat wurde nicht von einer Zertifizierungsstelle ausgestellt, die vom Server als vertrauenswürdig eingestuft wird. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                              |
| <dl> <dt>**Sekunde \_ E \_ unvollständige \_ Nachricht**</dt> </dl>     | Verwendung mit Schannel. Die Daten für die gesamte Nachricht wurden nicht aus der Übertragung gelesen.<br/> Wenn dieser Wert zurückgegeben wird, enthält der *pinput* -Puffer eine [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur mit einem **buffertype** -Member von **secbuffer \_ fehlt**. Der **cbbuffer** -Member von **secbuffer** enthält einen Wert, der die Anzahl zusätzlicher Bytes angibt, die die Funktion vom Client lesen muss, bevor diese Funktion erfolgreich ausgeführt wird. Obwohl diese Zahl nicht immer genau ist, kann Sie verwendet werden, um die Leistung zu verbessern, indem mehrere Aufrufe dieser Funktion vermieden werden.<br/> |
| <dl> <dt>**Sek. \_ E \_ OK**</dt> </dl>                      | Der [*Sicherheitskontext*](../secgloss/s-gly.md) wurde erfolgreich initialisiert. Es ist kein weiterer [**InitializeSecurityContext-(allgemeiner)**](initializesecuritycontext--general.md) aufrufbedarf erforderlich. Wenn die Funktion ein Ausgabe Token zurückgibt, d. h., wenn das secbuffer- \_ Token in *poutput* eine Länge ungleich NULL aufweist, muss dieses Token an den Server gesendet werden.<br/>                                                                                                                                                    |



 

Wenn die Funktion fehlschlägt, gibt die Funktion einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                          | Beschreibung                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt> </dl>          | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**Sek. \_ E ( \_ interner \_ Fehler)**</dt> </dl>               | Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**s \_ E \_ ungültiges \_ handle**</dt> </dl>               | Das an die Funktion über gegebene Handle ist ungültig.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ ungültiges \_ Token**</dt> </dl>                | Der Fehler tritt auf, wenn ein ungültiges Eingabe Token vorliegt, z. b. ein Token, das während der Übertragung beschädigt ist, ein Token falscher Größe oder ein Token, das an das falsche [*Sicherheitspaket*](../secgloss/s-gly.md)übermittelt wurde. Das Übergeben eines Tokens an das falsche Paket kann erfolgen, wenn der Client und der Server nicht das richtige [*Sicherheitspaket*](../secgloss/s-gly.md)ausgehandelt haben.<br/> |
| <dl> <dt>**Sek. \_ E- \_ Anmeldung \_ verweigert**</dt> </dl>                 | Die Anmeldung ist fehlgeschlagen.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ keine \_ authentifizier Ende Zertifizierungsstelle \_**</dt> </dl> | Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Der Domänen Name der authentifizier enden Partei ist möglicherweise falsch, die Domäne kann nicht erreichbar sein, oder es ist ein Fehler bei der Vertrauensstellung aufgetreten.<br/>                                                                                  |
| <dl> <dt>**s \_ E \_ keine \_ Anmelde Informationen**</dt> </dl>               | Im [*Sicherheitspaket*](../secgloss/s-gly.md)sind keine Anmelde Informationen verfügbar.<br/>                                                                                                                                                  |
| <dl> <dt>**Sekunde \_ E \_ Ziel \_ unbekannt**</dt> </dl>               | Das Ziel wurde nicht erkannt.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**s \_ E \_ nicht unterstützte \_ Funktion**</dt> </dl>         | \_ \_ \_ \_ \_ \_ Im *fContextReq* -Parameter wurde ein ungültiges Kontext Attribut Kennzeichen (ISC req-Delegat oder ISC req-Eingabeaufforderung für die Anmelde Informationen) angegeben.<br/>                                                                                                                                            |
| <dl> <dt>**SEK \_ . \_ falscher \_ Prinzipal**</dt> </dl>              | Der Prinzipal, der die Authentifizierungsanforderung empfangen hat, ist nicht mit dem Prinzipal identisch, der an den *psztargetname* -Parameter übergeben wurde. Dies weist auf einen Fehler bei der gegenseitigen Authentifizierung hin.<br/>                                                                                                          |



 

## <a name="remarks"></a>Bemerkungen

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die abschließenden Kontext Attribute ausreichend sind. Wenn beispielsweise Vertraulichkeit angefordert wurde, Sie aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden.

Wenn Attribute des [*Sicherheits Kontexts*](../secgloss/s-gly.md) nicht ausreichen, muss der Client den teilweise erstellten Kontext durch Aufrufen der [**Delta Context**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) -Funktion freigeben.

Die **InitializeSecurityContext (General)** -Funktion wird von einem Client verwendet, um einen ausgehenden Kontext zu initialisieren.

Bei einem zweistufigen [*Sicherheitskontext*](../secgloss/s-gly.md)sieht die aufrufende Sequenz wie folgt aus:

1.  Der Client ruft die-Funktion auf, wobei *phcontext* auf **null** festgelegt ist, und füllt den Puffer Deskriptor mit der Eingabe Nachricht.
2.  Das [*Sicherheitspaket*](../secgloss/s-gly.md) überprüft die Parameter und erstellt ein undurchsichtiges Token, das es im Token-Element im Puffer Array platziert. Wenn der *Parameter "Parameter" den Wert* "ISC \_ req \_ -Speicher Belegungs Flag" enthält \_ , ordnet das [*Sicherheitspaket*](../secgloss/s-gly.md) den Arbeitsspeicher zu und gibt den Zeiger im Token-Element zurück.
3.  Der Client sendet das Token, das im *poutput* -Puffer zurückgegeben wurde, an den Zielserver. Der Server übergibt dann das Token als Eingabe Argument in einem aufzurufenden Befehl an die Funktion " [**akzeptsecuritycontext (General)**](acceptsecuritycontext--general.md) ".
4.  " [**Akzeptsecuritycontext (allgemein)**](acceptsecuritycontext--general.md) " gibt möglicherweise ein Token zurück, das der Server für einen zweiten **callalizesecuritycontext (allgemein)** an den Client sendet, wenn der erste zurückgegebene Befehl "s Continue" zurückgegeben wird \_ \_ \_ .

Bei mehrstufigen [*Sicherheits Kontexten*](../secgloss/s-gly.md), wie z. b. der gegenseitigen Authentifizierung, sieht die Aufruf Sequenz wie folgt aus:

1.  Der Client ruft die-Funktion wie zuvor beschrieben auf, aber das Paket gibt den Fortschritt zurück, der für den \_ \_ \_ erfolgreichen Erfolg benötigt wird.
2.  Der Client sendet das Ausgabe Token an den Server und wartet auf die Antwort des Servers.
3.  Beim Empfang der Serverantwort ruft der Client erneut **InitializeSecurityContext (General)** auf, wobei *phcontext* auf das Handle festgelegt ist, das beim letzten Aufruf zurückgegeben wurde. Das vom Server empfangene Token wird im *pinput* -Parameter bereitgestellt.

Wenn der Server erfolgreich geantwortet hat, gibt das [*Sicherheitspaket*](../secgloss/s-gly.md) SEK \_ . E OK zurück, \_ und es wird eine sichere Sitzung eingerichtet.

Wenn die Funktion eine der Fehler Antworten zurückgibt, wird die Antwort des Servers nicht akzeptiert, und die Sitzung wird nicht festgelegt.

Wenn die Funktion Sekunden zurück \_ gibt \_ , die ich \_ benötigtes, SEK \_ ., \_ \_ benötigtes \_ \_ \_ und \_ fortfahren, werden die Schritte 2 und 3 wiederholt.

Um einen [*Sicherheitskontext*](../secgloss/s-gly.md)zu initialisieren, sind möglicherweise mehrere Aufrufe dieser Funktion erforderlich, je nach dem zugrunde liegenden Authentifizierungsmechanismus sowie den im *fContextReq* -Parameter angegebenen Optionen.

Die Parameter " *stmtreq* " und " *pfcontextattributes* " sind Bitmasken, die verschiedene Kontext Attribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md). Der *pfcontextattributes* -Parameter ist bei erfolgreicher Rückgabe gültig, aber nur bei der letzten erfolgreichen Rückgabe sollten Sie die Flags untersuchen, die die Sicherheitsaspekte des Kontexts betreffen. Zwischen Rückgabewerte können festgelegt werden, z. b. das von ISC \_ ret \_ zugewiesene \_ arbeitsspeicherflag.

Wenn das \_ Flag für die Verwendung von ISC req- \_ \_ \_ verwendender Kennwort festgelegt ist, muss das [*Sicherheitspaket*](../secgloss/s-gly.md) \_ \_ im *pinput* -Eingabepuffer nach einem secbuffer-pkg-Parametertyp suchen. Dabei handelt es sich nicht um eine generische Lösung, Sie ermöglicht jedoch eine starke Kopplung von [*Sicherheitspaketen*](../secgloss/s-gly.md) und Anwendungen, wenn dies angebracht ist.

Wenn ISC \_ req \_ Speicher belegt wurde, muss der Aufrufer \_ den Speicher freigeben, indem er die [**freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) -Funktion aufruft.

Das Eingabe Token könnte z. b. die Herausforderung von einem LAN-Manager sein. In diesem Fall wäre das Ausgabe Token die NTLM-verschlüsselte Antwort auf die Abfrage.

Welche Aktion der Client durchführt, hängt vom Rückgabecode dieser Funktion ab. Wenn der Rückgabecode sec \_ E \_ OK ist, wird kein zweiter **InitializeSecurityContext (allgemeiner)** -Befehl ausgeführt, und es wird keine Antwort vom Server erwartet. Wenn es sich bei dem Rückgabecode um "s" handelt \_ \_ \_ , erwartet der Client ein Token als Antwort vom Server und übergibt ihn in einem zweiten aufrufung\" **InitializeSecurityContext" (allgemein)**. Der von \_ mir \_ \_ benötigte Rückgabecode gibt an, dass der Client die Erstellung der Nachricht abschließen und die [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) -Funktion aufzurufen muss. Der Code "s \_ I \_ Complete \_ and \_ Continue" umfasst beide Aktionen.

Wenn **InitializeSecurityContext (allgemein)** beim ersten (oder einzigen) Aufruf Erfolg zurückgibt, muss der Aufrufer schließlich die [**Delta Context**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) -Funktion für das zurückgegebene Handle aufzurufen, auch wenn der Aufruf in einem späteren Abschnitt des Authentifizierungs Austauschs fehlschlägt.

Der Client ruft **InitializeSecurityContext (allgemein)** möglicherweise erneut auf, nachdem er erfolgreich abgeschlossen wurde. Dies gibt dem [*Sicherheitspaket*](../secgloss/s-gly.md) an, dass eine erneute Authentifizierung gewünscht wird.

Kernelmodusaufrufer haben die folgenden Unterschiede: der Zielname ist eine [*Unicode*](../secgloss/u-gly.md) -Zeichenfolge, die mithilfe von [**virtualbelegc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)im virtuellen Arbeitsspeicher zugeordnet werden muss. Er darf nicht aus dem Pool zugeordnet werden. Puffer, die in *pinput* und *poutput* übergeben und bereitgestellt werden, müssen sich im virtuellen Speicher befinden, nicht im Pool.

Wenn die Funktion "Schannel SSP" zurückgibt, wenn die Funktion "SEK \_ . I unvollständige Anmelde Informationen" zurückgibt \_ \_ , überprüfen Sie, ob Sie ein gültiges und vertrauenswürdiges Zertifikat in ihren Das Zertifikat wird angegeben, wenn die [**AcquireCredentialsHandle (General)**](acquirecredentialshandle--general.md) -Funktion aufgerufen wird. Bei dem Zertifikat muss es sich um ein Client Authentifizierungszertifikat handeln, das von einer Zertifizierungsstelle (Certification Authority, ca) ausgestellt wurde Rufen Sie zum Abrufen einer Liste der Zertifizierungsstellen, denen der Server vertraut, die Funktion [**QueryContextAttributes (allgemein)**](querycontextattributes--general.md) auf, und geben Sie das Attribut secpkg \_ attr \_ Aussteller \_ List \_ Ex an.

Wenn Sie den Schannel-SSP verwenden und eine Client Anwendung ein Authentifizierungszertifikat von einer Zertifizierungsstelle empfängt, die vom Server als vertrauenswürdig eingestuft wird, erstellt die Anwendung neue Anmelde Informationen, indem Sie die Funktion [**AcquireCredentialsHandle (allgemein)**](acquirecredentialshandle--general.md) aufruft und anschließend **InitializeSecurityContext (allgemein)** aufruft, wobei die neuen Anmelde Informationen im Parameter *phcredential* angegeben werden

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |
| Unicode- und ANSI-Name<br/>   | **Initializesecuritycontextw** (Unicode) und **initializesecuritycontexta** (ANSI)<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**Akzeptsecuritycontext (allgemein)**](acceptsecuritycontext--general.md)
</dt> <dt>

[**AcquireCredentialsHandle (allgemein)**](acquirecredentialshandle--general.md)
</dt> <dt>

[**CompleteAuthToken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken)
</dt> <dt>

[**Delta Context-Kontext**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext)
</dt> <dt>

[**Freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer)
</dt> <dt>

[**Secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**Secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
