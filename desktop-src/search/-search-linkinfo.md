---
description: Speichert Informationen zu Linktypen und wird von der IItemPreviewerExt-Schnittstelle verwendet.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: LINKINFO-Struktur
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
ms.openlocfilehash: 97c106a5a819ac1068501c77555f3eae238c935e2262894c6c250dfc6782188f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863943"
---
# <a name="linkinfo-structure"></a>LINKINFO-Struktur

\[**LINKINFO** und [**IItemPreviewerExt**](-search-iitempreviewerext.md) werden nur auf Windows XP und Windows Server 2003 unterstützt und sollten nicht mehr verwendet werden.\]

Speichert Informationen zu Linktypen und wird von der [**IItemPreviewerExt-Schnittstelle**](-search-iitempreviewerext.md) verwendet.

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

Typ: **[ **LINKTYPE**](-search-linktype.md)**

</dd> <dd>

Der Typ des Links, der beim Durchforsten oder Indizieren angegeben wird, der durch eine [**LINKTYPE-Konstante**](-search-linktype.md) angegeben wird.

</dd> <dt>

**bstrContentType**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Ein **BSTR-Wert,** der den Inhaltstyp angibt.

</dd> <dt>

**bstrEncoding**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Ein encodingStyle-Attribut, das in der WSDL-Datei (Web Services Description Language) angegeben ist.

</dd> <dt>

**bstrFileExt**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Ein **BSTR-Wert,** der die Dateinamenerweiterung angibt.

</dd> <dt>

**varData**
</dt> <dd>

Typ: **VARIANT**

</dd> <dd>

Eine Variante, die den Variablenwert angibt.

</dd> <dt>

**dwRelatedParts**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Ein **DWORD,** das die verknüpften Teile angibt.

</dd> <dt>

**bstrRelatedCid**
</dt> <dd>

Typ: **BSTR**

</dd> <dd>

Ein **BSTR-Wert,** der eine Cid-Eigenschaft angibt, eine nicht aufgefüllte Dezimalzeichenfolge mit Vorzeichen.

</dd> <dt>

**lCodePage**
</dt> <dd>

Typ: **Long**

</dd> <dd>

Die Codepage, die zum Codieren der Zeichenfolge verwendet werden soll.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die **LINKINFO-Struktur** und die folgenden APIs zu verwenden: die [**Methoden IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) und [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) sowie die [**LINKTYPE-Enumeration.**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>          |



 

 




