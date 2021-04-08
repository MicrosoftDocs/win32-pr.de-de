---
description: Ermöglicht die Verarbeitung eines Transformations Befehls, der in einer Vorschau Vorlage gefunden wurde.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: Iitempreviewerext::P rocesstransformcommand-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: 384294aac177679ea7445edb880198d250310625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862172"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>Iitempreviewerext::P rocesstransformcommand-Methode

Ermöglicht die Verarbeitung eines Transformations Befehls, der in einer Vorschau Vorlage gefunden wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwcontext* \[ in\]
</dt> <dd>

Typ: **DWORD**

Der Kontext Bezeichner für den Vorgang. Überschreiben Sie den *dwcontext* -Standard, um den Kontext Bezeichner auf einen Wert Ihrer Wahl festzulegen.

</dd> <dt>

*pwszName* \[ in\]
</dt> <dd>

Typ: **lpcolestr**

Ein Zeiger auf den Namen des Transformations Befehls als Unicode-Zeichenfolge.

</dd> <dt>

*pwszarg* \[ in\]
</dt> <dd>

Typ: **lpcolestr**

Ein Zeiger auf das Argument als Unicode-Zeichenfolge.

</dd> <dt>

*pVarResult* \[ Out, retval\]
</dt> <dd>

Typ: **Variant \** _

Ein Zeiger auf die Ergebnis Variante. _pvarResult * darf kein **null** -Zeiger sein.

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

 

 




