---
description: Die getgroupoutputpin-Methode ruft die Ausgabe-PIN für die angegebene Gruppe ab.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'Unenderengine:: getgroupoutputpin-Methode (qedit. h)'
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
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365540"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>Unenderengine:: getgroupoutputpin-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetGroupOutputPin` Methode ruft die Ausgabepin für die angegebene Gruppe ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gruppieren* 
</dt> <dd>

NULL basierter Index, der die Gruppe angibt.

</dd> <dt>

*pprenderpin* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Ausgabe-PIN.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                                  | Beschreibung                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                      | Die Gruppe verfügt über keine Ausgabe-PIN.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                                        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                 | Ungültiges Argument.<br/>                                               |
| <dl> <dt>**E \_ muss \_ Init \_ Renderer**</dt> </dl>       | Fehler beim Initialisieren der Rendering-Engine.<br/>                             |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>                    | Ungültiger Zeiger.<br/>                                                |
| <dl> <dt>**E- \_ Rendering- \_ Engine \_ ist \_ beschädigt.**</dt> </dl> | Fehler beim Vorgang, da das Projekt nicht erfolgreich gerendert wurde.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>                 | Unerwarteter Fehler.<br/>                                               |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie vor dem Aufrufen dieser Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " auf, um das Front-End des Diagramms zu erstellen. Jede Gruppe stellt einen einzelnen Mediendaten Strom dar, und das Front-End verfügt über eine entsprechende Ausgabe-PIN.

Mit dieser Methode können Sie den renderingteil eines Datei Schreib Diagramms erstellen. Verbinden Sie die Ausgabe Pins mit Multiplexer-Filtern und dateiwriter-filtern. Weitere Informationen finden Sie unter [Rendern eines Projekts](rendering-a-project.md).

In der Vorschauversion müssen Sie diese Methode nicht aufzurufen. Nennen Sie einfach **connectfrontend** , gefolgt von " [**irienderengine:: renderoutputpins**](irenderengine-renderoutputpins.md)".

Wenn die Methode S OK zurückgibt \_ , hat die zurückgegebene **IPin** -Schnittstelle einen ausstehenden Verweis Zähler. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

[**Schnittstelle ""**](irenderengine.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




