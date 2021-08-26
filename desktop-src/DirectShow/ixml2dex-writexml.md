---
description: Die WriteXML-Methode übersetzt eine Zeitachse in eine XML-Zeichenfolge.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: IXml2Dex::WriteXML-Methode (Qedit.h)
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
ms.openlocfilehash: a5285faad36f83dbab693c63a0c96ca2b1d2b6a25220bb601a9527aac9dc5ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051290"
---
# <a name="ixml2dexwritexml-method"></a>IXml2Dex::WriteXML-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `WriteXML` -Methode übersetzt eine Zeitachse in eine XML-Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTimeline* 
</dt> <dd>

Zeiger auf die **IUnknown-Schnittstelle des Zeitachsenobjekts.**

</dd> <dt>

*pbstrXML* 
</dt> <dd>

Zeiger auf eine Variable vom Typ BSTR, die die XML-Zeichenfolge empfängt, die die Zeitachse beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich. Wenn nicht genügend Arbeitsspeicher für die Konvertierung verfügbar ist, gibt E \_ OUTOFMEMORY zurück. Andernfalls wird ein weiterer Fehlercode zurückgegeben.

## <a name="remarks"></a>Hinweise

Die -Methode ordnet Arbeitsspeicher für die Zeichenfolge zu. Die Anwendung muss **SysFreeString aufrufen,** um den Arbeitsspeicher frei zu machen.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Internet Explorer 4.0 oder höher<br/>                                               |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IXml2Dex-Schnittstelle**](ixml2dex.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




