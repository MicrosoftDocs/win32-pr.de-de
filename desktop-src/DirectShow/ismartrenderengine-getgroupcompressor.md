---
description: Die GetGroupCompressor-Methode ruft den Komprimierungsfilter für die angegebene Gruppe ab.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: ISmartRenderEngine::GetGroupCompressor-Methode (Qedit.h)
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
ms.openlocfilehash: 65915039d26b3c8739441240419e61e0cbacf5a6f4212cbb1c8b456f55dfcbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817438"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a>ISmartRenderEngine::GetGroupCompressor-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetGroupCompressor` -Methode ruft den Komprimierungsfilter für die angegebene Gruppe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gruppe* 
</dt> <dd>

Nullbasierter Index der Gruppe.

</dd> <dt>

*pCompressor* 
</dt> <dd>

Empfängt einen Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Komprimierungsfilters. Er empfängt den Wert **NULL,** wenn kein Komprimierungsfilter vorhanden ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um Eigenschaften für den Komprimierungsfilter festzulegen, z. B. die Keyframerate. Rufen Sie diese Methode nach dem Aufruf von [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md)auf, aber vor dem Rendern des Projekts. Fragen Sie dann den Ausgabepin des Komprimierungsfilters für die [**IAMVideoCompression-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) ab, die Methoden zum Festlegen von Komprimierungsparametern enthält. Geben Sie die Schnittstelle frei, wenn Sie fertig sind. Wenn Sie nachfolgende Änderungen an der Zeitachse vornehmen, rufen **Sie ConnectFrontEnd** auf, und rufen Sie dann **Erneut GetGroupCompressor** auf, um die Komprimierungsparameter zurückzusetzen.

Wenn der Wert von \* *pCompressor* bei der Rückgabe ungleich **NULL** ist, verfügt die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie die -Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ISmartRenderEngine-Schnittstelle**](ismartrenderengine.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




