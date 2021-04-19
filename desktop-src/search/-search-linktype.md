---
description: Gibt den Linktyp beim Crawlen oder indizieren an.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Linktype-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343242"
---
# <a name="linktype-enumeration"></a>Linktype-Enumeration

\[Die **linktype** -Enumeration wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.\]

Gibt den Linktyp beim Crawlen oder indizieren an.

## <a name="syntax"></a>Syntax


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**linktype- \_ URL**
</dt> <dd>

Gibt an, ob der Linktyp der URLs indiziert werden soll.

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**linktype- \_ Inhalt**
</dt> <dd>

Gibt an, ob der Link Inhalt indiziert werden soll.

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**linktype \_ verwandt**
</dt> <dd>

Gibt einen zugehörigen Link an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die **linktype** -Flags und die folgenden anderen APIs zu verwenden: die Methoden [**iitempreviewerext:: getlinkedcontent**](-search-iitempreviewerext-getlinkedcontent.md) und [**iitempreviewerext:: getrelatedpart**](-search-iitempreviewerext-getrelatedpart.md) und die [**linkinfo**](-search-linkinfo.md) -Struktur

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |



 

 




