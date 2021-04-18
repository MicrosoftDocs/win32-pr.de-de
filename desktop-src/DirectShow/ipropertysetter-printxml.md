---
description: Die printxml-Methode konvertiert Eigenschafts Daten in eine XML-Zeichenfolge.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: Ipropertysetter::P rintxml-Methode (qedit. h)
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
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361559"
---
# <a name="ipropertysetterprintxml-method"></a>Ipropertysetter::P rintxml-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `PrintXML` Methode konvertiert Eigenschafts Daten in eine XML-Zeichenfolge.

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

*pszxml* \[ vorgenommen\]
</dt> <dd>

Zeiger auf einen Puffer, der die XML-Zeichenfolge empfängt.

</dd> <dt>

*cbxml* \[ in\]
</dt> <dd>

Größe des Puffers, auf den *pszxml* zeigt (in Bytes).

</dd> <dt>

*pcbprint* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Länge der XML-Zeichenfolge empfängt. Kann **null** sein.

</dd> <dt>

*Einzug* \[ in\]
</dt> <dd>

Anzahl der Einzugs Ebenen für das äußerste Tag.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück. Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt. Wenn die XML-Zeichenfolge länger als der Puffer ist, gibt die Methode E \_ outo-Memory zurück.

## <a name="remarks"></a>Bemerkungen

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

 

 




