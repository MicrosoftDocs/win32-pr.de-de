---
description: Die CloneProps-Methode klont einen Satz von Eigenschaften aus diesem Eigenschaftens setter und fügt sie einem neuen Eigenschaftens setter hinzu.
ms.assetid: dee93e41-2925-4b4b-b5b2-7cfd6ea10e05
title: IPropertySetter::CloneProps-Methode (Qedit.h)
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
ms.openlocfilehash: 54dd2ad08334a0c61918de74396e62fcc21e095df81c2d773995b6cfbdddc19d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755920"
---
# <a name="ipropertysettercloneprops-method"></a>IPropertySetter::CloneProps-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]

 

Die `CloneProps` -Methode klont einen Satz von Eigenschaften aus diesem Eigenschaftens setter und fügt sie einem neuen Eigenschaftens setter hinzu.

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

*ppSetter* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die **IPropertySetter-Schnittstelle** des neuen Eigenschaftensetters.

</dd> <dt>

*rtStart* \[ In\]
</dt> <dd>

Startzeit des Zu klonenden Wertebereichs in Einheiten von 100 Nanosekunden.

</dd> <dt>

*rtStop* \[ In\]
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Nur Werte, die nach der angegebenen Startzeit liegen, werden geklont. Die Zeiten für die geklonten Werte werden dann relativ zur Startzeit angepasst. Wenn *rtStart* beispielsweise 20000000 (2 Sekunden) ist, wird ein Wert zum Zeitpunkt 30000000 (3 Sekunden) mit der Zeit 100000000 (1 Sekunde) geklont. Schließlich erhält jede geklonte Eigenschaft einen Anfangswert, der dem Wert der ursprünglichen Eigenschaft zur Startzeit entspricht (bei Bedarf korrekt interpoliert). Tatsächlich werden die Eigenschaftsdaten zur angegebenen Startzeit aufgeteilt.

Wenn die Methode erfolgreich ist, verfügt die [**zurückgegebene IPropertySetter-Schnittstelle**](ipropertysetter.md) über eine ausstehende Verweisanzahl. Stellen Sie sicher, dass Sie die -Schnittstelle wieder frei geben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IPropertySetter-Schnittstelle**](ipropertysetter.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




