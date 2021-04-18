---
description: Die Methode "Write-grffile" schreibt ein Filter Diagramm in eine Datei im GRF-Format.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'IXml2Dex:: Beschreib tegrffile-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351331"
---
# <a name="ixml2dexwritegrffile-method"></a>IXml2Dex:: Beschreib tegrffile-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `WriteGrfFile` Methode schreibt ein Filter Diagramm in eine Datei im GRF-Format.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PGraph* 
</dt> <dd>

Zeiger auf die **IUnknown** -Schnittstelle des Filter Diagramms.

</dd> <dt>

*FileName* 
</dt> <dd>

Eine Zeichenfolge, die den Namen der zu schreibenden Datei angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück, der von der Implementierung der-Schnittstelle abhängig ist. HRESULT kann eine der folgenden Standard Konstanten oder andere nicht aufgelistete Werte enthalten.



| Rückgabecode                                                                                  | Beschreibung                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>       | Fehler.<br/>             |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Das Argument ist ungültig.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>             |



 

Diese Methode kann auch Fehlercodes zurückgeben, die von internen Aufrufen der Methoden **IStorage:: foratestream** und **ipersistent:: Save** generiert werden. Weitere Informationen finden Sie unter Platform SDK.

## <a name="remarks"></a>Bemerkungen

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

 

 




