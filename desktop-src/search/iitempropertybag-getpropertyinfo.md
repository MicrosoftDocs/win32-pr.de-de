---
description: Ruft die Informationen ab, die erforderlich sind, um die Eigenschaften in der Eigenschaften Sammlung zu lesen oder zu speichern. Die iitempropertybag-Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: 'Iitempropertybag:: GetPropertyInfo-Methode'
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
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346496"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>Iitempropertybag:: GetPropertyInfo-Methode

Ruft die Informationen ab, die erforderlich sind, um die Eigenschaften in der Eigenschaften Sammlung zu lesen oder zu speichern. Die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

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

*IProperty* \[ in\]
</dt> <dd>

Der null basierte Index der ersten Eigenschaft, für die Informationen angefordert werden.

</dd> <dt>

*cproperties* \[ in\]
</dt> <dd>

Die Anzahl der Eigenschaften, für die Informationen zu erhalten sind. Dieses Argument gibt die Anzahl der Array Elemente in *ppropbag* an.

</dd> <dt>

*ppropbag* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von [**ItemProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) -Strukturen, das die Informationen für die Eigenschaften empfängt.

</dd> <dt>

*pcProperties* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf eine **ulong** -Variable, die die Anzahl der Eigenschaften empfängt, für die Informationen abgerufen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, gibt Sie S \_ OK zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

Zum Anzeigen einer Vorschau von Anlagen mit einem Protokollhandler eines Drittanbieters auf Computern, auf denen Windows XP oder Windows Server 2003 ausgeführt wird, ist es möglicherweise erforderlich, die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle und die folgenden APIs zu verwenden: die Schnittstellen [**isearchprotocolui**](-search-isearchprotocolui.md), [**iitempreviewerext**](-search-iitempreviewerext.md) und [**isearchitem**](-search-isearchitem.md) [**, die-und**](-search-linkinfo.md) [**linktype**](-search-linktype.md) [**-**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) Enumeration.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/> |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iitempropertybag**](iitempropertybag.md)
</dt> </dl>

 

 




