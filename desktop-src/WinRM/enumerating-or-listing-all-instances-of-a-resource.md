---
title: Auflisten oder Auflisten aller Instanzen einer Ressource
description: Die Session.Enumerate-Methode ist Windows Remoteverwaltungsansatz zum Abrufen aller Instanzen einer angegebenen Ressource.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1f510d0e0cc8115ca4dca7c7e46dd5e987ef0dd15dd4fa7d92e47d737e467d8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679990"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Auflisten oder Auflisten aller Instanzen einer Ressource

Die [**Session.Enumerate-Methode**](session-enumerate.md) ist Windows Remoteverwaltungsansatz zum Abrufen aller Instanzen einer angegebenen Ressource.

Die [**Session.Enumerate-Methode**](session-enumerate.md) erhält keine Auflistung in einem [**SWbemObjectSet-Objekt**](/windows/desktop/WmiSdk/swbemobjectset) wie einen [**SWbemService.ExecQuery-Aufruf**](/windows/desktop/WmiSdk/swbemservices-execquery) mit einer [WMI-Abfrage](/windows/desktop/WmiSdk/querying-wmi) als Parameter (z. B. ) oder einen Aufruf einer Methode wie `ExecQuery("SELECT * from Win32_LogicalDisk")` [**SWbemObject.Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-). **Session.Enumerate** und die [**Enumerator-Objektmethoden**](enumerator.md) ähneln viel mehr dem Vorgang des Skripterstellungsobjekts [TextStream,](/previous-versions//312a5kbt(v=vs.85)) das zum Lesen von Dateien als Stream verwendet wird.

Um Dateien als Textstream zu lesen, müssen Sie das [Skriptobjekt TextStream](/previous-versions//312a5kbt(v=vs.85)) erstellen und die [TextStream.Readline-Methode](/previous-versions//h7se9d4f(v=vs.85)) aufrufen, um jede Zeile der Datei zu lesen. Auf ähnliche Weise können Sie die [**Session.Enumerate-Methode**](session-enumerate.md) aufrufen, um ein [**Enumeratorobjekt**](enumerator.md) zu erhalten, und die [**Enumerator.ReadItem-Methode**](enumerator-readitem.md) aufrufen, um das nächste Element zu erhalten. Wie beim Lesen aus der Textdatei können Sie die [**Enumerator.AtEndOfStream-Eigenschaft**](enumerator-atendofstream.md) aufrufen, um zu überprüfen, ob Sie das Ende der Datenelemente erreicht haben.

**So enumerieren Sie eine Ressource**

1.  Erstellen Sie eine Sitzung.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Set objWsman = CreateObject( "WSMan.Automation" )
    Set objSession = objWsman.CreateSession( "https://" _
        & RemoteComputer )
    ```

    

2.  Erstellen Sie den URI, um die Ressource zu identifizieren.

    ```VB
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
                 "wmi/root/cimv2/Win32_ScheduledJob"
    ```

    

3.  Rufen Sie [**die Session.Enumerate-Methode**](session-enumerate.md) auf. Dieser Aufruf startet eine Enumeration. In WinRM erhält ein Enumerationsvorgang eine Auflistung nicht auf die gleiche Weise wie WMI. Stattdessen richtet die **Session.Enumerate-Methode** einen WS-Management-Enumerationskontext ein, der im [**Enumeratorobjekt verwaltet**](enumerator.md) wird.

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Rufen Sie [**die Enumerator.ReadItem-Methode auf,**](enumerator-readitem.md) um das nächste Element der Ergebnisse zu erhalten. Im WS-Management entspricht dies dem Pullvorgang. Verwenden Sie [**die Enumerator.AtEndOfStream-Methode**](enumerator-atendofstream.md) als Steuerelement, um zu wissen, wann das Lesen nicht mehr möglich ist.

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

Das folgende VBScript-Codebeispiel zeigt das vollständige Skript.


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set EnumJobs = objSession.Enumerate( strResource )
NumOfJobs = 0
While Not EnumJobs.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( EnumJobs.ReadItem ) 
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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Windows Remoteverwaltungsreferenz](windows-remote-management-reference.md)
</dt> </dl>

 

 