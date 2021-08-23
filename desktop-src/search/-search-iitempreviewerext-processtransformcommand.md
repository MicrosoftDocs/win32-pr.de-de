---
description: Ermöglicht die Verarbeitung eines Transformationsbefehls, der in einer Vorschauvorlage gefunden wurde.
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: IItemPreviewerExt::P rocessTransformCommand-Methode
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
ms.openlocfilehash: f93d4be0bf9491c4fd2f6074c00692d6f634704ec820a34baeb4f1d52343c36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969775"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>IItemPreviewerExt::P rocessTransformCommand-Methode

Ermöglicht die Verarbeitung eines Transformationsbefehls, der in einer Vorschauvorlage gefunden wurde.

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

*dwContext* \[ In\]
</dt> <dd>

Typ: **DWORD**

Der Kontextbezeichner für den Vorgang. Überschreiben Sie den *dwContext-Standardwert,* um den Kontextbezeichner auf einen Wert Ihrer Wahl festzulegen.

</dd> <dt>

*pwszName* \[ In\]
</dt> <dd>

Typ: **LPCOLESTR**

Ein Zeiger auf den Namen des Transformationsbefehls als Unicode-Zeichenfolge.

</dd> <dt>

*pwszArg* \[ In\]
</dt> <dd>

Typ: **LPCOLESTR**

Ein Zeiger auf das Argument als Unicode-Zeichenfolge.

</dd> <dt>

*pvarResult* \[ out, retval\]
</dt> <dd>

Typ: **\* VARIANT**

Ein Zeiger auf die Ergebnisvariante. *pvarResult* darf kein **NULL-Zeiger** sein.

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

 

 




