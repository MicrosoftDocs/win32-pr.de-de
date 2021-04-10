---
title: Enumerator. ReadItem-Methode (WSManDisp. h)
description: Ruft ein Element aus der Ressource ab und gibt eine XML-Darstellung des Elements zurück.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- ReadItem-Methode Windows-Remoteverwaltung
- ReadItem-Methode Windows-Remoteverwaltung, Enumeratorobjekt
- Enumeratorobjekt Windows-Remoteverwaltung, ReadItem-Methode
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040380"
---
# <a name="enumeratorreaditem-method"></a>Enumerator. ReadItem-Methode

Ruft ein Element aus der Ressource ab und gibt eine XML-Darstellung des Elements zurück.

## <a name="syntax"></a>Syntax


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*resource* 
</dt> <dd>

Der URI des Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die XML-Darstellung des Elements.

## <a name="remarks"></a>Bemerkungen

Um die Anzahl der gelesenen Elemente einzuschränken, legen Sie die Eigenschaft [**Session.Batchitems**](session-batchitems.md) ) fest.

Beachten Sie, dass die Freigabe des Enumerationsobjekt alle ausstehenden enumerationsanforderungen bereinigt.

Die [**Session. Enumerate**](session-enumerate.md) -Methode ruft eine Auflistung nicht auf die gleiche Weise ab, wie eine [WMI-Abfrage](/windows/desktop/WmiSdk/querying-wmi), wie z `SELECT * from Win32_LogicalDisk` . b., eine Auflistung in einem [**errbewbjectset**](/windows/desktop/WmiSdk/swbemobjectset)zurückgibt. Um eine Datei als Textstream zu lesen, erstellen Sie das Skript- [Textstream](/previous-versions//312a5kbt(v=vs.85)) -Objekt, und rufen Sie die [Textstream. read line](/previous-versions//h7se9d4f(v=vs.85)) -Methode auf, um jede Zeile der Datei zu lesen. Auf ähnliche Weise rufen Sie die **Session. Enumerate** -Methode auf, um ein [**Enumeratorobjekt**](enumerator.md) zu erhalten, und rufen dann die **Enumerator. ReadItem** -Methode auf. Wie beim Lesen aus der Textdatei können Sie die [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) -Eigenschaft überprüfen, um zu überprüfen, ob Sie das Ende der Datenelemente erreicht haben.

## <a name="examples"></a>Beispiele

Im folgenden VBScript-Beispiel wird die [**Session. Enumerate**](session-enumerate.md) -Methode aufgerufen, um eine Liste geplanter Aufträge abzurufen. Die DisplayOutput-Unterroutine verwendet das WinRM-Befehlszeilen Tool XML Transform File (WsmTxt. Xsl), um die Daten in tabellarischer Form auszugeben.


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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

[**Enumerator**](enumerator.md)
</dt> <dt>

[Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

