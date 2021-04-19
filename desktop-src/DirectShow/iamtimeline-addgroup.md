---
description: Die addgroup-Methode fügt der Zeitachse eine Gruppe hinzu.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'Iamtimeline:: addgroup-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358344"
---
# <a name="iamtimelineaddgroup-method"></a>Iamtimeline:: addgroup-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `AddGroup` Methode fügt der Zeitachse eine Gruppe hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pgroup* 
</dt> <dd>

Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle der Gruppe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                   | Beschreibung                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                           |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Die maximale Anzahl von Gruppen wurde überschritten.<br/> |
| <dl> <dt>**E \_ nointerface**</dt> </dl> | Das Objekt ist keine Gruppe.<br/>         |



 

## <a name="remarks"></a>Bemerkungen

Derzeit unterstützen Zeitachsen maximal 32 Gruppen.

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

[**Iamtimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




