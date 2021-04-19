---
title: Beitreten zu heterogenen Daten
description: In typischen Organisationen werden Daten in mehreren heterogenen Datenbanken gespeichert. Personaldaten können in SQL Server gespeichert werden, während die Konto Verwaltungsdaten im Verzeichnis gespeichert werden. Andere Daten können in proprietären Formaten gespeichert werden.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1099028bc85dc6492eade0315b7308b4c6aaa9
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314613"
---
# <a name="joining-heterogeneous-data"></a><span data-ttu-id="c4568-105">Beitreten zu heterogenen Daten</span><span class="sxs-lookup"><span data-stu-id="c4568-105">Joining Heterogeneous Data</span></span>

<span data-ttu-id="c4568-106">In typischen Organisationen werden Daten in mehreren heterogenen Datenbanken gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c4568-106">Typical organizations store data in multiple heterogeneous databases.</span></span> <span data-ttu-id="c4568-107">Personaldaten können in SQL Server gespeichert werden, während die Konto Verwaltungsdaten im Verzeichnis gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c4568-107">Human Resources data may be stored in SQL Server, while account management data is stored in the directory.</span></span> <span data-ttu-id="c4568-108">Andere Daten können in proprietären Formaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c4568-108">Other data may be stored in proprietary formats.</span></span>

<span data-ttu-id="c4568-109">Mit SQL Server 7,0, ADSI und der OLE DB-Anbieter ist es möglich, Daten aus Active Directory mit Daten in SQL Server zu verknüpfen und eine Ansicht der verknüpften Daten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4568-109">With, SQL Server 7.0, ADSI, and the OLE DB Provider, it is possible to join data from Active Directory to data in SQL Server and create a view of the joined data.</span></span>

<span data-ttu-id="c4568-110">**So verknüpfen Sie Active Directory Daten mit SQL Server Daten**</span><span class="sxs-lookup"><span data-stu-id="c4568-110">**To join Active Directory Data with SQL Server Data**</span></span>

1.  <span data-ttu-id="c4568-111">Ausführen von **SQL Query Analyzer** ( \| Programme starten \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="c4568-111">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
2.  <span data-ttu-id="c4568-112">Melden Sie sich beim SQL Server Computer an.</span><span class="sxs-lookup"><span data-stu-id="c4568-112">Log on to the SQL Server computer.</span></span>
3.  <span data-ttu-id="c4568-113">Führen Sie die folgende Zeile aus (indem Sie Sie markieren und STRG + E drücken):</span><span class="sxs-lookup"><span data-stu-id="c4568-113">Execute the following line (by highlighting it and pressing CTRL+E):</span></span>

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    <span data-ttu-id="c4568-114">In dieser Zeile lauten die Argumente für die gespeicherte System Prozedur [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c4568-114">In this line, the arguments for the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure are as follows:</span></span>

    -   <span data-ttu-id="c4568-115">"ADSI" ist das **Server** Argument, bei dem es sich um den Namen dieses Verbindungs Servers handelt.</span><span class="sxs-lookup"><span data-stu-id="c4568-115">" ADSI" is the **server** argument, which will be the name of this linked server.</span></span>
    -   <span data-ttu-id="c4568-116">"Active Directory Services" ist das **srvproduct** -Argument, bei dem es sich um den Namen der OLE DB Datenquelle handelt, die Sie als Verbindungs Server hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c4568-116">"Active Directory Services" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
    -   <span data-ttu-id="c4568-117">"ADSDSOObject" ist das **Anbieter \_ Namen** Argument und gibt an, dass Sie den OLE DB Anbieter verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4568-117">"ADSDSOObject" is the **provider\_name** argument and indicates you are using the OLE DB Provider.</span></span>
    -   <span data-ttu-id="c4568-118">"adsdatasource" ist das **Daten \_ Quellen Argument**, bei dem es sich um den Namen der Datenquelle handelt, die vom OLE DB Anbieter interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="c4568-118">"adsdatasource" is the **data\_source argument**, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

    <span data-ttu-id="c4568-119">Sie können jetzt den Verbindungs Server verwenden, um auf Active Directory aus SQL Server zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c4568-119">You can now use the linked server to access Active Directory from SQL Server.</span></span>

4.  <span data-ttu-id="c4568-120">Im nächsten Beispiel wird eine Abfrage mithilfe der [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) -Anweisung durchführt.</span><span class="sxs-lookup"><span data-stu-id="c4568-120">The next example performs a query using the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="c4568-121">Diese Anweisung hat zwei Argumente: ADSI, den Namen des soeben erstellten Verbindungs Servers und eine Abfrage Anweisung.</span><span class="sxs-lookup"><span data-stu-id="c4568-121">This statement has two arguments: ADSI, which is the name of the linked server that you just created, and a query statement.</span></span> <span data-ttu-id="c4568-122">Die Abfrage Anweisung enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="c4568-122">The query statement contains the following items:</span></span>

    -   <span data-ttu-id="c4568-123">Die [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung enthält die Liste der Daten, die vom Verzeichnisdienst abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c4568-123">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="c4568-124">Sie müssen den LDAP-anzeigen Amen verwenden, um anzugeben, nach welchen Daten Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="c4568-124">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
    -   <span data-ttu-id="c4568-125">Die [from](https://msdn.microsoft.com/library/Aa258869.aspx) -Anweisung enthält den Namen des Verbindungs Verzeichnis Servers, von dem diese Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c4568-125">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
    -   <span data-ttu-id="c4568-126">Die [Where](https://msdn.microsoft.com/library/Aa260674.aspx) -Anweisung stellt die Suchbedingungen bereit.</span><span class="sxs-lookup"><span data-stu-id="c4568-126">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="c4568-127">In diesem Beispiel sucht es nach Benutzern.</span><span class="sxs-lookup"><span data-stu-id="c4568-127">In this example, it is searching for users.</span></span>

    <span data-ttu-id="c4568-128">Typ und Execute:</span><span class="sxs-lookup"><span data-stu-id="c4568-128">Type and execute:</span></span>

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    <span data-ttu-id="c4568-129">Sie können auch den ADSI [LDAP-Dialekt](ldap-dialect.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="c4568-129">You can also use the ADSI [LDAP dialect](ldap-dialect.md).</span></span> <span data-ttu-id="c4568-130">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c4568-130">For example:</span></span>

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    <span data-ttu-id="c4568-131">Im vorherigen Beispiel besteht die LDAP-Abfrage aus vier Teilen:</span><span class="sxs-lookup"><span data-stu-id="c4568-131">In the previous example, the LDAP query has four parts:</span></span>

    -   <span data-ttu-id="c4568-132">" \<LDAP://DC=Fabrikam,DC=COM> " ist der Distinguished Name des Verzeichnis Servers, der durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4568-132">"\<LDAP://DC=Fabrikam,DC=COM>" is the distinguished name of the directory server to search.</span></span>
    -   <span data-ttu-id="c4568-133">"(& (objectCategory = Person) (objectClass = User))" ist der LDAP-Suchfilter (siehe [Syntax für Suchfilter](search-filter-syntax.md)).</span><span class="sxs-lookup"><span data-stu-id="c4568-133">"(&(objectCategory=Person)(objectClass=user))" is the LDAP search filter (see [Search Filter Syntax](search-filter-syntax.md)).</span></span>
    -   <span data-ttu-id="c4568-134">"Name, ADsPath" sind die Namen (mit dem Format des LDAP-Anzeige namens) der abzurufenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="c4568-134">"name, adspath" are the names (using the LDAP display name format) of the attributes to retrieve.</span></span>
    -   <span data-ttu-id="c4568-135">"subtree" gibt den Such [Bereich](scope-of-query.md) an.</span><span class="sxs-lookup"><span data-stu-id="c4568-135">"subtree" indicates the [scope](scope-of-query.md) of the search.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4568-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4568-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4568-137">Erstellen und Ausführen einer Ansicht</span><span class="sxs-lookup"><span data-stu-id="c4568-137">Creating and Executing a View</span></span>](creating-and-executing-a-view.md)
</dt> </dl>

 

 




