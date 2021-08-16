---
description: Bewirkt, dass eine oder mehrere Eigenschaften aus dem Eigenschaftenbehälter gelesen werden. Die IItemPropertyBag-Schnittstelle wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: IItemPropertyBag::Read-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: c04cf34720871b1254f16822a090f48f8d68aaeb82398744d5139486fb6dd2f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226605"
---
# <a name="iitempropertybagread-method"></a>IItemPropertyBag::Read-Methode

Bewirkt, dass eine oder mehrere Eigenschaften aus dem Eigenschaftenbehälter gelesen werden. Die [**IItemPropertyBag-Schnittstelle**](iitempropertybag.md) wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cProperties* \[ In\]
</dt> <dd>

Die Anzahl der zu lesende Eigenschaften. Dieses Argument gibt die Anzahl der Elemente in den Arrays bei *pPropBag,* *pvarValue* und *phrError* an.

</dd> <dt>

*pPropBag* \[ In\]
</dt> <dd>

Zeiger auf ein Array von [**ITEMPROP-Strukturen,**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) das die angeforderten Eigenschaften angibt.

</dd> <dt>

*pvarValue* \[ out\]
</dt> <dd>

Empfängt einen Zeiger, der ein Array von **VARIANT-Strukturen** zurückgibt, die die Eigenschaftswerte empfangen.

</dd> <dt>

*phrError* \[ out\]
</dt> <dd>

Zeiger auf ein Array von **HRESULT-Werten,** das das Ergebnis der einzelnen gelesenen Eigenschaften empfängt. Dieses Array muss mindestens *cProperties-Elemente* enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, wird S \_ OK zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die [**IItemPropertyBag-Schnittstelle**](iitempropertybag.md) wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**IItemPropertyBag-Schnittstelle**](iitempropertybag.md) und die folgenden APIs zu verwenden: die [**ISearchProtocolUI-,**](-search-isearchprotocolui.md) [**IItemPreviewerExt-**](-search-iitempreviewerext.md) und [**ISearchItem-Schnittstellen,**](-search-isearchitem.md) die [**LINKINFO-**](-search-linkinfo.md) und [**ITEMPROP-Strukturen**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) und die [**LINKTYPE-Enumeration.**](-search-linktype.md)

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

 

 




