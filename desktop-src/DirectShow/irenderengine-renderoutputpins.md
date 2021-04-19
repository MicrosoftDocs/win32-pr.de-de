---
description: Die renderoutputpins-Methode erstellt den Teil der Vorschau des Filter Diagramms.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'Unenderengine:: renderoutputpins-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373896"
---
# <a name="irenderenginerenderoutputpins-method"></a>Unenderengine:: renderoutputpins-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `RenderOutputPins` Methode erstellt den Teil der Vorschau des Filter Diagramms.

## <a name="syntax"></a>Syntax


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                                  | Beschreibung                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                                        |
| <dl> <dt>**VFW \_ S \_ -Audiodatei \_ nicht \_ gerendert**</dt> </dl>  | Der Audiostream kann nicht wiedergegeben werden.<br/>                              |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                 | Ungültiges Argument.<br/>                                               |
| <dl> <dt>**E- \_ Rendering- \_ Engine \_ ist \_ beschädigt.**</dt> </dl> | Fehler beim Vorgang, da das Projekt nicht erfolgreich gerendert wurde.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>                 | Unerwarteter Fehler.<br/>                                               |



 

## <a name="remarks"></a>Bemerkungen

Rufen Sie vor dem Aufrufen dieser Methode " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md) " auf, um das Front-End des Diagramms zu erstellen. Um einen anderen Vorgang als die Vorschau auszuführen, dürfen Sie diese Methode nicht aufzurufen. Rufen Sie stattdessen " [**irienderengine:: getgroupoutputpin**](irenderengine-getgroupoutputpin.md) " auf, um Zeiger auf die Ausgabe Pins zu erhalten.

Wenn auf dem Computer des Benutzers keine Soundkarte vorhanden ist, gibt diese Methode VFW \_ s \_ -Audiodaten zurück, die \_ nicht \_ gerendert werden. In diesem Fall wird keine Audiovorschau angezeigt, aber die Video Vorschau ist nicht betroffen.

Wenn die PIN aus einer Videogruppe besteht, erstellt diese Methode ein Videofenster. Der aufrufenden Thread muss Nachrichten verteilen – beispielsweise, um das Fenster zu verschieben oder auf Mausklicks im Client Bereich des Fensters zu reagieren.

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

 

 




