---
description: Ruft ein Bytearray ab, das die anwendungsspezifischen und internen Eigenschaften Daten für diesen icontextnode enthält.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'Icontextnode:: savepropertiesdata-Methode (iacom. h)'
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
ms.openlocfilehash: f2ac064632eb9e5dd2b94f6e75b9b2836c75996d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958974"
---
# <a name="icontextnodesavepropertiesdata-method"></a>Icontextnode:: savepropertiesdata-Methode

Ruft ein Bytearray ab, das die anwendungsspezifischen und internen Eigenschaften Daten für diesen [**icontextnode**](icontextnode.md)enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulpropertiesdatasize* \[ in, out\]
</dt> <dd>

Die Größe des Daten Arrays, das die Eigenschaften Informationen enthält. Der Übergabe Wert wird nicht verwendet.

</dd> <dt>

*ppbpropertiesdata* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von 8-Bit-Ganzzahlen ohne Vorzeichen, das die anwendungsspezifischen und internen Eigenschaften Daten enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppbpropertiesdata* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Verwenden Sie diese Methode, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Diese Methode speichert die Eigenschafts Daten, die von **iinkanalyzer** auf dem [**icontextnode**](icontextnode.md)festgelegt wurden.

Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnode:: loadpropertiesdata**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**Icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**Icontextnode:: RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**Icontextnode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**Icontextnode:: ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

