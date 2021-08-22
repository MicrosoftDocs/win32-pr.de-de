---
title: Session.Enumerate-Methode (WSManDisp.h)
description: Enumeriert eine Tabelle, Datensammlung oder Protokollressource.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Aufzählen der Windows-Remoteverwaltung
- Enumerate method Windows-Remoteverwaltung , Session object
- Sitzungsobjekt Windows-Remoteverwaltung , Enumerate-Methode
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc40a45cc28179acd8e5dc9fff17df8b8accddd8dffda3ea299571e11d46564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642630"
---
# <a name="sessionenumerate-method"></a>Session.Enumerate-Methode

Enumeriert eine Tabelle, Datensammlung oder Protokollressource. Um eine Abfrage zu erstellen, schließen Sie einen *Filterparameter* und einen *Dialektparameter* in eine Enumeration ein. Sie können auch ein [**ResourceLocator-Objekt verwenden,**](resourcelocator.md) um Abfragen zu erstellen. Weitere Informationen finden Sie unter Auflisten oder Auflisten aller Instanzen [einer Ressource.](enumerating-or-listing-all-instances-of-a-resource.md)

## <a name="syntax"></a>Syntax


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resourceUri* \[ In\]
</dt> <dd>

Der Bezeichner der abzurufenden Ressource.

Dieser Parameter kann eine der folgenden Elemente enthalten:

-   Der URI der Ressource.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Ein [**ResourceLocator-Objekt.**](resourcelocator.md)
-   Eine [*WS-Adressierungsendpunktreferenz,*](windows-remote-management-glossary.md) wie im protokollbasierten WS-Management beschrieben. Weitere Informationen zur öffentlichen Spezifikation für WS-Management-Protokoll [finden](ws-management-protocol.md)Sie auf der [Indexseite für Verwaltungsspezifikationen.](/previous-versions/dotnet/articles/ms951267(v=msdn.10))

</dd> <dt>

*Filter* \[ in, optional\]
</dt> <dd>

Ein Filter, der definiert, welche Elemente in der Ressource von der -Enumeration zurückgegeben werden. Wenn die Ressource aufzählt wird, werden nur die Elemente zurückgegeben, die den Filterkriterien entsprechen. Durch das *Hinzufügen eines Filterparameters* und *eines Dialektparameters* in eine Enumeration wird die Enumeration in eine Abfrage konvertiert. Ein Beispiel finden Sie unter [Abfragen für bestimmte Instanzen einer Ressource.](querying-for-specific-instances-of-a-resource.md)

Wenn Sie über ein [**ResourceLocator-Objekt**](resourcelocator.md) für den *resourceURI-Parameter* verfügen, sollte dieser Parameter nicht verwendet werden.

</dd> <dt>

*Dialekt* \[ in, optional\]
</dt> <dd>

Die vom Filter verwendete Sprache. [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), eine Teilmenge von SQL, die von WMI verwendet wird, ist die einzige unterstützte Sprache.

Wenn Sie über ein [**ResourceLocator-Objekt**](resourcelocator.md) für den *resourceURI-Parameter* verfügen, sollte dieser Parameter nicht verwendet werden.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Ein Parameter, der ein Flag in der **\_ \_ WSManEnumFlags-Enumeration enthalten** muss. Weitere Informationen finden Sie unter [Enumerationskonst constants](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Enumeratorobjekt,**](enumerator.md) das die Ergebnisse der -Enumeration enthält.

## <a name="remarks"></a>Hinweise

Weitere Informationen zum Einschränken von Netzwerkaufrufen während einer Enumeration finden Sie unter der [**BatchItems-Eigenschaft.**](session-batchitems.md)

Beachten Sie Folgendes: Wenn die Flags die [**Enumerationskonst constants**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** oder **WSManFlagHierarchyShallow** enthalten, gibt der Windows-Remoteverwaltung-Dienst den Fehlercode **ERROR \_ WSMAN \_ POLYMORPHISM \_ MODE \_ UNSUPPORTED** zurück.

Wenn ein Filter angegeben wird, muss es sich um ein gültiges Dokument in Bezug auf das Schema der Ressource handelt. Der Dialektparameter ist optional. Wenn die Filterzeichenfolge jedoch mit < beginnt, aber kein XML-Fragment ist, schließen Sie entweder den *Dialektparameter* ein oder legen das **WSManFlagNonXmlText-Flag** im *flags-Parameter* fest. Weitere Informationen finden Sie unter [**Enumerationskonst constants**](enumeration-constants.md).

Die entsprechende C++-Methode ist [**IWSManSession::Enumerate.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden die [**Win32 \_ LogicalDisk-Instanzen**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) auf einem Remotecomputer aufzählt, der durch den vollqualifizierten Domänennamen (servername.domain.com. Beachten Sie, dass ausstehende Enumerationsanforderungen durch das Freiwerden des Enumerationsobjekts frei werden. Die DisplayOutput-Unterroutine verwendet die XML-Transformationsdatei des Winrm-Befehlszeilentools (WsmTxt.xsl), um die Daten in tabellarischer Form ausausgaben.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzung**](session.md)
</dt> <dt>

[Abfragen bestimmter Instanzen einer Ressource](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**BatchItems**](session-batchitems.md)
</dt> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

