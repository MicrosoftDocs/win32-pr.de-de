---
description: Bewirkt, dass eine oder mehrere Eigenschaften in der Eigenschaftentüte gespeichert werden. Die IItemPropertyBag-Schnittstelle wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: IItemPropertyBag::Write-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Write
api_type:
- COM
api_location: ''
ms.openlocfilehash: e8860653244cef53739c7d104405a176c1ec63d2de1d3434b1d25e3206c431aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863109"
---
# <a name="iitempropertybagwrite-method"></a>IItemPropertyBag::Write-Methode

Bewirkt, dass eine oder mehrere Eigenschaften in der Eigenschaftentüte gespeichert werden. Die [**IItemPropertyBag-Schnittstelle**](iitempropertybag.md) wird nur auf Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Write(
  [in] ULONG    cProperties,
  [in] ITEMPROP *pPropBag,
  [in] VARIANT  *pvarValue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cProperties* \[ In\]
</dt> <dd>

Die Anzahl der zu speichernden Eigenschaften. Dieses Argument gibt die Anzahl der Elemente in den Arrays unter *pPropBag* und *pvarValue an.*

</dd> <dt>

*pPropBag* \[ In\]
</dt> <dd>

Zeiger auf ein Array von [**ITEMPROP-Strukturen,**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) das die zu speichernden Eigenschaften angibt.

</dd> <dt>

*pvarValue* \[ In\]
</dt> <dd>

Zeiger auf eine **VARIANT-Datei,** deren Typ vom Datentyp der enthaltenen Eigenschaftsinformationen abhängt.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




