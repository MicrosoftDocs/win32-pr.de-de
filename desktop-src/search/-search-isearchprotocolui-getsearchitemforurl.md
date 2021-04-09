---
description: Ruft das Suchelement für die angegebenen Daten ab. Diese Methode wird einmal für jede URL aufgerufen, die vom Gatherer verarbeitet wird, und Ruft einen Zeiger auf das isearchitem-Objekt ab.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: 'Isearchprotocolui:: getsearchitemforurl-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: f8a9bbe3459109946b7a4789d9b9f0fb7473ff05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750400"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a>Isearchprotocolui:: getsearchitemforurl-Methode

Ruft das Suchelement für die angegebenen Daten ab. Diese Methode wird einmal für jede URL aufgerufen, die vom Gatherer verarbeitet wird, und Ruft einen Zeiger auf das [**isearchitem**](-search-isearchitem.md) -Objekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcwszurl* \[ in\]
</dt> <dd>

Typ: **lpcolestr**

Zeiger auf eine Unicode-Zeichenfolge mit NULL-Daten, die das Suchelement für die URL enthält, auf die zugegriffen wird

</dd> <dt>

*ppropertybag* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **iitempropertybag \** _

Zeiger auf ein [_ *iitempropertybag* *](iitempropertybag.md) -Objekt, das Informationen über das Suchelement enthält, einschließlich der Eigenschaften des Elements.

</dd> <dt>

*ppsearchitem* \[ Out, retval\]
</dt> <dd>

Typ: **[ **isearchitem**](-search-isearchitem.md)\*\***

Empfängt die Adresse eines Zeigers auf das [**isearchitem**](-search-isearchitem.md) -Objekt, das mit dieser Methode erstellt wurde. Dieses Objekt enthält Informationen über das Suchelement, z. b. den Dateinamen des Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die **isearchprotocolui:: getsearchitemforurl** -Methode wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler von Drittanbietern auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, kann es erforderlich sein, die [**isearchprotocolui**](-search-isearchprotocolui.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**iitempreviewerext**](-search-iitempreviewerext.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Isearchprotocolui**](-search-isearchprotocolui.md)
</dt> </dl>

 

 




