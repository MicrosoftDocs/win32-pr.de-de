---
description: Erweitert Eigenschaften, die für die Rowset-APIs definiert sind.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba37466c52f2fa9f83e3aa439ace03c1fba34f44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368959"
---
# <a name="dbpropset_msidxs_rowsetext"></a><span data-ttu-id="e69df-103">DBPROPSET \_ msidxs \_ rowsetext</span><span class="sxs-lookup"><span data-stu-id="e69df-103">DBPROPSET\_MSIDXS\_ROWSETEXT</span></span>

<span data-ttu-id="e69df-104">Erweitert Eigenschaften, die für die Rowset-APIs definiert sind.</span><span class="sxs-lookup"><span data-stu-id="e69df-104">Extends properties defined for the Rowset APIs.</span></span>

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

<span data-ttu-id="e69df-105">Der DBPROPSET \_ msidxs \_ rowsetext-Eigenschaften Satz enthält die folgenden Eigenschafts Konstanten:</span><span class="sxs-lookup"><span data-stu-id="e69df-105">The DBPROPSET\_MSIDXS\_ROWSETEXT property set contains the following property constants:</span></span>

<dl> <dt>

<span data-ttu-id="e69df-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>msidxsprop- \_ rowsetquerystatus</span><span class="sxs-lookup"><span data-stu-id="e69df-106"><span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP\_ROWSETQUERYSTATUS</span></span>
</dt> <dd>

<span data-ttu-id="e69df-107">Eigenschaften-ID 2.</span><span class="sxs-lookup"><span data-stu-id="e69df-107">Property ID 2.</span></span> <span data-ttu-id="e69df-108">Der Abfrage Status für das Rowset.</span><span class="sxs-lookup"><span data-stu-id="e69df-108">Query status for the rowset.</span></span> <span data-ttu-id="e69df-109">Die stat \_ \* -Konstanten geben den Ausführungs-und Zuverlässigkeits Status an.</span><span class="sxs-lookup"><span data-stu-id="e69df-109">The STAT\_\* constants indicate the execution and reliability status.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>Gebiets Schema \_ \_ \_ Zeichenfolge "msidxsprop"</span><span class="sxs-lookup"><span data-stu-id="e69df-110"><span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>MSIDXSPROP\_COMMAND\_LOCALE\_STRING</span></span>
</dt> <dd>

<span data-ttu-id="e69df-111">Eigen schafts-ID 3.</span><span class="sxs-lookup"><span data-stu-id="e69df-111">Property ID 3.</span></span> <span data-ttu-id="e69df-112">Gebiets Schema Zeichenfolge, die die für dieses Rowset zu verwendende sprach-und Gebiets Schema Einstellung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e69df-112">Locale string that represents the language and locale setting to use for this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>msidxsprop- \_ Abfrage \_ Einschränkung</span><span class="sxs-lookup"><span data-stu-id="e69df-113"><span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP\_QUERY\_RESTRICTION</span></span>
</dt> <dd>

<span data-ttu-id="e69df-114">Eigen schafts-ID 4.</span><span class="sxs-lookup"><span data-stu-id="e69df-114">Property ID 4.</span></span> <span data-ttu-id="e69df-115">Die Abfrage Zeichenfolge, die diesem Rowset zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="e69df-115">The query string associated with this rowset.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>msidxsprop-Analyse Struktur \_ \_</span><span class="sxs-lookup"><span data-stu-id="e69df-116"><span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP\_PARSE\_TREE</span></span>
</dt> <dd>

<span data-ttu-id="e69df-117">Eigen schafts-ID 5.</span><span class="sxs-lookup"><span data-stu-id="e69df-117">Property ID 5.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>Maximaler msidxsprop- \_ \_ Rang</span><span class="sxs-lookup"><span data-stu-id="e69df-118"><span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP\_MAX\_RANK</span></span> 
</dt> <dd>

<span data-ttu-id="e69df-119">Eigen schafts-ID 6.</span><span class="sxs-lookup"><span data-stu-id="e69df-119">Property ID 6.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>msidxsprop- \_ Ergebnisse \_ gefunden</span><span class="sxs-lookup"><span data-stu-id="e69df-120"><span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>MSIDXSPROP\_RESULTS\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="e69df-121">Eigen schafts-ID 7.</span><span class="sxs-lookup"><span data-stu-id="e69df-121">Property ID 7.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>msidxsprop \_ whereid</span><span class="sxs-lookup"><span data-stu-id="e69df-122"><span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP\_WHEREID</span></span>
</dt> <dd>

<span data-ttu-id="e69df-123">Eigen schafts-ID 8.</span><span class="sxs-lookup"><span data-stu-id="e69df-123">Property ID 8.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>msidxsprop- \_ Server \_ Version</span><span class="sxs-lookup"><span data-stu-id="e69df-124"><span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>MSIDXSPROP\_SERVER\_VERSION</span></span> 
</dt> <dd>

<span data-ttu-id="e69df-125">Neu in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e69df-125">New for Windows 7.</span></span> <span data-ttu-id="e69df-126">Eigen schafts-ID 9.</span><span class="sxs-lookup"><span data-stu-id="e69df-126">Property ID 9.</span></span> <span data-ttu-id="e69df-127">Die Server Version.</span><span class="sxs-lookup"><span data-stu-id="e69df-127">The server version.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>msidxsprop- \_ Server \_ winver- \_ Hauptversion</span><span class="sxs-lookup"><span data-stu-id="e69df-128"><span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP\_SERVER\_WINVER\_MAJOR</span></span>
</dt> <dd>

<span data-ttu-id="e69df-129">Eigen schafts-ID 10.</span><span class="sxs-lookup"><span data-stu-id="e69df-129">Property ID 10.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>msidxsprop- \_ Server \_ winver- \_ neben Version</span><span class="sxs-lookup"><span data-stu-id="e69df-130"><span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP\_SERVER\_WINVER\_MINOR</span></span>
</dt> <dd>

<span data-ttu-id="e69df-131">Eigen schafts-ID 11.</span><span class="sxs-lookup"><span data-stu-id="e69df-131">Property ID 11.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>msidxsprop- \_ Server \_ nlsversion</span><span class="sxs-lookup"><span data-stu-id="e69df-132"><span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP\_SERVER\_NLSVERSION</span></span>
</dt> <dd>

<span data-ttu-id="e69df-133">Eigen schafts-ID 12.</span><span class="sxs-lookup"><span data-stu-id="e69df-133">Property ID 12.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>msidxsprop- \_ Server, \_ nlsver \_ definiert</span><span class="sxs-lookup"><span data-stu-id="e69df-134"><span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP\_SERVER\_NLSVER\_DEFINED</span></span> 
</dt> <dd>

<span data-ttu-id="e69df-135">Eigen schafts-ID 13.</span><span class="sxs-lookup"><span data-stu-id="e69df-135">Property ID 13.</span></span>

</dd> <dt>

<span data-ttu-id="e69df-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>verwendeter msidxsprop- \_ \_ sortor \_</span><span class="sxs-lookup"><span data-stu-id="e69df-136"><span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP\_SAME\_SORTORDER\_USED</span></span> 
</dt> <dd>

<span data-ttu-id="e69df-137">Eigen schafts-ID 14.</span><span class="sxs-lookup"><span data-stu-id="e69df-137">Property ID 14.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e69df-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e69df-138">Remarks</span></span>

<span data-ttu-id="e69df-139">Zum Abfragen der msidxsprop- \_ Server \_ Version ist es erforderlich, die Dummy-Abfrage an den Server auszugeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="e69df-139">To query MSIDXSPROP\_SERVER\_VERSION, it is necessary to issue the dummy query to server, such as the following example.</span></span>

`SELECT top 1 workid from servername.systemindex`

<span data-ttu-id="e69df-140">Nachdem das Rowset zurückgegeben wurde, müssen Sie [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die Funktionen des Rowsets aufrufen und dann [IRowsetInfo:: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) für die neue Eigenschaft (msidxsprop- \_ Server \_ Version) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e69df-140">After the rowset has been returned, call [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the capabilities of the rowset and then call [IRowsetInfo::GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) for the new property (MSIDXSPROP\_SERVER\_VERSION).</span></span> <span data-ttu-id="e69df-141">Die-Eigenschaft hat den Typ **VT \_ I4** und kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="e69df-141">The property has a type of **VT\_I4** and can be one of the following values:</span></span>

<span data-ttu-id="e69df-142">\#CI \_ -Version definieren \_ WDS30 0x102//258</span><span class="sxs-lookup"><span data-stu-id="e69df-142">\#define CI\_VERSION\_WDS30 0x102 // 258</span></span>

<span data-ttu-id="e69df-143">\#CI \_ -Version definieren \_ WDS40 0x109//265</span><span class="sxs-lookup"><span data-stu-id="e69df-143">\#define CI\_VERSION\_WDS40 0x109 // 265</span></span>

<span data-ttu-id="e69df-144">\#CI \_ -Version definieren \_ WIN70 0x700//1792</span><span class="sxs-lookup"><span data-stu-id="e69df-144">\#define CI\_VERSION\_WIN70 0x700 // 1792</span></span>

<span data-ttu-id="e69df-145">Wenn der Wert bekannt ist, kann der Client eine Abfrage bilden, die vom Server unterstützt wird, und eine echte Abfrage ausgeben.</span><span class="sxs-lookup"><span data-stu-id="e69df-145">Once the value is known, the client can form a query which is supported by the server and issue a real query.</span></span>

<span data-ttu-id="e69df-146">DBPROPSET \_ msidxs \_ rowsetext ist in "ntquery. h" deklariert.</span><span class="sxs-lookup"><span data-stu-id="e69df-146">DBPROPSET\_MSIDXS\_ROWSETEXT is declared in ntquery.h.</span></span>

 

 
