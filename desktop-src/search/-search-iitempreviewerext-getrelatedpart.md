---
description: Ruft einen verknüpften Textteil zum Einbetten in den MHTML-Ausgabestream ab.
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: IItemPreviewerExt::GetRelatedPart-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9abc4415eef014697376c9df4b89af47037a99df5c9ab5a3c74a3d7825b344c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863973"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a>IItemPreviewerExt::GetRelatedPart-Methode

Ruft einen verknüpften Textteil zum Einbetten in den MHTML-Ausgabestream ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwContext* \[ In\]
</dt> <dd>

Typ: **DWORD**

Der Kontextbezeichner für den Vorgang. Überschreiben Sie den **dwContext-Standardwert,** um den Kontextbezeichner auf einen Wert Ihrer Wahl festzulegen.

</dd> <dt>

*pwszProp* \[ In\]
</dt> <dd>

Typ: **LPCOLESTR**

Ein Zeiger auf die -Eigenschaft des verknüpften Inhalts als Unicode-Zeichenfolge.

</dd> <dt>

*dwIndex* \[ In\]
</dt> <dd>

Typ: **DWORD**

Ein ganzzahliger Wert ohne Vorzeichen, der den nullbasierten Index des verknüpften Textteils enthält.

</dd> <dt>

*pInfo* \[ out, retval\]
</dt> <dd>

Typ: **[ **LINKINFO**](-search-linkinfo.md)\***

Empfängt einen Zeiger auf die [**LINKINFO-Struktur,**](-search-linkinfo.md) in der die Methode Informationen über die Transaktion zurückgibt. *pInfo* darf kein **NULL-Zeiger** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die [**IItemPreviewerExt-Schnittstelle**](-search-iitempreviewerext.md) wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**IItemPreviewerExt-Schnittstelle**](-search-iitempreviewerext.md) und die folgenden APIs zu verwenden: die Schnittstellen [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) und [**ISearchItem,**](-search-isearchitem.md) die [**LINKINFO-Struktur**](-search-linkinfo.md) und die [**LINKTYPE-Enumeration.**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




