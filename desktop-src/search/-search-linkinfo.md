---
description: Speichert Informationen zu Linktypen und wird von der iitempreviewerext-Schnittstelle verwendet.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Linkinfo-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214461"
---
# <a name="linkinfo-structure"></a>Linkinfo-Struktur

\[**Linkinfo** und [**iitempreviewerext**](-search-iitempreviewerext.md) werden nur unter Windows XP und Windows Server 2003 unterstützt und sollten nicht mehr verwendet werden.\]

Speichert Informationen zu Linktypen und wird von der [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle verwendet.

## <a name="syntax"></a>Syntax


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a>Member

<dl> <dt>

**type**
</dt> <dd>

Typ: **[ **linktype**](-search-linktype.md)**

</dd> <dd>

Der Linktyp, der beim Crawlen oder indizieren angegeben wird, angegeben durch eine [**linktype**](-search-linktype.md) -Konstante.

</dd> <dt>

**bstrincontenttype**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Ein **BSTR** -Wert, der den Inhaltstyp angibt.

</dd> <dt>

**bstrencoding**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Ein encodingStyle-Attribut, das in der Web Services Description Language (WSDL)-Datei angegeben ist.

</dd> <dt>

**bstraufileext**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Ein **BSTR** -Wert, der die Dateinamenerweiterung angibt.

</dd> <dt>

**VARDATA**
</dt> <dd>

Typ: **Variant**

</dd> <dd>

Eine Variante, die den Variablen Wert angibt.

</dd> <dt>

**dwrelatedparts**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein **DWORD** , das die zugehörigen Teile angibt.

</dd> <dt>

**bstrinrelatedcid**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Ein **BSTR** -Wert, der eine CID-Eigenschaft angibt, eine nicht aufgefüllte, dezimale Zeichenfolge mit Vorzeichen.

</dd> <dt>

**lcodepage**
</dt> <dd>

Type: **Long**

</dd> <dd>

Die Codepage, die zum Codieren der Zeichenfolge verwendet werden soll.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die **linkinfo** -Struktur und die folgenden APIs zu verwenden: die Methoden [**iitempreviewerext:: getlinkedcontent**](-search-iitempreviewerext-getlinkedcontent.md) und [**iitempreviewerext:: getrelatedpart**](-search-iitempreviewerext-getrelatedpart.md) und die [**linktype**](-search-linktype.md) -Enumeration

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>          |



 

 




