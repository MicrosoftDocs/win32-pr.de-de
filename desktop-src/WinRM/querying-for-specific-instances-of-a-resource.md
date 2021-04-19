---
title: Abfragen für bestimmte Instanzen einer Ressource
description: Der aufzurufende "Session. Enumerate" verfügt über optionale Parameter, die die Enumeration in eine Abfrage eingrenzen.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 30ae068c712dd04ba892220657ad64820a890040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342345"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Abfragen für bestimmte Instanzen einer Ressource

Der aufzurufende " [**Session. Enumerate**](session-enumerate.md) " verfügt über optionale Parameter, die die Enumeration in eine Abfrage eingrenzen. Da die [WinRM-Skript-API](winrm-scripting-api.md) und die [WinRM-C++-API](winrm-c---api.md) eng auf dem zugrunde liegenden WS-Management Protokoll modelliert sind, verwenden die Parameter dieselbe Terminologie für Abfragen wie das Protokoll –*Filter* und den *Filter Dialekt*.

Sie können entweder den Filter-und den Dialekt Parameter von [**Session. Enumerate**](session-enumerate.md) verwenden, oder Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt und die [**addselector**](resourcelocator-addselector.md) -Methode erstellen und bereitstellen, aber Sie können nicht beides tun.

Diese Prozedur führt eine Abfrage für Netzwerkadapter aus, bei denen TCP/IP gebunden und aktiviert ist. Die Abfrage fordert alle Instanzen von [**Win32 \_ networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) an, deren **ipabled** -Eigenschaft auf **true** festgelegt ist. Die Abfrage wird wie eine einfache Enumeration behandelt, außer wenn Sie den *Filter* und den *Dialekt* hinzufügen.

In diesem Beispiel wird der Ressourcen Name für die Ressourcen Konstante durch ein Sternchen "" dargestellt, \* da der Klassenname [**Win32 \_ networkadapterconfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)bereits in der Zeichenfolge " *strinfilter* " erwähnt wird.

**So Fragen Sie bestimmte Instanzen einer Ressource ab**

1.  Definieren Sie zum Vereinfachen des Lesens URIs als Konstanten.

    ```VB
    Const RemoteComputer = "servername.domain.com"
    Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    ```

    

2.  Erstellen Sie eine Sitzung.

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)
    ```

    

3.  Erstellen Sie die Filter Zeichenfolge. Windows-Remoteverwaltung unterstützt [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) als Filter Dialekt.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  Legen Sie alle erforderlichen [**Enumerationskonstanten**](enumeration-constants.md) im *Flags* -Parameter fest.

    Beachten Sie, dass der WinRM-Dienst den Fehlercode Fehler zurückgibt, wenn die Flags die [**Enumerationskonstanten**](enumeration-constants.md) **wsmanflaghierarchydeepbasepropsonly** oder **wsmanflaghierarchyflache** enthalten **\_ \_ \_ \_**.

5.  Ruft die [**Session. Enumerate**](session-enumerate.md) -Methode auf. Dieser Befehl startet eine Enumeration. Die **Session. Enumerate** -Methode stellt einen WS-Management protokollenumerationskontext her, der im [**Enumeratorobjekt**](enumerator.md) verwaltet wird.

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Rufen Sie die [**Enumerator. ReadItem**](enumerator-readitem.md) -Methode auf, um das nächste Element der Ergebnisse zu erhalten. In WS-Management-Protokoll entspricht dies dem Pull-Vorgang. Verwenden Sie die [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) -Methode als Steuerelement, um zu erfahren, wann der Lesevorgang beendet werden soll.

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

Das folgende VBScript-Codebeispiel zeigt das komplette Skript.


```VB
Const RemoteComputer = "servername.domain.com"
Const Resource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
Const Dialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"

Set objWsman = CreateObject("Wsman.Automation")
Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"

Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)

While Not objResultSet.AtEndOfStream
    DisplayOutput(objResultSet.ReadItem)
Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput(strWinRMXml)
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject("MSXml2.DOMDocument.3.0") 
    Set xslFile = CreateObject("MSXml2.DOMDocument.3.0")
    xmlFile.LoadXml(strWinRMXml)
    xslFile.Load("WsmTxt.xsl")
    Wscript.Echo xmlFile.TransformNode(xslFile) 
End Sub
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 