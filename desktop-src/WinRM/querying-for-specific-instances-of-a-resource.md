---
title: Abfragen bestimmter Instanzen einer Ressource
description: Der Aufruf von Session.Enumerate verfügt über optionale Parameter, die die Enumeration in eine Abfrage eingrenzen.
ms.assetid: 69d2fe79-9aad-4c8c-a65e-c6bb0e51c063
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f757b6392ec26f809004d599f6c5603629d23e8eb7a7f4b08a4f3a4ef18791a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642850"
---
# <a name="querying-for-specific-instances-of-a-resource"></a>Abfragen bestimmter Instanzen einer Ressource

Der Aufruf von [**Session.Enumerate**](session-enumerate.md) verfügt über optionale Parameter, die die Enumeration in eine Abfrage eingrenzen. Da die [WinRM-Skripterstellungs-API](winrm-scripting-api.md) und die [WinRM C++-API](winrm-c---api.md) eng auf dem zugrunde liegenden WS-Management Protokoll modelliert sind, verwenden die Parameter dieselbe Terminologie für Abfragen wie das Protokoll–*Filter-* und *Filterdialekt*.

Sie können entweder die Filter- und Dialektparameter von [**Session.Enumerate**](session-enumerate.md) verwenden oder ein [**ResourceLocator-Objekt**](resourcelocator.md) und die [**AddSelector-Methode**](resourcelocator-addselector.md) erstellen und bereitstellen. Beides ist jedoch nicht möglich.

Diese Prozedur führt eine Abfrage für Netzwerkadapter aus, für die TCP/IP gebunden und aktiviert ist. Die Abfrage fordert alle Instanzen von [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) an, für die die **IpEnabled-Eigenschaft** auf True festgelegt **ist.** Mit Ausnahme des Hinzufügens des *Filters* und *Dialekts* wird die Abfrage wie eine einfache Enumeration behandelt.

In diesem Beispiel wird der Ressourcenname für die Ressourcenkonstante durch ein Sternchen \* "" dargestellt, da der Klassenname [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)bereits in der *strFilter-Zeichenfolge* erwähnt wird.

**So fragen Sie bestimmte Instanzen einer Ressource ab**

1.  Um das Lesen zu erleichtern, definieren Sie URIs als Konstanten.

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

    

3.  Erstellen Sie die Filterzeichenfolge. Windows Die Remoteverwaltung unterstützt [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) als Filterdialekt.

    ```VB
    strFilter = "SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IpEnabled=TRUE"
    ```

    

4.  Legen Sie alle erforderlichen [**Enumerationskonstanten**](enumeration-constants.md) im *flags-Parameter* fest.

    Beachten Sie Folgendes: Wenn die Flags die [**Enumerationskonstanten**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** oder **WSManFlagHierarchyShallow** enthalten, gibt der WinRM-Dienst den Fehlercode **ERROR \_ WSMAN \_ POLYMORPHISM \_ MODE \_ UNSUPPORTED zurück.**

5.  Rufen Sie die [**Session.Enumerate-Methode auf.**](session-enumerate.md) Dieser Aufruf startet eine Enumeration. Die **Session.Enumerate-Methode** erstellt einen WS-Management Im [**Enumeratorobjekt verwalteten**](enumerator.md) Protokollenumerationskontext.

    ```VB
    Set objResultSet = objSession.Enumerate(Resource, strFilter, Dialect)
    ```

    

6.  Rufen Sie die [**Enumerator.ReadItem-Methode**](enumerator-readitem.md) auf, um das nächste Element der Ergebnisse abzurufen. In WS-Management Protokoll entspricht dies dem Pullvorgang. Verwenden Sie die [**Enumerator.AtEndOfStream-Methode**](enumerator-atendofstream.md) als Steuerelement, um zu wissen, wann das Lesen beendet werden soll.

    ```VB
    While Not objResultSet.AtEndOfStream
        DisplayOutput(objResultSet.ReadItem)
    Wend
    ```

    

Das folgende VBScript-Codebeispiel zeigt das vollständige Skript.


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

[Verwenden Windows Remoteverwaltung](using-windows-remote-management.md)
</dt> <dt>

[Auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[**Resourcelocator**](resourcelocator.md)
</dt> </dl>

 

 