---
description: Die GetGroup-Methode ruft eine angegebene Gruppe ab.
ms.assetid: 4ff651e5-a3aa-4da9-af23-a3a2bdbf7c5b
title: 'Iamtimeline:: GetGroup-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1241a125698cf78c1138d9264ecd8c73ff78056c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366918"
---
# <a name="iamtimelinegetgroup-method"></a>Iamtimeline:: GetGroup-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetGroup` Methode ruft eine angegebene Gruppe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGroup(
  [out] IAMTimelineObj **ppGroup,
        long           WhichGroup
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppgroup* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle der Gruppe.

</dd> <dt>

*Whichgroup* 
</dt> <dd>

Der Index der abzurufenden Gruppe, basierend auf der Reihenfolge, in der die Gruppen der Zeitachse hinzugefügt wurden. Die erste Gruppe, die der Zeitachse hinzugefügt wird, hat einen Index von 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode erfolgreich ausgeführt wird, weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

 

 




