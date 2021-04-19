---
description: Die setrecompformatfromsource-Methode legt das Format der Video Neukomprimierung mithilfe des Komprimierungs Formats aus einer Quelldatei fest.
ms.assetid: 2d42876a-524b-454d-b4f1-353afe3a4d28
title: 'Iamtimelinegroup:: abtrecompformatfromsource-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetRecompFormatFromSource
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: adf4bfcf9d76ed40092eba7c612f4213c7aacb0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352074"
---
# <a name="iamtimelinegroupsetrecompformatfromsource-method"></a>Iamtimelinegroup:: abtrecompformatfromsource-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetRecompFormatFromSource` Methode legt das Format der Video Neukomprimierung mit dem Komprimierungs Format aus einer Quelldatei fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRecompFormatFromSource(
   IAMTimelineSrc *pSource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*psource* 
</dt> <dd>

Ein Zeiger auf die [**iamtimelinesrc**](iamtimelinesrc.md) -Schnittstelle des Quell Objekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                             | Beschreibung                                                                                            |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Erfolg.<br/>                                                                                    |
| <dl> <dt>**E \_ keine \_ Zeitachse**</dt> </dl>          | Die Gruppe befindet sich nicht in einer Zeitachse.<br/>                                                         |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>           | Nicht genügend Arbeitsspeicher.<br/>                                                                        |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>               | **Null** -Zeigerargument.<br/>                                                                  |
| <dl> <dt>**VFW \_ E \_ invalidmediatype**</dt> </dl> | Ungültiger Medientyp. Die Gruppe ist keine Videogruppe, oder die Quelldatei enthält keinen Videostream.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode sucht nach der Quelldatei, die *psource* zugeordnet ist, Ruft den Medientyp des ersten Videostreams in der Datei ab und legt das Gruppen Komprimierungs Format mithilfe dieses Typs fest. Weitere Informationen zu den Komprimierungs Formaten finden Sie unter [**iamtimelinegroup:: See-martrecompressformat**](iamtimelinegroup-setsmartrecompressformat.md).

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

[**Iamtimelinegroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




