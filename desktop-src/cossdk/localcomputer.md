---
description: Enthält ein einzelnes -Objekt, das dem Computer entspricht, auf den Sie zugreifen. Dieses Objekt enthält Einstellungsinformationen auf Computerebene.
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
ms.openlocfilehash: b832da702942e8f84baee4303b7fa74a7fd74d683d62534cca619e8c7270e88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118813464"
---
# <a name="localcomputer-collection"></a>LocalComputer-Sammlung

Enthält ein einzelnes -Objekt, das dem Computer entspricht, auf den Sie zugreifen. Dieses Objekt enthält Einstellungsinformationen auf Computerebene. Wenn Sie die [**Verbinden-Methode**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-connect) für ein Objekt aufrufen, das aus der [**COMAdminCatalog-Klasse**](comadmincatalog.md) erstellt wurde, enthält das Objekt in der **LocalComputer** -Auflistung Informationen über den Remotecomputer, auf den Sie zugreifen.

Diese Sammlung unterstützt nicht die [**Add- und**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **LocalComputer-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**wurzel**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [ApplicationProxyRSN](#applicationproxyrsn)
-   [CISEnabled](#cisenabled)
-   [DCOMEnabled](#dcomenabled)
-   [DefaultAuthenticationLevel](#defaultauthenticationlevel)
-   [DefaultImpersonationLevel](#defaultimpersonationlevel)
-   [DefaultToInternetPorts](#defaulttointernetports)
-   [Beschreibung](#description)
-   [DSPartitionLookupEnabled](#dspartitionlookupenabled)
-   [InternetPortsListed](#internetportslisted)
-   [IsRouter](#isrouter)
-   [LoadBalancingCLSID](#loadbalancingclsid)
-   [LocalPartitionLookupEnabled](#localpartitionlookupenabled)
-   [Name](#name)
-   [Operatingsystem](#operatingsystem)
-   [PartitionsEnabled](#partitionsenabled)
-   [Ports](#defaulttointernetports)
-   [ResourcePoolingEnabled](#resourcepoolingenabled)
-   [RPCProxyEnabled](#rpcproxyenabled)
-   [SecureReferencesEnabled](#securereferencesenabled)
-   [SecurityTrackingEnabled](#securitytrackingenabled)
-   [SRPActivateAsActivatorChecks](#srpactivateasactivatorchecks)
-   [SRPRunningObjectChecks](#srprunningobjectchecks)
-   [TransactionTimeout](#transactiontimeout)

### <a name="applicationproxyrsn"></a>ApplicationProxyRSN



| Eingabe | Wert |
|----------------|------------------------------------------------------------|
| Beschreibung    | Remoteservername, der standardmäßig von Anwendungsproxies verwendet wird. |
| Zugriff         | ReadWrite                                                  |
| type           | String                                                     |
| Standard        | ""                                                         |
| Mindestsystem | Windows 2000                                               |



 

### <a name="cisenabled"></a>CISEnabled



| Eingabe | Wert |
|----------------|-----------------------------------------------------|
| Beschreibung    | Gibt an, ob COM-Internetdienste aktiviert sind. |
| Zugriff         | ReadWrite                                           |
| type           | Bool                                                |
| Standard        | Falsch                                               |
| Mindestsystem | Windows 2000                                        |



 

### <a name="dcomenabled"></a>DCOMEnabled



| Eingabe | Wert |
|----------------|---------------------------------------------|
| Beschreibung    | Legen Sie diese Option auf True fest, um DCOM auf dem Computer zu aktivieren. |
| Zugriff         | ReadWrite                                   |
| type           | Bool                                        |
| Standard        | Richtig                                        |
| Mindestsystem | Windows 2000                                |



 

### <a name="defaultauthenticationlevel"></a>DefaultAuthenticationLevel



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Authentifizierungsebene, die von Anwendungen verwendet wird, deren Authentifizierung auf Standard festgelegt ist. Die Werte entsprechen den RPC-Authentifizierungseinstellungen (Remote Procedure Call).                                                                                         |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                |
| type           | Long Possible values:COMAdminAuthenticationDefault (0)COMAdminAuthenticationNone (1) COMAdminAuthenticationConnect (2)COMAdminAuthenticationCall (3)COMAdminAuthenticationPacket (4)COMAdminAuthenticationIntegrity (5)COMAdminAuthenticationPrivacy (6) |
| Standard        | COMAdminAuthenticationConnect (2)                                                                                                                                                                                                                        |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                             |



 

> [!Note]  
> COMAdminAuthenticationDefault wird COMAdminAuthenticationConnect zugeordnet, wenn COM [**CoInitializeSecurity aufruft.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) Es wird empfohlen, die Konstanten in der Enumeration und nicht die numerischen Werte zu verwenden.

 

### <a name="defaultimpersonationlevel"></a>DefaultImpersonationLevel



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Die Identitätswechselebene, die zulässig ist, wenn keine festgelegt ist.                                                                                                               |
| Zugriff         | ReadWrite                                                                                                                                                     |
| type           | Lange mögliche Werte:COMAdminImpersonationAnonymous (1)COMAdminImpersonationIdentify (2)COMAdminImpersonationImpersonate (3)COMAdminImpersonationDelegate (4) |
| Standard        | COMAdminImpersonationIdentify (2)                                                                                                                             |
| Mindestsystem | Windows 2000                                                                                                                                                  |



 

> [!Note]  
> Es wird empfohlen, die Konstanten in der -Enumeration und nicht die numerischen Werte zu verwenden.

 

### <a name="defaulttointernetports"></a>DefaultToInternetPorts



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------|
| Beschreibung    | Bestimmt, ob der angegebene Standardporttyp Internet (True) oder Intranet (False) sein soll. |
| Zugriff         | ReadWrite                                                                                           |
| type           | Bool                                                                                                |
| Standard        | Falsch                                                                                               |
| Mindestsystem | Windows 2000                                                                                        |



 

### <a name="description"></a>Beschreibung



| Eingabe | Wert |
|----------------|--------------------------------|
| Beschreibung    | Eine Beschreibung des Computers. |
| Zugriff         | ReadWrite                      |
| type           | String                         |
| Standard        | ""                             |
| Mindestsystem | Windows 2000                   |



 

### <a name="dspartitionlookupenabled"></a>DSPartitionLookupEnabled



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob der Benutzer der Partitionszuordnungen in den Domänenspeicher eingecheckt wird. |
| Zugriff         | ReadWrite                                                                              |
| type           | Bool                                                                                   |
| Standard        | Richtig                                                                                   |
| Mindestsystem | Windows Server 2003                                                                    |



 

### <a name="internetportslisted"></a>InternetPortsListed



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Bestimmt, ob die in der Ports -Eigenschaft aufgeführten Ports für internet (True) oder für intranet (False) verwendet werden sollen. |
| Zugriff         | ReadWrite                                                                                                             |
| type           | Bool                                                                                                                  |
| Standard        | Falsch                                                                                                                 |
| Mindestsystem | Windows 2000                                                                                                          |



 

### <a name="isrouter"></a>IsRouter



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Legen Sie diese Einstellung auf True fest, wenn der Computer ein Router für den ClB-Dienst (Component Load Balancing) ist. Diese Eigenschaft kann nur auf True festgelegt werden, wenn der Lastenausgleichsdienst der Komponente derzeit auf dem Computer installiert ist. Andernfalls wird die Fehlermeldung COMADMIN \_ E REQUIRES DIFFERENT PLATFORM \_ \_ \_ angezeigt. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                           |
| type           | Bool                                                                                                                                                                                                                                                                                |
| Standard        | Falsch                                                                                                                                                                                                                                                                               |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                        |



 

Wenn diese Eigenschaft auf True festgelegt ist, wird der CLB-Server konfiguriert und beim Start gestartet. Der Server wird der ApplicationCluster-Sammlung hinzugefügt, wenn er noch nicht vorhanden ist.

### <a name="loadbalancingclsid"></a>LoadBalancingCLSID



| Eingabe | Wert |
|----------------|-------------------------------------|
| Beschreibung    | Die CLSID des objekts, das ausgeglichen werden soll. |
| Zugriff         | ReadWrite                           |
| type           | String                              |
| Standard        | NULL                                |
| Mindestsystem | Windows XP                          |



 

### <a name="localpartitionlookupenabled"></a>LocalPartitionLookupEnabled



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob der Benutzer der Partitionszuordnungen im lokalen Speicher eingecheckt wird. |
| Zugriff         | ReadWrite                                                                             |
| type           | Bool                                                                                  |
| Standard        | Richtig                                                                                  |
| Mindestsystem | Windows Server 2003                                                                   |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Name des Computers. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | WriteOnce                                                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                                                 |
| Standard        | "Arbeitsplatz"                                                                                                                                                                                                                                                          |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="operatingsystem"></a>OperatingSystem



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Das auf dem lokalen Computer installierte Betriebssystem.                                                                                                                                                                                                                                                                                                                                                                                                |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| type           | Long Possible values:COMAdminOSNotInitialized (0)COMAdminOSWindows3 \_ 1(1)COMAdminOSWindows9x (2)COMAdminOSWindows2000 (3)COMAdminOSWindows2000AdvancedServer (4)COMAdminOSWindows2000Unknown (5)COMAdminOSUnknownn (6)COMAdminOSWindowsXPPersonal (11)COMAdminOSWindowsXPProfessional (12)COMAdminOSWindowsNETStandardServer (13)COMAdminOSWindowsNETEnterpriseServer (14)COMAdminOSWindowsNETDatacenterServer (15)COMAdminOSWindowsNETWebServer (16) |
| Standard        | COMAdminOSNotInitialized (0)                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="partitionsenabled"></a>PartitionsEnabled



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Gibt an, ob COM+-Partitionen auf dem lokalen Computer verwendet werden können. Wenn diese Eigenschaft false ist, führt jeder Versuch, COM+-Partitionen zu verwenden, zu einem Fehler. |
| Zugriff         | ReadWrite                                                                                                                                               |
| type           | Bool                                                                                                                                                    |
| Standard        | Falsch                                                                                                                                                   |
| Mindestsystem | Windows Server 2003                                                                                                                                     |



 

### <a name="ports"></a>Ports



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Eine Zeichenfolge, die Ports beschreibt, die je nach InternetPortsListed-Eigenschaft für die Internet- oder Intranetnutzung gelten. Beispiel: "500-599: 600-800". |
| Zugriff         | ReadWrite                                                                                                                                               |
| type           | String                                                                                                                                                  |
| Standard        | ""                                                                                                                                                      |
| Mindestsystem | Windows 2000                                                                                                                                            |



 

### <a name="resourcepoolingenabled"></a>ResourcePoolingEnabled



| Eingabe | Wert |
|----------------|-------------------------------------|
| Beschreibung    | Ermöglicht die Verwendung von Ressourcenspendern. |
| Zugriff         | ReadWrite                           |
| type           | Bool                                |
| Standard        | Richtig                                |
| Mindestsystem | Windows 2000                        |



 

### <a name="rpcproxyenabled"></a>RPCProxyEnabled



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Steuert, ob der RPC-IIS-Proxy aktiviert ist. Der RPC-IIS-Proxy wird in Verbindung mit IIS verwendet, um Aufrufe an den RPC-Mechanismus von IIS weiter zu senden, und ist eines der Wichtigsten von COM-Internetdiensten, das durch Festlegen von CISEnabled auf True aktiviert wird. Weitere Informationen zu RPCProxyEnabled finden Sie unter [HTTP RPC Security](/windows/desktop/Rpc/rpc-over-http-security). |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                             |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                  |
| Standard        | Falsch                                                                                                                                                                                                                                                                                                                                                 |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                          |



 

### <a name="securereferencesenabled"></a>SecureReferencesEnabled



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Erzwingt auf DCOM-Computern, dass prozessübergreifende Aufrufe der [**Methoden IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) und [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) gesichert sind. |
| Zugriff         | ReadWrite                                                                                                                                                                 |
| type           | Bool                                                                                                                                                                      |
| Standard        | Falsch                                                                                                                                                                     |
| Mindestsystem | Windows 2000                                                                                                                                                              |



 

### <a name="securitytrackingenabled"></a>SecurityTrackingEnabled



| Eingabe | Wert |
|----------------|---------------------------------------------------------|
| Beschreibung    | Wird auf TRUE festgelegt, wenn die Sicherheitsnachverfolgung für Objekte aktiviert ist. |
| Zugriff         | ReadWrite                                               |
| type           | Bool                                                    |
| Standard        | Richtig                                                    |
| Mindestsystem | Windows 2000                                            |



 

### <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Bestimmt, wie die Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) Activate-as-Activator-Verbindungen verarbeitet. Bei True wird die SRP-Vertrauensebene, die für das Serverobjekt konfiguriert ist, mit der SRP-Vertrauensebene des Clientobjekts verglichen, und die höhere (strengere) Vertrauensebene wird zum Ausführen des Serverobjekts verwendet. Wenn false festgelegt ist, wird das Serverobjekt mit der SRP-Vertrauensebene des Clientobjekts ausgeführt, unabhängig von der SRP-Vertrauensebene, mit der der Server konfiguriert ist. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Standard        | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Bestimmt, wie die Softwareeinschränkungsrichtlinie (Software Restriction Policy, SRP) versucht, Verbindungen mit vorhandenen Prozessen herzustellen. Wenn false festgelegt ist, werden Versuche, eine Verbindung mit ausgeführten Objekten herzustellen, nicht auf geeignete SRP-Vertrauensebenen überprüft. Wenn der Wert auf True festgelegt ist, muss das ausgeführte Objekt eine gleiche oder eine höhere (strengere) SRP-Vertrauensebene als das Clientobjekt haben. Beispielsweise kann ein Clientobjekt mit einer uneingeschränkten SRP-Vertrauensebene keine Verbindung mit einem ausgeführten Objekt mit einer nicht zu verwendenden SRP-Vertrauensebene herstellen. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| type           | Bool                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Standard        | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Mindestsystem | Windows XP                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

### <a name="transactiontimeout"></a>TransactionTimeout



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Sollte auf einen ausreichenden Wert in Sekunden festgelegt werden, wenn Sie zahlreiche Vorgänge innerhalb einer Transaktion tun. Der Standard-Time out-Zeitraum beträgt 60 Sekunden, und der maximale Time out-Zeitraum beträgt 3.600 Sekunden (1 Stunde). Wenn Sie diese Eigenschaft auf 0 festlegen, werden Time outs für Transaktionen deaktiviert. Diese Eigenschaft kann von einzelnen Komponenten überschrieben werden, indem die ComponentTransactionTimeout-Eigenschaft der [**Components-Auflistung verwendet**](components.md) wird. |
| Zugriff         | ReadWrite                                                                                                                                                                                                                                                                                                                                                                                                                                |
| type           | Long (0-3600)                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Standard        | 60                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="example"></a>Beispiel

Im folgenden Microsoft Visual Basic-Beispiel wird veranschaulicht, wie Sie mithilfe der **LocalComputer-Sammlung** des Remotecomputers eine Verbindung mit einem Remotecomputer herstellen und dessen SecurityTrackingEnabled-Eigenschaft erhalten. Um dieses Beispiel zu verwenden, fügen Sie die COM+-Administratortypbibliothek als Verweis auf Ihr Visual Basic hinzu.


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



Um die Funktion zu verwenden, geben Sie einen Zeichenfolgenwert für den Namen des Remotecomputers an. Der folgende Visual Basic zeigt, wie Sie eine Verbindung mit dem Computer namens "RemoteComputerName" herstellen.


```VB
Sub Main()
    If Not RemoteComputerConnect("RemoteComputerName") Then
        MsgBox "RemoteComputerConnect failed."
    End If
End Sub

```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
