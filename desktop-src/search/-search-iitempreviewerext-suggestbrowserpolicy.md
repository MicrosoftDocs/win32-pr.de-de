---
description: Schlägt die Sicherheitsrichtlinie vor, die auf den Browser angewendet werden soll.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: IItemPreviewerExt::SuggestBrowserPolicy-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 84446b49ab723f161de8f148e95916202efe06176191e820ab8bafc88ed9158a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969759"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>IItemPreviewerExt::SuggestBrowserPolicy-Methode

Schlägt die Sicherheitsrichtlinie vor, die auf den Browser angewendet werden soll.

## <a name="syntax"></a>Syntax


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwContext* \[ In\]
</dt> <dd>

Typ: **DWORD**

Der Kontextbezeichner für den Vorgang. Überschreiben Sie den *dwContext-Standardwert,* um den Kontextbezeichner auf einen Wert Ihrer Wahl festzulegen.

</dd> <dt>

*pdwFlags* \[ out, retval\]
</dt> <dd>

Typ: **DWORD \***

Ein Zeiger auf einen DWORD-Wert, der Überprüfungsüberprüfungsflags enthält. Das **FLAG BROWSERPOLICY \_ UNTRUSTED \_ CONTENT** deaktiviert jede Möglichkeit, dass die Vorschau skript- oder ActiveX ausführen kann. Der *Parameter pdwFlags* darf kein **NULL-Zeiger** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die [**IItemPreviewerExt-Schnittstelle**](-search-iitempreviewerext.md) wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**IItemPreviewerExt-Schnittstelle**](-search-iitempreviewerext.md) und die folgenden APIs zu verwenden: die Schnittstellen [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) und [**ISearchItem,**](-search-isearchitem.md) die [**LINKINFO-Struktur**](-search-linkinfo.md) und die [**LINKTYPE-Enumeration.**](-search-linktype.md)

Es wird dringend empfohlen, das FLAG **BROWSERPOLICY \_ UNTRUSTED \_ CONTENT** zu verwenden, um die Möglichkeit zu deaktivieren, dass die Vorschau skript- oder ActiveX ausführen kann. Die **IItemPreviewerExt::SuggestBrowserPolicy-Methode** kann Informationen darüber zurückgeben, ob das in der Vorschau befindliche Element vertrauenswürdig ist oder nicht. Dadurch kann das Trident-Steuerelement der Vorschauversion Skripts ausführen und sogar Steuerelemente ActiveX. Da die Vorschauversion häufig temporäre Dateien verwendet, um die Vorschau zu generieren, kann dies zu unerwarteten Skript- und Codeausführungsausführungen in der Zone Lokaler Computer führen.

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

 

 




