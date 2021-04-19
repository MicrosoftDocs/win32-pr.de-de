---
description: Die Methode "Write texml" übersetzt eine Zeitachse in eine XML-Zeichenfolge.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'IXml2Dex:: Write texml-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372251"
---
# <a name="ixml2dexwritexml-method"></a>IXml2Dex:: Write texml-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `WriteXML` Methode übersetzt eine Zeitachse in eine XML-Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptimeline* 
</dt> <dd>

Zeiger auf die **IUnknown** -Schnittstelle des Timeline-Objekts.

</dd> <dt>

*pbstrauxml* 
</dt> <dd>

Zeiger auf eine Variable vom Typ BSTR, die die XML-Zeichenfolge empfängt, die die Zeitachse beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK zurück. Wenn nicht genügend Arbeitsspeicher für die Konvertierung vorhanden ist, wird E \_ outoiden Speicher zurückgegeben. Andernfalls wird ein anderer Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die-Methode ordnet Speicher für die Zeichenfolge zu. Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Internet Explorer 4,0 oder höher<br/>                                               |
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IXml2Dex-Schnittstelle**](ixml2dex.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




