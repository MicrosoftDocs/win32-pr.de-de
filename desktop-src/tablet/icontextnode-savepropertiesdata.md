---
description: Ruft ein Bytearray ab, das die anwendungsspezifischen und internen Eigenschaftsdaten für diesen IContextNode enthält.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: IContextNode::SavePropertiesData-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5b02f5df7526b429a65b2a0baf49bda4571dd718a9bff875c79b7e325de244ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719684"
---
# <a name="icontextnodesavepropertiesdata-method"></a>IContextNode::SavePropertiesData-Methode

Ruft ein Bytearray ab, das die anwendungsspezifischen und internen Eigenschaftsdaten für diesen [**IContextNode**](icontextnode.md)enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulPropertiesDataSize* \[ in, out\]
</dt> <dd>

Die Größe des Datenarrays, das die Eigenschafteninformationen enthält. Der übergebene Wert wird nicht verwendet.

</dd> <dt>

*ppbPropertiesData* \[ out\]
</dt> <dd>

Ein Zeiger auf ein 8-Bit-Ganzzahlarray ohne Vorzeichen, das die anwendungsspezifischen und internen Eigenschaftsdaten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, verwenden Sie [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher von \* *ppbPropertiesData* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Verwenden Sie diese Methode, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der des [**IInkAnalyzer**](iinkanalyzer.md)synchronisiert wird. Diese Methode speichert die Eigenschaftendaten, die **IInkAnalyzer** für [**IContextNode**](icontextnode.md)festgelegt hat.

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Freihandanalyse.](data-proxy-with-ink-analysis.md)

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

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

