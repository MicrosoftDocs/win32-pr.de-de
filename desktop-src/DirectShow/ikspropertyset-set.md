---
description: Die Set-Methode legt eine Eigenschaft fest, die durch eine Eigenschaften Satz-GUID und eine Eigenschaften-ID identifiziert wird.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'Ikspropertyset:: Set-Methode (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392605"
---
# <a name="ikspropertysetset-method"></a>Ikspropertyset:: Set-Methode

Die `Set` -Methode legt eine Eigenschaft fest, die durch eine Eigenschaften Satz-GUID und eine Eigenschaften-ID identifiziert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
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

*pinstancedata* \[ in\]
</dt> <dd>

Zeiger auf einen Puffer, der Instanzdaten für die Eigenschaft enthält.

</dd> <dt>

*cbinstancedata* \[ in\]
</dt> <dd>

Größe des *pinstancedata* -Puffers in Bytes.

</dd> <dt>

*ppropdata* \[ in\]
</dt> <dd>

Zeiger auf einen Puffer, der den Wert der Eigenschaft enthält.

</dd> <dt>

*cbpropdata* \[ in\]
</dt> <dd>

SISE des *ppropdata* -Puffers in Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                              | Beschreibung                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Erfolg.<br/>                                                         |
| <dl> <dt>**E- \_ Prop- \_ Satz \_ nicht unterstützt**</dt> </dl> | Der Eigenschaften Satz wird nicht unterstützt.<br/>                               |
| <dl> <dt>**E- \_ Prop- \_ ID \_ nicht unterstützt**</dt> </dl>  | Die eigen schafts-ID wird für den angegebenen Eigenschaften Satz nicht unterstützt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Eine weitere Schnittstelle mit diesem Namen ist in der Header Datei "DSound. h" vorhanden. Die beiden Schnittstellen sind nicht kompatibel. Die im DirectShow-DDK dokumentierte " **ikscontrol** "-Schnittstelle ist nun die empfohlene Schnittstelle zum Übergeben von Eigenschafts Sätzen zwischen WDM-Treibern und Benutzermoduskomponenten.

 

Sie müssen "KS. h" vor "ksproxy. h" einschließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothek<br/>                  | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> <dt>

[**"Ikspropertyset"-Schnittstelle**](ikspropertyset.md)
</dt> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




