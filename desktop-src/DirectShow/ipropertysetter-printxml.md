---
description: Die PrintXML-Methode konvertiert Eigenschaftsdaten in eine XML-Zeichenfolge.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: IPropertySetter::P rintXML-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5070a6906d7f30ab12171f551270f82b9851fa8c3990fade47aca6d2927509be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051510"
---
# <a name="ipropertysetterprintxml-method"></a>IPropertySetter::P rintXML-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `PrintXML` -Methode konvertiert Eigenschaftsdaten in eine XML-Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszXML* \[ out\]
</dt> <dd>

Zeiger auf einen Puffer, der die XML-Zeichenfolge empfängt.

</dd> <dt>

*cbXML* \[ In\]
</dt> <dd>

Größe des Puffers, auf den *pszXML zeigt,* in Bytes.

</dd> <dt>

*zeichenPrinted* \[ out\]
</dt> <dd>

Zeiger auf eine Variable, die die Länge der XML-Zeichenfolge empfängt. Kann NULL **sein.**

</dd> <dt>

*Einzug* \[ In\]
</dt> <dd>

Anzahl der Einzugsebenen für das äußerste Tag.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich. Andernfalls gibt einen **HRESULT-Wert** zurück, der die Ursache des Fehlers angibt. Wenn die XML-Zeichenfolge länger als der Puffer ist, gibt die Methode E \_ OUTOFMEMORY zurück.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




