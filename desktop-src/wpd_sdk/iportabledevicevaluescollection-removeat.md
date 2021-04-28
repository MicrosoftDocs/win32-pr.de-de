---
description: 'IPortableDeviceValuesCollection::RemoveAt-Methode: Die RemoveAt-Methode entfernt das Element, das an dem vom angegebenen Index angegebenen Speicherort gespeichert ist.'
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: IPortableDeviceValuesCollection::RemoveAt-Methode (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7db15480906bee8181bb0fc589c4f3e30ce4753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083168"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a>IPortableDeviceValuesCollection::RemoveAt-Methode

Die **RemoveAt-Methode** entfernt das Element, das an der vom angegebenen Index angegebenen Position gespeichert ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwIndex* \[ In\]
</dt> <dd>

Gibt den Index des zu entfernenden Elements an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt ein **HRESULT zurück.** Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                  | Beschreibung                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Methode wurde erfolgreich ausgeführt.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Der angegebene Index lag nicht im Bereich.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie müssen einen nullbasierten Index angeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPortableDeviceValuesCollection-Schnittstelle**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




