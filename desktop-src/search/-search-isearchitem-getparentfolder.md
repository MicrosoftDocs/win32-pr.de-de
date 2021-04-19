---
description: Ruft das isearchitem-Objekt ab, wenn die URL eine tatsächliche shelldatenquelle darstellt (wird auch als Shellnamespace-Erweiterung bezeichnet).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: 'Isearchitem:: getParser Folder-Methode'
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
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345020"
---
# <a name="isearchitemgetparentfolder-method"></a>Isearchitem:: getParser Folder-Methode

Ruft das [**isearchitem**](-search-isearchitem.md) -Objekt ab, wenn die URL eine tatsächliche shelldatenquelle darstellt (wird auch als Shellnamespace-Erweiterung bezeichnet).

## <a name="syntax"></a>Syntax


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IShellFolder* \[ vorgenommen\]
</dt> <dd>

Typ: **ppshellfolder \* \***

Enthält bei der Rückgabe die Adresse eines Zeigers auf den Ordner, der die aktuelle URL enthält. Die [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) wird von allen Shell-Namespace-Ordner Objekten bereitgestellt, und die zugehörigen Methoden werden zum Verwalten von Ordnern verwendet.

</dd> <dt>

*Lpitemittellist* \[ vorgenommen\]
</dt> <dd>

Typ: **ppidl \** _

Enthält bei der Rückgabe die Adresse eines Zeigers auf eine Element Bezeichner Liste (PIDL), die den übergeordneten Ordner identifiziert. Der Parameter "_LPITEMIDLIST *" kann auf ein Objekt auf jeder Ebene unterhalb des übergeordneten Ordners in der Namespace Hierarchie verweisen. Daher kann es sich um einen mehrstufigen Zeiger auf eine **PIDL** relativ zum übergeordneten Ordner handeln.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die **isearchitem:: getParser Folder** -Methode wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die [**isearchitem**](-search-isearchitem.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**iitempreviewerext**](-search-iitempreviewerext.md), [**iitempropertybag**](iitempropertybag.md)und [**isearchprotocolui**](-search-isearchprotocolui.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Isearchitem**](-search-isearchitem.md)
</dt> </dl>

 

 
