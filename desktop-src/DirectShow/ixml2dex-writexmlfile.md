---
description: Die WriteXMLFile-Methode übersetzt eine Zeitachse in XML und schreibt die XML-Daten in eine Datei.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: IXml2Dex::WriteXMLFile-Methode (Qedit.h)
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
ms.openlocfilehash: 81cb33222988b99b9484226e72110afc3eca1923441479adc8d600e2b80f273c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767010"
---
# <a name="ixml2dexwritexmlfile-method"></a>IXml2Dex::WriteXMLFile-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

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

*pTimeline* 
</dt> <dd>

Zeiger auf die **IUnknown-Schnittstelle des Zeitachsenobjekts.**

</dd> <dt>

*FileName* 
</dt> <dd>

Eine Zeichenfolge, die den Namen der zu schreibenden Datei angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung der -Schnittstelle abhängt. Das **HRESULT** kann eine der folgenden Standardkonst konstanten oder andere Werte enthalten, die nicht aufgeführt sind.



| Rückgabecode                                                                                   | Beschreibung                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Das Argument ist ungültig.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>             |



 

## <a name="remarks"></a>Hinweise

Diese Methode generiert eine XML-Datei, die alle Komponenten auf der Zeitachse darstellt.

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

 

 




