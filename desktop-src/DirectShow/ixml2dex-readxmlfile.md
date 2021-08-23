---
description: Die ReadXMLFile-Methode lädt eine XML-Projektdatei.
ms.assetid: 8269da74-fb33-42cf-ae8c-fe3d7db27aea
title: IXml2Dex::ReadXMLFile-Methode (Qedit.h)
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
ms.openlocfilehash: 37df0c93a17dadc2f6d6fbf94a662b89bf9630a0b0861f5bf5a0c676f7d369fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952439"
---
# <a name="ixml2dexreadxmlfile-method"></a>IXml2Dex::ReadXMLFile-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `ReadXMLFile` -Methode lädt eine XML-Projektdatei. Diese Methode erstellt Instanzen aller -Objekte, die in der XML-Datei ausgedrückt werden, und fügt sie in die Zeitachse ein. Außerdem werden alle für die Zeitachse angegebenen Attribute wie Framerate oder Standardeffekt verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadXMLFile(
   IUnknown *pTimeline,
   BSTR     XMLName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTimeline* 
</dt> <dd>

Zeiger auf die **IUnknown-Schnittstelle eines Zeitachsenobjekts.**

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
| <dl> <dt>**VFW \_ E \_ \_ UNGÜLTIGES \_ DATEIFORMAT**</dt> </dl> | Ungültiges Dateiformat<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode entfernt vorhandene Objekte nicht aus der Zeitachse, bevor sie die neuen Objekte einfügung, die in der XML-Datei definiert sind. Wenn Sie eine vorhandene Zeitachse aktualisieren müssen, rufen Sie [**zuerst IAMTimeline::ClearAllGroups**](iamtimeline-clearallgroups.md) auf.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Internet Explorer 4.0 oder höher<br/>                                               |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IXml2Dex-Schnittstelle**](ixml2dex.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




