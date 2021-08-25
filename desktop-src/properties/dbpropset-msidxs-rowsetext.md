---
description: Erweitert die für die Rowset-APIs definierten Eigenschaften.
ms.assetid: C1A2DF19-C68D-42CC-9CB2-190F22CB4158
title: DBPROPSET_MSIDXS_ROWSETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8c647d4b1ecbf9e5cc88ccae4af649c27093472456377e478ff80f7a76f3a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776410"
---
# <a name="dbpropset_msidxs_rowsetext"></a>DBPROPSET \_ MSIDXS \_ ROWSETEXT

Erweitert die für die Rowset-APIs definierten Eigenschaften.

``` syntax
#define DBPROPSET_MSIDXS_ROWSETEXT \
    { 0xaa6ee6b0, 0xe828, 0x11d0, \
        { 0xb2, 0x3e, 0x00, 0xaa, 0x00, 0x47, 0xfc, 0x01 } }
```

Der DBPROPSET \_ MSIDXS \_ ROWSETEXT-Eigenschaftensatz enthält die folgenden Eigenschaftenkonst constants:

<dl> <dt>

<span id="MSIDXSPROP_ROWSETQUERYSTATUS"></span><span id="msidxsprop_rowsetquerystatus"></span>MSIDXSPROP \_ ROWSETQUERYSTATUS
</dt> <dd>

Eigenschaften-ID 2. Abfragestatus für das Rowset. Die \_ \* STAT-Konstanten geben den Ausführungs- und Zuverlässigkeitsstatus an.

</dd> <dt>

<span id="MSIDXSPROP_COMMAND_LOCALE_STRING"></span><span id="msidxsprop_command_locale_string"></span>\_ \_ MSIDXSPROP-BEFEHLS-LOCALE-ZEICHENFOLGE \_
</dt> <dd>

Eigenschaften-ID 3. Eine Zeichenfolge des Locales, die die Sprache und die Für dieses Rowset zu verwendende Locale-Einstellung darstellt.

</dd> <dt>

<span id="MSIDXSPROP_QUERY_RESTRICTION"></span><span id="msidxsprop_query_restriction"></span>MSIDXSPROP-ABFRAGEEINSCHRÄNKUNG \_ \_
</dt> <dd>

Eigenschaften-ID 4. Die diesem Rowset zugeordnete Abfragezeichenfolge.

</dd> <dt>

<span id="MSIDXSPROP_PARSE_TREE"></span><span id="msidxsprop_parse_tree"></span>MSIDXSPROP-ANALYSESTRUKTUR \_ \_
</dt> <dd>

Eigenschaften-ID 5.

</dd> <dt>

<span id="MSIDXSPROP_MAX_RANK___"></span><span id="msidxsprop_max_rank___"></span>MSIDXSPROP \_ MAX \_ RANK 
</dt> <dd>

Eigenschaften-ID 6.

</dd> <dt>

<span id="MSIDXSPROP_RESULTS_FOUND"></span><span id="msidxsprop_results_found"></span>MSIDXSPROP-ERGEBNISSE \_ \_ GEFUNDEN
</dt> <dd>

Eigenschaften-ID 7.

</dd> <dt>

<span id="MSIDXSPROP_WHEREID"></span><span id="msidxsprop_whereid"></span>MSIDXSPROP \_ WHEREID
</dt> <dd>

Eigenschaften-ID 8.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_VERSION_"></span><span id="msidxsprop_server_version_"></span>\_MSIDXSPROP-SERVERVERSION \_ 
</dt> <dd>

Neu für Windows 7. Eigenschaften-ID 9. Die Serverversion.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MAJOR"></span><span id="msidxsprop_server_winver_major"></span>MSIDXSPROP \_ SERVER \_ WINVER \_ MAJOR
</dt> <dd>

Eigenschaften-ID 10.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_WINVER_MINOR"></span><span id="msidxsprop_server_winver_minor"></span>MSIDXSPROP \_ SERVER \_ WINVER \_ MINOR
</dt> <dd>

Eigenschaften-ID 11.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVERSION"></span><span id="msidxsprop_server_nlsversion"></span>MSIDXSPROP \_ SERVER \_ NLSVERSION
</dt> <dd>

Eigenschaften-ID 12.

</dd> <dt>

<span id="MSIDXSPROP_SERVER_NLSVER_DEFINED_"></span><span id="msidxsprop_server_nlsver_defined_"></span>MSIDXSPROP \_ SERVER \_ NLSVER \_ DEFINIERT 
</dt> <dd>

Eigenschaften-ID 13.

</dd> <dt>

<span id="MSIDXSPROP_SAME_SORTORDER_USED_"></span><span id="msidxsprop_same_sortorder_used_"></span>MSIDXSPROP \_ SAME \_ SORTORDER \_ USED 
</dt> <dd>

Eigenschaften-ID 14.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Zum Abfragen der MSIDXSPROP SERVER-VERSION muss die Dummyabfrage an den Server gesendet werden, wie \_ \_ im folgenden Beispiel.

`SELECT top 1 workid from servername.systemindex`

Nachdem das Rowset zurückgegeben wurde, rufen Sie [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die Funktionen des Rowsets auf, und rufen Sie [dann IRowsetInfo::GetProperties für](/previous-versions/windows/desktop/ms719611(v=vs.85)) die neue Eigenschaft (MSIDXSPROP \_ SERVER \_ VERSION) auf. Die -Eigenschaft hat den Typ **VT \_ I4** und kann einen der folgenden Werte haben:

\#Definieren der \_ CI-VERSION \_ WDS30 0x102 / 258

\#Definieren der \_ CI-VERSION \_ WDS40 0x109 / 265

\#DEFINE CI \_ VERSION \_ WIN70 0x700 / 1792

Sobald der Wert bekannt ist, kann der Client eine Abfrage erstellen, die vom Server unterstützt wird, und eine echte Abfrage ausführen.

DBPROPSET \_ MSIDXS \_ ROWSETEXT wird in ntquery.h deklariert.

 

 
