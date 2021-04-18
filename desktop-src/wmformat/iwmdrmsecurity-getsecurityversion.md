---
title: Iwmdrmsecurity getsecurityversion-Methode (wmdrmsdk. h)
description: Die getsecurityversion-Methode ruft die Version des DRM-Subsystems auf dem Client Computer ab.
ms.assetid: ec97dec8-61ba-4424-b5eb-2e6885cc1f48
keywords:
- Getsecurityversion-Methode Windows Media-Format
- Getsecurityversion-Methode Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getsecurityversion-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetSecurityVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33be994383a7e16d136aac340a77deef8256d62f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368489"
---
# <a name="iwmdrmsecuritygetsecurityversion-method"></a>Iwmdrmsecurity:: getsecurityversion-Methode

Die **getsecurityversion** -Methode ruft die Version des DRM-Subsystems auf dem Client Computer ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSecurityVersion(
  [out] BSTR *pbstrVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrauversion* \[ vorgenommen\]
</dt> <dd>

Adresse einer Variablen, die die Versionsnummer des DRM-Subsystems empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Versionsnummer wird als Zeichenfolge ausgedrückt, die aus vier Zahlen besteht, die durch Punkte getrennt sind. Die erste Zahl ist die Hauptversionsnummer, die normalerweise auf 2 festgelegt ist. Die zweite Zahl ist die neben Versionsnummer von 2 bis 10. Die dritte Zahl wird immer auf 0 festgelegt. Die vierte Zahl ist auf 0 oder 1 festgelegt, und ist ein boolescher Wert, der angibt, ob das Subsystem individualisiert wurde. Die Versionsnummer "2.4.0.1" gibt z. b. die individualisierte vierte neben Version der zweiten Hauptversion an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmdrmsecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





