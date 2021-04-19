---
title: WMDMMetadataView-Struktur
description: Die WMDMMetadataView-Struktur definiert die Metadatenansicht. Der Inhalt wird basierend auf dieser Definition organisiert.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- WMDMMetadataView Structure Windows Media Device Manager
topic_type:
- apiref
api_name:
- WMDMMetadataView
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aa38a8fe7f19137c5caff18417d48ea23168b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369933"
---
# <a name="wmdmmetadataview-structure"></a>WMDMMetadataView-Struktur

Die **WMDMMetadataView** -Struktur definiert die Metadatenansicht. Der Inhalt wird basierend auf dieser Definition organisiert.

## <a name="syntax"></a>Syntax


```C++
typedef struct _WMDMMetadataView {
  WCHAR *pwszViewName;
  UINT  nDepth;
  WCHAR **ppwszTags;
} WMDMMetadataView;
```



## <a name="members"></a>Member

<dl> <dt>

**pwszviewname**
</dt> <dd>

Zeiger auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die den Namen der Ansicht enthält. Diese wird als Name des Stamm Knotens verwendet, unter dem diese Ansicht angezeigt wird.

</dd> <dt>

**ntiefe**
</dt> <dd>

Eine ganze Zahl, die die Tiefe der Ansicht enthält, die angibt, wie viele schachtelte Metadatentags für die Sicht verwendet werden.

</dd> <dt>

**ppwsztags**
</dt> <dd>

Array von metadatentagzeichenfolgen für die geschachtelte-Tags.

</dd> </dl>

## <a name="examples"></a>Beispiele

Der folgende Code erstellt eine Metadatenansicht:


```C++
WMDMMetadataView view;
view.pwszName = L"My View";
view.nDepth = 3;  // genre, artist, album
LPCWSTR wszTagArray[3]; 
wszTagArray[0] = g_wszWMDMGenre;
wszTagArray[1] = g_wszWMDMAuthor;
wszTagArray[2] = g_wszWMDMAlbumTitle;
view.ppwszTags = wszTagArray;
```



Im vorangehenden Code werden die Inhalte wie folgt organisiert:

<dl> Meine Ansicht<dl> Genre1<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Artist1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> ...  
</dl> </dd> ...  
</dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





