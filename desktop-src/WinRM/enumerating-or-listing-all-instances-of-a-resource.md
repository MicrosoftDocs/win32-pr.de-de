---
title: Auflisten oder Auflisten aller Instanzen einer Ressource
description: Die Session. Enumerate-Methode ist der Windows-Remoteverwaltung Ansatz zum Abrufen aller Instanzen einer angegebenen Ressource.
ms.assetid: c50c37bf-e19a-473b-8d27-ab3bb4ec86a0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54587ce97ec6ed5e87af8b0424a6a18d684f7698
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209306"
---
# <a name="enumerating-or-listing-all-instances-of-a-resource"></a>Auflisten oder Auflisten aller Instanzen einer Ressource

Die [**Session. Enumerate**](session-enumerate.md) -Methode ist der Windows-Remoteverwaltung Ansatz zum Abrufen aller Instanzen einer angegebenen Ressource.

Die [**Session. Enumerate**](session-enumerate.md) -Methode ruft keine Auflistung in einem [**errbewbjectset**](/windows/desktop/WmiSdk/swbemobjectset) -Objekt ab, wie z. b. ein [**SWbemService.Execquery**](/windows/desktop/WmiSdk/swbemservices-execquery) -Aufrufes mit einer [WMI-Abfrage](/windows/desktop/WmiSdk/querying-wmi) als Parameter (z `ExecQuery("SELECT * from Win32_LogicalDisk")` . b.) oder ein Aufrufen einer Methode wie z. b. " [**errbemubject. Instance \_**](/windows/desktop/WmiSdk/swbemobject-instances-)". **Session. Enumerate** und die [**enumeratorobjektmethoden**](enumerator.md) ähneln dem Vorgang des [Textstream](/previous-versions//312a5kbt(v=vs.85)) -Skript Objekts, das zum Lesen von Dateien als Datenstrom verwendet wird.

Um Dateien als Textstream zu lesen, müssen Sie das Skript- [Textstream](/previous-versions//312a5kbt(v=vs.85)) -Objekt erstellen und die [Textstream. read line](/previous-versions//h7se9d4f(v=vs.85)) -Methode zum Lesen der einzelnen Zeilen der Datei aufzurufen. Auf ähnliche Weise können Sie die [**Session. Enumerate**](session-enumerate.md) -Methode zum Abrufen eines [**Enumeratorobjekts**](enumerator.md) und zum Abrufen der [**Enumerator. ReadItem**](enumerator-readitem.md) -Methode zum Abrufen des nächsten Elements aufruft. Wie beim Lesen aus der Textdatei können Sie auch die [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) -Eigenschaft aufzurufen, um zu überprüfen, ob Sie das Ende der Datenelemente erreicht haben.

**So zählen Sie eine Ressource auf**

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

    

3.  Ruft die [**Session. Enumerate**](session-enumerate.md) -Methode auf. Dieser Befehl startet eine Enumeration. In WinRM erhält ein Enumerationsvorgang eine Auflistung nicht auf dieselbe Weise wie WMI. Stattdessen stellt die **Session. Enumerate** -Methode einen WS-Management protokollenumerationskontext her, der im [**Enumeratorobjekt**](enumerator.md) verwaltet wird.

    ```VB
    Set EnumJobs = objSession.Enumerate( strResource )
    ```

    

4.  Rufen Sie die [**Enumerator. ReadItem**](enumerator-readitem.md) -Methode auf, um das nächste Element der Ergebnisse zu erhalten. In WS-Management-Protokoll entspricht dies dem Pull-Vorgang. Verwenden Sie die [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) -Methode als Steuerelement, um zu erfahren, wann der Lesevorgang beendet werden soll.

    ```VB
    While Not EnumJobs.AtEndOfStream
        NumOfJobs = NumOfJobs + 1
        DisplayOutput( EnumJobs.ReadItem ) 
    Wend
    ```

    

Das folgende VBScript-Codebeispiel zeigt das komplette Skript.


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

[Informationen zu Windows-Remoteverwaltung](about-windows-remote-management.md)
</dt> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Windows-Remoteverwaltung Referenz](windows-remote-management-reference.md)
</dt> </dl>

 

 