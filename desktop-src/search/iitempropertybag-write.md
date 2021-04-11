---
description: Bewirkt, dass eine oder mehrere Eigenschaften im Eigenschaften Behälter gespeichert werden. Die iitempropertybag-Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.
ms.assetid: 35491fbc-fb1c-4bad-86e8-9f19856ed7cb
title: 'Iitempropertybag:: Write-Methode'
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
ms.openlocfilehash: 7df66487bba0c2bbef40cf3642754dff56f65835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128508"
---
# <a name="iitempropertybagwrite-method"></a>Iitempropertybag:: Write-Methode

Bewirkt, dass eine oder mehrere Eigenschaften im Eigenschaften Behälter gespeichert werden. Die [**iitempropertybag**](iitempropertybag.md) -Schnittstelle wird nur unter Windows XP und Windows Server 2003 unterstützt und sollte nicht mehr verwendet werden.

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

*cproperties* \[ in\]
</dt> <dd>

Die Anzahl der zu speichernden Eigenschaften. Dieses Argument gibt die Anzahl der Elemente in den Arrays bei *ppropbag* und *pvarvalue* an.

</dd> <dt>

*ppropbag* \[ in\]
</dt> <dd>

Ein Zeiger auf ein Array von [**ItemProp**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) -Strukturen, das die zu speichernden Eigenschaften angibt.

</dd> <dt>

*pvarvalue* \[ in\]
</dt> <dd>

Ein Zeiger auf eine **Variante** , deren Typ vom Datentyp der darin enthaltenen Eigenschafts Informationen abhängt.

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

 

 




