---
description: Ruft die Informationen ab, die zum Lesen oder Speichern der Eigenschaften in der Eigenschaftentüte erforderlich sind. Die IItemPropertyBag-Schnittstelle wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: IItemPropertyBag::GetPropertyInfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7a69ceff2236a101f18ee06b4a87dd60e35ca69e73fdeb085232f102f8450d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863089"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>IItemPropertyBag::GetPropertyInfo-Methode

Ruft die Informationen ab, die zum Lesen oder Speichern der Eigenschaften in der Eigenschaftentüte erforderlich sind. Die [**IItemPropertyBag-Schnittstelle**](iitempropertybag.md) wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iProperty* \[ In\]
</dt> <dd>

Der nullbasierte Index der ersten Eigenschaft, für die Informationen angefordert werden.

</dd> <dt>

*cProperties* \[ In\]
</dt> <dd>

Die Anzahl der Eigenschaften, für die Informationen erhalten werden. Dieses Argument gibt die Anzahl der Arrayelemente in *pPropBag an.*

</dd> <dt>

*pPropBag* \[ out\]
</dt> <dd>

Zeiger auf ein Array von [**ITEMPROP-Strukturen,**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) das die Informationen für die Eigenschaften empfängt.

</dd> <dt>

*pcProperties* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf eine **ULONG-Variable,** die die Anzahl der Eigenschaften empfängt, für die Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die [**IItemPropertyBag-Schnittstelle**](iitempropertybag.md) wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Um eine Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern anzuzeigen, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**IItemPropertyBag-Schnittstelle**](iitempropertybag.md) und die folgenden APIs zu verwenden: die [**ISearchProtocolUI-,**](-search-isearchprotocolui.md) [**IItemPreviewerExt-**](-search-iitempreviewerext.md) und [**ISearchItem-Schnittstelle,**](-search-isearchitem.md) die [**LINKINFO-**](-search-linkinfo.md) und [**ITEMPROP-Strukturen**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) und die [**LINKTYPE-Enumeration.**](-search-linktype.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




