---
description: Initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informations Handle mithilfe der eingeschränkten SChannel- [*Delegierung*](../secgloss/s-gly.md).
ms.assetid: c451089a-d10d-469c-99dd-43d75a6b0b2a
title: InitializeSecurityContext (SChannel)-Funktion (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: ac552370727659e43b762d55019132ac1c4ea1e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343037"
---
# <a name="initializesecuritycontext-schannel-function"></a>InitializeSecurityContext-Funktion (SChannel)

Die Funktion **InitializeSecurityContext (SChannel)** initiiert den Client seitigen ausgehenden [*Sicherheitskontext*](../secgloss/s-gly.md) von einem Anmelde Informationen-handle. Die-Funktion wird verwendet, um einen [*Sicherheitskontext*](../secgloss/s-gly.md) zwischen der Client Anwendung und einem Remotepeer zu erstellen. **InitializeSecurityContext (SChannel)** gibt ein Token zurück, das der Client an den Remotepeer übergeben muss, den der Peer wiederum über den [**calltsecuritycontext (SChannel)**](acceptsecuritycontext--schannel.md) -Befehl an die lokale Sicherheits Implementierung übermittelt. Das generierte Token sollte von allen Aufrufern als nicht transparent angesehen werden.

In der Regel wird die **InitializeSecurityContext-Funktion (SChannel)** in einer Schleife aufgerufen, bis ein ausreichender [*Sicherheitskontext*](../secgloss/s-gly.md) eingerichtet wird.

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

Ein Handle für die Anmelde Informationen, die von [**AcquireCredentialsHandle (SChannel)**](acquirecredentialshandle--schannel.md)zurückgegeben werden. Dieses Handle wird zum Erstellen des [*Sicherheits Kontexts*](../secgloss/s-gly.md)verwendet. Die Funktion **InitializeSecurityContext (SChannel)** erfordert mindestens ausgehende Anmelde Informationen.

</dd> <dt>

*phcontext* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten Aufrufe von **InitializeSecurityContext (SChannel)** ist dieser Zeiger **null**. Beim zweiten-Befehl ist dieser Parameter ein Zeiger auf das Handle des partiell formatierten Kontexts, der durch den ersten-Befehl im *phnewcontext* -Parameter zurückgegeben wird.

Geben Sie beim ersten aufzurufen von **InitializeSecurityContext (SChannel)** **null** an. Geben Sie bei zukünftigen aufrufen das Token an, das nach dem ersten Aufruf dieser Funktion im Parameter " *phnewcontext* " empfangen wurde.

</dd> <dt>

*psztargetname* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine NULL-terminierte Zeichenfolge, die den Zielserver eindeutig identifiziert. SChannel verwendet diesen Wert, um das Serverzertifikat zu überprüfen. SChannel verwendet diesen Wert auch, um die Sitzung im Sitzungs Cache zu finden, wenn eine Verbindung wieder hergestellt wird. Die zwischengespeicherte Sitzung wird nur verwendet, wenn alle der folgenden Bedingungen erfüllt sind:

-   Der Zielname ist identisch.
-   Der Cache Eintrag ist nicht abgelaufen.
-   Der Anwendungsprozess, der die Funktion aufruft, ist identisch.
-   Die Anmelde Sitzung ist identisch.
-   Das Anmelde Informations Handle ist identisch.

</dd> <dt>

*"f"* \[ in\]
</dt> <dd>

Bitflags, die Anforderungen für den Kontext angeben. Nicht alle Pakete können alle Anforderungen unterstützen. Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC \_ req \_ , z \_ . b. ISC req-Delegat \_ . Dieser Parameter kann mindestens eines der folgenden Attributflags sein.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Wert</th><th>Bedeutung</th></tr></thead><tbody><tr class="odd"><td><span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt><strong>ISC_REQ_ALLOCATE_MEMORY</strong></dt> </dl></td><td>Das [*Sicherheitspaket*](../secgloss/s-gly.md) weist Ihnen Ausgabepuffer zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie Sie frei, indem Sie die [<strong>freecontextbuffer</strong>] (/Windows/Win32/API/SSPI/NF-SSPI-freecontextbuffer)-Funktion aufrufen.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_CONFIDENTIALITY"></span><span id="isc_req_confidentiality"></span><dl> <dt><strong>ISC_REQ_CONFIDENTIALITY</strong></dt> </dl></td><td>Verschlüsseln Sie Nachrichten mithilfe der [<strong>verschlüsseltmessage</strong>] (EncryptMessage--General.MD)-Funktion.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt><strong>ISC_REQ_CONNECTION</strong></dt> </dl></td><td>Der [*Sicherheitskontext*](../secgloss/s-gly.md) verarbeitet keine Formatierungs Meldungen.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt><strong>ISC_REQ_EXTENDED_ERROR</strong></dt> </dl></td><td>Wenn Fehler auftreten, wird die Remote Partei benachrichtigt.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_INTEGRITY"></span><span id="isc_req_integrity"></span><dl> <dt><strong>ISC_REQ_INTEGRITY</strong></dt> </dl></td><td>Signieren von Nachrichten und Überprüfen von Signaturen mithilfe der Funktionen [<strong>verschlüsseltmessage</strong>] (EncryptMessage--General.MD) und [<strong>makesignature</strong>] (makesignature.MD).<br/></td></tr><tr class="even"><td><span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt><strong>ISC_REQ_MANUAL_CRED_VALIDATION</strong></dt> </dl></td><td>SChannel darf den Server nicht automatisch authentifizieren.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt><strong>ISC_REQ_MUTUAL_AUTH</strong></dt> </dl></td><td>Die Richtlinie für die gegenseitige Authentifizierung des Dienstanbieter wird erfüllt.<br/><blockquote>[!Caution]<br />
Dies bedeutet nicht notwendigerweise, dass die gegenseitige Authentifizierung durchgeführt wird, sondern nur, dass die Authentifizierungs Richtlinie des Dienstanbieter erfüllt ist. Um sicherzustellen, dass die gegenseitige Authentifizierung erfolgt, wenden Sie die [<strong>QueryContextAttributes (SChannel)</strong>] (QueryContextAttributes--Schannel.MD)-Funktion an.</blockquote><br/></td></tr><tr class="even"><td><span id="ISC_REQ_REPLAY_DETECT"></span><span id="isc_req_replay_detect"></span><dl> <dt><strong>ISC_REQ_REPLAY_DETECT</strong></dt> </dl></td><td>Erkennen von wiedergegebenen Nachrichten, die mithilfe der Funktionen [<strong>verschlüsseltmessage</strong>] (EncryptMessage--General.MD) oder [<strong>makesignature</strong>] (makesignature.MD) codiert wurden.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt><strong>ISC_REQ_SEQUENCE_DETECT</strong></dt> </dl></td><td>Erkennen, dass Nachrichten außerhalb der Reihenfolge empfangen wurden.<br/></td></tr><tr class="even"><td><span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt><strong>ISC_REQ_STREAM</strong></dt> </dl></td><td>Unterstützen einer Datenstrom orientierten Verbindung.<br/></td></tr><tr class="odd"><td><span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt><strong>ISC_REQ_USE_SUPPLIED_CREDS</strong></dt> </dl></td><td>SChannel darf nicht versuchen, Anmelde Informationen für den Client automatisch bereitzustellen.<br/></td></tr></tbody></table>



 

Die angeforderten Attribute werden möglicherweise nicht vom Client unterstützt. Weitere Informationen finden Sie unter dem Parameter *pfContextAttr* .

Weitere Beschreibungen der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md).

</dd> <dt>

*"Reserved1"* \[ in\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*Targetdatarep* \[ in\]
</dt> <dd>

Dieser Parameter wird nicht mit SChannel verwendet. Legen Sie den Wert auf NULL fest.

</dd> <dt>

*pinput* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die Zeiger auf die Puffer enthält, die als Eingabe für das Paket bereitgestellt werden. Der Wert dieses Parameters muss beim ersten Aufrufen der Funktion **null** sein, es sei denn, der Client Kontext wurde vom Server initiiert. Bei nachfolgenden Aufrufen der Funktion oder wenn der Client Kontext vom Server initiiert wurde, ist der Wert dieses Parameters ein Zeiger auf einen Puffer, der ausreichend Arbeitsspeicher für das vom Remote Computer zurückgegebene Token zugeordnet ist.

Bei Aufrufen dieser Funktion nach dem ersten Aufruf müssen zwei Puffer vorhanden sein. Der erste verfügt über einen **typsecbuffer- \_ Token** und enthält das vom Server empfangene Token. Der zweite Puffer weist den Typ " **secbuffer \_ empty**" auf. Legen Sie die Member **pvbuffer** und **cbbuffer** auf NULL fest.

</dd> <dt>

*"Reserved2"* \[ in\]
</dt> <dd>

Dieser Parameter ist reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*phnewcontext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten Aufrufe von **InitializeSecurityContext (SChannel)** empfängt dieser Zeiger das neue Kontext handle. Beim zweiten-Befehl kann *phnewcontext* mit dem im *phcontext* -Parameter angegebenen Handle identisch sein.

Übergeben Sie bei aufrufen nach dem ersten Aufruf das hier zurückgegebene Handle als *phcontext* -Parameter, und geben Sie für *phnewcontext* **null** an.

</dd> <dt>

*poutput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die Zeiger auf die [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur enthält, die die Ausgabedaten empfängt. Wenn ein Puffer \_ in der Eingabe als Sek. gelesen wurde, wird er in der Ausgabe angezeigt. Das System weist einen Puffer für das Sicherheits Token zu, wenn dies angefordert wird (über den ISC \_ -req \_ \_ -Speicher Belegungs Speicher), und gibt die Adresse im Puffer Deskriptor für das Sicherheits Token ein.

Wenn das \_ kennflag für die ISC req- \_ \_ Speicher Belegungskapazität angegeben wird, belegt der Schannel-SSP Arbeitsspeicher für den Puffer und fügt die entsprechenden Informationen in [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)ein. Außerdem muss der Aufrufer einen Puffer vom Typ " **secbuffer- \_ Warnung**" übergeben. Wenn bei der Ausgabe eine Warnung generiert wird, enthält dieser Puffer Informationen zu dieser Warnung, und die Funktion schlägt fehl.

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

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion einen der folgenden Erfolgs Codes zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEK \_ . \_ \_ und \_ fortfahren**</dt> </dl> | Der Client muss das [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) -Element aufzurufen und die Ausgabe dann an den Server übergeben. Der Client wartet dann auf ein zurück gegebenes Token und übergibt es in einem anderen-Befehl an [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md).<br/>                                                                                                                                                                                                                                                                |
| <dl> <dt>**SEK \_ . \_ \_**</dt> </dl>        | Der Client muss die Erstellung der Nachricht abschließen und dann die [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) -Funktion aufzurufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**SEK \_ . \_ \_**</dt> </dl>        | Der Client muss das Ausgabe Token an den Server senden und auf ein Rückgabe Token warten. Das zurückgegebene Token wird dann in einem anderen Befehl von [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md)übergeben. Das Ausgabe Token kann leer sein.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**Sek., \_ \_ unvollständige \_ Anmelde Informationen**</dt> </dl> | Der Server hat die Client Authentifizierung angefordert, und die angegebenen Anmelde Informationen enthalten entweder kein Zertifikat, oder das Zertifikat wurde nicht von einer Zertifizierungsstelle (Certification Authority, ca) ausgestellt, die vom Server als vertrauenswürdig eingestuft wird. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                                         |
| <dl> <dt>**Sekunde \_ E \_ unvollständige \_ Nachricht**</dt> </dl>     | Die Daten für die gesamte Nachricht wurden nicht aus der Übertragung gelesen.<br/> Wenn dieser Wert zurückgegeben wird, enthält der *pinput* -Puffer eine [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur mit einem **buffertype** -Member von **secbuffer \_ fehlt**. Der **cbbuffer** -Member von **secbuffer** enthält einen Wert, der die Anzahl zusätzlicher Bytes angibt, die die Funktion vom Client lesen muss, bevor diese Funktion erfolgreich ausgeführt wird. Obwohl diese Zahl nicht immer genau ist, kann Sie verwendet werden, um die Leistung zu verbessern, indem mehrere Aufrufe dieser Funktion vermieden werden.<br/> |
| <dl> <dt>**Sek. \_ E \_ OK**</dt> </dl>                      | Der [*Sicherheitskontext*](../secgloss/s-gly.md) wurde erfolgreich initialisiert. Es ist kein weiterer [**InitializeSecurityContext (SChannel)**](initializesecuritycontext--schannel.md) -Aufrufe erforderlich. Wenn die Funktion ein Ausgabe Token zurückgibt, d. h., wenn das secbuffer- \_ Token in *poutput* eine Länge ungleich NULL aufweist, muss dieses Token an den Server gesendet werden.<br/>                                                                                                                               |



 

Wenn die Funktion fehlschlägt, gibt die Funktion einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                            | Beschreibung                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt> </dl>            | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**Sek. \_ E ( \_ interner \_ Fehler)**</dt> </dl>                 | Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>**s \_ E \_ ungültiges \_ handle**</dt> </dl>                 | Das an die Funktion über gegebene Handle ist ungültig.<br/>                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ ungültiges \_ Token**</dt> </dl>                  | Der Fehler tritt auf, wenn ein ungültiges Eingabe Token vorliegt, z. b. ein Token, das während der Übertragung beschädigt ist, ein Token falscher Größe oder ein Token, das an die falsche [*eingeschränkte Delegierung*](../secgloss/s-gly.md)geleitet wurde. Das Übergeben eines Tokens an das falsche Paket kann erfolgen, wenn der Client und der Server nicht die ordnungsgemäße [*eingeschränkte Delegierung*](../secgloss/s-gly.md)ausgehandelt haben.<br/> |
| <dl> <dt>**Sek. \_ E- \_ Anmeldung \_ verweigert**</dt> </dl>                   | Die Anmeldung ist fehlgeschlagen.<br/>                                                                                                                                                                                                                                                                        |
| <dl> <dt>**s \_ E \_ keine \_ authentifizier Ende Zertifizierungsstelle \_**</dt> </dl>   | Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Der Domänen Name der authentifizier enden Partei ist möglicherweise falsch, die Domäne kann nicht erreichbar sein, oder es ist ein Fehler bei der Vertrauensstellung aufgetreten.<br/>                                                                                  |
| <dl> <dt>**s \_ E \_ keine \_ Anmelde Informationen**</dt> </dl>                 | In der [*eingeschränkten Delegierung*](../secgloss/s-gly.md)sind keine Anmelde Informationen verfügbar.<br/>                                                                                                                                                  |
| <dl> <dt>**Sekunde \_ E \_ Ziel \_ unbekannt**</dt> </dl>                 | Das Ziel wurde nicht erkannt.<br/>                                                                                                                                                                                                                                                           |
| <dl> <dt>**s \_ E \_ nicht unterstützte \_ Funktion**</dt> </dl>           | \_ \_ \_ \_ \_ \_ Im *fContextReq* -Parameter wurde ein ungültiges Kontext Attribut Kennzeichen (ISC req-Delegat oder ISC req-Eingabeaufforderung für die Anmelde Informationen) angegeben.<br/>                                                                                                                                            |
| <dl> <dt>**SEK \_ . \_ falscher \_ Prinzipal**</dt> </dl>                | Der Prinzipal, der die Authentifizierungsanforderung empfangen hat, ist nicht mit dem Prinzipal identisch, der an den *psztargetname* -Parameter übergeben wurde. Dies weist auf einen Fehler bei der gegenseitigen Authentifizierung hin.<br/>                                                                                                          |
| <dl> <dt>**Sek. nicht übereinstimmende \_ \_ Anwendungs \_ Protokoll \_**</dt> </dl> | Zwischen dem Client und dem Server ist kein gängiges Anwendungsprotokoll vorhanden.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die abschließenden Kontext Attribute ausreichend sind. Wenn beispielsweise Vertraulichkeit angefordert wurde, Sie aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden.

Wenn Attribute des [*Sicherheits Kontexts*](../secgloss/s-gly.md) nicht ausreichen, muss der Client den teilweise erstellten Kontext durch Aufrufen der [**Delta Context**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) -Funktion freigeben.

Die Funktion **InitializeSecurityContext (SChannel)** wird von einem Client verwendet, um einen ausgehenden Kontext zu initialisieren.

Bei einem zweistufigen [*Sicherheitskontext*](../secgloss/s-gly.md)sieht die aufrufende Sequenz wie folgt aus:

1.  Der Client ruft die-Funktion auf, wobei *phcontext* auf **null** festgelegt ist, und füllt den Puffer Deskriptor mit der Eingabe Nachricht.
2.  Das [*Sicherheitspaket*](../secgloss/s-gly.md) überprüft die Parameter und erstellt ein undurchsichtiges Token, das es im Token-Element im Puffer Array platziert. Wenn der *Parameter "Parameter" den Wert* "ISC \_ req \_ -Speicher Belegungs Flag" enthält \_ , ordnet das [*Sicherheitspaket*](../secgloss/s-gly.md) den Arbeitsspeicher zu und gibt den Zeiger im Token-Element zurück.
3.  Der Client sendet das Token, das im *poutput* -Puffer zurückgegeben wurde, an den Zielserver. Der Server übergibt dann das Token als Eingabe Argument in einem Rückruf der Funktion " [**Accept-SecurityContext" (SChannel)**](acceptsecuritycontext--schannel.md) .
4.  " [**Akzeptsecuritycontext" (SChannel)**](acceptsecuritycontext--schannel.md) kann ein Token zurückgeben, das der Server für einen zweiten **callalizesecuritycontext (SChannel)** an den Client sendet, wenn der erste zurückgegebene Befehl "Sek." zurückgegeben wird \_ \_ \_ .

Bei mehrstufigen [*Sicherheits Kontexten*](../secgloss/s-gly.md), wie z. b. der gegenseitigen Authentifizierung, sieht die Aufruf Sequenz wie folgt aus:

1.  Der Client ruft die-Funktion wie zuvor beschrieben auf, aber das Paket gibt den Fortschritt zurück, der für den \_ \_ \_ erfolgreichen Erfolg benötigt wird.
2.  Der Client sendet das Ausgabe Token an den Server und wartet auf die Antwort des Servers.
3.  Beim Empfang der Serverantwort ruft der Client erneut **InitializeSecurityContext (SChannel)** auf, wobei *phcontext* auf das Handle festgelegt ist, das beim letzten Aufruf zurückgegeben wurde. Das vom Server empfangene Token wird im *pinput* -Parameter bereitgestellt.

Wenn der Server erfolgreich geantwortet hat, gibt das [*Sicherheitspaket*](../secgloss/s-gly.md) SEK \_ . E OK zurück, \_ und es wird eine sichere Sitzung eingerichtet.

Wenn die Funktion eine der Fehler Antworten zurückgibt, wird die Antwort des Servers nicht akzeptiert, und die Sitzung wird nicht festgelegt.

Wenn die Funktion Sekunden zurück \_ gibt \_ , die ich \_ benötigtes, SEK \_ ., \_ \_ benötigtes \_ \_ \_ und \_ fortfahren, werden die Schritte 2 und 3 wiederholt.

Um einen [*Sicherheitskontext*](../secgloss/s-gly.md)zu initialisieren, sind möglicherweise mehrere Aufrufe dieser Funktion erforderlich, je nach dem zugrunde liegenden Authentifizierungsmechanismus sowie den im *fContextReq* -Parameter angegebenen Optionen.

Die Parameter " *stmtreq* " und " *pfcontextattributes* " sind Bitmasken, die verschiedene Kontext Attribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md). Der *pfcontextattributes* -Parameter ist bei erfolgreicher Rückgabe gültig, aber nur bei der letzten erfolgreichen Rückgabe sollten Sie die Flags untersuchen, die die Sicherheitsaspekte des Kontexts betreffen. Zwischen Rückgabewerte können festgelegt werden, z. b. das von ISC \_ ret \_ zugewiesene \_ arbeitsspeicherflag.

Wenn das \_ Flag für die Verwendung von ISC req- \_ \_ \_ verwendender Kennwort festgelegt ist, muss das [*Sicherheitspaket*](../secgloss/s-gly.md) \_ \_ im *pinput* -Eingabepuffer nach einem secbuffer-pkg-Parametertyp suchen. Dabei handelt es sich nicht um eine generische Lösung, Sie ermöglicht jedoch eine starke Kopplung von [*Sicherheitspaketen*](../secgloss/s-gly.md) und Anwendungen, wenn dies angebracht ist.

Wenn ISC \_ req \_ Speicher belegt wurde, muss der Aufrufer \_ den Speicher freigeben, indem er die [**freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) -Funktion aufruft.

Das Eingabe Token könnte z. b. die Herausforderung von einem LAN-Manager sein. In diesem Fall wäre das Ausgabe Token die NTLM-verschlüsselte Antwort auf die Abfrage.

Welche Aktion der Client durchführt, hängt vom Rückgabecode dieser Funktion ab. Wenn der Rückgabecode sec \_ E \_ OK ist, gibt es keinen zweiten **InitializeSecurityContext (SChannel)** -Befehl, und es wird keine Antwort vom Server erwartet. Wenn es sich bei dem Rückgabecode um "s" handelt \_ \_ \_ , erwartet der Client ein Token als Antwort vom Server und übergibt ihn in einem zweiten **callalizesecuritycontext (SChannel)**. Der von \_ mir \_ \_ benötigte Rückgabecode gibt an, dass der Client die Erstellung der Nachricht abschließen und die [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) -Funktion aufzurufen muss. Der Code "s \_ I \_ Complete \_ and \_ Continue" umfasst beide Aktionen.

Wenn **InitializeSecurityContext (SChannel)** beim ersten (oder einzigen) Aufruf Erfolg zurückgibt, muss der Aufrufer schließlich die [**Delta Context**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) -Funktion für das zurückgegebene Handle aufzurufen, auch wenn der Aufruf in einem späteren Abschnitt des Authentifizierungs Austauschs fehlschlägt.

Der Client ruft **InitializeSecurityContext (SChannel)** möglicherweise erneut auf, nachdem er erfolgreich abgeschlossen wurde. Dies gibt dem [*Sicherheitspaket*](../secgloss/s-gly.md) an, dass eine erneute Authentifizierung gewünscht wird.

Kernelmodusaufrufer haben die folgenden Unterschiede: der Zielname ist eine [*Unicode*](../secgloss/u-gly.md) -Zeichenfolge, die mithilfe von [**virtualbelegc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)im virtuellen Arbeitsspeicher zugeordnet werden muss. Er darf nicht aus dem Pool zugeordnet werden. Puffer, die in *pinput* und *poutput* übergeben und bereitgestellt werden, müssen sich im virtuellen Speicher befinden, nicht im Pool.

Wenn die Funktion "SEK \_ . I" unvollständige Anmelde Informationen zurückgibt \_ \_ , überprüfen Sie, ob in Ihren Anmelde Informationen ein gültiges und vertrauenswürdiges Zertifikat angegeben Das Zertifikat wird angegeben, wenn die [**AcquireCredentialsHandle-Funktion (SChannel)**](acquirecredentialshandle--schannel.md) aufgerufen wird. Bei dem Zertifikat muss es sich um ein Client Authentifizierungszertifikat handeln, das von einer Zertifizierungsstelle (Certification Authority, ca) ausgestellt wurde Rufen Sie zum Abrufen einer Liste der Zertifizierungsstellen, denen der Server vertraut, die [**QueryContextAttributes-Funktion (SChannel)**](querycontextattributes--schannel.md) auf, und geben Sie das Attribut "secpkg \_ attr \_ Aussteller \_ List Ex" an \_ .

Nachdem eine Client Anwendung ein Authentifizierungszertifikat von einer Zertifizierungsstelle erhalten hat, die vom Server als vertrauenswürdig eingestuft wird, erstellt die Anwendung neue Anmelde Informationen, indem Sie die Funktion [**AcquireCredentialsHandle (SChannel)**](acquirecredentialshandle--schannel.md) aufruft und anschließend **InitializeSecurityContext (SChannel)** aufruft, wobei die neuen Anmelde Informationen im Parameter *phcredential* angegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**Akzeptsecuritycontext (SChannel)**](acceptsecuritycontext--schannel.md)
</dt> <dt>

[**AcquireCredentialsHandle (SChannel)**](acquirecredentialshandle--schannel.md)
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

 

 
