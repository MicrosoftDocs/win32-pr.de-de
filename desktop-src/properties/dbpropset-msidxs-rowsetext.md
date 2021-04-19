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
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ msidxs \_ rowsetext

Erweitert Eigenschaften, die für die Rowset-APIs definiert sind.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

Der DBPROPSET \_ msidxs \_ rowsetext-Eigenschaften Satz enthält die folgenden Eigenschafts Konstanten:

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>msidxsprop- \_ rowsetquerystatus
</dt> <dd>

Eigenschaften-ID 2. Der Abfrage Status für das Rowset. Die stat \_ \* -Konstanten geben den Ausführungs-und Zuverlässigkeits Status an.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>Gebiets Schema \_ \_ \_ Zeichenfolge "msidxsprop"
</dt> <dd>

Eigen schafts-ID 3. Gebiets Schema Zeichenfolge, die die für dieses Rowset zu verwendende sprach-und Gebiets Schema Einstellung darstellt.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>msidxsprop- \_ Abfrage \_ Einschränkung
</dt> <dd>

Eigen schafts-ID 4. Die Abfrage Zeichenfolge, die diesem Rowset zugeordnet ist.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>msidxsprop-Analyse Struktur \_ \_
</dt> <dd>

Eigen schafts-ID 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>Maximaler msidxsprop- \_ \_ Rang 
</dt> <dd>

Eigen schafts-ID 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>msidxsprop- \_ Ergebnisse \_ gefunden
</dt> <dd>

Eigen schafts-ID 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>msidxsprop \_ whereid
</dt> <dd>

Eigen schafts-ID 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>msidxsprop- \_ Server \_ Version 
</dt> <dd>

Neu in Windows 7. Eigen schafts-ID 9. Die Server Version.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>msidxsprop- \_ Server \_ winver- \_ Hauptversion
</dt> <dd>

Eigen schafts-ID 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>msidxsprop- \_ Server \_ winver- \_ neben Version
</dt> <dd>

Eigen schafts-ID 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>msidxsprop- \_ Server \_ nlsversion
</dt> <dd>

Eigen schafts-ID 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>msidxsprop- \_ Server, \_ nlsver \_ definiert 
</dt> <dd>

Eigen schafts-ID 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>verwendeter msidxsprop- \_ \_ sortor \_ 
</dt> <dd>

Eigen schafts-ID 14.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zum Abfragen der msidxsprop- \_ Server \_ Version ist es erforderlich, die Dummy-Abfrage an den Server auszugeben, wie im folgenden Beispiel gezeigt.

`SELECT top 1 workid from servername.systemindex`

Nachdem das Rowset zurückgegeben wurde, müssen Sie [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die Funktionen des Rowsets aufrufen und dann [IRowsetInfo:: GetProperties](/previous-versions/windows/desktop/ms719611(v=vs.85)) für die neue Eigenschaft (msidxsprop- \_ Server \_ Version) aufrufen. Die-Eigenschaft hat den Typ **VT \_ I4** und kann einen der folgenden Werte aufweisen:

\#CI \_ -Version definieren \_ WDS30 0x102//258

\#CI \_ -Version definieren \_ WDS40 0x109//265

\#CI \_ -Version definieren \_ WIN70 0x700//1792

Wenn der Wert bekannt ist, kann der Client eine Abfrage bilden, die vom Server unterstützt wird, und eine echte Abfrage ausgeben.

DBPROPSET \_ msidxs \_ rowsetext ist in "ntquery. h" deklariert.

 

 
