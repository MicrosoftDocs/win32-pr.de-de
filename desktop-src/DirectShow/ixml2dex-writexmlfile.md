---
description: Die Methode "Write texmlfile" übersetzt eine Zeitachse in XML und schreibt die XML-Daten in eine Datei.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'IXml2Dex:: Write texmlfile-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358752"
---
# <a name="ixml2dexwritexmlfile-method"></a>IXml2Dex:: Write texmlfile-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `WriteXMLFile` -Methode übersetzt eine Zeitachse in XML und schreibt die XML-Daten in eine Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptimeline* 
</dt> <dd>

Zeiger auf die **IUnknown** -Schnittstelle des Timeline-Objekts.

</dd> <dt>

*FileName* 
</dt> <dd>

Eine Zeichenfolge, die den Namen der zu schreibenden Datei angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück, der von der Implementierung der-Schnittstelle abhängig ist. Das **HRESULT** kann eine der folgenden Standard Konstanten oder andere nicht aufgelistete Werte enthalten.



| Rückgabecode                                                                                   | Beschreibung                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Das Argument ist ungültig.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode generiert eine XML-Datei, die alle Komponenten in der Zeitachse darstellt.

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

 

 




