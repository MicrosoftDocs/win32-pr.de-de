---
description: Ruft das Suchelement für die angegebenen Daten ab. Diese Methode wird einmal für jede URL aufgerufen, die vom Gatherer verarbeitet wird, und ruft einen Zeiger auf das ISearchItem-Objekt ab.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: ISearchProtocolUI::GetSearchItemForUrl-Methode
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
ms.openlocfilehash: 8636f42026fe44131e149b0e378089b70c7d4f49b9e23b5d48ebe50aa5721d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594810"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a>ISearchProtocolUI::GetSearchItemForUrl-Methode

Ruft das Suchelement für die angegebenen Daten ab. Diese Methode wird einmal für jede URL aufgerufen, die vom Gatherer verarbeitet wird, und ruft einen Zeiger auf das [**ISearchItem-Objekt**](-search-isearchitem.md) ab.

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

*pcwszURL* \[ In\]
</dt> <dd>

Typ: **LPCOLESTR**

Zeiger auf eine auf NULL-Daten beendete Unicode-Zeichenfolge, die das Suchelement für die URL enthält, auf die zugegriffen wird.

</dd> <dt>

*pPropertyBag* \[ In\]
</dt> <dd>

Typ: **IItemPropertyBag \***

Zeiger auf ein [**IItemPropertyBag-Objekt,**](iitempropertybag.md) das Informationen über das Suchelement enthält, einschließlich der Eigenschaften des Elements.

</dd> <dt>

*ppSearchItem* \[ out, retval\]
</dt> <dd>

Typ: **[ **ISearchItem**](-search-isearchitem.md)\*\***

Empfängt die Adresse eines Zeigers auf das von dieser Methode erstellte [**ISearchItem-Objekt.**](-search-isearchitem.md) Dieses Objekt enthält Informationen zum Suchelement, z. B. den Dateinamen des Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die **ISearchProtocolUI::GetSearchItemForUrl-Methode** wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Um eine Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern anzuzeigen, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**ISearchProtocolUI-Schnittstelle**](-search-isearchprotocolui.md) und die folgenden APIs zu verwenden: die [**Schnittstellen IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md) und [**ISearchItem,**](-search-isearchitem.md) die [**LINKINFO-Struktur**](-search-linkinfo.md) und die [**LINKTYPE-Enumeration.**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISearchProtocolUI**](-search-isearchprotocolui.md)
</dt> </dl>

 

 




