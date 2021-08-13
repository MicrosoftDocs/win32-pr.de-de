---
description: Fügt anwendungsspezifische Daten hinzu.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: IContextNode::AddPropertyData-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8c9988217aed21ff1142f0e2083bee568ed12c31d90530ac1f3e9f5719c46446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719694"
---
# <a name="icontextnodeaddpropertydata-method"></a>IContextNode::AddPropertyData-Methode

Fügt anwendungsspezifische Daten hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pPropertyDataId* \[ In\]
</dt> <dd>

Ein GUID (Globally Unique Identifier), der zum Identifizieren des Datentyps verwendet wird.

</dd> <dt>

*ulPropertyDataSize* \[ In\]
</dt> <dd>

Die Größe der Daten in Bytes.

</dd> <dt>

*pbPropertiesData* \[ In\]
</dt> <dd>

\[in, size \_ is(ulPropertyDataSize)\]

Ein 8-Bit-Ganzzahlarray ohne Vorzeichen, das die hinzuzufügenden Eigenschaftsinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Verwenden **Sie IContextNode::AddPropertyData,** um Einem Kontextknoten Daten zu zuordnen. Verwenden Sie [**IContextNode::GetPropertyData,**](icontextnode-getpropertydata.md)um die Daten später abzurufen.

Die Ink-Analyse kann den Knoten im Rahmen der Ink-Analyse löschen, es sei denn, der Kontextknoten wird bestätigt (siehe [**IContextNode::Confirm**](icontextnode-confirm.md)). Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Ink-Analyse.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




