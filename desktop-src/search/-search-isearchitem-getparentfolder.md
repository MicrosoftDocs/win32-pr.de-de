---
description: Ruft das ISearchItem-Objekt ab, wenn die URL eine tatsächliche Shell-Datenquelle darstellt (auch als Shellnamespaceerweiterung bekannt).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: ISearchItem::GetParentFolder-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: a5e5aded87ca197af8774a7b5506e21c958dc564eb0af67396e100877ac53e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094910"
---
# <a name="isearchitemgetparentfolder-method"></a>ISearchItem::GetParentFolder-Methode

Ruft das [**ISearchItem-Objekt**](-search-isearchitem.md) ab, wenn die URL eine tatsächliche Shell-Datenquelle darstellt (auch als Shellnamespaceerweiterung bekannt).

## <a name="syntax"></a>Syntax


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IShellFolder* \[ out\]
</dt> <dd>

Typ: **ppShellFolder \* \***

Enthält bei der Rückgabe die Adresse eines Zeigers auf den Ordner, der die aktuelle URL enthält. [Die IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) wird von allen Shell-Namespaceordnerobjekten verfügbar gemacht, und ihre Methoden werden zum Verwalten von Ordnern verwendet.

</dd> <dt>

*LPITEMIDLIST* \[ out\]
</dt> <dd>

Typ: **dl \***

Enthält bei der Rückgabe die Adresse eines Zeigers auf eine Elementbezeichnerliste (PIDL), die den übergeordneten Ordner identifiziert. Der *LPITEMIDLIST-Parameter* kann auf ein Objekt auf einer beliebigen Ebene unterhalb des übergeordneten Ordners in der Namespacehierarchie verweisen und kann daher ein Zeiger auf mehrere Ebenen auf eine **Pidl** relativ zum übergeordneten Ordner sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die **ISearchItem::GetParentFolder-Methode** wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Um eine Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern anzuzeigen, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**ISearchItem-Schnittstelle**](-search-isearchitem.md) und die folgenden APIs zu verwenden: die [**Schnittstellen IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md)und [**ISearchProtocolUI,**](-search-isearchprotocolui.md) die [**LINKINFO-Struktur**](-search-linkinfo.md) und die [**LINKTYPE-Enumeration.**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISearchItem**](-search-isearchitem.md)
</dt> </dl>

 

 
