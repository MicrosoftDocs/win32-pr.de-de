---
description: Die querysupported-Methode bestimmt, ob ein Objekt einen angegebenen Eigenschaften Satz unterstützt.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'Ikspropertyset:: querysupported-Methode (". h")'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213903"
---
# <a name="ikspropertysetquerysupported-method"></a>Ikspropertyset:: querysupported-Methode

Die- `QuerySupported` Methode bestimmt, ob ein Objekt einen angegebenen Eigenschaften Satz unterstützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*guidpropset* \[ in\]
</dt> <dd>

Eigenschaften Satz-GUID.

</dd> <dt>

*dwpropid* \[ in\]
</dt> <dd>

Der Bezeichner der Eigenschaft innerhalb des Eigenschaften Satzes.

</dd> <dt>

*ptypesupport* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Wert, in dem Flags gespeichert werden, die die vom Treiber bereitgestellte Unterstützung angeben. Folgende Flags werden unterstützt:



| Wert                    | BESCHREIBUNG                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| ksproperty- \_ Unterstützung abrufen \_ | Sie können die-Eigenschaft abrufen, indem Sie die " [**ikspropertyset:: Get**](ikspropertyset-get.md) "-Methode aufrufen. |
| ksproperty- \_ Unterstützungs \_ Satz | Sie können die Eigenschaft ändern, indem Sie " [**ikspropertyset:: Set**](ikspropertyset-set.md)" aufrufen.              |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                              | Beschreibung                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Die angegebene Kombination aus Eigenschaften Satz und Eigenschaften-ID wird unterstützt.<br/> |
| <dl> <dt>**E \_ notimpl**</dt> </dl>                | Der Eigenschaften Satz wird nicht unterstützt.<br/>                                       |
| <dl> <dt>**E- \_ Prop- \_ ID \_ nicht unterstützt**</dt> </dl>  | Die eigen schafts-ID wird für den angegebenen Eigenschaften Satz nicht unterstützt.<br/>         |
| <dl> <dt>**E- \_ Prop- \_ Satz \_ nicht unterstützt**</dt> </dl> | Der Eigenschaften Satz wird nicht unterstützt.<br/>                                       |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Eine weitere Schnittstelle mit diesem Namen ist in der Header Datei "DSound. h" vorhanden. Die beiden Schnittstellen sind nicht kompatibel. Die im DirectShow-DDK dokumentierte " **ikscontrol** "-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten.

 

Sie müssen "KS. h" vor "ksproxy. h" einschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                             |
| Header<br/>                   | <dl> <dt>. H. </dt> <dt>Ksproxy. h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>"" "" ". Lib"</dt> </dl>                                                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[**"Ikspropertyset"-Schnittstelle**](ikspropertyset.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




