---
title: Session. Enumerate-Methode (WSManDisp. h)
description: Listet eine Tabelle, eine Datensammlung oder eine Protokoll Ressource auf.
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- Enumerate-Methode Windows-Remoteverwaltung
- Enumerate-Methode Windows-Remoteverwaltung, Session-Objekt
- Sitzungs Objekt Windows-Remoteverwaltung, Enumerate-Methode
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
ms.openlocfilehash: ca6b66b910251c641832cde3ddd93d6479f66be7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040379"
---
# <a name="sessionenumerate-method"></a>Session. Enumerate-Methode

Listet eine Tabelle, eine Datensammlung oder eine Protokoll Ressource auf. Um eine Abfrage zu erstellen, schließen Sie einen *Filter* Parameter und einen *Dialekt* Parameter in eine Enumeration ein. Sie können auch ein [**ResourceLocator**](resourcelocator.md) -Objekt verwenden, um Abfragen zu erstellen. Weitere Informationen finden Sie unter [auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md).

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

*resourceUri* \[ in\]
</dt> <dd>

Der Bezeichner der abzurufenden Ressource.

Dieser Parameter kann einen der folgenden Parameter enthalten:

-   Der URI der Ressource.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   Ein [**ResourceLocator**](resourcelocator.md) -Objekt.
-   Ein [*WS-adressierungsend*](windows-remote-management-glossary.md) Punkt Verweis, wie im WS-Management Protocol-Standard beschrieben. Weitere Informationen zur öffentlichen Spezifikation für [WS-Management-Protokoll](ws-management-protocol.md)finden Sie auf der [Seite Verwaltungs Spezifikationen Index](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*Filter* \[ in, optional\]
</dt> <dd>

Ein Filter, der definiert, welche Elemente in der Ressource von der-Enumeration zurückgegeben werden. Wenn die Ressource aufgelistet ist, werden nur die Elemente zurückgegeben, die mit den Filterkriterien übereinstimmen. Wenn Sie einen *Filter* Parameter und einen *Dialekt* Parameter in eine Enumeration einschließen, wird die Enumeration in eine Abfrage konvertiert. Ein Beispiel finden Sie unter [Abfragen für bestimmte Instanzen einer Ressource](querying-for-specific-instances-of-a-resource.md).

Wenn Sie über ein [**ResourceLocator**](resourcelocator.md) -Objekt für den *resourceUri* -Parameter verfügen, sollte dieser Parameter nicht verwendet werden.

</dd> <dt>

*Dialekt* \[ in, optional\]
</dt> <dd>

Die Sprache, die vom Filter verwendet wird. [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi), eine Teilmenge von SQL, die von WMI verwendet wird, ist die einzige unterstützte Sprache.

Wenn Sie über ein [**ResourceLocator**](resourcelocator.md) -Objekt für den *resourceUri* -Parameter verfügen, sollte dieser Parameter nicht verwendet werden.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Ein Parameter, der in der **\_ \_ wsmanenumflags** -Enumeration ein Flag enthalten muss. Weitere Informationen finden Sie unter [Enumerationskonstanten](enumeration-constants.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein [**Enumeratorobjekt**](enumerator.md) , das die Ergebnisse der-Enumeration enthält.

## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum Einschränken von Netzwerk aufrufen während einer Enumeration finden Sie in der Eigenschaft [**batchitems**](session-batchitems.md) .

Beachten Sie, dass wenn die Flags die [**Enumerationskonstanten**](enumeration-constants.md) **wsmanflaghierarchydeepbasepropsonly** oder **wsmanflaghierarchyflache** enthalten, Windows-Remoteverwaltung Dienst den Fehlercode **Fehler \_ WSMAN \_ Polymorphism- \_ Modus \_ nicht unterstützt** zurückgibt.

Wenn ein Filter angegeben wird, muss es sich um ein gültiges Dokument in Bezug auf das Schema der Ressource handeln. Der Dialekt Parameter ist optional. Wenn die Filter Zeichenfolge jedoch mit < beginnt, aber kein XML-Fragment ist, fügen Sie entweder den *Dialekt* Parameter ein, oder legen Sie das **wsmanflagnonxmltext** -Flag im *Flags* -Parameter fest. Weitere Informationen finden Sie unter [**Enumerationskonstanten**](enumeration-constants.md).

Die entsprechende C++-Methode ist [**iwsmansession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Codebeispiel werden die [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Instanzen auf einem Remote Computer aufgelistet, der durch den voll qualifizierten Domänen Namen (Servername.Domain.com) angegeben wird. Beachten Sie, dass das Freigeben des Enumerationsobjekt ausstehende enumerationsanforderungen löscht. Die DisplayOutput-Unterroutine verwendet die XML-Transformations Datei (WsmTxt. Xsl) des WinRM-Befehlszeilen Tools, um die Daten in tabellarischer Form auszugeben.


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
| Header<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sitzung**](session.md)
</dt> <dt>

[Abfragen für bestimmte Instanzen einer Ressource](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**Batchitems**](session-batchitems.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

