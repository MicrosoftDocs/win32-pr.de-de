---
description: Die GetGroupOutputPin-Methode ruft den Ausgabepin für die angegebene Gruppe ab.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: IRenderEngine::GetGroupOutputPin-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 99a1f3c60dcafdda219dc8a05f5523d7c2386249ff500bbb9abb463294ca7239
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767150"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>IRenderEngine::GetGroupOutputPin-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetGroupOutputPin` -Methode ruft den Ausgabepin für die angegebene Gruppe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gruppe* 
</dt> <dd>

Nullbasierter Index, der die Gruppe angibt.

</dd> <dt>

*ppRenderPin* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Ausgabepins.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                                  | Beschreibung                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | Die Gruppe verfügt nicht über einen Ausgabepin.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Ungültiges Argument.<br/>                                               |
| <dl> <dt>**E \_ MUSS \_ RENDERER INIT \_**</dt> </dl>       | Fehler beim Initialisieren der Render-Engine.<br/>                             |
| <dl> <dt>**E \_ POINTER**</dt> </dl>                    | Ungültiger Zeiger.<br/>                                                |
| <dl> <dt>**E \_ \_ RENDER-ENGINE \_ IST \_ FEHLERHAFT**</dt> </dl> | Fehler beim Vorgang, weil das Projekt nicht erfolgreich gerendert wurde.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | Unerwarteter Fehler.<br/>                                               |



 

## <a name="remarks"></a>Hinweise

Rufen Sie vor dem Aufrufen dieser Methode [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) auf, um das Front-End des Graphen zu erstellen. Jede Gruppe stellt einen einzelnen Medienstream dar, und das Front-End verfügt über einen entsprechenden Ausgabepin.

Sie können diese Methode verwenden, um den Renderingteil eines Dateischreibgraphen zu erstellen. Verbinden die Ausgabepins an Multiplexerfilter und Dateiwriterfilter an. Weitere Informationen finden Sie unter [Rendern eines Project](rendering-a-project.md).

Für die Vorschau müssen Sie diese Methode nicht aufrufen. Rufen Sie einfach **ConnectFrontEnd** gefolgt von [**IRenderEngine::RenderOutputPins auf.**](irenderengine-renderoutputpins.md)

Wenn die Methode S \_ OK zurückgibt, verfügt die **zurückgegebene IPin-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IRenderEngine-Schnittstelle**](irenderengine.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




