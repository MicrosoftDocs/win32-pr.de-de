---
title: Suchen nach Objekten
description: Julie Bankert muss Telefonnummern für alle Programm-Manager finden, die in der Abteilung 101 arbeiten. Sie können ein Skript erstellen, das ADO und ADSI verwendet, um dies zu erreichen.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- Suchen nach Objekten ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103858040"
---
# <a name="searching-for-objects"></a><span data-ttu-id="6e43f-105">Suchen nach Objekten</span><span class="sxs-lookup"><span data-stu-id="6e43f-105">Searching for Objects</span></span>

<span data-ttu-id="6e43f-106">Julie Bankert muss Telefonnummern für alle Programm-Manager finden, die in der Abteilung 101 arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6e43f-106">Julie Bankert must find telephone numbers for all Program Managers who work in Department 101.</span></span> <span data-ttu-id="6e43f-107">Sie können ein Skript erstellen, das ADO und ADSI verwendet, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="6e43f-107">She can create a script that uses ADO and ADSI to accomplish this.</span></span>

<span data-ttu-id="6e43f-108">Wenn der ADO-Anbieter zum Ausführen einer Abfrage verwendet wird, gibt das Resultset nur die ersten 1000-Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="6e43f-108">When using the ADO provider to perform a query, the result set will only return the first 1000 objects.</span></span> <span data-ttu-id="6e43f-109">Aus diesem Grund ist es wichtig, eine auslagerbare Abfrage zu verwenden, damit Sie alle Objekte im Resultset abrufen können, solange der Verzeichnisdienst nicht so festgelegt wurde, dass die Anzahl der Elemente in einem Resultset beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="6e43f-109">For this reason, it is important to use a paged query so that you can retrieve all of the objects in the result set, as long as the directory service has not been set to limit the number of items in a result set.</span></span> <span data-ttu-id="6e43f-110">Rückgabe Sätze enthalten die Anzahl der Elemente, die Sie im Seiten Format angeben, und Auslagerungs Gruppen werden weiterhin zurückgegeben, bis alle Elemente im Resultset zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="6e43f-110">Return sets will contain the number of items that you specify in the page size, and paged sets will continue to be returned until all items in the result set have been returned.</span></span>


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



<span data-ttu-id="6e43f-111">Zum Ausführen einer ADSI-Suche in Visual Basic oder einer Skript Umgebung sind drei ADO-Komponenten erforderlich: **Connection**, **Command** und **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="6e43f-111">To perform an ADSI search in Visual Basic or a scripting environment, three ADO components are required: **Connection**, **Command**, and **Recordset**.</span></span> <span data-ttu-id="6e43f-112">Das **Connection** -Objekt ermöglicht Ihnen, ggf. den Anbieter Namen, Alternative Anmelde Informationen und andere Flags anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6e43f-112">The **Connection** object enables you to specify the provider name, alternate credentials, if applicable, and other flags.</span></span> <span data-ttu-id="6e43f-113">Das **Command** -Objekt ermöglicht es Ihnen, Sucheinstellungen und die Abfrage Zeichenfolge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6e43f-113">The **Command** object enables you to specify search preferences and the query string.</span></span> <span data-ttu-id="6e43f-114">Sie müssen das **Verbindungs** Objekt einem **Befehls** Objekt vor der Ausführung der Abfrage zuordnen.</span><span class="sxs-lookup"><span data-stu-id="6e43f-114">You must associate the **Connection** object to a **Command** object before the execution of the query.</span></span> <span data-ttu-id="6e43f-115">Zum Schluss wird das **Recordset** -Objekt verwendet, um das Resultset zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="6e43f-115">Finally, the **Recordset** object is used to iterate the result set.</span></span>

<span data-ttu-id="6e43f-116">ADSI unterstützt zwei Typen von Abfrage Zeichenfolgen oder-Dialekten.</span><span class="sxs-lookup"><span data-stu-id="6e43f-116">ADSI supports two types of query strings or dialects.</span></span> <span data-ttu-id="6e43f-117">Im vorangehenden Codebeispiel wird der SQL-Dialekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e43f-117">The preceding code example uses the SQL dialect.</span></span> <span data-ttu-id="6e43f-118">Sie können auch den LDAP-Dialekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e43f-118">You can also use the LDAP dialect.</span></span> <span data-ttu-id="6e43f-119">Die Abfrage Zeichenfolge des LDAP-Dialekts basiert auf [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (eine RFC ist eine Anforderung für ein Kommentar Dokument, das die Grundlage für die Entwicklung von LDAP-Standards ist).</span><span class="sxs-lookup"><span data-stu-id="6e43f-119">The LDAP dialect query string is based on [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (an RFC is a Request For Comments document, which is the basis for developing LDAP standards).</span></span> <span data-ttu-id="6e43f-120">Das vorangehende Beispiel kann in das folgende Codebeispiel übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="6e43f-120">The preceding example can be translated to the following code example.</span></span>


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



<span data-ttu-id="6e43f-121">Warum ist das Wort "subtree" am Ende der Zeichenfolge?</span><span class="sxs-lookup"><span data-stu-id="6e43f-121">Why is the word "subtree" at the end of the string?</span></span> <span data-ttu-id="6e43f-122">In der Verzeichnis Welt können Sie den Suchbereich angeben.</span><span class="sxs-lookup"><span data-stu-id="6e43f-122">In the directory world, you can specify the scope of search.</span></span> <span data-ttu-id="6e43f-123">Folgende Optionen stehen zur Auswahl: "Base", "onelevel" und "subtree".</span><span class="sxs-lookup"><span data-stu-id="6e43f-123">The choices are: "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="6e43f-124">"Base" wird verwendet, um das Objekt selbst zu lesen. "onelevel" bezieht sich auf die unmittelbaren untergeordneten Elemente, ähnlich wie der **dir** -Befehl. "subtree" wird verwendet, um Tiefe oder mehrere Ebenen zu durchsuchen (ähnlich wie **dir/s**).</span><span class="sxs-lookup"><span data-stu-id="6e43f-124">"base" is used to read the object itself; "onelevel" refers to the immediate children, similar to the **dir** command; "subtree" is used to search deep or down multiple levels (similar to **dir /s**).</span></span>

<span data-ttu-id="6e43f-125">Mit dem SQL-Dialekt können Sie den Bereich in der Befehls Eigenschaft angeben, z. b. im folgenden Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="6e43f-125">With the SQL dialect, you can specify scope in the command property, such as in the following code example.</span></span>


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



<span data-ttu-id="6e43f-126">Wenn der Bereich nicht angegeben wird, wird standardmäßig eine Unterstruktur Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e43f-126">If scope is not specified, by default it uses a subtree search.</span></span>

> [!Note]  
> <span data-ttu-id="6e43f-127">Wenn Sie C++ verwenden, können Sie die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle von ADSI verwenden.</span><span class="sxs-lookup"><span data-stu-id="6e43f-127">If you use C++, you can use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface from ADSI.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6e43f-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e43f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e43f-129">Neuorganisation</span><span class="sxs-lookup"><span data-stu-id="6e43f-129">Reorganization</span></span>](reorganization.md)
</dt> </dl>

 

 




