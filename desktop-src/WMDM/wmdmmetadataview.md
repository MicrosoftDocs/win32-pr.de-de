---
title: WMDMMetadataView-Struktur
description: Die WMDMMetadataView-Struktur definiert die Metadatenansicht. Der Inhalt wird basierend auf dieser Definition organisiert.
ms.assetid: 787d2295-d433-451d-a1fc-6f73585e10d6
keywords:
- WMDMMetadataView-Strukturfenster Media Geräte-Manager
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
ms.openlocfilehash: 8e442ed3058f1982ac7607c6b8a29e5df321d69776695821b278049e27cd7589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862590"
---
# <a name="wmdmmetadataview-structure"></a>WMDMMetadataView-Struktur

Die **WMDMMetadataView-Struktur** definiert die Metadatenansicht. Der Inhalt wird basierend auf dieser Definition organisiert.

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

**pwszViewName**
</dt> <dd>

Zeiger auf eine auf NULL endende Breitzeichenzeichenzeichenfolge, die den Namen der Ansicht enthält. Dies wird als Name des Stammknotens verwendet, unter dem diese Ansicht angezeigt wird.

</dd> <dt>

**nDepth**
</dt> <dd>

Ganze Zahl, die die Tiefe der Sicht enthält, die angibt, wie viele geschachtelte Metadatentags für die Sicht verwendet werden.

</dd> <dt>

**ppwszTags**
</dt> <dd>

Array von Metadatentagzeichenfolgen für die geschachtelten Tags.

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



Der vorangehende Code organisiert Inhalt wie folgt:

<dl> Meine Ansicht<dl> Genre1<dl> Interpret1<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> Artist2<dl> Album1<dl> Song1  
Song2  
...  
</dl> </dd> Album2  
...  
</dl> </dd> </dl> </dd> Genre2<dl> Interpret1<dl> Album1<dl> Song1  
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
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





