---
description: Gibt den Typ des Links beim Durchforsten oder Indizieren an.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: LINKTYPE-Enumeration
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
ms.openlocfilehash: 16c61f8d92a6f90be0fa4b64ddd9d582987ac0bdf52ca1c596c7db3a7fa4b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463043"
---
# <a name="linktype-enumeration"></a>LINKTYPE-Enumeration

\[Die **LINKTYPE-Enumeration** wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.\]

Gibt den Typ des Links beim Durchforsten oder Indizieren an.

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

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**\_LINKTYPE-URL**
</dt> <dd>

Gibt an, ob der URL-Linktyp indiziert werden soll.

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**\_LINKTYPE-INHALT**
</dt> <dd>

Gibt an, ob der Linkinhalt indiziert werden soll.

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE \_ RELATED**
</dt> <dd>

Gibt einen verknüpften Link an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um eine Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern anzuzeigen, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die **LINKTYPE-Flags** und die folgenden anderen APIs zu verwenden: [**die Methoden IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) und [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) und die [**LINKINFO-Struktur.**](-search-linkinfo.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |



 

 




