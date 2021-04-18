---
description: Ermöglicht der Erweiterung den umfangreichen Inhalt für eine Eigenschaft.
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: 'Iitempreviewerext:: getlinkedcontent-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345490"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a>Iitempreviewerext:: getlinkedcontent-Methode

Ermöglicht der Erweiterung den umfangreichen Inhalt für eine Eigenschaft.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwcontext* \[ in\]
</dt> <dd>

Typ: **DWORD**

Der Kontext Bezeichner für den Vorgang. Überschreiben Sie den *dwcontext* -Standard, um den Kontext Bezeichner auf einen Wert Ihrer Wahl festzulegen.

</dd> <dt>

*pwszprop* \[ in\]
</dt> <dd>

Typ: **lpcolestr**

Ein Zeiger auf die-Eigenschaft des verknüpften Inhalts als Unicode-Zeichenfolge.

</dd> <dt>

*pinfo* \[ Out, retval\]
</dt> <dd>

Typ: **[**linkinfo**](-search-linkinfo.md) \** _

Empfängt einen Zeiger auf die [_ *linkinfo* *](-search-linkinfo.md) -Struktur, in der die-Methode Informationen über die Transaktion zurückgibt. *pinfo* darf kein **null** -Zeiger sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iitempreviewerext**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




