---
description: Die getgroupcompressor-Methode ruft den Komprimierungs Filter für die angegebene Gruppe ab.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'Ismartrenderengine:: getgroupcompressor-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351339"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a>Ismartrenderengine:: getgroupcompressor-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetGroupCompressor` Methode ruft den Komprimierungs Filter für die angegebene Gruppe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gruppieren* 
</dt> <dd>

Der null basierte Index der Gruppe.

</dd> <dt>

*pkompressor* 
</dt> <dd>

Empfängt einen Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Komprimierungs Filters. Er empfängt den Wert **null** , wenn kein Komprimierungs Filter vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um Eigenschaften für den Komprimierungs Filter festzulegen, z. b. die Keyframe-Rate. Rufen Sie diese Methode nach dem Aufrufen von " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md)" auf, aber bevor Sie das Projekt rendern. Fragen Sie dann die Ausgabepin des Komprimierungs Filters für die [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) -Schnittstelle ab, die Methoden zum Festlegen von Komprimierungs Parametern enthält. Geben Sie die Schnittstelle frei, wenn Sie abgeschlossen sind. Wenn Sie nachfolgende Änderungen an der Zeitachse vornehmen, müssen Sie **connectfrontend** aufrufen und **getgroupcompressor** erneut aufrufen, um die Komprimierungs Parameter zurückzusetzen.

Wenn der Wert von \* *pkompressor* bei der Rückgabe nicht **null** ist, weist die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

[**Ismartrenderengine-Schnittstelle**](ismartrenderengine.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




