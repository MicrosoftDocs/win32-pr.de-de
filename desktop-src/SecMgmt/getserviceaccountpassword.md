---
description: Ruft das Dienst Konto Kennwort ab.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Getserviceaccountpassword-Funktion (secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368913"
---
# <a name="getserviceaccountpassword-function"></a>Getserviceaccountpassword-Funktion

Ruft das Dienst Konto Kennwort ab, das für SSPs ( [*Security Support Providers*](/windows/desktop/SecGloss/s-gly) ) verfügbar ist, z. b. Kerberos SSP.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Accountname* \[ in\]
</dt> <dd>

Mit NULL endender Kontoname des Gruppen verwalteten Dienst Konto Kontos (GMSA). Der Benutzername kann eine der folgenden Formen aufweisen:

-   SAM-Kontoname des GMSA.
-   Benutzername in einem voll qualifizierten Domänen Namen (Fully Qualified Domain Name, FQDN), z *. b. Domain Name * **\\** _username_ oder **www.** _Domäne_* _. com \\_ * _Name_. Der Benutzername darf nur ein SAM-Name sein. Der Domänen Name kann ein DNS-Name oder ein NetBIOS-Name sein.
-   Impliziter Benutzer Prinzipal Name (User Principal Name, UPN) für das GMSA-Konto, z. b. *somename * **@** _Domain_*_. com_*, wobei die *Domäne * * *. com** der tatsächliche DNS-Domänen Name ist.

</dd> <dt>

*Domain Name* \[ in, optional\]
</dt> <dd>

Optionaler null-terminierter Domänen Name. Dies ist nur gültig, wenn der *Accountname* -Parameter ein SAM-Konto Name ist. Der Domänen Name darf nur ein NetBIOS-Name oder ein voll qualifizierter Domänen Name (Fully Qualified Domain Name, FQDN) sein.

</dd> <dt>

" *Fedfetch* \[ " in\]
</dt> <dd>

Ein Wert der [**Fed- \_ Fetch-**](cred-fetch.md) Enumeration, der angibt, wie die Anmelde Informationen abgerufen werden sollen.



| Wert                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <dt>**"Kredfetchdefault"**</dt> </dl> | Das Betriebssystem versucht zunächst, das Kennwort aus dem lokalen Cache abzurufen, wenn das Kennwort nicht abgerufen werden kann. Wenn es an der Zeit ist, das Kennwort abzurufen, kontaktiert das Betriebssystem den Domänen Controller, andernfalls werden alle zwischengespeicherten Kenn Wörter mit dem Statuswert Erfolg zurückgegeben.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <dt>**"Kredfetchdpapi"**</dt> </dl>         | Gibt die lokalen DPAPI-Anmelde Informationen an den Aufrufer zurück. Für SSPs ist es im Allgemeinen nicht erforderlich, diesen Wert zu verwenden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <dt>**"Kredfetchforced"**</dt> </dl>     | Erzwingt, dass das Betriebssystem versucht, das Kennwort vom Domänen Controller zu lesen. Während der Kenn Wort rolloverzeit wurde das Kennwort möglicherweise auf dem Domänen Controller und anderen Mitglieds Hosts geändert, aber der GMSA-Mitglieds Host erkennt das Kennwort als noch gültig. Dies kann auf Probleme mit der Takt Abweichung zwischen verschiedenen Domänen Controllern zurückzuführen sein. Wenn dieser Wert angegeben ist, bestimmt das Betriebssystem, ob eine mögliche Kenn Wort Änderung aufgrund von Zeit Schiefe möglicherweise möglich ist, und ruft das Kennwort ab, wenn dies der Fall ist. Andernfalls werden die zwischengespeicherten Anmelde Informationen zurückgegeben. Wenn keine zwischengespeicherten Anmelde Informationen vorhanden sind, versucht das Betriebssystem, eine vom Domänen Controller zu erhalten.<br/> |



 

</dd> <dt>

*Filetimeablauf* \[ in, out, optional\]
</dt> <dd>

Wenn bei der Eingabe dieser Wert nicht NULL ist und keine **Datei** mit dem Wert 0 (null) ist, enthält *filetimestamp* die Ablaufzeit der Dienst Konto-Anmelde Informationen, die dem Aufrufer bekannt sind. Wenn der *filetimesink* -Parameter mit einem der aktuellen Anmelde Informationen übereinstimmt, schlägt dieser Vorgang fehl. Bei der Ausgabe enthält der *filetimesink* -Parameter die Ablaufzeit der zurückgegebenen Anmelde Informationen.

</dd> <dt>

*CurrentPassword* \[ vorgenommen\]
</dt> <dd>

Das aktuelle Kennwort des GMSA.

</dd> <dt>

*Previouspassword* \[ vorgenommen\]
</dt> <dd>

Das vorherige Kennwort des GMSA.

</dd> <dt>

*Filetimecurrpwdvalidforoutbound* \[ Out, optional\]
</dt> <dd>

Gibt die Zeit an, nach der das aktuelle Kennwort für ausgehende Anforderungen gültig ist. Der Aufrufer sollte die aktuelle Uhrzeit mit diesem Wert vergleichen und das aktuelle Kennwort verwenden, das nur dann zurückgegeben wird, wenn die aktuelle Zeit größer oder gleich dem Wert ist, der von diesem Parameter zurückgegeben wird. Die Verwendung dieses Parameters wurde für Aufrufer entworfen, die keinen Wiederholungsversuch in der ausgehenden Logik haben, z. b. NTLM.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert Status \_ Success.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein NTSTATUS-Code. Weitere Informationen finden Sie unter [Rückgabewerte von LSA-Richtlinien Funktionen](management-return-values.md).

Sie können die [**lsantstatustowinerror**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) -Funktion verwenden, um den NTSTATUS-Code in einen Windows-Fehlercode zu konvertieren.

Wenn Sie mit der Verwendung der in den Parametern *CurrentPassword* und *previouspassword* zurückgegebenen Puffer fertig sind, können Sie diese freigeben, indem Sie die [**freelsaheap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) -Funktion aufrufen.

## <a name="remarks"></a>Bemerkungen

Die **getserviceaccountpassword** -Funktion kann in den folgenden Szenarien aufgerufen werden:

-   Aus den Anmelde Funktionen von Security Support Providers (SSP) sollte der SSP erkennen, dass das Kennwort des Dienst Kontos für die \_ \_ Anmeldung bei der Entität verwendet wird, und überprüfen, ob der Aufrufer über TCB-Berechtigungen verfügt oder ein Netzwerkdienst ist. Anschließend sollte der SSP zulassen, dass der Anmeldevorgang fortgesetzt wird, indem die aktuellen Anmelde Informationen abgerufen werden, indem die **getserviceaccountpassword** -Funktion mit dem **credfetchdefault** -Wert in der [**cred- \_ Fetch-**](cred-fetch.md) Enumeration aufgerufen wird.

-   Von SSPs in Ihren [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) -und [**Accept-SecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) -aufrufen. SSPs sollten erkennen, dass das \_ Kennwort des Dienst Kontos \_ für diese Aufrufe verwendet wird. wenn der Aufruf nicht primäre Anmelde Informationen ist, sollte der SSP sicherstellen, dass der Aufrufer entweder über eine TCB-Berechtigung verfügt oder ein Netzwerkdienst ist. Anschließend sollte der SSP die **getserviceaccountpassword** -Funktion mit dem Wert " **kredfetchdefault** " in der " [**Fed \_ Fetch**](cred-fetch.md) "-Enumeration aufrufen und den-Befehl fortsetzen. Wenn die **InitializeSecurityContext** -und die **Accept-SecurityContext** -Aufrufe fehlschlagen, sollte der SSP den aus dem vorherigen Aufruf von **getserviceaccountpassword** abgerufenen *filetimeablauf* verwenden und ihn als Eingabe für den Aufruf von **getserviceaccountpassword** mithilfe des **credfetchforced** -Werts in der **cred- \_ Fetch-** Enumeration verwenden. Wenn ein neues GMSA-Anmelde Informationssystem verfügbar ist, wird der zweite-Befehl mit neuen Anmelde Informationen erfolgreich ausgeführt, und der SSP sollte dann mit den neuen Anmelde Informationen erneut versuchen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 

