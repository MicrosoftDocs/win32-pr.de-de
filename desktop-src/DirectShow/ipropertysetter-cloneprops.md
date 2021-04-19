---
description: Die cloneproperties-Methode klont eine Reihe von Eigenschaften aus diesem Eigenschaften Setter und fügt Sie einem neuen Eigenschaften Setter hinzu.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: 'Ipropertysetter:: cloneproperemethode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.CloneProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9954b98085ba2de9eac6bc62bf784732448f613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352876"
---
# <a name="ipropertysettercloneprops-method"></a>Ipropertysetter:: clonerequismethode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

`CloneProps`Mit der-Methode wird ein Satz von Eigenschaften aus diesem Eigenschaften Setter geklont und einem neuen Eigenschaften Setter hinzugefügt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CloneProps(
  [out] IPropertySetter **ppSetter,
  [in]  REFERENCE_TIME  rtStart,
  [in]  REFERENCE_TIME  rtStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppsetter* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die **ipropertysetter** -Schnittstelle des neuen Eigenschaften Setters.

</dd> <dt>

*rtstart* \[ in\]
</dt> <dd>

Die Startzeit des zu klonenden Wertebereichs in 100-Nanosecond-Einheiten.

</dd> <dt>

*rtstopps* \[ in\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Nur die Werte, die nach der angegebenen Startzeit liegen, werden geklont. Die Uhrzeiten für die geklonten Werte werden dann in Relation zur Startzeit angepasst. Wenn *rtstart* beispielsweise 20 Millionen (2 Sekunden) ist, wird ein Wert zur Zeit 30 Millionen (3 Sekunden) mit der Zeit 10 Millionen (1 Sekunde) geklont. Zum Schluss erhält jede geklonte Eigenschaft einen Anfangswert, der dem Wert der ursprünglichen Eigenschaft zur Startzeit entspricht (bei Bedarf korrekt interpoliert). Tatsächlich werden die Eigenschaften Daten zur angegebenen Startzeit aufgeteilt.

Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene [**ipropertysetter**](ipropertysetter.md) -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ipropertysetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




