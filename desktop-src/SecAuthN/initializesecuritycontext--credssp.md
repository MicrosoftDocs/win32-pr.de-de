---
description: Initiiert den Client seitigen ausgehenden Sicherheitskontext von einem Anmelde Informations handle.
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
title: InitializeSecurityContext (CredSSP)-Funktion (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: aa359fc0cedf96f43d93cfb7d962035453328759
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346272"
---
# <a name="initializesecuritycontext-credssp-function"></a>InitializeSecurityContext (kredssp)-Funktion

Die Funktion **InitializeSecurityContext (kredssp)** initiiert den Client seitigen ausgehenden Sicherheitskontext von einem Anmelde Informations handle. Die-Funktion erstellt einen Sicherheitskontext zwischen der Client Anwendung und einem Remotepeer. **InitializeSecurityContext (kredssp)** gibt ein Token zurück, das der Client an den Remotepeer übergeben muss. der Peer sendet dieses Token wiederum über den [**calltsecuritycontext (aufrufsp)**](acceptsecuritycontext--credssp.md) -Befehl an die lokale Sicherheits Implementierung. Das generierte Token sollte von allen Aufrufern als nicht transparent angesehen werden.

In der Regel wird die **InitializeSecurityContext (** aufgerufene)-Funktion in einer Schleife aufgerufen, bis ein ausreichender Sicherheitskontext eingerichtet wird.

## <a name="syntax"></a>Syntax


```C++
SECURITY_STATUS SEC_ENTRY InitializeSecurityContext(
  _In_opt_    PCredHandle    phCredential,
  _In_opt_    PCtxtHandle    phContext,
  _In_opt_    SEC_CHAR       *pszTargetName,
  _In_        unsigned long  fContextReq,
  _Reserved_  unsigned long  Reserved1,
  _In_        unsigned long  TargetDataRep,
  _Inout_opt_ PSecBufferDesc pInput,
  _In_        unsigned long  Reserved2,
  _Inout_opt_ PCtxtHandle    phNewContext,
  _Out_opt_   PSecBufferDesc pOutput,
  _Out_       unsigned long  *pfContextAttr,
  _Out_opt_   PTimeStamp     ptsExpiry
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phcredential* \[ in, optional\]
</dt> <dd>

Ein Handle für die Anmelde Informationen, die von [**AcquireCredentialsHandle (kredssp)**](acquirecredentialshandle--credssp.md)zurückgegeben werden. Dieses Handle wird zum Erstellen des Sicherheits Kontexts verwendet. Die **InitializeSecurityContext (aufwärtssp)** -Funktion erfordert mindestens ausgehende Anmelde Informationen.

</dd> <dt>

*phcontext* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten Aufrufen von **InitializeSecurityContext (kredssp)** ist dieser Zeiger **null**. Beim zweiten-Befehl ist dieser Parameter ein Zeiger auf das Handle des partiell formatierten Kontexts, der durch den ersten-Befehl im *phnewcontext* -Parameter zurückgegeben wird.

Geben Sie beim ersten Aufrufen von **InitializeSecurityContext (kredssp)** **null** an. Geben Sie bei zukünftigen aufrufen das Token an, das nach dem ersten Aufruf dieser Funktion im Parameter " *phnewcontext* " empfangen wurde.

</dd> <dt>

*ptargetname* \[ in, optional\]
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

Bitflags, die Anforderungen für den Kontext angeben. Nicht alle Pakete können alle Anforderungen unterstützen. Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC \_ req \_ , z \_ . b. ISC req-Delegat \_ .

Dieser Parameter kann mindestens eines der folgenden Attributflags sein.



| Wert                                                                                                                                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ISC_REQ_ALLOCATE_MEMORY"></span><span id="isc_req_allocate_memory"></span><dl> <dt>**ISC \_ Req \_ Arbeits \_ Speicher zuordnen**</dt> <dt>0x100</dt> </dl>                         | Das Sicherheitspaket ordnet Ausgabepuffer für den Aufrufer zu. Wenn Sie die Ausgabepuffer nicht mehr verwenden, geben Sie Sie frei, indem Sie die [**freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) -Funktion aufrufen.<br/>                                                        |
| <span id="ISC_REQ_CONNECTION"></span><span id="isc_req_connection"></span><dl> <dt>**ISC \_ Req- \_ Verbindung**</dt> <dt>0x800</dt> </dl>                                         | Der Sicherheitskontext verarbeitet keine Formatierungs Meldungen.<br/>                                                                                                                                                                                               |
| <span id="ISC_REQ_EXTENDED_ERROR"></span><span id="isc_req_extended_error"></span><dl> <dt>**ISC \_ Erweiterter req- \_ \_ Fehler**</dt> <dt>0x4000</dt> </dl>                           | Wenn Fehler auftreten, wird die Remote Partei benachrichtigt.<br/>                                                                                                                                                                                                   |
| <span id="ISC_REQ_MANUAL_CRED_VALIDATION"></span><span id="isc_req_manual_cred_validation"></span><dl> <dt>**ISC \_ \_Manuelle req \_ -über \_ Prüfung**</dt> <dt>0x80.000</dt> </dl> | Der Anmelde Informationsanbieter für Sicherheitsunterstützung (Security Support Provider, kredssp) darf den Server nicht automatisch authentifizieren. Dieses Flag wird immer festgelegt, wenn Sie "kredssp" verwenden.<br/>                                                                                                              |
| <span id="ISC_REQ_SEQUENCE_DETECT"></span><span id="isc_req_sequence_detect"></span><dl> <dt>**ISC \_ Req- \_ Sequenz \_ Erkennung**</dt> <dt>0x8</dt> </dl>                           | Erkennen, dass Nachrichten außerhalb der Reihenfolge empfangen wurden.<br/>                                                                                                                                                                                                               |
| <span id="ISC_REQ_STREAM"></span><span id="isc_req_stream"></span><dl> <dt>**ISC \_ Req- \_ Stream**</dt> <dt>0X8000</dt> </dl>                                                    | Unterstützen einer Datenstrom orientierten Verbindung.<br/>                                                                                                                                                                                                                   |
| <span id="ISC_REQ_USE_SUPPLIED_CREDS"></span><span id="isc_req_use_supplied_creds"></span><dl> <dt>**ISC \_ Von req \_ verwendete verwendende \_ \_ Befehle**</dt> <dt>0x80</dt> </dl>                | Von "kredssp" darf nicht versucht werden, automatisch Anmelde Informationen für den Client bereitzustellen.<br/>                                                                                                                                                                            |
| <span id="ISC_REQ_DELEGATE"></span><span id="isc_req_delegate"></span><dl> <dt>**ISC \_ Req \_**</dt> -Delegat <dt>0x1</dt> </dl>                                                 | Gibt an, dass die Anmelde Informationen des Benutzers an den Server delegiert werden sollen.<br/> Wenn dieses Flag nicht angegeben wird, wird ein leerer Satz von Anmelde Informationen an den Server delegiert.<br/> **Windows Server 2008 und Windows Vista:** Dieses Flag ist erforderlich.<br/> |
| <span id="ISC_REQ_MUTUAL_AUTH"></span><span id="isc_req_mutual_auth"></span><dl> <dt>**ISC \_ Req \_ - \_ gegenseitige**</dt> Authentifizierung <dt>0x2</dt> </dl>                                       | Gibt an, dass keine Server Authentifizierung erforderlich ist. Delegierungs Richtlinien werden weiterhin erzwungen, wenn dieses Flag nicht angegeben wird.<br/> **Windows Server 2008 und Windows Vista:** Dieses Flag wird ignoriert.<br/>                                                 |



 

Die angeforderten Attribute werden möglicherweise nicht vom Client unterstützt. Weitere Informationen finden Sie unter dem Parameter *pfContextAttr* .

Weitere Beschreibungen der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md).

</dd> <dt>

*"Reserved1"* \[ in\]
</dt> <dd>

Reserviert. Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> <dt>

*Targetdatarep* \[ in\]
</dt> <dd>

Die Datendarstellung (z. b. Byte Reihenfolge) für das Ziel. Dieser Parameter kann entweder " **Security \_ native \_ drep** " oder " **Security \_ Network \_ drep**" lauten.

</dd> <dt>

*pinput* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur, die Zeiger auf die Puffer enthält, die als Eingabe für das Paket bereitgestellt werden. Der Wert dieses Parameters muss beim ersten Aufrufen der Funktion **null** sein, es sei denn, der Client Kontext wurde vom Server initiiert. Bei nachfolgenden Aufrufen der Funktion oder wenn der Client Kontext vom Server initiiert wurde, ist der Wert dieses Parameters ein Zeiger auf einen Puffer, der ausreichend Arbeitsspeicher für das vom Remote Computer zurückgegebene Token zugeordnet ist.

Bei Aufrufen dieser Funktion nach dem ersten Aufruf müssen zwei Puffer vorhanden sein. Der erste verfügt über einen **typsecbuffer- \_ Token** und enthält das vom Server empfangene Token. Der zweite Puffer weist den Typ " **secbuffer \_ empty**" auf. Legen Sie die Member **pvbuffer** und **cbbuffer** auf NULL fest.

</dd> <dt>

*"Reserved2"* \[ in\]
</dt> <dd>

Reserviert. Dieser Parameter muss auf 0 (null) festgelegt werden.

</dd> <dt>

*phnewcontext* \[ in, out, optional\]
</dt> <dd>

Ein Zeiger auf eine [ctxthandle](sspi-handles.md) -Struktur. Beim ersten Aufrufen von **InitializeSecurityContext (kredssp)** empfängt dieser Zeiger das neue Kontext handle. Beim zweiten-Befehl kann *phnewcontext* mit dem im *phcontext* -Parameter angegebenen Handle identisch sein.

Übergeben Sie bei aufrufen nach dem ersten Aufruf das hier zurückgegebene Handle als *phcontext* -Parameter, und geben Sie für *phnewcontext* **null** an.

</dd> <dt>

*poutput* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**secbufferdebug**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) -Struktur. Diese Struktur enthält wiederum Zeiger auf die [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur, die die Ausgabedaten empfängt. Wenn ein Puffer in der Eingabe als **Sek. \_ gelesen** wurde, wird er in der Ausgabe angezeigt. Das System weist einen Puffer für das Sicherheits Token zu, wenn dies angefordert wird (über den **ISC- \_ req- \_ Speicher \_** Belegungs Speicher), und gibt die Adresse im Puffer Deskriptor für das Sicherheits Token ein.

Wenn das kennflag für die **ISC \_ req- \_ \_ Speicher** belegungsfunktion angegeben wird, belegt "kredssp" Arbeitsspeicher für den Puffer und legt die entsprechenden Informationen in " [**secbufferdesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)" ab.

</dd> <dt>

*pfContextAttr* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Satz von Bitflags, die die [*Attribute*](../secgloss/a-gly.md#_security_attribute_gly) des eingerichteten Kontexts angeben. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md).

Flags, die für diesen Parameter verwendet werden, haben das Präfix ISC \_ RET, wie z. b. **ISC \_ \_** Eine Liste gültiger Werte finden Sie unter dem Parameter *fContextReq* .

Suchen Sie erst nach sicherheitsbezogenen Attributen, wenn der abschließende Funktions aufruger erfolgreich zurückgegeben wurde. Attributflags, die sich nicht auf die Sicherheit beziehen, wie z. b. das von **ASC \_ ret \_ zugewiesene \_ arbeitsspeicherflag** , können vor der letzten Rückgabe geprüft werden.

> [!Note]  
> Bestimmte Kontext Attribute können während der Aushandlung mit einem Remotepeer geändert werden.

 

</dd> <dt>

*ptsexpiry* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf eine [**Zeitstempel**](timestamp.md) Struktur, die die Ablaufzeit des Kontexts empfängt. Es wird empfohlen, dass das Sicherheitspaket diesen Wert immer in der lokalen Zeit zurückgibt. Dieser Parameter ist optional, und für kurzlebige Clients sollte **null** übergeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie einen der folgenden Erfolgs Codes zurück.



| Rückgabecode                                                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Sekunde \_ E \_ unvollständige \_ Nachricht**</dt> </dl>     | Die Daten für die gesamte Nachricht wurden nicht aus der Übertragung gelesen.<br/> Wenn dieser Wert zurückgegeben wird, enthält der *pinput* -Puffer eine [**secbuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) -Struktur mit einem **buffertype** -Member von **secbuffer \_ fehlt**. Das **cbbuffer** -Member von **secbuffer** gibt die Anzahl zusätzlicher Bytes an, die die Funktion vom Client lesen muss, bevor diese Funktion erfolgreich ausgeführt wird. Obwohl diese Zahl nicht immer genau ist, kann Sie verwendet werden, um die Leistung zu verbessern, indem mehrere Aufrufe dieser Funktion vermieden werden.<br/> |
| <dl> <dt>**Sek. \_ E \_ OK**</dt> </dl>                      | Der Sicherheitskontext wurde erfolgreich initialisiert. Es ist kein weiterer [**InitializeSecurityContext (**](initializesecuritycontext--credssp.md) aufzurufen)-Aufrufe erforderlich. Wenn die Funktion ein Ausgabe Token zurückgibt, d. h., wenn das **secbuffer- \_ Token** in *poutput* eine Länge ungleich NULL aufweist, muss dieses Token an den Server gesendet werden.<br/>                                                                                                   |
| <dl> <dt>**SEK \_ . \_ \_ und \_ fortfahren**</dt> </dl> | Der Client muss das [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) -Element aufzurufen und die Ausgabe dann an den Server übergeben. Der Client wartet dann auf ein zurück gegebenes Token und übergibt es in einem anderen-Befehl an [**InitializeSecurityContext (**](initializesecuritycontext--credssp.md)aufzurufen).<br/>                                                                                                                                                                                                                                            |
| <dl> <dt>**SEK \_ . \_ \_**</dt> </dl>        | Der Client muss die Erstellung der Nachricht abschließen und dann die [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) -Funktion aufzurufen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEK \_ . \_ \_**</dt> </dl>        | Der Client muss das Ausgabe Token an den Server senden und auf ein Rückgabe Token warten. Der Client übergibt das zurückgegebene Token in einem anderen Aufrufen von [**InitializeSecurityContext (kredssp)**](initializesecuritycontext--credssp.md). Das Ausgabe Token kann leer sein.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**Sek., \_ \_ unvollständige \_ Anmelde Informationen**</dt> </dl> | Der Server hat die Client Authentifizierung angefordert, aber entweder enthalten die angegebenen Anmelde Informationen kein Zertifikat, oder das Zertifikat wurde nicht von einer Zertifizierungsstelle ausgestellt, der der Server vertraut. Weitere Informationen finden Sie in den Hinweisen.<br/>                                                                                                                                                                              |



 

Wenn die Funktion fehlschlägt, gibt die Funktion einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                                          | Beschreibung                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEK \_ b \_ nicht genügend Arbeits \_ Speicher**</dt> </dl>          | Es ist nicht genügend Arbeitsspeicher verfügbar, um die angeforderte Aktion abzuschließen.<br/>                                                                                                                                                                                                     |
| <dl> <dt>**Sek. \_ E ( \_ interner \_ Fehler)**</dt> </dl>               | Es ist ein Fehler aufgetreten, der keinem SSPI-Fehlercode zugeordnet wurde.<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**s \_ E \_ ungültiges \_ handle**</dt> </dl>               | Das an die Funktion über gegebene Handle ist ungültig.<br/>                                                                                                                                                                                                                            |
| <dl> <dt>**s \_ E \_ ungültiges \_ Token**</dt> </dl>                | Das Eingabe Token ist falsch formatiert. Zu den möglichen Ursachen gehören ein Token, das während der Übertragung beschädigt ist, ein Token falscher Größe und ein Token, das an das falsche Sicherheitspaket übermittelt wurde. Diese letzte Bedingung kann eintreten, wenn der Client und der Server das richtige Sicherheitspaket nicht ausgehandelt haben.<br/> |
| <dl> <dt>**Sek. \_ E- \_ Anmeldung \_ verweigert**</dt> </dl>                 | Die Anmeldung ist fehlgeschlagen.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ keine \_ authentifizier Ende Zertifizierungsstelle \_**</dt> </dl> | Es konnte keine Autorität für die Authentifizierung kontaktiert werden. Der Domänen Name der authentifizier enden Partei ist möglicherweise falsch, die Domäne kann nicht erreichbar sein, oder es ist ein Fehler bei der Vertrauensstellung aufgetreten.<br/>                                                                    |
| <dl> <dt>**s \_ E \_ keine \_ Anmelde Informationen**</dt> </dl>               | Im Sicherheitspaket sind keine Anmelde Informationen verfügbar.<br/>                                                                                                                                    |
| <dl> <dt>**Sekunde \_ E \_ Ziel \_ unbekannt**</dt> </dl>               | Das Ziel wurde nicht erkannt.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ nicht unterstützte \_ Funktion**</dt> </dl>         | Der Wert des *fContextReq* -Parameters ist ungültig. Entweder wurde ein erforderliches Flag nicht angegeben, oder es wurde ein Flag angegeben, das nicht von "kredssp" unterstützt wird.<br/>                                                                                                                 |
| <dl> <dt>**SEK \_ . \_ falscher \_ Prinzipal**</dt> </dl>              | Der Prinzipal, der die Authentifizierungsanforderung empfangen hat, ist nicht mit dem Prinzipal identisch, der an den *psztargetname* -Parameter übergeben wurde. Dieser Fehler weist auf einen Fehler bei der gegenseitigen Authentifizierung hin.<br/>                                                                                      |
| <dl> <dt>**SEC \_ E \_ \_ Delegierungs Richtlinie**</dt> </dl>            | Die Richtlinie unterstützt nicht die Delegierung von Anmelde Informationen an den Zielserver.<br/>                                                                                                                                                                                                |
| <dl> <dt>**s \_ E \_ Richtlinie \_ nur NLTM \_**</dt> </dl>            | Die Delegierung von Anmelde Informationen an den Zielserver ist nicht zulässig, wenn keine gegenseitige Authentifizierung erfolgt.<br/>                                                                                                                                                                  |
| <dl> <dt>**SEK \_ \_ . E gegenseitige Authentifizierung \_ \_ fehlgeschlagen**</dt> </dl>          | Fehler bei der Server Authentifizierung, wenn das \_ Flag für die gegenseitige Authentifizierung von ISC req \_ \_ im Parameter " *SQ treq* " angegeben wird.<br/>                                                                                                                                                             |



 

## <a name="remarks"></a>Bemerkungen

Der Aufrufer ist dafür verantwortlich, zu bestimmen, ob die abschließenden Kontext Attribute ausreichend sind. Wenn beispielsweise Vertraulichkeit angefordert wurde, Sie aber nicht eingerichtet werden konnte, können einige Anwendungen die Verbindung sofort beenden.

Wenn Attribute des Sicherheits Kontexts nicht ausreichen, muss der Client den teilweise erstellten Kontext durch Aufrufen der [**Delta Context**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) -Funktion freigeben.

Der Client ruft die **InitializeSecurityContext (** aufzurufende)-Funktion auf, um einen ausgehenden Kontext zu initialisieren.

Bei einem zweistufigen Sicherheitskontext sieht die aufrufende Sequenz wie folgt aus:

1.  Der Client ruft die-Funktion auf, wobei *phcontext* auf **null** festgelegt ist, und füllt den Puffer Deskriptor mit der Eingabe Nachricht.
2.  Das Sicherheitspaket überprüft die Parameter und erstellt ein undurchsichtiges Token, das es im Token-Element im Puffer Array platziert. Wenn der *Parameter "Parameter" den Wert* " **ISC \_ req \_ - \_ Speicher** Belegungs Flag" enthält, ordnet das Sicherheitspaket den Arbeitsspeicher zu und gibt den Zeiger im Token-Element zurück.
3.  Der Client sendet das Token, das im *poutput* -Puffer zurückgegeben wurde, an den Zielserver. Der Server übergibt dann das Token als Eingabe Argument in einem Aufrufen der Funktion " [**Accept tsecuritycontext (**](acceptsecuritycontext--credssp.md) aufzurufen)".
4.  " [**Accept-SecurityContext" (kredssp)**](acceptsecuritycontext--credssp.md) gibt möglicherweise ein Token zurück. Der Server sendet dieses Token über einen zweiten **InitializeSecurityContext (** aufzurufen)-Befehl an den Client, wenn der **erste zurückgegebene \_ \_ \_** Befehl zurückgegeben wird.

Wenn der Server erfolgreich geantwortet hat, gibt das Sicherheitspaket **Sek. \_ E \_ OK** zurück, und es wird eine sichere Sitzung eingerichtet.

Wenn die Funktion eine der Fehler Antworten zurückgibt, wird die Antwort des Servers nicht akzeptiert, und die Sitzung wird nicht festgelegt.

Wenn die Funktion Sekunden zurückgibt, die **\_ ich \_ \_ benötigtes**, Sek., **\_ \_ \_ benötigtes** **\_ \_ \_ und \_ fortfahren**, werden die Schritte 2 und 3 wiederholt.

Die Initialisierung des Sicherheits Kontexts erfordert möglicherweise mehr als einen Aufrufen dieser Funktion, je nach dem zugrunde liegenden Authentifizierungsmechanismus sowie den im *fContextReq* -Parameter angegebenen Optionen.

Die Parameter " *stmtreq* " und " *pfcontextattributes* " sind Bitmasken, die verschiedene Kontext Attribute darstellen. Eine Beschreibung der verschiedenen Attribute finden Sie unter [Kontext Anforderungen](context-requirements.md). Während der Parameter " *pfcontextattributes* " bei erfolgreicher Rückgabe gültig ist, sollten Sie die Flags, die die Sicherheitsaspekte des Kontexts betreffen, nur bei der letzten erfolgreichen Rückgabe überprüfen. Zwischen Rückgabewerte können festgelegt werden, z. b. das von **ISC \_ ret \_ zugewiesene \_ arbeitsspeicherflag** .

Wenn das Flag für die **Verwendung von ISC \_ req- \_ \_ \_ verwendender** Kennwort festgelegt ist, muss das Sicherheitspaket im *pinput* -Eingabepuffer nach einem **secbuffer- \_ pkg \_** -Parametertyp suchen. Obwohl es sich hierbei nicht um eine generische Lösung handelt, lässt sich das Sicherheitspaket und die Anwendung bei Bedarf stark kombinieren.

Wenn **ISC \_ req \_ \_ Speicher** belegt wurde, muss der Aufrufer den Speicher freigeben, indem er die [**freecontextbuffer**](/windows/win32/api/sspi/nf-sspi-freecontextbuffer) -Funktion aufruft.

Das Eingabe Token könnte z. b. die Herausforderung von einem LAN-Manager sein. In diesem Fall wäre das Ausgabe Token die NTLM-verschlüsselte Antwort auf die Abfrage.

Welche Aktion der Client durchführt, hängt vom Rückgabecode dieser Funktion ab. Wenn der Rückgabecode **sec \_ E \_ OK** ist, gibt es keinen zweiten **InitializeSecurityContext (** aufzurufen)-Befehl, und es wird keine Antwort vom Server erwartet. Wenn es sich bei dem Rückgabecode um "s" handelt, erwartet der Client ein Token als Antwort vom Server und übergibt ihn in einem zweiten Aufrufen von " **InitializeSecurityContext (kredssp)**". **\_ \_ \_** Der **von \_ mir \_ \_ benötigte** Rückgabecode gibt an, dass der Client die Erstellung der Nachricht abschließen und die [**completeauthtoken**](/windows/win32/api/sspi/nf-sspi-completeauthtoken) -Funktion aufzurufen muss. Der Code "s **\_ I \_ Complete \_ and \_ Continue** " umfasst beide Aktionen.

Wenn **InitializeSecurityContext (kredssp)** beim ersten (oder einzigen) Aufruf Erfolg zurückgibt, muss der Aufrufer schließlich die [**Delta Context**](/windows/win32/api/sspi/nf-sspi-deletesecuritycontext) -Funktion für das zurückgegebene Handle aufrufen, auch wenn der Aufruf in einem späteren Abschnitt des Authentifizierungs Austauschs fehlschlägt.

Der Client ruft **InitializeSecurityContext (kredssp)** möglicherweise erneut auf, nachdem er erfolgreich abgeschlossen wurde. Dies gibt dem Sicherheitspaket an, dass eine erneute Authentifizierung gewünscht wird.

Für den kernelmodusaufrufer gibt es die folgenden Unterschiede: der Zielname ist eine [*Unicode*](../secgloss/u-gly.md#_security_unicode_gly) -Zeichenfolge, die mithilfe von [**virtualbelegc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)im virtuellen Speicher zugeordnet werden muss. Er darf nicht aus dem Pool zugeordnet werden. Puffer, die in *pinput* und *poutput* übergeben und bereitgestellt werden, müssen sich im virtuellen Speicher befinden, nicht im Pool.

Wenn die Funktion " **Sek. \_ I \_ unvollständige \_ Anmelde** Informationen" zurückgibt, überprüfen Sie, ob die an die Funktion " [**AcquireCredentialsHandle**](acquirecredentialshandle--credssp.md) " übergebenen r-Anmelde Informationen ein gültiges und vertrauenswürdiges Zertifikat angegeben haben. das Zertifikat muss ein Client Authentifizierungszertifikat sein, das von einer Zertifizierungsstelle ausgestellt wurde, der der Server vertraut Rufen Sie zum Abrufen einer Liste der Zertifizierungsstellen, die vom Server als vertrauenswürdig eingestuft werden, die [**QueryContextAttributes (kredssp)**](querycontextattributes--credssp.md) -Funktion mit dem Attribut **secpkg \_ attr \_ Aussteller \_ List \_ Ex** auf.

Nachdem Sie ein Authentifizierungszertifikat von einer Zertifizierungsstelle erhalten haben, der der Server vertraut, erstellt die Client Anwendung neue Anmelde Informationen. Dies erfolgt durch Aufrufen der Funktion [**AcquireCredentialsHandle (CredSSP)**](acquirecredentialshandle--credssp.md) und anschließendes Aufrufen von **InitializeSecurityContext (CredSSP)** , wobei die neuen Anmelde Informationen im Parameter *phcredential* angegeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>SSPI. h (Include Security. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[SSPI-Funktionen](authentication-functions.md#sspi-functions)
</dt> <dt>

[**Accept-SecurityContext (kredssp)**](acceptsecuritycontext--credssp.md)
</dt> <dt>

[**AcquireCredentialsHandle (kredssp)**](acquirecredentialshandle--credssp.md)
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

 

 
