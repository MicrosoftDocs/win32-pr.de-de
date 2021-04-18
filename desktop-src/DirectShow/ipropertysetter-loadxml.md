---
description: Die LoadXml-Methode lädt Eigenschafts Daten, die in Extensible Markup Language (XML) ausgedrückt werden.
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'Ipropertysetter:: LoadXml-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368318"
---
# <a name="ipropertysetterloadxml-method"></a>Ipropertysetter:: LoadXml-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `LoadXML` Methode lädt Eigenschafts Daten, die in Extensible Markup Language (XML) ausgedrückt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pxml* \[ in\]
</dt> <dd>

Ein Zeiger auf die **IUnknown** -Schnittstelle eines vom Microsoft XML-Parser erstellten XML-Elements.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                                  | Beschreibung                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                      | Keine Eigenschafts Daten.<br/>    |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>             |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>                | Nicht genügend Arbeitsspeicher.<br/> |
| <dl> <dt>**VFW \_ E \_ ungültiges \_ Datei \_ Format.**</dt> </dl> | Ungültiges Format.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

In der Regel müssen Anwendungen diese Methode nicht verwenden. Von des wird es intern verwendet, um Eigenschaften aus XTL-Dateien zu laden.

Um diese Methode zu verwenden, erstellen Sie ein **IXMLDocument** -Objekt, und verwenden Sie es zum Analysieren einer XML-Datei. Verwenden Sie dann das **IXMLDocument** -Objekt, um **IXmlElement** -Objekte abzurufen. Wenn das Objekt über Eigenschaften verfügt, können Sie den **IXmlElement** -Zeiger an die **LoadXml** -Methode übergeben. Die-Methode lädt die Eigenschaften in den Eigenschaften Setter.

> [!Note]  
> Die **IXMLDocument** -Schnittstelle und die **IXmlElement** -Schnittstelle sind in Microsoft XML Core Services (MSXML) Version 1,0 implementiert, aber in neueren Versionen von MSXML nicht implementiert.

 

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

 

 




