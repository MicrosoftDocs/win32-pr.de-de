---
description: Schlägt die Sicherheitsrichtlinie vor, die auf den Browser angewendet werden soll.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'Iitempreviewerext:: Vorschlags-browserpolicy-Methode'
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
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484427"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>Iitempreviewerext:: Vorschlags-browserpolicy-Methode

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

*dwcontext* \[ in\]
</dt> <dd>

Typ: **DWORD**

Der Kontext Bezeichner für den Vorgang. Überschreiben Sie den *dwcontext* -Standard, um den Kontext Bezeichner auf einen Wert Ihrer Wahl festzulegen.

</dd> <dt>

*pdwflags* \[ Out, retval\]
</dt> <dd>

Typ: **DWORD \** _

Ein Zeiger auf einen DWORD-Wert, der Überprüfungs Prüfungs Flags enthält. Das Flag _ *browserpolicy \_ nicht vertrauenswürdiges \_ Content** deaktiviert jede Möglichkeit, dass die Vorschau das Skript oder ActiveX ausführen kann. Der *pdwflags* -Parameter darf kein **null** -Zeiger sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempreviewerext**](-search-iitempreviewerext.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempropertybag**](iitempropertybag.md) und [**isearchitem**](-search-isearchitem.md) , die [**linkinfo**](-search-linkinfo.md) -Struktur und die [**linktype**](-search-linktype.md)

Die Verwendung des Flags " **browserpolicy \_ nicht vertrauenswürdiger \_ Inhalt** " wird dringend empfohlen, um die Möglichkeit zu deaktivieren, dass die Vorschau Skripts oder ActiveX ausführen kann. Die **iitempreviewerext:: Vorschlags-browserpolicy** -Methode kann Informationen darüber zurückgeben, ob das Element, das in der Vorschau angezeigt wird, vertrauenswürdig ist oder nicht. Dies ermöglicht es dem Vorschau-Steuerelement, das Skript und sogar ActiveX-Steuerelemente auszuführen. Da der Vorschau häufig temporäre Dateien verwendet, um die Vorschau zu generieren, kann dies dazu führen, dass in der lokalen Computer Zone unerwartete Skript-und Code Ausführungen ausgeführt werden.

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

 

 




