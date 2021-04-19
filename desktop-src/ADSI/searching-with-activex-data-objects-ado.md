---
title: Suchen mit ActiveX Data Objects (ADO)
description: Das ADO-Modell (ActiveX Data Object) besteht aus den in der folgenden Tabelle aufgeführten Objekten.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI, suchen mit ADO
- Suchen mit ActiveX Data Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341553"
---
# <a name="searching-with-activex-data-objects-ado"></a><span data-ttu-id="2d51c-105">Suchen mit ActiveX Data Objects (ADO)</span><span class="sxs-lookup"><span data-stu-id="2d51c-105">Searching with ActiveX Data Objects (ADO)</span></span>

<span data-ttu-id="2d51c-106">Das ADO-Modell (ActiveX Data Object) besteht aus den in der folgenden Tabelle aufgeführten Objekten.</span><span class="sxs-lookup"><span data-stu-id="2d51c-106">The ActiveX Data Object (ADO) model consists of objects listed in the following table.</span></span>



| <span data-ttu-id="2d51c-107">Object</span><span class="sxs-lookup"><span data-stu-id="2d51c-107">Object</span></span>         | <span data-ttu-id="2d51c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d51c-108">Description</span></span>                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d51c-109">**Connection**</span><span class="sxs-lookup"><span data-stu-id="2d51c-109">**Connection**</span></span> | <span data-ttu-id="2d51c-110">Eine offene Verbindung mit einer OLE DB Datenquelle, z. b. ADSI.</span><span class="sxs-lookup"><span data-stu-id="2d51c-110">An open connection to an OLE DB data source such as ADSI.</span></span>                                                                          |
| <span data-ttu-id="2d51c-111">**Befehl**</span><span class="sxs-lookup"><span data-stu-id="2d51c-111">**Command**</span></span>    | <span data-ttu-id="2d51c-112">Definiert einen bestimmten Befehl, der für die Datenquelle ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d51c-112">Defines a specific command to run against the data source.</span></span>                                                                         |
| <span data-ttu-id="2d51c-113">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="2d51c-113">**Parameter**</span></span>  | <span data-ttu-id="2d51c-114">Eine optionale-Auflistung für alle Parameter, die für das Command-Objekt bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-114">An optional collection for any parameters to provide to the command object.</span></span>                                                        |
| <span data-ttu-id="2d51c-115">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="2d51c-115">**RecordSet**</span></span>  | <span data-ttu-id="2d51c-116">Ein Satz von Datensätzen aus einer Tabelle, einem Befehls Objekt oder einer SQL-Syntax.</span><span class="sxs-lookup"><span data-stu-id="2d51c-116">A set of records from a table, command object, or SQL syntax.</span></span> <span data-ttu-id="2d51c-117">Ein Recordset kann ohne ein zugrunde liegendes Verbindungs Objekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d51c-117">A recordset can be created without any underlying connection object.</span></span> |
| <span data-ttu-id="2d51c-118">**Feld**</span><span class="sxs-lookup"><span data-stu-id="2d51c-118">**Field**</span></span>      | <span data-ttu-id="2d51c-119">Eine einzelne Datenspalte in einem Recordset.</span><span class="sxs-lookup"><span data-stu-id="2d51c-119">A single column of data in a recordset.</span></span>                                                                                            |
| <span data-ttu-id="2d51c-120">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="2d51c-120">**Property**</span></span>   | <span data-ttu-id="2d51c-121">Eine Auflistung von Werten, die vom Anbieter für ADO bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d51c-121">A collection of values supplied by the provider for ADO.</span></span>                                                                           |
| <span data-ttu-id="2d51c-122">**Fehler**</span><span class="sxs-lookup"><span data-stu-id="2d51c-122">**Error**</span></span>      | <span data-ttu-id="2d51c-123">Enthält Daten zu Datenzugriffs Fehlern.</span><span class="sxs-lookup"><span data-stu-id="2d51c-123">Contains data about data access errors.</span></span> <span data-ttu-id="2d51c-124">Wird aktualisiert, wenn ein Fehler in einem einzelnen Vorgang auftritt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-124">Refreshed when an error occurs in a single operation.</span></span>                                      |



 

<span data-ttu-id="2d51c-125">Damit ADO mit ADSI kommunizieren kann, müssen mindestens zwei ADO-Objekte vorhanden sein: **Connection** und **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2d51c-125">For ADO to communicate with ADSI, there must be, at least, two ADO objects: **Connection** and **RecordSet**.</span></span> <span data-ttu-id="2d51c-126">Diese ADO-Objekte dienen zum Authentifizieren von Benutzern und zum Auflisten der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="2d51c-126">These ADO objects serve to authenticate users and enumerate results, respectively.</span></span> <span data-ttu-id="2d51c-127">In der Regel verwenden Sie ein **Command** -Objekt, um eine aktive Verbindung beizubehalten, Abfrage Parameter anzugeben, z. b. die Seitengröße und den Suchbereich, und eine Abfrage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-127">Typically, you will also use a **Command** object to maintain an active connection, specify query parameters, such as page size and search scope, and perform a query.</span></span> <span data-ttu-id="2d51c-128">Weitere Informationen zur Suchfilter Syntax finden Sie unter [Syntax für Suchfilter](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="2d51c-128">For more information about the search filter syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

<span data-ttu-id="2d51c-129">Das **Verbindungs** Objekt lädt den OLE DB Anbieter und überprüft die Anmelde Informationen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="2d51c-129">The **Connection** object loads the OLE DB provider, and validates user credentials.</span></span> <span data-ttu-id="2d51c-130">Aufrufen Sie in **Visual Basic die Funktion** "Funktion" mit "ADODB". Verbindung "zum Erstellen einer Instanz eines **Verbindungs** Objekts, und legen Sie dann die **Provider** -Eigenschaft des **Verbindungs** Objekts auf" ADSDSOObject "fest.</span><span class="sxs-lookup"><span data-stu-id="2d51c-130">In Visual Basic, call the **CreateObject** function with "ADODB.Connection" to create an instance of a **Connection** object, and then set the **Provider** property of the **Connection** object to "ADsDSOObject".</span></span> <span data-ttu-id="2d51c-131">ADODB. Connection "ist die ProgID des **Verbindungs** Objekts, und" ADSDSOObject "ist der Name des OLE DB Anbieters in ADSI.</span><span class="sxs-lookup"><span data-stu-id="2d51c-131">"ADODB.Connection" is the ProgID of the **Connection** object and "ADsDSOObject" is the name of the OLE DB provider in ADSI.</span></span> <span data-ttu-id="2d51c-132">Wenn keine Anmelde Informationen angegeben sind, werden die Anmelde Informationen des aktuell angemeldeten Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d51c-132">If no credentials are specified, the credentials of the currently logged on user are used.</span></span>

<span data-ttu-id="2d51c-133">Im folgenden Codebeispiel wird gezeigt, wie eine Instanz eines **Verbindungs** Objekts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2d51c-133">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="2d51c-134">Im folgenden Codebeispiel wird gezeigt, wie eine Instanz eines **Verbindungs** Objekts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2d51c-134">The following code example shows how to create an instance of a **Connection** object.</span></span>


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



<span data-ttu-id="2d51c-135">Im folgenden Codebeispiel wird gezeigt, wie eine Instanz eines **Verbindungs** Objekts erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2d51c-135">The following code example shows how to create an instance of a **Connection** object.</span></span> <span data-ttu-id="2d51c-136">Beachten Sie, dass Sie die ADO-Typbibliothek (msadoXX.dll) als einen der Verweise im Visual Basic Projekt einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-136">Be aware that you must include the ADO type library (msadoXX.dll) as one of the references in the Visual Basic project.</span></span>


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



<span data-ttu-id="2d51c-137">Geben Sie die Benutzer Authentifizierungsdaten an, indem Sie die Eigenschaften des **Verbindungs** Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-137">Specify user authentication data by setting the properties of the **Connection** object.</span></span> <span data-ttu-id="2d51c-138">In der folgenden Tabelle sind die von ADSI unterstützten Eigenschaften für Benutzerauthentifizierung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-138">The following table lists ADSI-supported user-authentication properties.</span></span>



| <span data-ttu-id="2d51c-139">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2d51c-139">Property</span></span>           | <span data-ttu-id="2d51c-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d51c-140">Description</span></span>                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d51c-141">"Benutzer-ID"</span><span class="sxs-lookup"><span data-stu-id="2d51c-141">"User ID"</span></span>          | <span data-ttu-id="2d51c-142">Eine Zeichenfolge, die den Benutzer angibt, dessen Sicherheitskontext beim Ausführen der Suche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d51c-142">A string that identifies the user whose security context is used when performing the search.</span></span> <span data-ttu-id="2d51c-143">Weitere Informationen zum Format der Benutzernamen Zeichenfolge finden Sie unter [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span><span class="sxs-lookup"><span data-stu-id="2d51c-143">For more information about the format of the user name string, see [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject).</span></span> <span data-ttu-id="2d51c-144">Wenn nicht angegeben, ist der Standardwert der angemeldete Benutzer, oder der Benutzer hat den Aufruf durch den aufrufenden Prozess angenommen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-144">If not specified, the default is the logged on user, or the user impersonated by the calling process.</span></span> |
| <span data-ttu-id="2d51c-145">Password</span><span class="sxs-lookup"><span data-stu-id="2d51c-145">"Password"</span></span>         | <span data-ttu-id="2d51c-146">Eine Zeichenfolge, die das Kennwort des Benutzers angibt, der durch die Benutzer-ID identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2d51c-146">A string that specifies the password of the user identified by "User ID".</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="2d51c-147">"Kennwort verschlüsseln"</span><span class="sxs-lookup"><span data-stu-id="2d51c-147">"Encrypt Password"</span></span> | <span data-ttu-id="2d51c-148">Ein boolescher Wert, der angibt, ob das Kennwort verschlüsselt ist.</span><span class="sxs-lookup"><span data-stu-id="2d51c-148">A Boolean value that specifies whether the password is encrypted.</span></span> <span data-ttu-id="2d51c-149">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2d51c-149">The default is **false**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="2d51c-150">"ADSI-Flag"</span><span class="sxs-lookup"><span data-stu-id="2d51c-150">"ADSI Flag"</span></span>        | <span data-ttu-id="2d51c-151">Ein Satz von Flags aus der Enumeration der [**ADS- \_ \_ authentifizierungsenumeration**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) , die die Bindungs Authentifizierungs Optionen angeben.</span><span class="sxs-lookup"><span data-stu-id="2d51c-151">A set of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration that specify the binding authentication options.</span></span> <span data-ttu-id="2d51c-152">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="2d51c-152">The default is zero.</span></span>                                                                                                                                                                         |



 

<span data-ttu-id="2d51c-153">Im folgenden Codebeispiel wird gezeigt, wie die-Eigenschaften festgelegt werden, bevor das **Command** -Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2d51c-153">The following code example shows how the properties are set before creating the **Command** object.</span></span>


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



<span data-ttu-id="2d51c-154">Das zweite ADO-Objekt ist das **Command** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-154">The second ADO object is the **Command** object.</span></span> <span data-ttu-id="2d51c-155">Die ProgID des **Command** -Objekts ist "ADODB. Command".</span><span class="sxs-lookup"><span data-stu-id="2d51c-155">The ProgID of the **Command** object is "ADODB.Command".</span></span> <span data-ttu-id="2d51c-156">Mit diesem Objekt können Sie mithilfe der aktiven Verbindung Abfrage Anweisungen und andere Befehle an ADSI ausgeben.</span><span class="sxs-lookup"><span data-stu-id="2d51c-156">This object enables you to issue query statements and other commands to ADSI using the active connection.</span></span> <span data-ttu-id="2d51c-157">Das **Command** -Objekt verwendet seine **ActiveConnection** -Eigenschaft, um eine aktive Verbindung beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="2d51c-157">The **Command** object uses its **ActiveConnection** property to maintain an active connection.</span></span> <span data-ttu-id="2d51c-158">Außerdem wird die **CommandText** -Eigenschaft zum Speichern von Abfrage Anweisungen verwaltet, die von einem Benutzer ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2d51c-158">It also maintains the **CommandText** property to hold query statements issued by a user.</span></span> <span data-ttu-id="2d51c-159">Die Abfrage Anweisungen werden entweder im SQL- [Dialekt](sql-dialect.md) oder im [LDAP-Dialekt](ldap-dialect.md)ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-159">The query statements are expressed in either the [SQL dialect](sql-dialect.md) or the [LDAP dialect](ldap-dialect.md).</span></span>

<span data-ttu-id="2d51c-160">In den folgenden Codebeispielen wird gezeigt, wie ein **Befehls** Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2d51c-160">The following code examples show how to create a **Command** object.</span></span>


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



<span data-ttu-id="2d51c-161">Fügen Sie im folgenden Codebeispiel die ADO-Typbibliothek (msadoXX.dll) als einen der Verweise ein.</span><span class="sxs-lookup"><span data-stu-id="2d51c-161">In the following code example, include ADO type library (msadoXX.dll) as one of the references.</span></span>


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



<span data-ttu-id="2d51c-162">Suchoptionen für das **Command** -Objekt werden durch Festlegen der **Properties** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="2d51c-162">Search options for the **Command** object are specified by setting the **Properties** property.</span></span> <span data-ttu-id="2d51c-163">In der folgenden Tabelle sind die zulässigen benannten Eigenschaften für **Eigenschaften** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-163">The following table lists acceptable named properties for **Properties**.</span></span>



| <span data-ttu-id="2d51c-164">Benannte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2d51c-164">Named property</span></span>      | <span data-ttu-id="2d51c-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d51c-165">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d51c-166">Asynchronen</span><span class="sxs-lookup"><span data-stu-id="2d51c-166">"Asynchronous"</span></span>      | <span data-ttu-id="2d51c-167">Ein boolescher Wert, der angibt, ob die Suche synchron oder asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="2d51c-167">A Boolean value that specifies whether the search is synchronous or asynchronous.</span></span> <span data-ttu-id="2d51c-168">Der Standardwert ist false (synchron).</span><span class="sxs-lookup"><span data-stu-id="2d51c-168">The default is False (synchronous).</span></span> <span data-ttu-id="2d51c-169">Ein synchroner Suchvorgang wird blockiert, bis der Server das gesamte Ergebnis oder für eine seitenweise Suche die gesamte Seite zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-169">A synchronous search blocks until the server returns the entire result, or for a paged search, the entire page.</span></span> <span data-ttu-id="2d51c-170">Ein asynchroner Suchvorgang blockiert, bis eine Zeile der Suchergebnisse verfügbar ist, oder bis die durch die Timeout-Eigenschaft angegebene Zeit abläuft.</span><span class="sxs-lookup"><span data-stu-id="2d51c-170">An asynchronous search blocks until one row of the search results is available, or until the time specified by the "Timeout" property elapses.</span></span>                           |
| <span data-ttu-id="2d51c-171">"Cache Ergebnisse"</span><span class="sxs-lookup"><span data-stu-id="2d51c-171">"Cache results"</span></span>     | <span data-ttu-id="2d51c-172">Ein boolescher Wert, der angibt, ob das Ergebnis auf der Clientseite zwischengespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2d51c-172">A Boolean value that specifies whether the result should be cached on the client side.</span></span> <span data-ttu-id="2d51c-173">Der Standardwert ist " **true**". ADSI speichert das Resultset zwischen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-173">The default is **true**; ADSI caches the result set.</span></span> <span data-ttu-id="2d51c-174">Das Deaktivieren dieser Option kann für große Resultsets wünschenswert sein.</span><span class="sxs-lookup"><span data-stu-id="2d51c-174">Turning off this option may be desirable for large result sets.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="2d51c-175">"Verweigerungen"</span><span class="sxs-lookup"><span data-stu-id="2d51c-175">"Chase referrals"</span></span>   | <span data-ttu-id="2d51c-176">Ein Wert aus der [**Werbe \_ \_ \_ Einblendungen referenziert**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) die Enumeration, die angibt, wie die Suche auf Verweise verweist.</span><span class="sxs-lookup"><span data-stu-id="2d51c-176">A value from the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) that specifies how the search chases referrals.</span></span> <span data-ttu-id="2d51c-177">Der Standardwert ist " **ADS \_ Chase \_ verweirals \_**". Weitere Informationen zu dieser Eigenschaft finden Sie unter [referenrals](/windows/desktop/AD/referrals).</span><span class="sxs-lookup"><span data-stu-id="2d51c-177">The default is **ADS\_CHASE\_REFERRALS\_NEVER**.For more information about this property, see [Referrals](/windows/desktop/AD/referrals).</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="2d51c-178">"Nur Spaltennamen"</span><span class="sxs-lookup"><span data-stu-id="2d51c-178">"Column Names Only"</span></span> | <span data-ttu-id="2d51c-179">Ein boolescher Wert, der angibt, dass bei der Suche nur der Name der Attribute abgerufen werden soll, denen Werte zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="2d51c-179">A Boolean value that indicates that the search should retrieve only the name of attributes to which values have been assigned.</span></span> <span data-ttu-id="2d51c-180">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2d51c-180">The default is **false**.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2d51c-181">"Deref-Aliase"</span><span class="sxs-lookup"><span data-stu-id="2d51c-181">"Deref Aliases"</span></span>     | <span data-ttu-id="2d51c-182">Ein boolescher Wert, der angibt, ob Aliase von gefundenen Objekten aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="2d51c-182">A Boolean value that specifies whether aliases of found objects are resolved.</span></span> <span data-ttu-id="2d51c-183">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="2d51c-183">The default is **false**.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2d51c-184">"Seitengröße"</span><span class="sxs-lookup"><span data-stu-id="2d51c-184">"Page size"</span></span>         | <span data-ttu-id="2d51c-185">Ein ganzzahliger Wert, der das Paging schaltet und die maximale Anzahl von Objekten angibt, die in einem Resultset zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-185">An integer value that turns on paging and specifies the maximum number of objects to return in a results set.</span></span> <span data-ttu-id="2d51c-186">Der Standardwert ist keine Seitengröße.</span><span class="sxs-lookup"><span data-stu-id="2d51c-186">The default is no page size.</span></span> <span data-ttu-id="2d51c-187">Weitere Informationen finden Sie unter [Abrufen großer Resultsets](retrieving-large-results-sets.md).</span><span class="sxs-lookup"><span data-stu-id="2d51c-187">For more information, see [Retrieving Large Results Sets](retrieving-large-results-sets.md).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="2d51c-188">SearchScope</span><span class="sxs-lookup"><span data-stu-id="2d51c-188">"SearchScope"</span></span>       | <span data-ttu-id="2d51c-189">Ein Wert aus der [**ADS- \_ scopeenumeration**](/windows/win32/api/iads/ne-iads-ads_scopeenum) -Enumeration, der den Suchbereich angibt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-189">A value from the [**ADS\_SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) enumeration that specifies the search scope.</span></span> <span data-ttu-id="2d51c-190">Der Standardwert ist die **AD- \_ Bereichs \_ Teilstruktur**.</span><span class="sxs-lookup"><span data-stu-id="2d51c-190">The default is **ADS\_SCOPE\_SUBTREE**.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2d51c-191">"Größenbeschränkung"</span><span class="sxs-lookup"><span data-stu-id="2d51c-191">"Size Limit"</span></span>        | <span data-ttu-id="2d51c-192">Ein ganzzahliger Wert, der die Größenbeschränkung für die Suche angibt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-192">An integer value that specifies the size limit for the search.</span></span> <span data-ttu-id="2d51c-193">Für Active Directory gibt die Größenbeschränkung die maximale Anzahl von zurückgegebenen Objekten an.</span><span class="sxs-lookup"><span data-stu-id="2d51c-193">For Active Directory, the size limit specifies the maximum number of returned objects.</span></span> <span data-ttu-id="2d51c-194">Der Server beendet die Suche, wenn die Größenbeschränkung erreicht ist, und gibt die gesammelten Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="2d51c-194">The server stops searching when the size limit is reached and returns the results accumulated.</span></span> <span data-ttu-id="2d51c-195">Der Standardwert ist "No Limit".</span><span class="sxs-lookup"><span data-stu-id="2d51c-195">The default is no limit.</span></span>                                                                                                                                  |
| <span data-ttu-id="2d51c-196">"Sortieren nach"</span><span class="sxs-lookup"><span data-stu-id="2d51c-196">"Sort on"</span></span>           | <span data-ttu-id="2d51c-197">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von Attributen angibt, die als Sortierschlüssel verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-197">A string that specifies a comma-separated list of attributes to use as sort keys.</span></span> <span data-ttu-id="2d51c-198">Diese Eigenschaft funktioniert nur für Verzeichnisserver, die das LDAP-Steuerelement für die serverseitige Sortierung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-198">This property works only for directory servers that support the LDAP control for server-side sorting.</span></span> <span data-ttu-id="2d51c-199">Active Directory unterstützt das Sortier Steuerelement, kann sich jedoch auf die Serverleistung auswirken, insbesondere dann, wenn das Resultset groß ist.</span><span class="sxs-lookup"><span data-stu-id="2d51c-199">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="2d51c-200">Beachten Sie, dass Active Directory nur einen einzelnen Sortierschlüssel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-200">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="2d51c-201">Der Standardwert ist keine Sortierung.</span><span class="sxs-lookup"><span data-stu-id="2d51c-201">The default is no sorting.</span></span> |
| <span data-ttu-id="2d51c-202">"Zeitlimit"</span><span class="sxs-lookup"><span data-stu-id="2d51c-202">"Time Limit"</span></span>        | <span data-ttu-id="2d51c-203">Ein ganzzahliger Wert, der das Zeitlimit für die Suche in Sekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-203">An integer value that specifies the time limit, in seconds, for the search.</span></span> <span data-ttu-id="2d51c-204">Wenn das Zeitlimit erreicht ist, beendet der Server die Suche und gibt die gesammelten Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="2d51c-204">When the time limit is reached, the server stops searching and returns the results accumulated.</span></span> <span data-ttu-id="2d51c-205">Der Standardwert ist kein Zeit Limit.</span><span class="sxs-lookup"><span data-stu-id="2d51c-205">The default is no time limit.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="2d51c-206">Zeit</span><span class="sxs-lookup"><span data-stu-id="2d51c-206">"Timeout"</span></span>           | <span data-ttu-id="2d51c-207">Ein ganzzahliger Wert, der den Client seitigen Timeout Wert in Sekunden angibt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-207">An integer value that specifies the client-side timeout value, in seconds.</span></span> <span data-ttu-id="2d51c-208">Dieser Wert gibt die Zeit an, die der Client auf Ergebnisse vom Server wartet, bevor die Suche beendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d51c-208">This value indicates the time the client waits for results from the server before stopping the search.</span></span> <span data-ttu-id="2d51c-209">Der Standardwert ist kein Timeout.</span><span class="sxs-lookup"><span data-stu-id="2d51c-209">The default is no time-out.</span></span>                                                                                                                                                                                                  |



 

<span data-ttu-id="2d51c-210">Im folgenden Codebeispiel wird gezeigt, wie Suchoptionen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2d51c-210">The following code example shows how to set search options.</span></span>


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



<span data-ttu-id="2d51c-211">Das dritte ADO-Objekt ist **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="2d51c-211">The third ADO object is **RecordSet**.</span></span> <span data-ttu-id="2d51c-212">Sie erhalten dieses Objekt, wenn Sie die **Execute** -Methode für ein **Command** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-212">You obtain this object when you invoke the **Execute** method on a **Command** object.</span></span> <span data-ttu-id="2d51c-213">Die primäre Funktion des **Recordset** -Objekts ist das Aufzählen des Resultsets und das Abrufen der Daten.</span><span class="sxs-lookup"><span data-stu-id="2d51c-213">The primary function of the **RecordSet** object is to enumerate the result set and obtain the data.</span></span> <span data-ttu-id="2d51c-214">Das Resultset kann Werte für Attribute enthalten, die sowohl einzelne als auch mehrere Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2d51c-214">The result set can contain values for attributes that have both single or multiple values.</span></span> <span data-ttu-id="2d51c-215">Das erhalten eines einwertigen Attributs ist einfach, ähnlich wie beim erhalten des Spaltenwerts in der relationalen Datenbank, z. b.:</span><span class="sxs-lookup"><span data-stu-id="2d51c-215">Getting a single-valued attribute is simple, similar to getting the column value in the relational database, for example:</span></span>


```VB
Fields('name').Value
```



<span data-ttu-id="2d51c-216">Es ist jedoch schwieriger, ein Attribut mit mehreren Werten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2d51c-216">Getting an attribute with multiple values, however, is more challenging.</span></span> <span data-ttu-id="2d51c-217">In diesem Fall ist " **field. Value** " ein Array, und Sie müssen die untere und obere Grenze des Arrays überprüfen, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2d51c-217">In this case, the **Field.Value** is an array and you must check the lower and upper bound of the array, as shown in the following code example.</span></span>


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



<span data-ttu-id="2d51c-218">Im folgenden Codebeispiel werden die Benutzerkonten auf einem LDAP-Server deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2d51c-218">The following code example disables the user accounts on an LDAP server.</span></span>


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



<span data-ttu-id="2d51c-219">Weitere Informationen zum ADO-Objektmodell finden Sie unter [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span><span class="sxs-lookup"><span data-stu-id="2d51c-219">For more information about the ADO object model, see [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).</span></span>

 

