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
# <a name="getting-started-with-asp-for-adsi"></a><span data-ttu-id="7ee4f-107">Einstieg in ASP für ADSI</span><span class="sxs-lookup"><span data-stu-id="7ee4f-107">Getting Started with ASP for ADSI</span></span>

<span data-ttu-id="7ee4f-108">ADSI kann verwendet werden, um mithilfe einer ASP-Seite auf Verzeichnis Daten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-108">ADSI can be used to access directory data using an ASP page.</span></span> <span data-ttu-id="7ee4f-109">Dies kann eine bequeme Möglichkeit zum Ausführen von Verwaltungsaufgaben und-Abfragen auf einer Webseite oder zur Bereitstellung von Informationen für Mitarbeiter in einem Intranet darstellen.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-109">This can be a convenient way to run administration tasks and queries from a webpage or provide information to employees on an intranet.</span></span>

<span data-ttu-id="7ee4f-110">Ein Vorteil der Verwendung von ADSI mit ASP besteht darin, dass Sie eine umfassendere Benutzer Darstellung erstellen können, da Sie mit Visual Basic eine ADSI-Anwendung erstellen und Sie einem Benutzer über eine Standard Webseite anbieten können.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-110">One advantage of using ADSI with ASP is that you can create a richer user experience because you can use Visual Basic to create an ADSI application and offer it to a user through a standard webpage.</span></span> <span data-ttu-id="7ee4f-111">Beispielsweise können Sie eine Webseite erstellen, die es Mitarbeitern ermöglicht, den Nachnamen eines Mitarbeiters einzugeben und eine Telefonnummer für diesen Mitarbeiter zu erhalten, oder ein Formular zu erstellen, mit dem Mitarbeiter persönliche Informationen in einer Datenbank für Personalwesen aktualisieren können.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-111">For example, you could create a webpage that enables employees to enter the last name of an employee and get back a phone number for that employee, or create a form that allows employees to update personal information in a company human resources database.</span></span>

<span data-ttu-id="7ee4f-112">Der ASP-Code beginnt mit ' <% ' und endet mit '% > '.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-112">ASP code starts with '<%' and ends with '%>'.</span></span> <span data-ttu-id="7ee4f-113">Sie können ADSI-Code als VBScript oder Visual Basic hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-113">You can add ADSI code as VBScript or Visual Basic.</span></span>

<span data-ttu-id="7ee4f-114">Zum Erstellen einer ASP-Seite können Sie einen Webseiten-Editor, einen Editor oder einen anderen Text-Editor oder das Microsoft Visual Studio .NET-Entwicklungssystem verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-114">To create an ASP page, you can use a webpage editor, Notepad or other text editor, or the Microsoft Visual Studio .NET development system.</span></span>

<span data-ttu-id="7ee4f-115">Richten Sie vor dem Ausführen der ASP-Seite die Anwendung oder den IIS-Server gemäß den Anweisungen in [Authentifizierungs Probleme für ADSI mit ASP](authentication-issues-for-adsi-with-asp.md)ein.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-115">Before you run your ASP page, set up your application or IIS server according to the instructions found in [Authentication Issues for ADSI with ASP](authentication-issues-for-adsi-with-asp.md).</span></span>

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a><span data-ttu-id="7ee4f-116">Ein einfaches ASP-Beispiel: Auflisten von Objekten in einem Container</span><span class="sxs-lookup"><span data-stu-id="7ee4f-116">A Simple ASP Sample: Enumerating Objects in a Container</span></span>

<span data-ttu-id="7ee4f-117">Erstellen Sie mithilfe eines Webseiten-Editors eine neue HTML-Seite, die den Distinguished Name eines Container Objekts akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-117">Using a webpage editor, create a new html page which accepts the distinguished name of a container object.</span></span> <span data-ttu-id="7ee4f-118">Geben Sie das folgende Codebeispiel ein.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-118">Enter the following code example.</span></span>


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



<span data-ttu-id="7ee4f-119">Diese Seite kann nun einen Container Namen akzeptieren, der an Sie übermittelt wird, und ADSI zum Auflisten von Objekten im Container verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-119">This page can now accept a container name that is passed to it and use ADSI to enumerate objects in the container.</span></span>

<span data-ttu-id="7ee4f-120">Erstellen Sie eine neue ASP-Seite mit dem Namen "", und geben Sie das folgende Codebeispiel ein.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-120">Create a new ASP page called Enum.asp and enter the following code example.</span></span> <span data-ttu-id="7ee4f-121">Speichern Sie diese Seite im Stammverzeichnis des lokalen Webservers.</span><span class="sxs-lookup"><span data-stu-id="7ee4f-121">Save this page at the root of the local web server.</span></span>


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



 

 




