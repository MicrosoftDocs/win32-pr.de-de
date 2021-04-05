---
title: Einstieg in ASP für ADSI
description: ADSI kann verwendet werden, um mithilfe einer ASP-Seite auf Verzeichnis Daten zuzugreifen. Dies kann eine bequeme Möglichkeit zum Ausführen von Verwaltungsaufgaben und-Abfragen auf einer Webseite oder zur Bereitstellung von Informationen für Mitarbeiter in einem Intranet darstellen.
ms.assetid: 2007257c-6c4e-415e-9ab5-e65d8d9e5dd4
ms.tgt_platform: multiple
keywords:
- ASP ADSI
- ADSI, ASP-Seiten
- ADSI, ASP Pages, ASP-Code Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5b18093c3817d7a6c3d0224b722f8dd4983c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707421"
---
# <a name="getting-started-with-asp-for-adsi"></a>Einstieg in ASP für ADSI

ADSI kann verwendet werden, um mithilfe einer ASP-Seite auf Verzeichnis Daten zuzugreifen. Dies kann eine bequeme Möglichkeit zum Ausführen von Verwaltungsaufgaben und-Abfragen auf einer Webseite oder zur Bereitstellung von Informationen für Mitarbeiter in einem Intranet darstellen.

Ein Vorteil der Verwendung von ADSI mit ASP besteht darin, dass Sie eine umfassendere Benutzer Darstellung erstellen können, da Sie mit Visual Basic eine ADSI-Anwendung erstellen und Sie einem Benutzer über eine Standard Webseite anbieten können. Beispielsweise können Sie eine Webseite erstellen, die es Mitarbeitern ermöglicht, den Nachnamen eines Mitarbeiters einzugeben und eine Telefonnummer für diesen Mitarbeiter zu erhalten, oder ein Formular zu erstellen, mit dem Mitarbeiter persönliche Informationen in einer Datenbank für Personalwesen aktualisieren können.

Der ASP-Code beginnt mit ' <% ' und endet mit '% > '. Sie können ADSI-Code als VBScript oder Visual Basic hinzufügen.

Zum Erstellen einer ASP-Seite können Sie einen Webseiten-Editor, einen Editor oder einen anderen Text-Editor oder das Microsoft Visual Studio .NET-Entwicklungssystem verwenden.

Richten Sie vor dem Ausführen der ASP-Seite die Anwendung oder den IIS-Server gemäß den Anweisungen in [Authentifizierungs Probleme für ADSI mit ASP](authentication-issues-for-adsi-with-asp.md)ein.

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a>Ein einfaches ASP-Beispiel: Auflisten von Objekten in einem Container

Erstellen Sie mithilfe eines Webseiten-Editors eine neue HTML-Seite, die den Distinguished Name eines Container Objekts akzeptiert. Geben Sie das folgende Codebeispiel ein.


```HTML
<html>
<body>

<form method="POST" action="https://localhost/Enum.asp" ID="Form1">
<p>Distinguished name of container:<input type="text" name="inpContainer" size="100" ID="Text2"></p>
<p><input type="SUBMIT" value="GO" ID="Submit1" NAME="Submit1"></p>
</form>

</body>
</html>
```



Diese Seite kann nun einen Container Namen akzeptieren, der an Sie übermittelt wird, und ADSI zum Auflisten von Objekten im Container verwenden.

Erstellen Sie eine neue ASP-Seite mit dem Namen "", und geben Sie das folgende Codebeispiel ein. Speichern Sie diese Seite im Stammverzeichnis des lokalen Webservers.


```VB
<%@ Language=VBScript %>
<%
' Get the inputs.
containerName = Request.Form("inpContainer")
' Validate compName before using.

If Not ("" = containerName) Then
  ' Bind to the object.
  adsPath = "LDAP://" & containerName
  Set comp = GetObject(adsPath)

  ' Write the ADsPath of each of the child objects.
  Response.Write("<p>Enumeration:</p>")
  For Each obj in comp
    Response.Write(obj.ADsPath + "<BR>")
  Next
End If
%>
```



 

 




