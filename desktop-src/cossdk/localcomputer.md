---
description: Enthält ein einzelnes-Objekt, das dem Computer entspricht, auf den Sie zugreifen. Dieses Objekt enthält Einstellungs Informationen auf Computer Ebene.
ms.assetid: 75f14cad-9cd5-44a6-9afa-2c8ad1e87027
title: LocalComputer-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocalComputer
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4e1ce08f3bf1fef74af0d77ada15716abb4530a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749000"
---
# <a name="localcomputer-collection"></a>LocalComputer-Sammlung

Enthält ein einzelnes-Objekt, das dem Computer entspricht, auf den Sie zugreifen. Dieses Objekt enthält Einstellungs Informationen auf Computer Ebene. Wenn Sie die [**Connect**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) -Methode für ein Objekt aufrufen, das aus der [**comadmincatalog**](comadmincatalog.md) -Klasse erstellt wurde, enthält das-Objekt in der **LocalComputer** -Auflistung Informationen über den Remote Computer, auf den Sie zugreifen.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts nicht.

## <a name="members"></a>Member

Die **LocalComputer** -Sammlung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Mitglieder.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Applicationproxyrsn](#applicationproxyrsn)
-   [Cisenabled](#cisenabled)
-   [Dcomaktiviert](#dcomenabled)
-   [DefaultAuthenticationLevel](#defaultauthenticationlevel)
-   [DefaultImpersonationLevel](#defaultimpersonationlevel)
-   [Defaultdeinternetports](#defaulttointernetports)
-   [Beschreibung](#description)
-   [Dspartitionlookupabled](#dspartitionlookupenabled)
-   [Internetportslisted](#internetportslisted)
-   [Isrouter](#isrouter)
-   [Loadbalancingclsid](#loadbalancingclsid)
-   [Localpartitionlookupabled](#localpartitionlookupenabled)
-   [Name](#name)
-   [OperatingSystem](#operatingsystem)
-   [Partitionsenabled](#partitionsenabled)
-   [Ports](#defaulttointernetports)
-   [Resourcepoolingenabled](#resourcepoolingenabled)
-   [Rpcproxyaktivierte](#rpcproxyenabled)
-   [Securereferencesaktiviert](#securereferencesenabled)
-   [Securitytrackingenabled](#securitytrackingenabled)
-   [Srpactivateasactivatorchecks](#srpactivateasactivatorchecks)
-   [Srprunningobjectchecks](#srprunningobjectchecks)
-   [TransactionTimeout](#transactiontimeout)

### <a name="applicationproxyrsn"></a>Applicationproxyrsn



| Eingabe | Wert |
|----------------|------------------------------------------------------------|
| BESCHREIBUNG    | Standardmäßig von Anwendungs Proxys verwendeter Remote Servername. |
| Access         | ReadWrite                                                  |
| type           | String                                                     |
| Standard        | ""                                                         |
| Minimalsystem | Windows 2000                                               |



 

### <a name="cisenabled"></a>Cisenabled



| Eingabe | Wert |
|----------------|-----------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob com-Internet Dienste aktiviert sind. |
| Access         | ReadWrite                                           |
| type           | Bool                                                |
| Standard        | Falsch                                               |
| Minimalsystem | Windows 2000                                        |



 

### <a name="dcomenabled"></a>Dcomaktiviert



| Eingabe | Wert |
|----------------|---------------------------------------------|
| BESCHREIBUNG    | Legen Sie diese Option auf true fest, um DCOM auf dem Computer zu aktivieren |
| Access         | ReadWrite                                   |
| type           | Bool                                        |
| Standard        | Richtig                                        |
| Minimalsystem | Windows 2000                                |



 

### <a name="defaultauthenticationlevel"></a>DefaultAuthenticationLevel



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Authentifizierungs Ebene, die von Anwendungen verwendet wird, deren Authentifizierung auf Standard festgelegt ist. Die Werte entsprechen den Authentifizierungs Einstellungen für Remote Prozedur Aufrufe (RPC).                                                                                         |
| Access         | ReadWrite                                                                                                                                                                                                                                                |
| type           | Lange mögliche Werte: comadminauthenticationdefault (0) comadminauthenticationnone (1) comadminauthenticationconnect (2) comadminauthentication-Aufruf (3) comadminauthenticationpacket (4) comadminauthenticationintegrity (5) comadminauthenticationprivacy (6) |
| Standard        | Comadminauthenticationconnect (2)                                                                                                                                                                                                                        |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                             |



 

> [!Note]  
> Comadminauthenticationdefault wird comadminauthenticationconnect zugeordnet, wenn com [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)aufruft. Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.

 

### <a name="defaultimpersonationlevel"></a>DefaultImpersonationLevel



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Die Identitätswechsel Ebene, um zuzulassen, wenn eine nicht festgelegt ist.                                                                                                               |
| Access         | ReadWrite                                                                                                                                                     |
| type           | Lange mögliche Werte: comadminimpersonationanonymous (1) comadminimpersonationidentifiout (2) comadminimpersonationidentität (3) comadminimpersonationdelegat (4) |
| Standard        | Comadminimpersonationidentifi(2)                                                                                                                             |
| Minimalsystem | Windows 2000                                                                                                                                                  |



 

> [!Note]  
> Es wird empfohlen, die Konstanten in der-Enumeration und nicht die numerischen Werte zu verwenden.

 

### <a name="defaulttointernetports"></a>Defaultdeinternetports



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob der Standardtyp des angegebenen Ports Internet (true) oder Intranet (false) sein soll. |
| Access         | ReadWrite                                                                                           |
| type           | Bool                                                                                                |
| Standard        | Falsch                                                                                               |
| Minimalsystem | Windows 2000                                                                                        |



 

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|--------------------------------|
| BESCHREIBUNG    | Eine Beschreibung des Computers. |
| Access         | ReadWrite                      |
| type           | String                         |
| Standard        | ""                             |
| Minimalsystem | Windows 2000                   |



 

### <a name="dspartitionlookupenabled"></a>Dspartitionlookupabled



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob der Benutzer der Partitions Zuordnungen in den Domänen Speicher eingecheckt wird. |
| Access         | ReadWrite                                                                              |
| type           | Bool                                                                                   |
| Standard        | Richtig                                                                                   |
| Minimalsystem | Windows Server 2003                                                                    |



 

### <a name="internetportslisted"></a>Internetportslisted



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, ob die in der Eigenschaft Ports aufgelisteten Ports für das Internet (true) oder für das Intranet (false) verwendet werden sollen. |
| Access         | ReadWrite                                                                                                             |
| type           | Bool                                                                                                                  |
| Standard        | Falsch                                                                                                                 |
| Minimalsystem | Windows 2000                                                                                                          |



 

### <a name="isrouter"></a>Isrouter



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Legen Sie diese Einstellung auf true fest, wenn der Computer ein Router für den CLB-Dienst (Component Load Balancing) ist. Diese Eigenschaft kann nur auf "true" festgelegt werden, wenn der Komponenten Lastenausgleich-Dienst derzeit auf dem Computer installiert ist. Andernfalls erfordert IT-Fehler mit COMAdmin \_ E eine \_ \_ andere \_ Plattform. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                           |
| type           | Bool                                                                                                                                                                                                                                                                                |
| Standard        | Falsch                                                                                                                                                                                                                                                                               |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                        |



 

Wenn diese Eigenschaft auf true festgelegt ist, wird der CLB-Server konfiguriert und beim Start gestartet. Der Server wird der ApplicationCluster-Sammlung hinzugefügt, wenn er nicht bereits vorhanden ist.

### <a name="loadbalancingclsid"></a>Loadbalancingclsid



| Eingabe | Wert |
|----------------|-------------------------------------|
| BESCHREIBUNG    | Die CLSID des-Objekts, das ausgeglichen werden soll. |
| Access         | ReadWrite                           |
| type           | String                              |
| Standard        | NULL                                |
| Minimalsystem | Windows XP                          |



 

### <a name="localpartitionlookupenabled"></a>Localpartitionlookupabled



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob der Benutzer der Partitions Zuordnungen in den lokalen Speicher eingecheckt wird. |
| Access         | ReadWrite                                                                             |
| type           | Bool                                                                                  |
| Standard        | Richtig                                                                                  |
| Minimalsystem | Windows Server 2003                                                                   |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name des Computers. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                                                 |
| Standard        | "Arbeitsplatz"                                                                                                                                                                                                                                                          |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a>OperatingSystem



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Das auf dem lokalen Computer installierte Betriebssystem.                                                                                                                                                                                                                                                                                                                                                                                                |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| type           | Lange mögliche Werte: comadminosnotinitialized (0) COMAdminOSWindows3 \_ 1 (1) COMAdminOSWindows9x (2) COMAdminOSWindows2000 (3) COMAdminOSWindows2000AdvancedServer (4) COMAdminOSWindows2000Unknown (5) comadminosunknown (6) comadminoswindowsxppersonal (11) comadminoswindowsxpprofessional (12) comadminoswindowsnetstandardserver (13) comadminoswindowsnetenterpriseserver (14) comadminoswindowsnetdatacenterserver (15) comadminoswindowsnetwebserver (16) |
| Standard        | Comadminosnotinitialized (0)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a>Partitionsenabled



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob COM+-Partitionen auf dem lokalen Computer verwendet werden können. Wenn diese Eigenschaft false ist, führt jeder Versuch, com+-Partitionen zu verwenden, zu einem Fehler. |
| Access         | ReadWrite                                                                                                                                               |
| type           | Bool                                                                                                                                                    |
| Standard        | Falsch                                                                                                                                                   |
| Minimalsystem | Windows Server 2003                                                                                                                                     |



 

### <a name="ports"></a>Ports



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Eine Zeichenfolge, die Ports für die Internet-oder Intranetverwendung beschreibt, abhängig von der internetportslisted-Eigenschaft. Beispiel: "500-599:600-800". |
| Access         | ReadWrite                                                                                                                                               |
| type           | String                                                                                                                                                  |
| Standard        | ""                                                                                                                                                      |
| Minimalsystem | Windows 2000                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a>Resourcepoolingenabled



| Eingabe | Wert |
|----------------|-------------------------------------|
| BESCHREIBUNG    | Ermöglicht die Verwendung von Ressourcen Spendern. |
| Access         | ReadWrite                           |
| type           | Bool                                |
| Standard        | Richtig                                |
| Minimalsystem | Windows 2000                        |



 

### <a name="rpcproxyenabled"></a>Rpcproxyaktivierte



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Steuert, ob der RPC-IIS-Proxy aktiviert ist. Der RPC-IIS-Proxy wird zusammen mit IIS verwendet, um Aufrufe an den RPC-Mechanismus von IIS weiterzuleiten. dabei handelt es sich um eines der Kernteile von com-Internet Diensten, die durch Festlegen von cisenabled auf true aktiviert werden. Weitere Informationen zu rpcproxyaktiviertem finden Sie unter [http-RPC-Sicherheit](/windows/desktop/Rpc/rpc-over-http-security). |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                             |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                  |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                                                                 |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a>Securereferencesaktiviert



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Erzwingt in DCOM-Computern, dass prozessübergreifende Aufrufe von [**IUnknown:: adressf**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) -und [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) -Methoden gesichert werden. |
| Access         | ReadWrite                                                                                                                                                                 |
| type           | Bool                                                                                                                                                                      |
| Standard        | Falsch                                                                                                                                                                     |
| Minimalsystem | Windows 2000                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a>Securitytrackingenabled



| Eingabe | Wert |
|----------------|---------------------------------------------------------|
| BESCHREIBUNG    | Auf "true" festgelegt, wenn die Sicherheitsüberwachung für Objekte aktiviert ist. |
| Access         | ReadWrite                                               |
| type           | Bool                                                    |
| Standard        | Richtig                                                    |
| Minimalsystem | Windows 2000                                            |



 

### <a name="srpactivateasactivatorchecks"></a>Srpactivateasactivatorchecks



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, wie die Software Einschränkungs Richtlinie (Software Einschränkungs Richtlinie, SRP) Aktivierungs-as-activatorverbindungen behandelt. Wenn diese Einstellung auf true festgelegt ist, wird die für das Server Objekt konfigurierte SRP-Vertrauens Ebene mit der SRP-Vertrauens Ebene des Client Objekts verglichen, und die höhere (strengere) Vertrauens Ebene wird zum Ausführen des Server Objekts verwendet. Wenn false festgelegt ist, wird das Server Objekt mit der SRP-Vertrauens Ebene des Client Objekts ausgeführt, unabhängig von der SRP-Vertrauens Ebene, mit der der Server konfiguriert ist. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Standard        | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a>Srprunningobjectchecks



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Bestimmt, wie die Software Einschränkungs Richtlinie (SRP) Verbindungsversuche mit vorhandenen Prozessen behandelt. Wenn der Wert auf false festgelegt ist, werden Verbindungsversuche mit laufenden Objekten nicht auf die entsprechenden SRP-Vertrauens Ebenen geprüft. Wenn der Wert auf true festgelegt ist, muss das laufende Objekt eine gleichmäßige oder höhere (strengere) SRP-Vertrauens Ebene aufweisen als das Client Objekt. Beispielsweise kann ein Client Objekt mit einer uneingeschränkten SRP-Vertrauens Ebene keine Verbindung mit einem laufenden Objekt mit einer unzulässigen SRP-Vertrauens Ebene herstellen. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Standard        | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Minimalsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a>TransactionTimeout



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Sollte auf einen ausreichenden Wert in Sekunden festgelegt werden, wenn Sie zahlreiche Vorgänge innerhalb einer Transaktion durchgeführt haben. Der Standard Timeout Zeitraum beträgt 60 Sekunden, und der maximale Timeout Zeitraum beträgt 3600 Sekunden (1 Stunde). Wenn Sie diese Eigenschaft auf 0 festlegen, werden Transaktions Timeouts deaktiviert. Diese Eigenschaft kann von einzelnen Komponenten überschrieben werden, indem die componenttransaktiontimeout-Eigenschaft der [**Components**](components.md) -Auflistung verwendet wird. |
| Access         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                |
| type           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Standard        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a>Beispiel

Im folgenden Microsoft Visual Basic Beispiel wird veranschaulicht, wie Sie eine Verbindung mit einem Remote Computer herstellen und seine securitytrackingenabled-Eigenschaft mithilfe der **LocalComputer** -Sammlung des Remote Computers erhalten. Um dieses Beispiel zu verwenden, fügen Sie die com+ admin-Typbibliothek als Verweis auf Ihr Visual Basic Projekt hinzu.


```VB
Function RemoteComputerConnect(strComputer As String _
) As Boolean  ' Return False if any errors occur.
    
    RemoteComputerConnect = False   ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim boolSTE As Boolean
    Dim objCatalog As COMAdminCatalog
    Dim objRemoteRootColl As COMAdminCatalogCollection
    Dim objRemoteComputerColl As COMAdminCatalogCollection
    Dim objRemoteComputerItem As COMAdminCatalogObject
    
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objRemoteRootColl = objCatalog.Connect(strComputer)
    Set objRemoteComputerColl = objRemoteRootColl.GetCollection( _
      "LocalComputer", objRemoteRootColl.Name)
    objRemoteComputerColl.Populate
    Set objRemoteComputerItem = objRemoteComputerColl.Item(0)
    boolSTE = objRemoteComputerItem.Value("SecurityTrackingEnabled")
    If boolSTE Then
        MsgBox "Security Tracking is enabled on " & strComputer
    Else
        MsgBox "Security Tracking is NOT enabled on " & strComputer
    End If

    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
    RemoteComputerConnect = True  ' Successful end to procedure
    Exit Function

My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objRemoteComputerItem = Nothing
    Set objRemoteComputerColl = Nothing
    Set objRemoteRootColl = Nothing
    Set objCatalog = Nothing
End Function


```



Um die Funktion zu verwenden, geben Sie einen Zeichen folgen Wert für den Namen des Remote Computers an. Der folgende Visual Basic Code zeigt, wie Sie eine Verbindung mit dem Computer "Remotecomputername" herstellen.


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
