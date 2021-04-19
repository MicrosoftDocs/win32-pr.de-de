---
description: Die Methode "Read xmlfile" lädt eine XML-Projektdatei.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: 'IXml2Dex:: infoxmlfile-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.ReadXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5b0fb5104e56afbcc4dd25e28981f0c382d7888e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370812"
---
# <a name="ixml2dexreadxmlfile-method"></a>IXml2Dex:: infoxmlfile-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `ReadXMLFile` Methode lädt eine XML-Projektdatei. Diese Methode erstellt Instanzen aller-Objekte, die in der XML-Datei ausgedrückt werden, fügt Sie in die Zeitachse ein und wendet alle für die Zeitachse angegebenen Attribute an, wie z. b. die Framerate oder die Standard Effekte.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptimeline* 
</dt> <dd>

Zeiger auf die **IUnknown** -Schnittstelle eines Timeline-Objekts.

</dd> <dt>

*XMLName* 
</dt> <dd>

Eine Zeichenfolge, die den Namen der zu ladenden Datei angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen HRESULT-Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                                  | Beschreibung                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg<br/>             |
| <dl> <dt>**VFW \_ E \_ ungültiges \_ Datei \_ Format.**</dt> </dl> | Ungültiges Dateiformat<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode löscht keine vorhandenen Objekte aus der Zeitachse, bevor die neuen Objekte eingefügt werden, die in der XML-Datei definiert sind. Wenn Sie eine vorhandene Zeitachse aktualisieren müssen, müssen Sie zuerst [**iamtimeline:: clearallgroups**](iamtimeline-clearallgroups.md) aufrufen.

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

 

 




